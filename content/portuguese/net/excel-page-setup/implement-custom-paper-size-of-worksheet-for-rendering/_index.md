---
title: Implementar tamanho de papel personalizado de planilha para renderização
linktitle: Implementar tamanho de papel personalizado de planilha para renderização
second_title: Referência da API Aspose.Cells para .NET
description: Guia passo a passo para implementar tamanho de planilha personalizado com Aspose.Cells for .NET. Defina as dimensões, adicione uma mensagem e salve como PDF.
type: docs
weight: 50
url: /pt/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Implementar um tamanho personalizado para sua planilha pode ser muito útil quando você deseja criar um documento PDF com um tamanho específico. Neste tutorial, aprenderemos como usar Aspose.Cells for .NET para definir um tamanho personalizado para uma planilha e, em seguida, salvar o documento como PDF.

## Passo 1: Criando a pasta de saída

Antes de começar, você precisa criar uma pasta de saída onde o arquivo PDF gerado será salvo. Você pode usar qualquer caminho que desejar para sua pasta de saída.

```csharp
// Diretórios de saída
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Certifique-se de especificar o caminho correto para sua pasta de saída.

## Etapa 2: Criando o objeto Pasta de Trabalho

Para começar, você precisa criar um objeto Workbook usando Aspose.Cells. Este objeto representa sua planilha.

```csharp
// Crie o objeto Pasta de Trabalho
Workbook wb = new Workbook();
```

## Passo 3: Acesso à primeira planilha

Depois de criar o objeto Workbook, você pode acessar a primeira planilha dentro dele.

```csharp
// Acesso à primeira planilha
Worksheet ws = wb.Worksheets[0];
```

## Etapa 4: definir o tamanho da planilha personalizada

 Agora você pode definir o tamanho da planilha personalizada usando`CustomPaperSize(width, height)` método da classe PageSetup.

```csharp
// Definir tamanho de planilha personalizado (em polegadas)
ws.PageSetup.CustomPaperSize(6, 4);
```

Neste exemplo, definimos o tamanho da planilha como 6 polegadas de largura e 4 polegadas de altura.

## Passo 5: Acesso à célula B4

Depois disso, podemos acessar uma célula específica da planilha. Neste caso, acessaremos a célula B4.

```csharp
// Acesso à célula B4
Cell b4 = ws.Cells["B4"];
```

## Etapa 6: Adicionar a mensagem na célula B4

 Agora podemos adicionar uma mensagem à célula B4 usando o`PutValue(value)` método.

```csharp
// Adicione a mensagem na célula B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

Neste exemplo, adicionamos a mensagem "Tamanho da página PDF: 6,00" x 4,00" na célula B4.

## Passo 7: Salvando a planilha em formato PDF

 Finalmente, podemos salvar a planilha em formato PDF usando o`Save(filePath)` método do objeto Workbook.

```csharp
// Salve a planilha em formato PDF
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Especifique o caminho desejado para o arquivo PDF gerado, usando a pasta de saída criada anteriormente.

### Exemplo de código-fonte para implementar tamanho de papel personalizado de planilha para renderização usando Aspose.Cells for .NET 
```csharp
//Diretório de saída
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Criar objeto de pasta de trabalho
Workbook wb = new Workbook();
//Acesse a primeira planilha
Worksheet ws = wb.Worksheets[0];
//Defina o tamanho do papel personalizado em unidades de polegadas
ws.PageSetup.CustomPaperSize(6, 4);
//Acesse a célula B4
Cell b4 = ws.Cells["B4"];
//Adicione a mensagem na célula B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Salve a pasta de trabalho em formato pdf
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Conclusões

Neste tutorial, você aprendeu como implementar o tamanho personalizado de uma planilha usando Aspose.Cells for .NET. Você pode usar estas etapas para definir dimensões específicas para suas planilhas e depois salvar os documentos em formato PDF. Esperamos que este guia tenha sido útil para a compreensão do processo de implementação de um tamanho de planilha personalizado.

### Perguntas frequentes (FAQ)

#### Pergunta 1: Posso personalizar ainda mais o layout da planilha?

Sim, Aspose.Cells oferece muitas opções para personalizar o layout de sua planilha. Você pode definir dimensões personalizadas, orientação de página, margens, cabeçalhos e rodapés e muito mais.

#### Pergunta 2: Que outros formatos de saída o Aspose.Cells suporta?

Aspose.Cells suporta muitos formatos de saída diferentes, incluindo PDF, XLSX, XLS, CSV, HTML, TXT e muitos mais. Você pode escolher o formato de saída desejado de acordo com suas necessidades.