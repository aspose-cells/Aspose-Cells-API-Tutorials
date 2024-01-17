---
title: Proteger linha na planilha do Excel
linktitle: Proteger linha na planilha do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Descubra neste tutorial como proteger as linhas de uma planilha Excel usando Aspose.Cells for .NET. Tutorial passo a passo em C#.
type: docs
weight: 60
url: /pt/net/protect-excel-file/protect-row-in-excel-worksheet/
---
Neste tutorial, veremos alguns códigos-fonte C# que usam a biblioteca Aspose.Cells para proteger linhas em uma planilha do Excel. Examinaremos cada etapa do código e explicaremos como ele funciona. Siga as instruções cuidadosamente para obter os resultados desejados.

## Etapa 1: Pré-requisitos

Antes de começar, certifique-se de ter instalado a biblioteca Aspose.Cells para .NET. Você pode obtê-lo no site oficial do Aspose. Certifique-se também de ter uma versão recente do Visual Studio ou qualquer outro ambiente de desenvolvimento C#.

## Etapa 2: importar namespaces necessários

Para usar a biblioteca Aspose.Cells, precisamos importar os namespaces necessários para nosso código. Adicione as seguintes linhas ao topo do seu arquivo de origem C#:

```csharp
using Aspose.Cells;
```

## Etapa 3: Criando uma pasta de trabalho do Excel

Nesta etapa, criaremos uma nova pasta de trabalho do Excel. Use o seguinte código para criar uma pasta de trabalho do Excel:

```csharp
// Caminho para o diretório de documentos.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Crie uma nova pasta de trabalho.
Workbook wb = new Workbook();
```

 Certifique-se de substituir`"YOUR_DOCUMENTS_DIR"` com o caminho apropriado para o diretório de documentos.

## Passo 4: Criando uma planilha

Agora que criamos a pasta de trabalho do Excel, vamos criar uma planilha e obter a primeira planilha. Use o seguinte código:

```csharp
// Crie um objeto de planilha e obtenha a primeira planilha.
Worksheet sheet = wb.Worksheets[0];
```

## Etapa 5: definindo o estilo

Nesta etapa definiremos o estilo a ser aplicado às linhas da planilha. Use o seguinte código:

```csharp
// Definição do objeto de estilo.
Styling styling;
```

## Etapa 6: Loop para desbloquear todas as colunas

Agora iremos percorrer todas as colunas da planilha e desbloqueá-las. Use o seguinte código:

```csharp
// Percorra todas as colunas da planilha e desbloqueie-as.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Passo 7: Bloqueando a primeira linha

Nesta etapa, bloquearemos a primeira linha da planilha. Use o seguinte código:

```csharp
// Obtenha o estilo da primeira linha.
style = sheet.Cells.Rows[0].Style;
// Bloqueie o estilo.
style. IsLocked = true;
// Aplique o estilo à primeira linha.
sheet.Cells.ApplyRowStyle(0, style);
```

## Passo 8: Protegendo a planilha

Agora que definimos os estilos e bloqueamos as linhas, vamos proteger a planilha. Use o seguinte código:

```csharp
// Proteja a planilha.
sheet.Protect(ProtectionType.All);
```

## Etapa 9: Salvando o arquivo Excel

Por fim, salvaremos o arquivo Excel modificado. Use o seguinte código:

```csharp
// Salve o arquivo Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Certifique-se de especificar o caminho correto para salvar o arquivo Excel modificado.

### Exemplo de código-fonte para proteger linha na planilha do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crie um diretório se ainda não estiver presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Crie uma nova pasta de trabalho.
Workbook wb = new Workbook();
// Crie um objeto de planilha e obtenha a primeira planilha.
Worksheet sheet = wb.Worksheets[0];
// Defina o objeto de estilo.
Style style;
// Defina o objeto styleflag.
StyleFlag flag;
// Percorra todas as colunas da planilha e desbloqueie-as.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Obtenha o estilo da primeira linha.
style = sheet.Cells.Rows[0].Style;
// Bloqueie-o.
style.IsLocked = true;
//Instancie a bandeira.
flag = new StyleFlag();
// Defina a configuração de bloqueio.
flag.Locked = true;
// Aplique o estilo à primeira linha.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Proteja a folha.
sheet.Protect(ProtectionType.All);
// Salve o arquivo Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusão

Parabéns! Agora você tem código-fonte C# que permite proteger linhas em uma planilha do Excel usando a biblioteca Aspose.Cells para .NET. Certifique-se de seguir as etapas cuidadosamente e personalizar o código de acordo com suas necessidades específicas.

### FAQs (perguntas frequentes)

#### Este código funciona com versões recentes do Excel?

Sim, este código funciona com versões recentes do Excel, incluindo arquivos no formato Excel 2010 e superior.

#### Posso proteger apenas linhas específicas em vez de todas as linhas da planilha?

Sim, você pode modificar o código para especificar as linhas específicas que deseja proteger. Você precisará ajustar o loop e os índices de acordo.

#### Como posso desbloquear linhas bloqueadas novamente?

 Você pode usar o`IsLocked` método do`Style` objeto para definir o valor como`false` e desbloquear as linhas.

#### É possível proteger várias planilhas na mesma pasta de trabalho do Excel?

Sim, você pode repetir as etapas de criação de uma planilha, definindo o estilo e protegendo cada planilha da pasta de trabalho.

#### Como posso alterar a senha de proteção da planilha?

 Você pode alterar a senha usando o`Protect` método e especificando uma nova senha como argumento.