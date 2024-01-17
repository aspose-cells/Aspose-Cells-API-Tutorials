---
title: Definir título de impressão do Excel
linktitle: Definir título de impressão do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda a manipular facilmente arquivos Excel e personalizar opções de impressão usando Aspose.Cells for .NET.
type: docs
weight: 170
url: /pt/net/excel-page-setup/set-excel-print-title/
---
Neste guia, orientaremos você sobre como definir títulos de impressão em uma planilha do Excel usando Aspose.Cells for .NET. Siga as etapas abaixo para realizar esta tarefa.

## Passo 1: Configurando o ambiente

Certifique-se de ter configurado seu ambiente de desenvolvimento e instalado o Aspose.Cells for .NET. Você pode baixar a versão mais recente da biblioteca no site oficial do Aspose.

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

## Passo 5: Acesso à primeira planilha

Navegue até a primeira planilha da pasta de trabalho do Excel usando o seguinte código:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Etapa 6: Definindo Colunas de Título

Defina as colunas de título usando o seguinte código:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Aqui definimos as colunas A e B como colunas de título. Você pode ajustar esse valor de acordo com suas necessidades.

## Passo 7: Definindo Linhas de Título

Defina as linhas de título usando o seguinte código:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Definimos as linhas 1 e 2 como linhas de título. Você pode ajustar esses valores de acordo com suas necessidades.

## Etapa 8: Salvando a pasta de trabalho do Excel

 Para salvar a pasta de trabalho do Excel com os títulos de impressão definidos, use o`Save` método do objeto Workbook:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Isso salvará a pasta de trabalho do Excel com o nome de arquivo "SetPrintTitle_out.xls" no diretório especificado.

### Exemplo de código-fonte para definir título de impressão do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Obtendo a referência do PageSetup da planilha
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Definindo os números das colunas A e B como colunas de título
pageSetup.PrintTitleColumns = "$A:$B";
// Definindo os números das linhas 1 e 2 como linhas de título
pageSetup.PrintTitleRows = "$1:$2";
// Salve a pasta de trabalho.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Conclusão

Parabéns! Você aprendeu como definir títulos de impressão em uma planilha do Excel usando Aspose.Cells for .NET. Os títulos impressos permitem exibir linhas e colunas específicas em cada página impressa, facilitando a leitura e a referência dos dados.

### Perguntas frequentes

#### 1. Posso definir títulos de impressão para colunas específicas no Excel?

 Sim, com Aspose.Cells for .NET você pode definir colunas específicas como títulos de impressão usando o`PrintTitleColumns` propriedade do`PageSetup` objeto.

#### 2. É possível definir títulos de colunas e imprimir títulos de linhas?

 Sim, você pode definir títulos de colunas e linhas de impressão usando o`PrintTitleColumns` e`PrintTitleRows` propriedades do`PageSetup` objeto.

#### 3. Que outras configurações de layout posso personalizar com Aspose.Cells for .NET?

Com Aspose.Cells for .NET, você pode personalizar várias configurações de layout de página, como margens, orientação de página, escala de impressão e muito mais.