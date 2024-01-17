---
title: Obtenha a largura do papel e a altura da planilha
linktitle: Obtenha a largura do papel e a altura da planilha
second_title: Referência da API Aspose.Cells para .NET
description: Crie um guia passo a passo para explicar o seguinte código-fonte C# para obter a largura e a altura do papel de uma planilha usando Aspose.Cells for .NET.
type: docs
weight: 80
url: /pt/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
Neste tutorial, iremos guiá-lo passo a passo para explicar o seguinte código-fonte C# para obter a largura e a altura do papel de uma planilha usando Aspose.Cells for .NET. Siga os passos abaixo:

## Etapa 1: crie a pasta de trabalho
 Comece criando uma nova pasta de trabalho usando o`Workbook` aula:

```csharp
Workbook wb = new Workbook();
```

## Passo 2: Acesse a primeira planilha
 Em seguida, navegue até a primeira planilha da pasta de trabalho usando o`Worksheet` aula:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Etapa 3: Defina o tamanho do papel como A2 e mostre a largura e a altura do papel em polegadas
 Use o`PaperSize` propriedade do`PageSetup` objeto para definir o tamanho do papel como A2 e, em seguida, use o`PaperWidth` e`PaperHeight` propriedades para obter a largura e a altura do papel, respectivamente. Exiba esses valores usando o`Console.WriteLine` método:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Etapa 4: Repita as etapas para outros tamanhos de papel
Repita as etapas anteriores, alterando o tamanho do papel para A3, A4 e Letter e exibindo os valores de largura e altura do papel para cada tamanho:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Exemplo de código-fonte para obter largura e altura do papel da planilha usando Aspose.Cells for .NET 

```csharp
//Criar pasta de trabalho
Workbook wb = new Workbook();
//Acesse a primeira planilha
Worksheet ws = wb.Worksheets[0];
//Defina o tamanho do papel como A2 e imprima a largura e a altura do papel em polegadas
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Defina o tamanho do papel como A3 e imprima a largura e a altura do papel em polegadas
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Defina o tamanho do papel como A4 e imprima a largura e a altura do papel em polegadas
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Defina o tamanho do papel como Carta e imprima a largura e a altura do papel em polegadas
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Conclusão

Você aprendeu como usar Aspose.Cells for .NET para obter a largura e a altura do papel de uma planilha. Este recurso pode ser útil para a configuração e layout preciso de seus documentos Excel.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca poderosa para manipular e processar arquivos Excel em aplicativos .NET. Oferece muitos recursos para criar, modificar, converter e analisar arquivos Excel.

#### Como posso obter o tamanho do papel de uma planilha com Aspose.Cells for .NET?

 Você pode usar o`PageSetup` classe do`Worksheet` objeto para acessar o tamanho do papel. Use o`PaperSize` propriedade para definir o tamanho do papel e o`PaperWidth` e`PaperHeight` propriedades para obter a largura e a altura do papel, respectivamente.

#### Quais tamanhos de papel o Aspose.Cells for .NET suporta?

Aspose.Cells for .NET oferece suporte a uma ampla variedade de tamanhos de papel comumente usados, como A2, A3, A4 e Carta, bem como muitos outros tamanhos personalizados.

#### Posso personalizar o tamanho do papel de uma planilha com Aspose.Cells for .NET?

 Sim, você pode definir um tamanho de papel personalizado especificando as dimensões exatas de largura e altura usando o botão`PaperWidth` e`PaperHeight` propriedades do`PageSetup` aula.