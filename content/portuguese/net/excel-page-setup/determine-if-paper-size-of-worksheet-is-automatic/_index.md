---
title: Determine se o tamanho do papel da planilha é automático
linktitle: Determine se o tamanho do papel da planilha é automático
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como determinar se o tamanho do papel de uma planilha é automático com Aspose.Cells for .NET.
type: docs
weight: 20
url: /pt/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
Neste artigo, iremos guiá-lo passo a passo para explicar o seguinte código-fonte C#: Determine se o tamanho do papel de uma planilha é automático usando Aspose.Cells for .NET. Usaremos a biblioteca Aspose.Cells para .NET para realizar esta operação. Siga as etapas abaixo para determinar se o tamanho do papel de uma planilha é automático.

## Etapa 1: carregar pastas de trabalho
A primeira etapa é carregar as pastas de trabalho. Teremos duas pastas de trabalho: uma com tamanho automático de papel desabilitado e outra com tamanho automático de papel habilitado. Aqui está o código para carregar as pastas de trabalho:

```csharp
// diretório de origem
string sourceDir = "YOUR_SOURCE_DIR";
// Diretório de saída
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Carregue a primeira pasta de trabalho com o tamanho automático do papel desativado
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Carregue a segunda pasta de trabalho com o tamanho automático de papel ativado
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Passo 2: Acessando Planilhas
Agora que carregamos as pastas de trabalho, precisamos acessar as planilhas para verificar o tamanho automático do papel. Iremos para a primeira planilha das duas apostilas. Aqui está o código para acessá-lo:

```csharp
//Vá para a primeira planilha da primeira pasta de trabalho
Worksheet ws11 = wb1.Worksheets[0];

// Vá para a primeira planilha da segunda pasta de trabalho
Worksheet ws12 = wb2.Worksheets[0];
```

## Etapa 3: Verifique o tamanho automático do papel
 Nesta etapa verificaremos se o tamanho do papel da planilha é automático. Usaremos o`PageSetup.IsAutomaticPaperSize` propriedade para obter essas informações. Em seguida, exibiremos o resultado. Aqui está o código para isso:

```csharp
// Exibir a propriedade IsAutomaticPaperSize da primeira planilha na primeira pasta de trabalho
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Exibir a propriedade IsAutomaticPaperSize da primeira planilha na segunda pasta de trabalho
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Exemplo de código-fonte para determinar se o tamanho do papel da planilha é automático usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Diretório de saída
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Carregue a primeira pasta de trabalho com tamanho de papel automático falso
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Carregue a segunda pasta de trabalho com tamanho de papel automático verdadeiro
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Acesse a primeira planilha de ambas as pastas de trabalho
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Imprima a propriedade PageSetup.IsAutomaticPaperSize de ambas as planilhas
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Conclusão
Neste artigo, aprendemos como determinar se o tamanho do papel de uma planilha é automático usando Aspose.Cells for .NET. Seguimos os seguintes passos: carregar as pastas de trabalho,

acesso a planilhas e verificação automática de tamanho de papel. Agora você pode usar esse conhecimento para determinar se o tamanho do papel de suas planilhas é automático.

### Perguntas frequentes

#### P: Como posso carregar pastas de trabalho com Aspose.Cells for .NET?

R: Você pode carregar pastas de trabalho usando a classe Workbook da biblioteca Aspose.Cells. Use o método Workbook.Load para carregar uma pasta de trabalho de um arquivo.

#### P: Posso verificar o tamanho automático do papel para outras planilhas?

R: Sim, você pode verificar o tamanho automático do papel de qualquer planilha acessando a propriedade PageSetup.IsAutomaticPaperSize do objeto Worksheet correspondente.

#### P: Como posso alterar o tamanho automático do papel de uma planilha?

R: Para alterar o tamanho automático do papel de uma planilha, você pode usar a propriedade PageSetup.IsAutomaticPaperSize e configurá-la para o valor desejado (verdadeiro ou falso).

#### P: Que outros recursos o Aspose.Cells for .NET oferece?

R: Aspose.Cells for .NET oferece muitos recursos para trabalhar com planilhas, como criação, modificação e conversão de pastas de trabalho, bem como manipulação de dados, fórmulas e formatação.