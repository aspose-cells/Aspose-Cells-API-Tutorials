---
title: Extrair arquivo Mol incorporado da pasta de trabalho
linktitle: Extrair arquivo Mol incorporado da pasta de trabalho
second_title: API de processamento do Aspose.Cells .NET Excel
description: Aprenda como extrair arquivos MOL incorporados de pastas de trabalho do Excel usando o Aspose.Cells para .NET neste tutorial detalhado passo a passo.
type: docs
weight: 18
url: /pt/net/workbook-operations/extract-embedded-mol-file/
---
## Introdução
Quando se trata de gerenciar dados em planilhas do Excel, às vezes você encontra vários objetos incorporados que não estão em um formato padrão. Um desses formatos é o MOL (Molecular Structure File), que é comumente usado em química para representar informações moleculares. Se você está procurando extrair esses arquivos MOL de uma planilha do Excel usando o Aspose.Cells for .NET, você chegou ao guia certo. Neste artigo, nós o guiaremos pelo processo passo a passo, desmistificando cada parte ao longo do caminho.
## Pré-requisitos
Antes de mergulhar no código, é essencial garantir que você tenha as habilidades e ferramentas necessárias. Aqui está o que você vai precisar:
1. Noções básicas de programação .NET: você deve estar familiarizado com C# e o framework .NET.
2.  Aspose.Cells para .NET: Certifique-se de ter a biblioteca Aspose.Cells. Você pode[baixe aqui](https://releases.aspose.com/cells/net/).
3. Um IDE: você pode usar o Visual Studio ou qualquer outro IDE compatível com .NET.
4. Pasta de trabalho do Excel com arquivos MOL incorporados: para este tutorial, você precisa de um arquivo do Excel contendo objetos MOL. Você pode criar o seu próprio ou usar qualquer arquivo de amostra.
## Pacotes de importação
Para começar, você precisará importar os namespaces necessários no seu projeto. Isso é crucial para acessar as funcionalidades do Aspose.Cells. Veja como você pode fazer isso:

```csharp
using Aspose.Cells.Drawing;
using Aspose.Cells.WebExtensions;
using System;
using System.IO;
```

Esses namespaces permitirão que você manipule pastas de trabalho, acesse planilhas e trabalhe com arquivos em geral.
Agora que resolvemos nossos pré-requisitos, vamos mergulhar no código e entender cada etapa envolvida na extração de arquivos MOL incorporados de uma pasta de trabalho do Excel. 
## Etapa 1: Configurando seus diretórios
O primeiro passo é definir onde seu documento de origem está localizado e onde você quer salvar os arquivos MOL extraídos. Vamos configurar esses diretórios.
```csharp
string SourceDir = "Your Document Directory"; // Substitua pelo caminho do seu diretório
string outputDir = "Your Document Directory"; // Substitua pelo seu caminho de saída
```
 Aqui, você substitui`"Your Document Directory"`com o caminho para seus diretórios reais. É importante que tanto o diretório de origem quanto o de saída sejam acessíveis para seu aplicativo.
## Etapa 2: Carregando a pasta de trabalho
Depois que você tiver seus diretórios configurados, a próxima tarefa é carregar a pasta de trabalho do Excel. Vamos fazer isso agora.

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

 Estamos criando uma instância do`Workbook` classe e passando o caminho para nosso arquivo Excel chamado`EmbeddedMolSample.xlsx`. Esta etapa inicializa a pasta de trabalho, permitindo que você acesse seu conteúdo.
## Etapa 3: Iterando sobre planilhas
Agora que sua pasta de trabalho está carregada, você precisa fazer um loop em cada planilha dentro da pasta de trabalho. Isso permite que você examine cada planilha em busca de objetos incorporados.

```csharp
var index = 1; // Usado para nomear arquivos MOL extraídos
foreach (Worksheet sheet in workbook.Worksheets)
{
    OleObjectCollection oles = sheet.OleObjects;
    // Mais lógica de extração vai aqui
}
```

 Aqui, você está usando um`foreach` loop para navegar pelas planilhas. Para cada planilha, você acessa o`OleObjects` coleção, que contém todos os objetos incorporados.
## Etapa 4: Extraindo arquivos MOL
Agora vem a parte crítica — extrair os arquivos MOL dos objetos OLE. Isso requer outro loop dentro do loop da planilha.

```csharp
foreach (OleObject ole in oles)
{
    string fileName = outputDir + "OleObject" + index + ".mol ";
    FileStream fs = File.Create(fileName);
    fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
    fs.Close();
    index++;
}
```

 Para cada objeto OLE que você encontrou, você está criando um novo arquivo no diretório de saída. O`ObjectData` propriedade do`OleObject` contém os dados do objeto incorporado, que você grava em um arquivo recém-criado usando um`FileStream`. O arquivo é nomeado sequencialmente (`OleObject1.mol`, `OleObject2.mol` , etc.) com base no`index` variável.
## Etapa 5: Confirmação da conclusão do processo
Por fim, depois que todos os arquivos MOL forem extraídos, é uma boa prática informar ao usuário que o processo foi concluído com sucesso.

```csharp
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Esta linha simplesmente imprime uma mensagem no console informando que a extração foi bem-sucedida. É um toque legal para feedback do usuário.
## Conclusão
aí está! Você extraiu com sucesso arquivos MOL incorporados de uma pasta de trabalho do Excel usando o Aspose.Cells para .NET. Este processo integra algumas etapas principais, garantindo uma abordagem estruturada para lidar com objetos incorporados. Quer você esteja em pesquisa científica, análise química ou simplesmente lidando com conjuntos de dados complexos, ser capaz de extrair e manipular esses tipos de arquivo pode fazer uma diferença significativa em como você gerencia suas informações. 
## Perguntas frequentes
### Posso extrair outros tipos de arquivo além de MOL do Excel?
Sim, você pode extrair vários outros tipos de arquivos incorporados com técnicas semelhantes.
### O Aspose.Cells é gratuito?
 Aspose.Cells é uma biblioteca comercial, mas você pode[experimente gratuitamente por um período limitado](https://releases.aspose.com/).
### Este método funciona com todas as versões do Excel?
Sim, desde que o formato do arquivo seja suportado pelo Aspose.Cells.
### Posso automatizar esse processo de extração?
Absolutamente! Você pode automatizar esse processo colocando o código em uma tarefa agendada ou em um script.
### Onde posso encontrar mais documentação sobre o Aspose.Cells?
 Você pode conferir o[Documentação do Aspose.Cells](https://reference.aspose.com/cells/net/) para mais detalhes e exemplos.