---
title: Inserir imagem no rodapé do cabeçalho
linktitle: Inserir imagem no rodapé do cabeçalho
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como inserir uma imagem no cabeçalho ou rodapé de um documento Excel usando Aspose.Cells for .NET. Guia passo a passo com código fonte em C#.
type: docs
weight: 60
url: /pt/net/excel-page-setup/insert-image-in-header-footer/
---
A possibilidade de inserir uma imagem no cabeçalho ou rodapé de um documento Excel pode ser muito útil para personalizar seus relatórios ou adicionar logotipos de empresas. Neste artigo, iremos guiá-lo passo a passo para inserir uma imagem no cabeçalho ou rodapé de um documento Excel usando Aspose.Cells for .NET. Você aprenderá como fazer isso usando o código-fonte C#.

## Passo 1: Configurando o ambiente

Antes de começar, certifique-se de ter o Aspose.Cells for .NET instalado em sua máquina. Crie também um novo projeto em seu ambiente de desenvolvimento preferido.

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

## Etapa 5: armazenar o URL da imagem

Defina a URL ou caminho da imagem que deseja inserir no cabeçalho ou rodapé. Use o seguinte código para armazenar o URL da imagem:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Certifique-se de que o caminho especificado esteja correto e que a imagem exista nesse local.

## Passo 6: Abrindo o arquivo de imagem

Para abrir o arquivo de imagem, usaremos um objeto FileStream e leremos os dados binários da imagem. Aqui está o código correspondente:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Certifique-se de que o caminho da imagem esteja correto e que você tenha as permissões corretas para acessá-la.

## Etapa 7: configurando o PageSetup

O objeto PageSetup é usado para definir as configurações da página do documento Excel, incluindo cabeçalho e rodapé. Use o código a seguir para obter o objeto PageSetup da primeira planilha:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Isso permitirá que você acesse as configurações de página da primeira planilha da pasta de trabalho.

## Passo 8: Adicionando a imagem ao cabeçalho

Use o método SetHeaderPicture() do objeto PageSetup para definir a imagem na seção intermediária do cabeçalho da página. Aqui está o código correspondente:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Isso adicionará a imagem especificada ao cabeçalho da página.

## Etapa 9: Adicionando um script ao cabeçalho

Para adicionar script ao cabeçalho da página, use o método SetHeader() do objeto PageSetup. Aqui está o código correspondente:

```csharp
pageSetup.SetHeader(1, "&G");
```

Isso adicionará o script especificado ao cabeçalho da página. Neste exemplo, o script “&G” exibe o número da página.

## Etapa 10: adicionar o nome da planilha ao cabeçalho

Para exibir o nome da planilha no cabeçalho da página, use o método SetHeader() do objeto PageSetup novamente. Aqui está o código correspondente:

```csharp
pageSetup.SetHeader(2, "&A");
```

Isso adicionará o nome da planilha ao cabeçalho da página. O script "&A" é usado para representar o nome da planilha.

## Etapa 11: salvando a pasta de trabalho

Para salvar alterações na pasta de trabalho, use o método Save() do objeto Workbook. Aqui está o código correspondente:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Isso salvará a pasta de trabalho com as alterações no diretório especificado.

## Etapa 12: Fechando o FileStream

Depois de ler os dados binários da imagem, feche o FileStream para liberar os recursos. Use o seguinte código para fechar o FileStream:

```csharp
inFile.Close();
```

Certifique-se de sempre fechar o FileStreams quando terminar de usá-los.

### Exemplo de código-fonte para inserir imagem no rodapé do cabeçalho usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Criando um objeto Pasta de Trabalho
Workbook workbook = new Workbook();
// Criando uma variável de string para armazenar a URL do logotipo/imagem
string logo_url = dataDir + "aspose-logo.jpg";
// Declarando um objeto FileStream
FileStream inFile;
// Declarando uma matriz de bytes
byte[] binaryData;
// Criando a instância do objeto FileStream para abrir o logotipo/imagem no stream
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Instanciando a matriz de bytes do tamanho do objeto FileStream
binaryData = new Byte[inFile.Length];
// Lê um bloco de bytes do fluxo e grava dados em um determinado buffer de matriz de bytes.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Criando um objeto PageSetup para obter as configurações de página da primeira planilha da pasta de trabalho
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Definir o logotipo/imagem na seção central do cabeçalho da página
pageSetup.SetHeaderPicture(1, binaryData);
// Configurando o script para o logotipo/imagem
pageSetup.SetHeader(1, "&G");
// Definir o nome da planilha na seção direita do cabeçalho da página com o script
pageSetup.SetHeader(2, "&A");
// Salvando a pasta de trabalho
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Fechando o objeto FileStream
inFile.Close();       
```
## Conclusão

Parabéns! Agora você sabe inserir uma imagem no cabeçalho ou rodapé de um documento Excel usando Aspose.Cells for .NET. Este tutorial orientou você em todas as etapas do processo, desde a configuração do ambiente até salvar a pasta de trabalho modificada. Sinta-se à vontade para experimentar mais os recursos do Aspose.Cells para criar documentos Excel personalizados e profissionais.

### Perguntas frequentes

#### Q1: É possível inserir várias imagens no cabeçalho ou rodapé de um documento Excel?

R1: Sim, você pode inserir várias imagens no cabeçalho ou rodapé de um documento Excel repetindo as etapas 8 e 9 para cada imagem adicional.

#### P2: Quais formatos de imagem são suportados para inserção no cabeçalho ou rodapé?
A2: Aspose.Cells suporta uma variedade de formatos de imagem comuns, como JPEG, PNG, GIF, BMP, etc.

#### P3: Posso personalizar ainda mais a aparência do cabeçalho ou rodapé?

A3: Sim, você pode usar scripts e códigos especiais para formatar e personalizar ainda mais a aparência do cabeçalho ou rodapé. Consulte a documentação do Aspose.Cells para obter mais informações sobre opções de personalização.

#### Q4: O Aspose.Cells funciona com diferentes versões do Excel?

A4: Sim, Aspose.Cells é compatível com diferentes versões do Excel, incluindo Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 e Excel 2019.

#### P5: É possível inserir imagens em outras partes do documento Excel, como células ou gráficos?

R5: Sim, Aspose.Cells oferece ampla funcionalidade para inserir imagens em diferentes partes do documento Excel, incluindo células, gráficos e objetos de desenho.