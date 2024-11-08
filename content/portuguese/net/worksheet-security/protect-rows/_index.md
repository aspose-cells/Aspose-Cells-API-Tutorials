---
title: Proteger linhas na planilha usando Aspose.Cells
linktitle: Proteger linhas na planilha usando Aspose.Cells
second_title: API de processamento do Aspose.Cells .NET Excel
description: Aprenda a proteger linhas em uma planilha do Excel usando Aspose.Cells for .NET. Proteja seus dados com proteção em nível de linha e evite alterações acidentais.
type: docs
weight: 18
url: /pt/net/worksheet-security/protect-rows/
---
## Introdução
Trabalhar com arquivos do Excel programaticamente é frequentemente uma tarefa que requer não apenas manipulação de dados, mas também proteção de dados. Se você precisa proteger dados confidenciais ou evitar edições acidentais, proteger linhas em uma planilha pode ser uma etapa crucial. Neste tutorial, vamos nos aprofundar em como proteger linhas específicas em uma planilha do Excel usando o Aspose.Cells para .NET. Vamos percorrer todas as etapas necessárias, desde a preparação do seu ambiente até a implementação dos recursos de proteção de uma maneira simples e fácil de seguir.
## Pré-requisitos
Antes de começar a proteger linhas em uma planilha, há algumas coisas que você precisa ter em mãos:
1.  Aspose.Cells para .NET: Certifique-se de ter o Aspose.Cells para .NET instalado em sua máquina de desenvolvimento. Se você ainda não fez isso, você pode baixá-lo facilmente do[Página de download do Aspose Cells](https://releases.aspose.com/cells/net/).
2. Visual Studio ou qualquer IDE .NET: Para implementar a solução, você precisa ter um ambiente de desenvolvimento configurado. O Visual Studio é uma ótima opção, mas qualquer IDE compatível com .NET funcionará.
3. Conhecimento básico de C#: entender os conceitos básicos de programação em C# ajudará você a acompanhar o tutorial e modificar o código de exemplo para atender às suas necessidades.
4.  Documentação da API Aspose.Cells: Familiarize-se com a[Documentação do Aspose.Cells para .NET](https://reference.aspose.com/cells/net/) para obter uma visão geral da estrutura de classe e dos métodos usados na biblioteca.
Se você tiver todos os pré-requisitos definidos, podemos começar imediatamente a implementação.
## Pacotes de importação
Para começar, você precisa importar os pacotes necessários. Essas bibliotecas são cruciais para interagir com arquivos Excel no seu projeto C#.
```csharp
using System.IO;
using Aspose.Cells;
```
Depois de importar os pacotes necessários, você pode começar a codificar. 
Agora, vamos dividir o processo em etapas menores para que seja superfácil para você seguir. Cada etapa se concentrará em uma parte específica da implementação, garantindo que você possa entendê-la e aplicá-la rapidamente. 
## Etapa 1: Crie uma nova pasta de trabalho e planilha
Antes de poder aplicar quaisquer configurações de proteção, você precisa criar uma nova pasta de trabalho e selecionar a planilha com a qual deseja trabalhar. Este será seu documento de trabalho.
```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";
// Crie um diretório se ele ainda não estiver presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// Crie uma nova pasta de trabalho.
Workbook wb = new Workbook();
// Crie um objeto de planilha e obtenha a primeira planilha.
Worksheet sheet = wb.Worksheets[0];
```
Neste exemplo, estamos criando uma nova pasta de trabalho com uma única planilha (que é a configuração padrão quando você cria uma nova pasta de trabalho usando Aspose.Cells). Então, pegamos a primeira planilha na pasta de trabalho, que será o alvo para nossa proteção de linha.
## Etapa 2: Definir objetos Style e StyleFlag
O próximo passo é definir os objetos style e style flag. Esses objetos permitem que você modifique as propriedades da célula, como se ela está bloqueada ou desbloqueada.
```csharp
// Defina o objeto de estilo.
Style style;
// Defina o objeto styleflag.
StyleFlag flag;
```
Você usará esses objetos em etapas posteriores para personalizar as propriedades da célula e aplicá-las à sua planilha.
## Etapa 3: Desbloqueie todas as colunas na planilha
Por padrão, todas as células em uma planilha do Excel são bloqueadas. No entanto, quando você protege uma planilha, o status bloqueado é imposto. Para garantir que apenas linhas ou células específicas sejam protegidas, você pode desbloquear todas as colunas primeiro. Esta etapa é essencial se você quiser proteger apenas certas linhas.
```csharp
// Percorra todas as colunas da planilha e desbloqueie-as.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```
 Neste código, percorremos todas as 256 colunas da planilha (as planilhas do Excel têm no máximo 256 colunas, indexadas de 0 a 255) e definimos suas`IsLocked` propriedade para`false`. Essa ação garante que todas as colunas sejam desbloqueadas, mas ainda bloquearemos linhas específicas mais tarde.
## Etapa 4: Bloqueie a primeira linha
Depois de desbloquear as colunas, o próximo passo é bloquear linhas específicas que você deseja proteger. Neste exemplo, bloquearemos a primeira linha. Isso garante que os usuários não possam modificá-la enquanto outras linhas forem deixadas desbloqueadas.
```csharp
//Obtenha o estilo da primeira linha.
style = sheet.Cells.Rows[0].Style;
// Tranque-o.
style.IsLocked = true;
//Instanciar o sinalizador.
flag = new StyleFlag();
// Defina a configuração de bloqueio.
flag.Locked = true;
// Aplique o estilo à primeira linha.
sheet.Cells.ApplyRowStyle(0, style, flag);
```
Aqui, acessamos o estilo da primeira linha e definimos seu`IsLocked` propriedade para`true` . Depois disso, usamos o`ApplyRowStyle()` método para aplicar o estilo de bloqueio à linha inteira. Você pode repetir esta etapa para bloquear quaisquer outras linhas que queira proteger.
## Etapa 5: Proteja a folha
Agora que desbloqueamos e bloqueamos as linhas necessárias, é hora de proteger a planilha. A proteção garante que ninguém possa modificar as linhas ou células bloqueadas, a menos que removam a senha de proteção (se fornecida).
```csharp
// Proteja a folha.
sheet.Protect(ProtectionType.All);
```
 Nesta etapa, aplicamos proteção a toda a folha usando`ProtectionType.All`. Esse tipo de proteção significa que todos os aspectos da planilha, incluindo linhas e células bloqueadas, são protegidos. Você também pode personalizar essa proteção especificando diferentes tipos de proteção, se necessário.
## Etapa 6: Salve a pasta de trabalho
Por fim, precisamos salvar a pasta de trabalho após aplicar os estilos e a proteção necessários. A pasta de trabalho pode ser salva em vários formatos, como Excel 97-2003, Excel 2010, etc.
```csharp
// Salve o arquivo Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
Esta linha de código salva a pasta de trabalho no formato Excel 97-2003 com as alterações aplicadas. Você pode alterar o formato do arquivo conforme suas necessidades, selecionando entre uma variedade de`SaveFormat` opções.
## Conclusão
E aí está! Você aprendeu com sucesso como proteger linhas em uma planilha usando Aspose.Cells for .NET. Seguindo os passos acima, você pode desbloquear ou bloquear quaisquer linhas ou colunas conforme necessário, e aplicar proteção para garantir a integridade dos seus dados.
## Perguntas frequentes
### Como posso proteger várias linhas de uma só vez?  
 Você pode fazer um loop por várias linhas e aplicar o estilo de bloqueio a cada uma individualmente. Simplesmente substitua`0` com o índice de linha que você deseja bloquear.
### Posso definir uma senha para a proteção da planilha?  
 Sim! Você pode passar uma senha para o`sheet.Protect()` método para impor proteção por senha.
### Posso desbloquear células em vez de colunas inteiras?  
Sim! Em vez de desbloquear colunas, você pode desbloquear células individuais modificando suas propriedades de estilo.
### O que acontece se eu tentar editar uma linha protegida?  
Quando uma linha é protegida, o Excel impede que quaisquer edições sejam feitas nas células bloqueadas, a menos que você desproteja a planilha.
### Posso proteger intervalos específicos em sequência?  
 Sim! Você pode bloquear intervalos individuais em uma linha definindo o`IsLocked` propriedade para células específicas dentro do intervalo.