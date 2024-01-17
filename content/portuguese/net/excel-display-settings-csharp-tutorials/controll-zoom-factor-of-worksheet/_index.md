---
title: Controlar o fator de zoom da planilha
linktitle: Controlar o fator de zoom da planilha
second_title: Referência da API Aspose.Cells para .NET
description: Controle o fator de zoom da planilha do Excel com Aspose.Cells for .NET.
type: docs
weight: 20
url: /pt/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
Controlar o fator de zoom de uma planilha é um recurso essencial ao trabalhar com arquivos Excel usando a biblioteca Aspose.Cells para .NET. Neste guia, mostraremos como usar Aspose.Cells para controlar o fator de zoom de uma planilha usando código-fonte C# passo a passo.

## Etapa 1: importar as bibliotecas necessárias

Antes de começar, certifique-se de ter instalado a biblioteca Aspose.Cells para .NET e importe as bibliotecas necessárias para o seu projeto C#.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## Etapa 2: definir o caminho do diretório e abrir o arquivo Excel

 Para começar, defina o caminho para o diretório que contém o arquivo Excel e abra-o usando um`FileStream` objeto e instanciar um`Workbook` objeto para representar a pasta de trabalho do Excel.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Passo 3: Acesse a planilha e altere o fator de zoom

Nesta etapa, acessamos a primeira planilha da pasta de trabalho do Excel usando o índice`0` e defina o fator de zoom da planilha como`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## Etapa 4: salve as alterações e feche o arquivo

 Depois de alterar o fator de zoom da planilha, salvamos as alterações no arquivo Excel usando o`Save` método do`Workbook` objeto. Em seguida, fechamos o fluxo de arquivos para liberar todos os recursos usados.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### Exemplo de código-fonte para Controll Zoom Factor Of Worksheet usando Aspose.Cells for .NET 

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
// Configurando o fator de zoom da planilha para 75
worksheet.Zoom = 75;
// Salvando o arquivo Excel modificado
workbook.Save(dataDir + "output.xls");
// Fechando o fluxo de arquivos para liberar todos os recursos
fstream.Close();
```

## Conclusão

Este guia passo a passo mostrou como controlar o fator de zoom de uma planilha usando Aspose.Cells for .NET. Usando o código-fonte C# fornecido, você pode ajustar facilmente o fator de zoom de uma planilha em seus aplicativos .NET.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca de arquivamento rica em recursos para manipulação de arquivos Excel em aplicativos .NET.

#### Como posso instalar o Aspose.Cells para .NET?

 Para instalar o Aspose.Cells for .NET, você precisa baixar o pacote NuGet correspondente em[Aspose Lançamentos](https://releases/aspose.com/cells/net/) e adicione-o ao seu projeto .NET.

#### Quais recursos o Aspose.Cells for .NET oferece?

Aspose.Cells for .NET oferece recursos como criação, edição, conversão e manipulação avançada de arquivos Excel.

#### Quais formatos de arquivo são suportados pelo Aspose.Cells for .NET?

Aspose.Cells for .NET suporta vários formatos de arquivo, incluindo XLSX, XLSM, CSV, HTML, PDF e muitos mais.
