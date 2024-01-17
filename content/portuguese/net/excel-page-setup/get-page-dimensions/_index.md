---
title: Obtenha as dimensões da página
linktitle: Obtenha as dimensões da página
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como recuperar dimensões de página no Excel usando Aspose.Cells for .NET. Guia passo a passo com código fonte em C#.
type: docs
weight: 40
url: /pt/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET é uma biblioteca poderosa que permite aos desenvolvedores trabalhar com arquivos do Microsoft Excel programaticamente. Ele oferece uma ampla gama de recursos para manipulação de documentos Excel, incluindo a capacidade de obter dimensões de páginas. Neste tutorial, orientaremos você nas etapas para recuperar dimensões de página usando Aspose.Cells for .NET.

## Etapa 1: crie uma instância da classe Workbook

Para começar, precisamos criar uma instância da classe Workbook, que representa a pasta de trabalho do Excel. Isso pode ser conseguido usando o seguinte código:

```csharp
Workbook book = new Workbook();
```

## Passo 2: Acessando a planilha

Em seguida, precisamos navegar até a planilha da pasta de trabalho onde queremos definir as dimensões da página. Neste exemplo, suponha que queiramos trabalhar com a primeira planilha. Podemos acessá-lo usando o seguinte código:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Etapa 3: Defina o tamanho do papel como A2 e imprima a largura e a altura em polegadas

Agora definiremos o tamanho do papel para A2 e imprimiremos a largura e a altura da página em polegadas. Isso pode ser conseguido usando o seguinte código:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Etapa 4: Defina o tamanho do papel como A3 e imprima a largura e a altura em polegadas

A seguir, definiremos o tamanho do papel como A3 e imprimiremos a largura e a altura da página em polegadas. Aqui está o código correspondente:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Etapa 5: Defina o tamanho do papel como A4 e imprima a largura e a altura em polegadas

Agora definiremos o tamanho do papel para A4 e imprimiremos a largura e a altura da página em polegadas. Aqui está o código:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Etapa 6: Defina o tamanho do papel como Carta e imprima a largura e a altura em polegadas

Por fim, definiremos o tamanho do papel como Carta e imprimiremos a largura e a altura da página em polegadas. Aqui está o código:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Exemplo de código-fonte para obter dimensões da página usando Aspose.Cells for .NET 
```csharp
// Crie uma instância da classe Workbook
Workbook book = new Workbook();
// Acesse a primeira planilha
Worksheet sheet = book.Worksheets[0];
// Defina o tamanho do papel como A2 e imprima a largura e a altura do papel em polegadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Defina o tamanho do papel como A3 e imprima a largura e a altura do papel em polegadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Defina o tamanho do papel como A4 e imprima a largura e a altura do papel em polegadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Defina o tamanho do papel como Carta e imprima a largura e a altura do papel em polegadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Conclusão

Parabéns! Você aprendeu como recuperar dimensões de página usando Aspose.Cells for .NET. Este recurso pode ser útil quando você precisa realizar operações específicas com base nas dimensões da página em seus arquivos Excel.

Não se esqueça de explorar mais a documentação do Aspose.Cells para descobrir todos os recursos poderosos que ele oferece.

### Perguntas frequentes

#### 1. Quais outros tamanhos de papel o Aspose.Cells for .NET suporta?

Aspose.Cells for .NET suporta uma variedade de tamanhos de papel, incluindo A1, A5, B4, B5, Executivo, Ofício, Carta e muitos mais. Você pode verificar a documentação para obter a lista completa de tamanhos de papel suportados.

#### 2. Posso definir dimensões de página personalizadas com Aspose.Cells for .NET?

Sim, você pode definir dimensões de página personalizadas especificando a largura e a altura desejadas. Aspose.Cells oferece total flexibilidade para personalizar as dimensões da página de acordo com suas necessidades.

#### 3. Posso obter dimensões de página em unidades diferentes de polegadas?

Sim, Aspose.Cells for .NET permite obter dimensões de página em diferentes unidades, incluindo polegadas, centímetros, milímetros e pontos.

#### 4. O Aspose.Cells for .NET oferece suporte a outros recursos de edição de configurações de página?

Sim, Aspose.Cells oferece uma gama completa de recursos para edição de configurações de página, incluindo configuração de margens, orientação, cabeçalhos e rodapés, etc.