---
title: Exibir e ocultar linhas de grade da planilha
linktitle: Exibir e ocultar linhas de grade da planilha
second_title: Referência da API Aspose.Cells para .NET
description: Controle a exibição de linhas de grade na planilha do Excel com Aspose.Cells for .NET.
type: docs
weight: 30
url: /pt/net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
Neste tutorial, mostraremos como mostrar e ocultar linhas de grade em uma planilha do Excel usando código-fonte C# com Aspose.Cells for .NET. Siga as etapas abaixo para obter o resultado desejado.

## Passo 1: Importe as bibliotecas necessárias

Certifique-se de ter instalado a biblioteca Aspose.Cells para .NET e importe as bibliotecas necessárias para o seu projeto C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Etapa 2: definir o caminho do diretório e abrir o arquivo Excel

 Defina o caminho para o diretório que contém seu arquivo Excel e abra o arquivo criando um fluxo de arquivos e instanciando um`Workbook` objeto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Etapa 3: vá para a primeira planilha e oculte as linhas de grade

 Acesse a primeira planilha do arquivo Excel usando o`Worksheets` propriedade do`Workbook` objeto. Então use o`IsGridlinesVisible` propriedade do`Worksheet` objeto para ocultar as linhas de grade.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## Etapa 4: salvar alterações

 Depois de fazer as alterações necessárias, salve o arquivo Excel modificado usando o`Save` método do`Workbook` objeto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exemplo de código-fonte para exibir e ocultar linhas de grade da planilha usando Aspose.Cells for .NET 

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Criando um fluxo de arquivos contendo o arquivo Excel a ser aberto
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciando um objeto Workbook
// Abrindo o arquivo Excel por meio do fluxo de arquivos
Workbook workbook = new Workbook(fstream);
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ocultando as linhas de grade da primeira planilha do arquivo Excel
worksheet.IsGridlinesVisible = false;
// Salvando o arquivo Excel modificado
workbook.Save(dataDir + "output.xls");
// Fechando o fluxo de arquivos para liberar todos os recursos
fstream.Close();
```

## Conclusão

Este guia passo a passo mostrou como mostrar e ocultar linhas de grade em uma planilha do Excel usando Aspose.Cells for .NET. Usando o código-fonte C# fornecido, você pode personalizar facilmente a exibição de linhas de grade em seus arquivos Excel.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca poderosa para manipular arquivos Excel em aplicativos .NET.

#### Como posso instalar o Aspose.Cells para .NET?

 Para instalar o Aspose.Cells for .NET, você precisa baixar o pacote relevante em[Aspose Lançamentos](https://releases/aspose.com/cells/net/) e adicione-o ao seu projeto .NET.

#### Como posso mostrar ou ocultar linhas de grade em uma planilha do Excel com Aspose.Cells for .NET?

 Você pode usar o`IsGridlinesVisible` propriedade do`Worksheet` objeto para mostrar ou ocultar linhas de grade. Defina-o para`true` para mostrá-los e para`false` para escondê-los.

#### Quais outros formatos de arquivo Excel são suportados pelo Aspose.Cells for .NET?

Aspose.Cells for .NET suporta vários formatos de arquivo Excel, como XLS, XLSX, CSV, HTML, PDF e muitos mais.

