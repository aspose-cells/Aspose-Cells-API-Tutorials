---
title: Excel copiar planilha de outra pasta de trabalho
linktitle: Excel copiar planilha de outra pasta de trabalho
second_title: Referência da API Aspose.Cells para .NET
description: Copie facilmente uma planilha do Excel de uma pasta de trabalho para outra usando Aspose.Cells for .NET.
type: docs
weight: 10
url: /pt/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
Neste tutorial, orientaremos você nas etapas para copiar uma planilha do Excel de outra pasta de trabalho usando a biblioteca Aspose.Cells para .NET. Siga as instruções abaixo para concluir esta tarefa.

## Etapa 1: Preparação

Antes de começar, certifique-se de ter instalado o Aspose.Cells for .NET e criado um projeto C# em seu ambiente de desenvolvimento integrado (IDE) preferido.

## Etapa 2: definir o caminho do diretório do documento

 Declarar um`dataDir` variável e inicialize-a com o caminho para o diretório de documentos. Por exemplo :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Certifique-se de substituir`"YOUR_DOCUMENTS_DIRECTORY"` com o caminho real para o seu diretório.

## Etapa 3: crie uma nova pasta de trabalho do Excel

 Use o`Workbook` classe de Aspose.Cells para criar uma nova pasta de trabalho do Excel:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Etapa 4: obtenha a primeira planilha da pasta de trabalho

Navegue até a primeira planilha da pasta de trabalho usando o índice 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Etapa 5: adicionar dados às linhas de cabeçalho (A1:A4)

 Use um`for` loop para adicionar dados às linhas de cabeçalho (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Etapa 6: adicionar dados detalhados (A5:A999)

 Use outro`for` loop para adicionar dados detalhados (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Etapa 7: definir opções de layout

 Defina as opções de configuração de página para a planilha usando o`PageSetup` objeto:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Etapa 8: Crie outra pasta de trabalho do Excel

Crie outra pasta de trabalho do Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Etapa 9: obtenha a primeira planilha da segunda pasta de trabalho

Navegue até a primeira planilha da segunda pasta de trabalho:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Etapa 10: nomeie a planilha

nomeie o fogo

ilha de cálculo:

```csharp
ws1.Name = "MySheet";
```

## Etapa 11: Copie os dados da primeira planilha da primeira pasta de trabalho para a primeira planilha da segunda pasta de trabalho

Copie os dados da primeira planilha da primeira pasta de trabalho para a primeira planilha da segunda pasta de trabalho:

```csharp
ws1.Copy(ws0);
```

## Etapa 12: salve o arquivo Excel

Salve o arquivo Excel:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Certifique-se de especificar o caminho e o nome de arquivo desejados para o arquivo de saída.

### Exemplo de código-fonte para Excel Copiar planilha de outra pasta de trabalho usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crie uma nova pasta de trabalho.
Workbook excelWorkbook0 = new Workbook();
// Obtenha a primeira planilha do livro.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Coloque alguns dados nas linhas de cabeçalho (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Coloque alguns dados detalhados (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Defina um objeto pagesetup com base na primeira planilha.
PageSetup pagesetup = ws0.PageSetup;
// As primeiras cinco linhas são repetidas em cada página...
// Isso pode ser visto na visualização da impressão.
pagesetup.PrintTitleRows = "$1:$5";
// Crie outra pasta de trabalho.
Workbook excelWorkbook1 = new Workbook();
// Obtenha a primeira planilha do livro.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Dê um nome à planilha.
ws1.Name = "MySheet";
// Copie os dados da primeira planilha da primeira pasta de trabalho para o
// primeira planilha da segunda pasta de trabalho.
ws1.Copy(ws0);
// Salve o arquivo Excel.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Conclusão

Parabéns! Agora você aprendeu como copiar uma planilha do Excel de outra pasta de trabalho usando Aspose.Cells for .NET. Sinta-se à vontade para usar esse método em seus próprios projetos para manipular arquivos Excel com eficiência.

### Perguntas frequentes

#### P. Quais bibliotecas são necessárias para usar Aspose.Cells for .NET?

A. Para usar Aspose.Cells for .NET, você deve incluir a biblioteca Aspose.Cells em seu projeto. Certifique-se de ter referenciado esta biblioteca corretamente em seu ambiente de desenvolvimento integrado (IDE).

#### P. O Aspose.Cells oferece suporte a outros formatos de arquivo Excel, como XLSX?

A. Sim, Aspose.Cells suporta vários formatos de arquivo Excel, incluindo XLSX, XLS, CSV, HTML e muitos mais. Você pode manipular esses formatos de arquivo usando os recursos do Aspose.Cells for .NET.

#### P. Posso personalizar as opções de layout ao copiar a planilha?

A.  Sim, você pode personalizar as opções de configuração da página ao copiar a planilha usando as propriedades do`PageSetup` objeto. Você pode especificar cabeçalhos de página, rodapés, margens, orientações, etc.