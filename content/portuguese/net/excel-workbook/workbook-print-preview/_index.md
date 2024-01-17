---
title: Visualização de impressão da pasta de trabalho
linktitle: Visualização de impressão da pasta de trabalho
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como gerar uma visualização de impressão de uma pasta de trabalho usando Aspose.Cells for .NET.
type: docs
weight: 170
url: /pt/net/excel-workbook/workbook-print-preview/
---
visualização de impressão de uma pasta de trabalho é um recurso essencial ao trabalhar com arquivos Excel com Aspose.Cells for .NET. Você pode gerar facilmente uma visualização de impressão seguindo estas etapas:

## Etapa 1: especifique o diretório de origem

Primeiro, você precisa especificar o diretório de origem onde está localizado o arquivo Excel que deseja visualizar. Veja como fazer isso:

```csharp
// diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Etapa 2: carregar a pasta de trabalho

Então você precisa carregar a pasta de trabalho do arquivo Excel especificado. Veja como fazer isso:

```csharp
// Carregar a pasta de trabalho
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Etapa 3: configurar opções de imagem e impressão

Antes de gerar a visualização da impressão, você pode configurar a imagem e as opções de impressão conforme necessário. Neste exemplo, estamos usando as opções padrão. Veja como fazer isso:

```csharp
// Opções de imagem e impressão
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Etapa 4: gerar a visualização de impressão da pasta de trabalho

Agora você pode gerar a visualização de impressão da pasta de trabalho da pasta de trabalho usando a classe WorkbookPrintingPreview. Veja como fazer isso:

```csharp
// Visualização de impressão da pasta de trabalho
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Etapa 5: gerar a visualização de impressão da planilha

Se você deseja gerar a visualização da impressão de uma planilha específica, você pode usar a classe SheetPrintingPreview. Aqui está um exemplo :

```csharp
// Visualização de impressão da planilha
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Exemplo de código-fonte para visualização de impressão da pasta de trabalho usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Conclusão

Gerar a visualização de impressão de uma pasta de trabalho é um recurso poderoso oferecido pelo Aspose.Cells for .NET. Seguindo as etapas fornecidas acima, você pode visualizar facilmente sua pasta de trabalho do Excel e obter informações sobre o número de páginas a serem impressas.

### Perguntas frequentes

#### P: Como posso especificar um diretório de origem diferente para carregar minha pasta de trabalho?
    
 R: Você pode usar o`Set_SourceDirectory` método para especificar um diretório de origem diferente. Por exemplo:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### P: Posso personalizar as opções de imagem e impressão ao gerar a visualização da impressão?
    
 R: Sim, você pode personalizar as opções de imagem e impressão alterando as propriedades do`ImageOrPrintOptions` objeto. Por exemplo, você pode definir a resolução da imagem, formato do arquivo de saída, etc.

#### P: É possível gerar uma visualização de impressão para várias planilhas em uma pasta de trabalho?
    
R: Sim, você pode iterar nas diferentes planilhas da pasta de trabalho e gerar uma visualização de impressão para cada planilha usando o`SheetPrintingPreview` aula.

#### P: Como faço para salvar a visualização da impressão como uma imagem ou arquivo PDF?
    
 R: Você pode usar`ToImage` ou`ToPdf` método de`WorkbookPrintingPreview` ou`SheetPrintingPreview` objeto para salvar a visualização da impressão como imagem ou arquivo PDF.

#### P: O que posso fazer com a visualização da impressão depois de gerada?
    
R: Depois de gerar a visualização da impressão, você poderá visualizá-la na tela, salvá-la como imagem ou arquivo PDF ou utilizá-la para outras operações, como envio por e-mail ou impressão.
	