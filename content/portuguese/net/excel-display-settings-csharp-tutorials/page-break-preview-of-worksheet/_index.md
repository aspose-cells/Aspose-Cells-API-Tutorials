---
title: Visualização da quebra de página da planilha
linktitle: Visualização da quebra de página da planilha
second_title: Referência da API Aspose.Cells para .NET
description: Guia passo a passo para mostrar a visualização da quebra de página da planilha usando Aspose.Cells for .NET.
type: docs
weight: 110
url: /pt/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
Neste tutorial, vamos explicar como mostrar a visualização da quebra de página de uma planilha usando Aspose.Cells for .NET. Siga estas etapas para obter o resultado desejado:

## Passo 1: Configurando o ambiente

Certifique-se de ter instalado o Aspose.Cells for .NET e configurado seu ambiente de desenvolvimento. Além disso, certifique-se de ter uma cópia do arquivo Excel no qual deseja exibir a visualização da quebra de página.

## Passo 2: Importe as dependências necessárias

Adicione as diretivas necessárias para usar as classes de Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Etapa 3: inicialização do código

Comece inicializando o caminho para o diretório que contém seus documentos Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Etapa 4: abrindo o arquivo Excel

 Criar uma`FileStream` objeto que contém o arquivo Excel a ser aberto:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Instanciar um`Workbook` objeto e abra o arquivo Excel usando o fluxo de arquivos:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Etapa 5: acessando a planilha

Navegue até a primeira planilha do arquivo Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Etapa 6: exibindo a visualização página por página

Ative a visualização página por página da planilha:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Etapa 7: salvando alterações

Salve as alterações feitas no arquivo Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Etapa 8: Fechando o fluxo de arquivos

Feche o fluxo de arquivos para liberar todos os recursos:

```csharp
fstream.Close();
```

### Exemplo de código-fonte para visualização de quebra de página da planilha usando Aspose.Cells for .NET 
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
// Exibindo a planilha na visualização de quebra de página
worksheet.IsPageBreakPreview = true;
// Salvando o arquivo Excel modificado
workbook.Save(dataDir + "output.xls");
// Fechando o fluxo de arquivos para liberar todos os recursos
fstream.Close();
```

## Conclusão

Neste tutorial, você aprendeu como exibir a visualização da quebra de página de uma planilha usando Aspose.Cells for .NET. Seguindo as etapas descritas, você pode controlar facilmente a aparência e o layout dos seus arquivos Excel.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca de software popular para manipulação de arquivos Excel em aplicativos .NET.

#### Posso mostrar a visualização página por página de uma planilha específica em vez de toda a planilha?

Sim, usando Aspose.Cells você pode habilitar a visualização da quebra de página para uma planilha específica acessando o objeto Worksheet correspondente.

#### O Aspose.Cells oferece suporte a outros recursos de edição de arquivos do Excel?

Sim, Aspose.Cells oferece uma ampla gama de recursos para edição e manipulação de arquivos Excel, como adição de dados, formatação, criação de gráficos, etc.

#### O Aspose.Cells funciona apenas com arquivos Excel no formato .xls?

Não, Aspose.Cells suporta vários formatos de arquivo Excel, incluindo .xls e .xlsx.
	