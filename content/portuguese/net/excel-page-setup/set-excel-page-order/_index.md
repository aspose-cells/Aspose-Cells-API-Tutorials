---
title: Definir ordem das páginas do Excel
linktitle: Definir ordem das páginas do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Guia passo a passo para definir a ordem das páginas no Excel usando Aspose.Cells for .NET. Instruções detalhadas e código fonte incluídos.
type: docs
weight: 120
url: /pt/net/excel-page-setup/set-excel-page-order/
---
Neste artigo, iremos guiá-lo passo a passo para explicar o seguinte código-fonte C# para definir a ordem das páginas do Excel usando Aspose.Cells for .NET. Mostraremos como configurar o diretório de documentos, instanciar um objeto Workbook, obter a referência PageSetup, definir a ordem de impressão da página e salvar a pasta de trabalho.

## Etapa 1: configuração do diretório de documentos

 Antes de começar, você precisa configurar o diretório do documento onde deseja salvar o arquivo Excel. Você pode especificar o caminho do diretório substituindo o valor do`dataDir` variável com seu próprio caminho.

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Etapa 2: instanciando um objeto de pasta de trabalho

A primeira etapa é instanciar um objeto Workbook. Isso representa a pasta de trabalho do Excel com a qual trabalharemos.

```csharp
// Instanciar um objeto Workbook
Workbook workbook = new Workbook();
```

## Etapa 3: Obtendo a referência PageSetup

Em seguida, precisamos obter a referência do objeto PageSetup da planilha na qual queremos definir a ordem das páginas.

```csharp
// Obtenha a referência PageSetup da planilha
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Etapa 4: definir a ordem de impressão das páginas

Agora podemos definir a ordem de impressão das páginas. Neste exemplo, estamos usando a opção “OverThenDown”, o que significa que as páginas serão impressas da esquerda para a direita e depois de cima para baixo.

```csharp
// Defina a ordem de impressão da página como "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Etapa 5: salvando a pasta de trabalho

Por fim, salvamos a pasta de trabalho do Excel com as alterações na ordem das páginas.

```csharp
// Salve a pasta de trabalho
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Exemplo de código-fonte para definir a ordem das páginas do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Obtendo a referência do PageSetup da planilha
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Definir a ordem de impressão das páginas para cima e para baixo
pageSetup.Order = PrintOrderType.OverThenDown;
// Salve a pasta de trabalho.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Conclusão

Neste tutorial, explicamos como definir a ordem das páginas em um arquivo Excel usando Aspose.Cells for .NET. Seguindo as etapas fornecidas, você pode configurar facilmente o diretório do documento, instanciar um objeto Workbook, obter a referência PageSetup, definir a ordem de impressão da página e salvar a pasta de trabalho.

### Perguntas frequentes

#### Q1: Por que é importante definir a ordem das páginas em um arquivo Excel?

Definir a ordem das páginas em um arquivo Excel é importante porque determina como as páginas serão impressas ou exibidas. Ao especificar uma ordem específica, você pode organizar os dados de forma lógica e facilitar a leitura ou impressão do arquivo.

#### Q2: Posso usar outros pedidos de impressão de páginas com Aspose.Cells for .NET?

Sim, Aspose.Cells for .NET suporta pedidos de impressão de múltiplas páginas, como "DownThenOver", "OverThenDown", "DownThenOverThenDownAgain", etc.

#### Q3: Posso definir opções adicionais para imprimir páginas com Aspose.Cells for .NET?

Sim, você pode definir várias opções de impressão de página, como escala, orientação, margens, etc., usando as propriedades do objeto PageSetup em Aspose.Cells for .NET.

#### Q4: O Aspose.Cells for .NET oferece suporte a outros formatos de arquivo Excel?

Sim, Aspose.Cells for .NET suporta uma ampla variedade de formatos de arquivo Excel, como XLSX, XLS, CSV, HTML, PDF, etc.