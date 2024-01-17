---
title: Definir o número da primeira página do Excel
linktitle: Definir o número da primeira página do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como definir o número da primeira página no Excel usando Aspose.Cells for .NET.
type: docs
weight: 90
url: /pt/net/excel-page-setup/set-excel-first-page-number/
---
Neste tutorial, orientaremos você sobre como definir o número da primeira página no Excel usando Aspose.Cells for .NET. Usaremos o código-fonte C# para ilustrar o processo.

## Passo 1: Configurando o ambiente

Certifique-se de ter o Aspose.Cells for .NET instalado em sua máquina. Crie também um novo projeto em seu ambiente de desenvolvimento preferido.

## Etapa 2: importe as bibliotecas necessárias

Em seu arquivo de código, importe as bibliotecas necessárias para trabalhar com Aspose.Cells. Aqui está o código correspondente:

```csharp
using Aspose.Cells;
```

## Etapa 3: definir diretório de dados

Defina o diretório de dados onde deseja salvar o arquivo Excel modificado. Use o seguinte código:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Certifique-se de especificar o caminho completo do diretório.

## Etapa 4: Criando a pasta de trabalho e a planilha

Crie um novo objeto Workbook e navegue até a primeira planilha da pasta de trabalho usando o seguinte código:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Isso criará uma pasta de trabalho vazia com uma planilha.

## Passo 5: Definir o número da primeira página

Defina o número da primeira página das páginas da planilha usando o seguinte código:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Isso definirá o número da primeira página como 2.

## Etapa 6: salvando a pasta de trabalho modificada

Salve a pasta de trabalho modificada usando o seguinte código:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Isso salvará a pasta de trabalho modificada no diretório de dados especificado.

### Exemplo de código-fonte para definir o número da primeira página do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = workbook.Worksheets[0];
// Configurando o número da primeira página das páginas da planilha
worksheet.PageSetup.FirstPageNumber = 2;
// Salve a pasta de trabalho.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Conclusão

Agora você aprendeu como definir o número da primeira página no Excel usando Aspose.Cells for .NET. Este tutorial orientou você em todas as etapas do processo, desde a configuração do ambiente até a definição do número da primeira página. Agora você pode usar esse conhecimento para personalizar a numeração de páginas em seus arquivos Excel.

### Perguntas frequentes

#### Q1: Posso definir um número de primeira página diferente para cada planilha?

 A1: Sim, você pode definir um número de primeira página diferente para cada planilha acessando o`FirstPageNumber`propriedade da respectiva planilha`PageSetup` objeto.

#### P2: Como posso verificar o número da primeira página de uma planilha existente?

 A2: Você pode verificar o número da primeira página de uma planilha existente acessando o`FirstPageNumber` propriedade do`PageSetup` objeto correspondente a essa planilha.

#### Q3: A numeração de páginas sempre começa em 1 por padrão?

A3: Sim, a numeração das páginas começa em 1 por padrão no Excel. No entanto, você pode usar o código mostrado neste tutorial para definir um número de primeira página diferente.

#### P4: As alterações no número da primeira página são permanentes no arquivo Excel editado?

A4: Sim, as alterações feitas no número da primeira página são salvas permanentemente no arquivo Excel modificado.

#### P5: Este método funciona para todos os formatos de arquivo Excel, como .xls e .xlsx?

A5: Sim, este método funciona para todos os formatos de arquivo Excel suportados pelo Aspose.Cells, incluindo .xls e .xlsx.