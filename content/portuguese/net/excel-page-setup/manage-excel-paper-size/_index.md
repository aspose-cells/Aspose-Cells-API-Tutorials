---
title: Gerenciar tamanho de papel do Excel
linktitle: Gerenciar tamanho de papel do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como gerenciar o tamanho do papel no Excel com Aspose.Cells for .NET. Tutorial passo a passo com código fonte em C#.
type: docs
weight: 70
url: /pt/net/excel-page-setup/manage-excel-paper-size/
---
Neste tutorial, iremos guiá-lo passo a passo sobre como gerenciar o tamanho do papel em um documento Excel usando Aspose.Cells for .NET. Mostraremos como configurar o tamanho do papel usando código-fonte C#.

## Passo 1: Configurando o ambiente

Certifique-se de ter o Aspose.Cells for .NET instalado em sua máquina. Crie também um novo projeto em seu ambiente de desenvolvimento preferido.

## Etapa 2: importe as bibliotecas necessárias

Em seu arquivo de código, importe as bibliotecas necessárias para trabalhar com Aspose.Cells. Aqui está o código correspondente:

```csharp
using Aspose.Cells;
```

## Etapa 3: definir diretório de documentos

Defina o diretório onde está localizado o documento Excel com o qual deseja trabalhar. Use o seguinte código para definir o diretório:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Certifique-se de especificar o caminho completo do diretório.

## Etapa 4: Criando um objeto de pasta de trabalho

O objeto Workbook representa o documento Excel com o qual você trabalhará. Você pode criá-lo usando o seguinte código:

```csharp
Workbook workbook = new Workbook();
```

Isso cria um novo objeto Workbook vazio.

## Passo 5: Acesso à primeira planilha

Para acessar a primeira planilha do documento Excel, utilize o seguinte código:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

Isso permitirá que você trabalhe com a primeira planilha da pasta de trabalho.

## Etapa 6: configuração do tamanho do papel

Use a propriedade PageSetup.PaperSize do objeto Worksheet para definir o tamanho do papel. Neste exemplo, definiremos o tamanho do papel para A4. Aqui está o código correspondente:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

Isso define o tamanho do papel da planilha para A4.

## Passo 7: Salvando a pasta de trabalho

Para salvar alterações na pasta de trabalho, use o método Save() do objeto Workbook. Aqui está o código correspondente:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

Isso salvará a pasta de trabalho com as alterações no diretório especificado.

### Exemplo de código-fonte para gerenciar tamanho de papel do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = workbook.Worksheets[0];
// Configurando o tamanho do papel para A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Salve a pasta de trabalho.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Conclusão

Agora você aprendeu como gerenciar o tamanho do papel em um documento Excel usando Aspose.Cells for .NET. Este tutorial orientou você em todas as etapas do processo, desde a configuração do ambiente até salvar as alterações. Agora você pode usar esse conhecimento para personalizar o tamanho do papel dos seus documentos Excel.

### Perguntas frequentes

#### Q1: Posso definir um tamanho de papel personalizado diferente de A4?

A1: Sim, Aspose.Cells oferece suporte a uma variedade de tamanhos de papel predefinidos, bem como a capacidade de definir um tamanho de papel personalizado especificando as dimensões desejadas.

#### P2: Como posso saber o tamanho atual do papel em um documento Excel?

 A2: Você pode usar o`PageSetup.PaperSize` propriedade do`Worksheet` objeto para obter o tamanho de papel atualmente definido.

#### P3: É possível definir margens extras de página com o tamanho do papel?

 A3: Sim, você pode usar`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` e`PageSetup.BottomMargin` propriedades para definir margens de página adicionais além do tamanho do papel.

#### P4: Este método funciona para todos os formatos de arquivo Excel, como .xls e .xlsx?

A4: Sim, este método funciona para formatos de arquivo .xls e .xlsx.

#### P5: Posso aplicar tamanhos de papel diferentes a planilhas diferentes na mesma pasta de trabalho?

 A5: Sim, você pode aplicar tamanhos de papel diferentes a planilhas diferentes na mesma pasta de trabalho usando o`PageSetup.PaperSize` propriedade de cada planilha.