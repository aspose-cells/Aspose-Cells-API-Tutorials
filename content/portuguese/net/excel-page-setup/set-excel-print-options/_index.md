---
title: Definir opções de impressão do Excel
linktitle: Definir opções de impressão do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda a manipular arquivos Excel e personalizar opções de impressão com facilidade usando Aspose.Cells for .NET.
type: docs
weight: 150
url: /pt/net/excel-page-setup/set-excel-print-options/
---
Neste guia, orientaremos você sobre como definir opções de impressão para uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Orientaremos você passo a passo pelo código-fonte C# fornecido para realizar essa tarefa.

## Passo 1: Configurando o ambiente

Antes de começar, certifique-se de ter configurado seu ambiente de desenvolvimento e instalado o Aspose.Cells for .NET. Você pode baixar a versão mais recente da biblioteca no site oficial do Aspose.

## Etapa 2: importar namespaces necessários

No seu projeto C#, importe os namespaces necessários para trabalhar com Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Etapa 3: definir o caminho para o diretório de documentos

 Declarar um`dataDir` variável para especificar o caminho para o diretório onde deseja salvar o arquivo Excel gerado:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Certifique-se de substituir`"YOUR_DOCUMENT_DIRECTORY"` com o caminho correto em seu sistema.

## Etapa 4: Criando um objeto de pasta de trabalho

Instancie um objeto Workbook que representa a pasta de trabalho do Excel que você deseja criar:

```csharp
Workbook workbook = new Workbook();
```

## Etapa 5: Obtendo a referência PageSetup da planilha

Para definir as opções de impressão, primeiro precisamos obter a referência PageSetup da planilha. Use o seguinte código para obter a referência:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Etapa 6: ativar a impressão de linhas de grade

Para permitir a impressão de linhas de grade, use o seguinte código:

```csharp
pageSetup. PrintGridlines = true;
```

## Etapa 7: Habilitar impressão de cabeçalho de linha/coluna

Para habilitar a impressão de cabeçalhos de linhas e colunas, use o seguinte código:

```csharp
pageSetup.PrintHeadings = true;
```

## Etapa 8: ativar o modo de impressão em preto e branco

Para habilitar a impressão da planilha no modo preto e branco, utilize o seguinte código:

```csharp
pageSetup.BlackAndWhite = true;
```

## Etapa 9: Habilitando a impressão de comentários

Para permitir que os comentários sejam impressos conforme aparecem na planilha, use o seguinte código:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Etapa 10: ativar impressão em modo rascunho

Para habilitar a impressão da planilha em modo rascunho, use o seguinte código:

```csharp
pageSetup.PrintDraft = true;
```

## Etapa 11: ativar a impressão de erros de células como N/A

Para permitir que erros de célula sejam impressos como

  que N/A, use o seguinte código:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Etapa 12: Salvando a pasta de trabalho do Excel

 Para salvar a pasta de trabalho do Excel com as opções de impressão definidas, use o`Save` método do objeto Workbook:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Isso salvará a pasta de trabalho do Excel com o nome de arquivo "OtherPrintOptions_out.xls" no diretório especificado.

### Exemplo de código-fonte para definir opções de impressão do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Obtendo a referência do PageSetup da planilha
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Permitindo imprimir linhas de grade
pageSetup.PrintGridlines = true;
// Permitindo imprimir cabeçalhos de linha/coluna
pageSetup.PrintHeadings = true;
// Permitindo imprimir planilha no modo preto e branco
pageSetup.BlackAndWhite = true;
// Permitindo imprimir comentários conforme exibidos na planilha
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Permitindo imprimir planilha com qualidade de rascunho
pageSetup.PrintDraft = true;
// Permitindo imprimir erros de células como N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Salve a pasta de trabalho.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Conclusão

Agora você aprendeu como definir opções de impressão para uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Esta biblioteca poderosa e fácil de usar permite personalizar as configurações de impressão de suas pastas de trabalho do Excel de maneira fácil e eficiente.

### Perguntas frequentes


#### 1. Posso personalizar ainda mais as opções de impressão, como margens ou orientação da página?

Sim, Aspose.Cells for .NET oferece uma ampla gama de opções de impressão personalizáveis, como margens, orientação da página, escala, etc.

#### 2. O Aspose.Cells for .NET oferece suporte a outros formatos de arquivo Excel?

Sim, Aspose.Cells for .NET suporta uma variedade de formatos de arquivo Excel, como XLSX, XLS, CSV, HTML, PDF, etc.

#### 3. O Aspose.Cells for .NET é compatível com todas as versões do .NET Framework?

Aspose.Cells for .NET é compatível com .NET Framework 2.0 ou posterior, incluindo versões 3.5, 4.0, 4.5, 4.6, etc.