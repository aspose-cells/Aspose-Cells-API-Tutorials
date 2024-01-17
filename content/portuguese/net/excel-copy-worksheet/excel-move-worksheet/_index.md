---
title: Planilha de movimentação do Excel
linktitle: Planilha de movimentação do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Mova facilmente a planilha para uma pasta de trabalho do Excel usando Aspose.Cells for .NET.
type: docs
weight: 40
url: /pt/net/excel-copy-worksheet/excel-move-worksheet/
---
Neste tutorial, orientaremos você nas etapas para mover uma planilha para uma pasta de trabalho do Excel usando a biblioteca Aspose.Cells para .NET. Siga as instruções abaixo para concluir esta tarefa.


## Etapa 1: Preparação

Certifique-se de ter instalado o Aspose.Cells for .NET e criado um projeto C# em seu ambiente de desenvolvimento integrado (IDE) preferido.

## Etapa 2: definir o caminho do diretório do documento

 Declarar um`dataDir` variável e inicialize-a com o caminho para o diretório de documentos. Por exemplo :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Certifique-se de substituir`"YOUR_DOCUMENTS_DIRECTORY"` com o caminho real para o seu diretório.

## Etapa 3: Defina o caminho do arquivo de entrada

 Declarar um`InputPath` variável e inicialize-a com o caminho completo do arquivo Excel existente que você deseja modificar. Por exemplo :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Certifique-se de ter o arquivo Excel`book1.xls` no diretório de documentos ou especifique o nome e o local corretos do arquivo.

## Etapa 4: abra o arquivo Excel

 Use o`Workbook` classe de Aspose.Cells para abrir o arquivo Excel especificado:

```csharp
Workbook wb = new Workbook(InputPath);
```

## Etapa 5: obtenha a coleção de planilhas

 Criar uma`WorksheetCollection` objeto para se referir a planilhas na pasta de trabalho:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Etapa 6: obtenha a primeira planilha

Obtenha a primeira planilha da pasta de trabalho:

```csharp
Worksheet worksheet = sheets[0];
```

## Etapa 7: mover a planilha

 Use o`MoveTo` método para mover a primeira planilha para a terceira posição na pasta de trabalho:

```csharp
worksheet.MoveTo(2);
```

## Etapa 8: salve o arquivo Excel modificado

Salve o arquivo Excel com a planilha movida:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Certifique-se de especificar o caminho e o nome de arquivo desejados para o arquivo de saída.

### Exemplo de código-fonte para planilha de movimentação do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Abra um arquivo Excel existente.
Workbook wb = new Workbook(InputPath);
// Crie um objeto Planilhas com referência a
// as planilhas da apostila.
WorksheetCollection sheets = wb.Worksheets;
// Obtenha a primeira planilha.
Worksheet worksheet = sheets[0];
// Mova a primeira planilha para a terceira posição na pasta de trabalho.
worksheet.MoveTo(2);
// Salve o arquivo Excel.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Conclusão

Parabéns! Agora você aprendeu como mover uma planilha para uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Sinta-se à vontade para usar esse método em seus próprios projetos para manipular arquivos Excel com eficiência.

### Perguntas frequentes

#### P. Posso mover uma planilha para outra posição na mesma pasta de trabalho do Excel?

A.  Sim, você pode mover uma planilha para outra posição na mesma pasta de trabalho do Excel usando`MoveTo` método do objeto Worksheet. Basta especificar o índice da posição de destino na pasta de trabalho.

#### P. Posso mover uma planilha para outra pasta de trabalho do Excel?

A.  Sim, você pode mover uma planilha para outra pasta de trabalho do Excel usando o`MoveTo` método do objeto Planilha. Basta especificar o índice da posição de destino na pasta de trabalho de destino.

#### P. O código-fonte fornecido funciona com outros formatos de arquivo Excel, como XLSX?

A. Sim, o código-fonte fornecido funciona com outros formatos de arquivo Excel, incluindo XLSX. Aspose.Cells for .NET suporta uma variedade de formatos de arquivo Excel, permitindo manipular e mover planilhas para diferentes tipos de arquivo.

#### P. Como posso especificar o caminho e o nome do arquivo de saída ao salvar o arquivo Excel modificado?

A.  Ao salvar o arquivo Excel modificado, use o`Save` método do objeto Workbook especificando o caminho completo e o nome do arquivo de saída. Certifique-se de especificar a extensão de arquivo apropriada, como`.xls` ou`.xlsx`, dependendo do formato de arquivo desejado.