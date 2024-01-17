---
title: Remover painéis da planilha
linktitle: Remover painéis da planilha
second_title: Referência da API Aspose.Cells para .NET
description: Guia passo a passo para remover painéis de uma planilha do Excel usando Aspose.Cells for .NET.
type: docs
weight: 120
url: /pt/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
Neste tutorial, explicaremos como remover painéis de uma planilha do Excel usando Aspose.Cells for .NET. Siga estas etapas para obter o resultado desejado:

## Passo 1: Configurando o ambiente

Certifique-se de ter instalado o Aspose.Cells for .NET e configurado seu ambiente de desenvolvimento. Além disso, certifique-se de ter uma cópia do arquivo Excel do qual deseja remover os painéis.

## Passo 2: Importe as dependências necessárias

Adicione as diretivas necessárias para usar as classes de Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Etapa 3: inicialização do código

Comece inicializando o caminho para o diretório que contém seus documentos Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Etapa 4: abrindo o arquivo Excel

 Instanciar um novo`Workbook` objeto e abra o arquivo Excel usando o`Open` método:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Passo 5: Defina a célula ativa

 Defina a célula ativa da planilha usando o`ActiveCell` propriedade:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Etapa 6: Excluindo os painéis

 Remova painéis da janela da planilha usando o`RemoveSplit` método:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Etapa 7: salvando alterações

Salve as alterações feitas no arquivo Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Exemplo de código-fonte para remover painéis da planilha usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instancie uma nova pasta de trabalho e abra um arquivo de modelo
Workbook book = new Workbook(dataDir + "Book1.xls");
// Defina a célula ativa
book.Worksheets[0].ActiveCell = "A20";
// Dividir a janela da planilha
book.Worksheets[0].RemoveSplit();
// Salve o arquivo Excel
book.Save(dataDir + "output.xls");
```

## Conclusão

Neste tutorial, você aprendeu como remover painéis de uma planilha do Excel usando Aspose.Cells for .NET. Seguindo as etapas descritas, você pode personalizar facilmente a aparência e o comportamento dos seus arquivos Excel.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca de software popular para manipulação de arquivos Excel em aplicativos .NET.

#### Como posso definir a célula ativa de uma planilha em Aspose.Cells?

 Você pode definir a célula ativa usando o`ActiveCell`propriedade do objeto Planilha.

#### Posso remover apenas painéis horizontais ou verticais da janela da planilha?

 Sim, usando Aspose.Cells você pode remover apenas painéis horizontais ou verticais usando os métodos apropriados, como`RemoveHorizontalSplit` ou`RemoveVerticalSplit`.

#### O Aspose.Cells funciona apenas com arquivos Excel no formato .xls?

Não, Aspose.Cells suporta vários formatos de arquivo Excel, incluindo .xls e .xlsx.
	