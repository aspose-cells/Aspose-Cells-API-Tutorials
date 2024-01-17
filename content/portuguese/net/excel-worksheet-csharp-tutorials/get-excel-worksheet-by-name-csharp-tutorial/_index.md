---
title: Obtenha planilha do Excel por nome Tutorial C#
linktitle: Obtenha planilha do Excel por nome
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como obter uma planilha do Excel por nome usando Aspose.Cells for .NET. Tutorial passo a passo com exemplos de código.
type: docs
weight: 50
url: /pt/net/excel-worksheet-csharp-tutorials/get-excel-worksheet-by-name-csharp-tutorial/
---
Neste tutorial, iremos guiá-lo passo a passo para explicar o código-fonte C# abaixo, que pode obter uma planilha do Excel usando Aspose.Cells for .NET usando seu nome. Incluiremos código de amostra para cada etapa para ajudá-lo a entender o processo em detalhes.

## Etapa 1: definir o diretório de documentos

Para começar, você precisa definir o caminho do diretório onde seu arquivo Excel está localizado. Substitua “SEU DIRETÓRIO DE DOCUMENTOS” no código pelo caminho real do seu arquivo Excel.

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Etapa 2: definir o caminho de entrada do arquivo Excel

Em seguida, você precisa definir o caminho de entrada do arquivo Excel que deseja abrir. Este caminho será usado para criar um fluxo de arquivos.

```csharp
// Caminho de entrada do arquivo Excel
string InputPath = dataDir + "book1.xlsx";
```

## Etapa 3: crie um fluxo de arquivos e abra o arquivo Excel

 Em seguida, você precisa criar um fluxo de arquivos e abrir o arquivo Excel usando o`FileStream` aula.

```csharp
// Crie um fluxo de arquivos contendo o arquivo Excel para abrir
FileStream fstream = new FileStream(InputPath, FileMode.Open);
```

## Etapa 4: instanciar um objeto de pasta de trabalho

 Depois de abrir o arquivo Excel, você precisa instanciar um`Workbook`objeto. Este objeto representa a pasta de trabalho do Excel e oferece vários métodos e propriedades para manipular a pasta de trabalho.

```csharp
// Instanciar um objeto Workbook
// Abra o arquivo Excel por meio do fluxo de arquivos
Workbook workbook = new Workbook(fstream);
```

## Etapa 5: acesse uma planilha por nome

Para acessar uma planilha específica por nome, você pode usar o`Worksheets` propriedade do`Workbook` objeto e indexe o nome da planilha.

```csharp
// Acesse uma planilha usando seu nome de planilha
Worksheet worksheet = workbook.Worksheets["Sheet1"];
```

## Passo 6: Acesse uma célula específica

 Depois de navegar até a planilha desejada, você pode navegar até uma célula específica usando o botão`Cells` propriedade do`Worksheet` objeto e indexe a referência da célula.

```csharp
// Acesso a uma célula específica
Cell cell = worksheet.Cells["A1"];
```

## Etapa 7: recuperar o valor da célula

 Finalmente, você pode recuperar o valor da célula usando o`Value` propriedade do`Cell` objeto.

```csharp
// Recuperar o valor da célula
Console.WriteLine(cell.Value);
```

### Exemplo de código-fonte para o tutorial Obter planilha do Excel por nome C# usando Aspose.Cells para .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xlsx";
// Criando um fluxo de arquivos contendo o arquivo Excel a ser aberto
FileStream fstream = new FileStream(InputPath, FileMode.Open);
// Instanciando um objeto Workbook
// Abrindo o arquivo Excel por meio do fluxo de arquivos
Workbook workbook = new Workbook(fstream);
// Acessando uma planilha usando seu nome de planilha
Worksheet worksheet = workbook.Worksheets["Sheet1"];
Cell cell = worksheet.Cells["A1"];
Console.WriteLine(cell.Value);
```

## Conclusão

Neste tutorial, cobrimos o processo passo a passo para obter uma planilha específica do Excel por seu nome usando Aspose.Cells for .NET. Agora você pode usar esse conhecimento para manipular e processar dados em arquivos Excel com eficiência e precisão.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca poderosa que permite aos desenvolvedores criar, manipular e converter arquivos Excel em seus aplicativos .NET. Oferece uma ampla gama de recursos para trabalhar com planilhas, células, fórmulas, estilos e muito mais.

#### Como posso instalar o Aspose.Cells para .NET?

Para instalar o Aspose.Cells for .NET, você pode baixar o pacote de instalação do Aspose.Releases (https://releases.aspose.com/cells/net) e siga as instruções fornecidas. Você precisará de uma licença válida para usar a biblioteca em seus aplicativos.

#### Posso obter uma planilha do Excel usando seu nome em Aspose.Cells for .NET?

 Sim, você pode obter uma planilha do Excel usando seu nome em Aspose.Cells for .NET. Você pode usar o`Worksheets` propriedade do`Workbook` objeto e indexe o nome da planilha para acessá-lo.

#### E se o nome da planilha não existir no arquivo Excel?

Se o nome da planilha especificada não existir no arquivo Excel, uma exceção será lançada ao tentar acessar essa planilha. Certifique-se de verificar se o nome da planilha foi inserido corretamente e se existe no arquivo Excel antes de acessá-la.

#### Posso usar o Aspose.Cells for .NET para manipular dados de células em uma planilha?

Sim, Aspose.Cells for .NET oferece muitos recursos para manipular dados de células em uma planilha. Você pode ler e escrever valores de células, aplicar formatos, adicionar fórmulas, mesclar células, realizar operações matemáticas e muito mais. A biblioteca fornece uma interface abrangente para trabalhar com dados de células no Excel.