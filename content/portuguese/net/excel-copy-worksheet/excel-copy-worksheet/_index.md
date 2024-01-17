---
title: Planilha de cópia do Excel
linktitle: Planilha de cópia do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Copie uma planilha do Excel para outra com Aspose.Cells for .NET.
type: docs
weight: 20
url: /pt/net/excel-copy-worksheet/excel-copy-worksheet/
---

Neste guia, explicaremos como copiar uma planilha do Excel usando a biblioteca Aspose.Cells para .NET. Forneceremos o código-fonte C# e orientaremos você nas etapas necessárias para concluir esta tarefa. Ao final mostraremos o resultado esperado. Siga as instruções abaixo para começar.

## Etapa 1: Preparação

Antes de começar, certifique-se de ter instalado o Aspose.Cells for .NET e criado um projeto C# em seu ambiente de desenvolvimento integrado (IDE) preferido. Certifique-se também de ter uma cópia do arquivo Excel que deseja manipular.

## Etapa 2: importar as bibliotecas necessárias

 Em seu arquivo de origem C#, importe as bibliotecas necessárias de Aspose.Cells usando o`using` diretiva:

```csharp
using Aspose.Cells;
```

## Passo 3: Defina o caminho do arquivo

 Declarar um`dataDir` variável e inicialize-a com o diretório que contém seu arquivo Excel. Por exemplo :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Certifique-se de substituir`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` com o caminho real para o seu diretório.

## Etapa 4: carregar o arquivo Excel existente

 Use o`Workbook` class de Aspose.Cells para abrir o arquivo Excel existente. Use o`InputPath` variável para especificar o caminho do arquivo:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Certifique-se de ter substituído`"book1.xls"` com o nome real do seu arquivo Excel.

## Etapa 5: copie a planilha

 Agora copiaremos a planilha existente para uma nova planilha. Use o`Worksheets` propriedade do`Workbook` objeto para acessar a coleção de planilhas:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Então use o`AddCopy` método para copiar a planilha especificada. Por exemplo, para copiar "Folha1":

```csharp
sheets.AddCopy("Sheet1");
```

## Etapa 6: salve o arquivo Excel

 Use o`Save` método do`Workbook` objeto para salvar as alterações em um novo arquivo:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Certifique-se de especificar o caminho e o nome de arquivo desejados para o arquivo de saída.

### Exemplo de código-fonte para planilha de cópia do Excel usando Aspose.Cells for .NET 

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Abra um arquivo Excel existente.
Workbook wb = new Workbook(InputPath);
// Crie um objeto Planilhas com referência a
// as planilhas da apostila.
WorksheetCollection sheets = wb.Worksheets;
// Copiar dados para uma nova planilha de uma existente
// planilha dentro da pasta de trabalho.
sheets.AddCopy("Sheet1");
// Salve o arquivo Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Conclusão

Parabéns! Agora você aprendeu como copiar uma planilha do Excel usando Aspose.Cells for .NET. Este guia passo a passo mostrou como importar as bibliotecas necessárias, carregar um arquivo Excel existente, copiar a planilha e salvar o arquivo modificado. Sinta-se à vontade para usar esse método em seus próprios projetos para manipular arquivos Excel com eficiência.

### Perguntas frequentes

#### P. O Aspose.Cells é compatível com outras linguagens de programação?

A. Sim, Aspose.Cells oferece suporte a várias linguagens de programação, incluindo C#, Java, Python e muito mais.

#### P. Posso copiar uma planilha para outra pasta de trabalho do Excel?

A.  Sim, você pode usar o`AddCopy` método para copiar uma planilha para outra pasta de trabalho do Excel.

#### P. O Aspose.Cells preserva fórmulas e formatação ao copiar a planilha?

A. Sim, Aspose.Cells preserva fórmulas, formatação e outras propriedades ao copiar uma planilha.

#### P. O Aspose.Cells requer uma licença para uso comercial?

A. Sim, Aspose.Cells é um produto comercial e requer a compra de uma licença para uso comercial. Você pode encontrar mais informações de licenciamento no site oficial da Aspose.