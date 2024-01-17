---
title: Excel copiar planilhas entre pastas de trabalho
linktitle: Excel copiar planilhas entre pastas de trabalho
second_title: Referência da API Aspose.Cells para .NET
description: Copie facilmente planilhas entre pastas de trabalho do Excel usando Aspose.Cells for .NET.
type: docs
weight: 30
url: /pt/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
Neste tutorial, iremos guiá-lo pelas etapas para copiar planilhas entre pastas de trabalho do Excel usando a biblioteca Aspose.Cells para .NET. Siga as instruções abaixo para concluir esta tarefa.

## Etapa 1: Preparação

Certifique-se de ter instalado o Aspose.Cells for .NET e criado um projeto C# em seu ambiente de desenvolvimento integrado (IDE) preferido.

## Etapa 2: definir o caminho do diretório do documento

 Declarar um`dataDir` variável e inicialize-a com o caminho para o diretório de documentos. Por exemplo :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Certifique-se de substituir`"YOUR_DOCUMENTS_DIRECTORY"` com o caminho real para o seu diretório.

## Etapa 3: Defina o caminho do arquivo de entrada

 Declarar um`InputPath` variável e inicialize-a com o caminho completo do arquivo Excel do qual deseja copiar a planilha. Por exemplo :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Certifique-se de ter o arquivo Excel`book1.xls` no diretório de documentos ou especifique o nome e o local corretos do arquivo.

## Etapa 4: crie uma primeira pasta de trabalho do Excel

 Use o`Workbook` classe de Aspose.Cells para criar uma primeira pasta de trabalho do Excel e abrir o arquivo especificado:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Etapa 5: crie uma segunda pasta de trabalho do Excel

Crie uma segunda pasta de trabalho do Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Etapa 6: copie a planilha da primeira pasta de trabalho para a segunda pasta de trabalho

 Use o`Copy`método para copiar a primeira planilha da primeira pasta de trabalho para a segunda pasta de trabalho:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Etapa 7: salve o arquivo Excel

Salve o arquivo Excel contendo a planilha copiada:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Certifique-se de especificar o caminho e o nome de arquivo desejados para o arquivo de saída.

### Exemplo de código-fonte para Excel Copiar planilhas entre pastas de trabalho usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Crie uma pasta de trabalho.
// Abra um arquivo no primeiro livro.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Crie outra pasta de trabalho.
Workbook excelWorkbook1 = new Workbook();
// Copie a primeira folha do primeiro livro para o segundo livro.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Salve o arquivo.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Conclusão

Parabéns! Agora você aprendeu como copiar planilhas entre pastas de trabalho do Excel usando Aspose.Cells for .NET. Sinta-se à vontade para usar esse método em seus próprios projetos para manipular arquivos Excel com eficiência.

### Perguntas frequentes

#### P. Quais bibliotecas são necessárias para usar Aspose.Cells for .NET?

A. Para usar Aspose.Cells for .NET, você deve incluir a biblioteca Aspose.Cells em seu projeto. Certifique-se de ter referenciado esta biblioteca corretamente em seu ambiente de desenvolvimento integrado (IDE).

#### P. O Aspose.Cells oferece suporte a outros formatos de arquivo Excel, como XLSX?

A. Sim, Aspose.Cells suporta vários formatos de arquivo Excel, incluindo XLSX, XLS, CSV, HTML e muitos mais. Você pode manipular esses formatos de arquivo usando os recursos do Aspose.Cells for .NET.

#### P. Posso personalizar as opções de layout ao copiar a planilha?

A.  Sim, você pode personalizar as opções de configuração da página ao copiar a planilha usando as propriedades do`PageSetup` objeto. Você pode especificar cabeçalhos de página, rodapés, margens, orientações, etc.