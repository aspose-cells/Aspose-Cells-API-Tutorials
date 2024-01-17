---
title: Ocultar e exibir planilha
linktitle: Ocultar e exibir planilha
second_title: Referência da API Aspose.Cells para .NET
description: Uma biblioteca poderosa para trabalhar com arquivos Excel, incluindo criação, modificação e manipulação de dados.
type: docs
weight: 90
url: /pt/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
Neste tutorial, iremos guiá-lo passo a passo para explicar o seguinte código-fonte C# que é usado para ocultar e mostrar uma planilha usando Aspose.Cells for .NET. Siga os passos abaixo:

## Passo 1: Preparando o ambiente

Antes de começar, certifique-se de ter o Aspose.Cells for .NET instalado em seu sistema. Se ainda não o instalou, você pode baixá-lo no site oficial do Aspose. Depois de instalado, você pode criar um novo projeto em seu ambiente de desenvolvimento integrado (IDE) preferido.

## Etapa 2: importar namespaces necessários

No arquivo de origem C#, adicione os namespaces necessários para usar os recursos do Aspose.Cells. Adicione as seguintes linhas ao início do seu arquivo:

```csharp
using Aspose.Cells;
using System.IO;
```

## Etapa 3: carregue o arquivo Excel

Antes de ocultar ou exibir uma planilha, você deve carregar o arquivo Excel em seu aplicativo. Certifique-se de ter o arquivo Excel que deseja usar no mesmo diretório do seu projeto. Use o seguinte código para carregar o arquivo Excel:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Certifique-se de substituir "PATH TO YOUR DOCUMENTS DIRECTORY" pelo caminho real para o diretório que contém seu arquivo Excel.

## Passo 4: Acesse a planilha

Depois que o arquivo Excel for carregado, você poderá navegar até a planilha que deseja ocultar ou exibir. Use o código a seguir para acessar a primeira planilha do arquivo:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Etapa 5: ocultar a planilha

 Agora que você acessou a planilha, você pode ocultá-la usando o`IsVisible` propriedade. Use o código a seguir para ocultar a primeira planilha do arquivo:

```csharp
worksheet. IsVisible = false;
```

## Etapa 6: exibir novamente a planilha

Se quiser exibir novamente a planilha oculta anteriormente, você pode usar o mesmo código alterando o valor do`IsVisible` propriedade. Use o código a seguir para exibir novamente a primeira planilha:

```csharp
worksheet. IsVisible = true;
```

## Etapa 7: salvar alterações

Uma vez que você

  tiver ocultado ou reexibido a planilha conforme necessário, você deverá salvar as alterações no arquivo Excel. Use o seguinte código para salvar as alterações:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Certifique-se de especificar o caminho de saída correto para salvar o arquivo Excel modificado.

### Exemplo de código-fonte para planilha Hide And Unhide usando Aspose.Cells for .NET 

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Criando um fluxo de arquivos contendo o arquivo Excel a ser aberto
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciando um objeto Workbook abrindo o arquivo Excel por meio do fluxo de arquivos
Workbook workbook = new Workbook(fstream);
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ocultando a primeira planilha do arquivo Excel
worksheet.IsVisible = false;
// Mostra a primeira planilha do arquivo Excel
//Planilha.IsVisible = true;
// Salvando o arquivo Excel modificado no formato padrão (ou seja, Excel 2003)
workbook.Save(dataDir + "output.out.xls");
// Fechando o fluxo de arquivos para liberar todos os recursos
fstream.Close();
```

## Conclusão

Parabéns! Você aprendeu como ocultar e mostrar uma planilha usando Aspose.Cells for .NET. Agora você pode usar esse recurso para controlar a visibilidade de suas planilhas em arquivos Excel.

### Perguntas frequentes (FAQ)

#### Como posso instalar o Aspose.Cells para .NET?

 Você pode instalar o Aspose.Cells for .NET baixando o pacote NuGet relevante em[Aspose Lançamentos](https://releases/aspose.com/cells/net/) e adicionando-o ao seu projeto do Visual Studio.

#### Qual é a versão mínima necessária do .NET Framework para usar o Aspose.Cells for .NET?

Aspose.Cells for .NET suporta .NET Framework 2.0 e posterior.

#### Posso abrir e editar arquivos Excel existentes com Aspose.Cells for .NET?

Sim, você pode abrir e editar arquivos Excel existentes usando Aspose.Cells for .NET. Você pode acessar planilhas, células, fórmulas e outros elementos do arquivo Excel.

#### O Aspose.Cells for .NET oferece suporte a relatórios e exportação para outros formatos de arquivo?

Sim, Aspose.Cells for .NET suporta geração de relatórios e exportação para formatos como PDF, HTML, CSV, TXT, etc.

#### A modificação do arquivo Excel é permanente?

Sim, a edição do arquivo Excel é permanente depois de salva. Certifique-se de salvar uma cópia de backup antes de fazer qualquer alteração no arquivo original.