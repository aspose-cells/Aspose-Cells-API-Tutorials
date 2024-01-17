---
title: Copiar configurações de configuração de página de outra planilha
linktitle: Copiar configurações de configuração de página de outra planilha
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como copiar as configurações da página de uma planilha para outra usando Aspose.Cells for .NET. Um guia passo a passo para otimizar o uso desta biblioteca.
type: docs
weight: 10
url: /pt/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Neste artigo, iremos guiá-lo passo a passo para explicar o seguinte código-fonte C#: Copie as configurações da página de outra planilha usando Aspose.Cells for .NET. Usaremos a biblioteca Aspose.Cells para .NET para realizar esta operação. Se quiser copiar as configurações de página de uma planilha para outra, siga as etapas abaixo.

## Etapa 1: Criando a pasta de trabalho
primeiro passo é criar uma pasta de trabalho. No nosso caso, usaremos a classe Workbook fornecida pela biblioteca Aspose.Cells. Aqui está o código para criar uma pasta de trabalho:

```csharp
Workbook wb = new Workbook();
```

## Etapa 2: adicionar planilhas de teste
Depois de criar a pasta de trabalho, precisamos adicionar planilhas de teste. Neste exemplo, adicionaremos duas planilhas. Aqui está o código para adicionar duas planilhas:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Etapa 3: acessando planilhas
Agora que adicionamos as planilhas, precisamos acessá-las para poder alterar suas configurações. Acessaremos as planilhas "TestSheet1" e "TestSheet2" usando seus nomes. Aqui está o código para acessá-lo:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Etapa 4: definir o tamanho do papel
 Nesta etapa, definiremos o tamanho do papel da planilha “TestSheet1”. Usaremos o`PageSetup.PaperSize` propriedade para definir o tamanho do papel. Por exemplo, definiremos o tamanho do papel como "PaperA3ExtraTransverse". Aqui está o código para isso:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Etapa 5: copiar configurações de página
Agora copiaremos as configurações da página da planilha "TestSheet1" para "TestSheet2". Usaremos o`PageSetup.Copy` método para realizar esta operação. Aqui está o código para isso:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Etapa 6: Imprimindo tamanhos de papel
 Após copiar as configurações de configuração da página, imprimiremos os tamanhos de papel das duas planilhas. Nós vamos usar`Console.WriteLine` para exibir os tamanhos de papel. Aqui está o código para isso:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Exemplo de código-fonte para copiar configurações de página de outra planilha usando Aspose.Cells for .NET 
```csharp
//Criar pasta de trabalho
Workbook wb = new Workbook();
//Adicione duas planilhas de teste
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Acesse ambas as planilhas como TestSheet1 e TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Defina o tamanho do papel de TestSheet1 como PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Imprima o tamanho do papel de ambas as planilhas
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Copie o PageSetup de TestSheet1 para TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Imprima o tamanho do papel de ambas as planilhas
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Conclusão
Neste artigo, aprendemos como copiar as configurações da página de uma planilha para outra usando Aspose.Cells for .NET. Seguimos as seguintes etapas: criação da pasta de trabalho, adição de planilhas de teste, acesso às planilhas, configuração do tamanho do papel, cópia das configurações de página e impressão dos tamanhos do papel. Agora você pode usar esse conhecimento para copiar definições de configuração de página em seus próprios projetos.

### Perguntas frequentes

#### P: Posso copiar definições de configuração de página entre diferentes instâncias de pasta de trabalho?

 R: Sim, você pode copiar configurações de página entre diferentes instâncias de pasta de trabalho usando o`PageSetup.Copy` método da biblioteca Aspose.Cells.

#### P: Posso copiar outras configurações de página, como orientação ou margens?

 R: Sim, você pode copiar outras configurações de página usando o`PageSetup.Copy` método com as opções apropriadas. Por exemplo, você pode copiar a orientação usando`CopyOptions.Orientation` e margens usando`CopyOptions.Margins`.

#### P: Como posso saber quais opções estão disponíveis para tamanho de papel?

R: Você pode verificar a referência da API da biblioteca Aspose.Cells para obter as opções disponíveis para tamanho de papel. Existe um enum chamado`PaperSizeType` que lista os diferentes tamanhos de papel suportados.

#### P: Como posso baixar a biblioteca Aspose.Cells para .NET?

 R: Você pode baixar a biblioteca Aspose.Cells para .NET em[Aspose Lançamentos](https://releases.aspose.com/cells/net). Existem versões de teste gratuitas disponíveis, bem como licenças pagas para uso comercial.

#### P: A biblioteca Aspose.Cells oferece suporte a outras linguagens de programação?

R: Sim, a biblioteca Aspose.Cells oferece suporte a várias linguagens de programação, incluindo C#, Java, Python e muito mais.