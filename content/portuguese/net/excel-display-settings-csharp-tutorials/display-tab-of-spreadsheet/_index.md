---
title: Exibir guia da planilha
linktitle: Exibir guia da planilha
second_title: Referência da API Aspose.Cells para .NET
description: Exiba uma guia de planilha do Excel usando Aspose.Cells for .NET.
type: docs
weight: 60
url: /pt/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
Neste tutorial, mostraremos como exibir a guia de uma planilha do Excel usando código-fonte C# com Aspose.Cells for .NET. Siga as etapas abaixo para obter o resultado desejado.

## Passo 1: Importe as bibliotecas necessárias

Certifique-se de ter instalado a biblioteca Aspose.Cells para .NET e importe as bibliotecas necessárias para o seu projeto C#.

```csharp
using Aspose.Cells;
```

## Etapa 2: definir o caminho do diretório e abrir o arquivo Excel

 Defina o caminho para o diretório que contém seu arquivo Excel e abra o arquivo instanciando um`Workbook` objeto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Etapa 3: mostrar a guia da planilha

 Use o`ShowTabs` propriedade do`Workbook.Settings` objeto para mostrar a guia da planilha do Excel.

```csharp
workbook.Settings.ShowTabs = true;
```

## Etapa 4: salvar alterações

 Depois de fazer as alterações necessárias, salve o arquivo Excel modificado usando o`Save` método do`Workbook` objeto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exemplo de código-fonte para exibir guia da planilha usando Aspose.Cells for .NET 

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
// Abrindo o arquivo Excel
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Ocultando as guias do arquivo Excel
workbook.Settings.ShowTabs = true;
// Salvando o arquivo Excel modificado
workbook.Save(dataDir + "output.xls");
```

### Conclusão

Este guia passo a passo mostrou como mostrar a guia de uma planilha do Excel usando Aspose.Cells for .NET. Usando o código-fonte C# fornecido, você pode personalizar facilmente a exibição de guias em seus arquivos Excel.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca poderosa para manipular arquivos Excel em aplicativos .NET.

#### Como posso instalar o Aspose.Cells para .NET?

 Para instalar o Aspose.Cells for .NET, você precisa baixar o pacote relevante em[Aspose Lançamentos](https://releases/aspose.com/cells/net/) e adicione-o ao seu projeto .NET.

#### Como exibir a aba de uma planilha Excel usando Aspose.Cells for .NET?

 Você pode usar o`ShowTabs` propriedade do`Workbook.Settings` objeto e configurá-lo para`true` para mostrar a guia da planilha.

#### Quais outros formatos de arquivo Excel são suportados pelo Aspose.Cells for .NET?

Aspose.Cells for .NET suporta uma variedade de formatos de arquivo Excel, como XLS, XLSX, CSV, HTML, PDF, etc.
