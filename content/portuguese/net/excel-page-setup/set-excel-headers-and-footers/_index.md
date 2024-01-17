---
title: Definir cabeçalhos e rodapés do Excel
linktitle: Definir cabeçalhos e rodapés do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como definir cabeçalhos e rodapés no Excel usando Aspose.Cells for .NET.
type: docs
weight: 100
url: /pt/net/excel-page-setup/set-excel-headers-and-footers/
---

Neste tutorial, mostraremos passo a passo como definir cabeçalhos e rodapés no Excel usando Aspose.Cells for .NET. Usaremos o código-fonte C# para ilustrar o processo.

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
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Isso criará uma pasta de trabalho vazia com uma planilha e fornecerá acesso ao objeto PageSetup dessa planilha.

## Etapa 5: definir cabeçalhos

 Defina os cabeçalhos da planilha usando o`SetHeader` métodos do objeto PageSetup. Aqui está um exemplo de código:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Isso definirá o nome da planilha, a data e hora atuais e o nome do arquivo nos cabeçalhos, respectivamente.

## Etapa 6: definindo rodapés

 Defina rodapés de planilhas usando o`SetFooter` métodos do objeto PageSetup. Aqui está um exemplo de código:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Isso definirá respectivamente uma sequência de texto, o número da página atual e o número total de páginas nos rodapés.

## Etapa 7: salvando a pasta de trabalho modificada

Salve a pasta de trabalho modificada usando o seguinte código:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Isso salvará a pasta de trabalho modificada no diretório de dados especificado.

### Exemplo de código-fonte para definir cabeçalhos e rodapés do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook excel = new Workbook();
// Obtendo a referência do PageSetup da planilha
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Definir o nome da planilha na seção esquerda do cabeçalho
pageSetup.SetHeader(0, "&A");
//Definir a data e a hora atuais na seção central do cabeçalho
// e alterando a fonte do cabeçalho
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Definir o nome do arquivo atual na seção direita do cabeçalho e alterar o
// fonte do cabeçalho
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Definir uma string na seção esquerda do rodapé e alterar a fonte
// de uma parte desta string ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Definir o número da página atual na seção central do rodapé
pageSetup.SetFooter(1, "&P");
// Definir contagem de páginas na seção direita do rodapé
pageSetup.SetFooter(2, "&N");
// Salve a pasta de trabalho.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Conclusão

Agora você aprendeu como definir cabeçalhos e rodapés no Excel usando Aspose.Cells for .NET. Este tutorial orientou você em todas as etapas do processo, desde a configuração do ambiente até salvar a pasta de trabalho modificada. Sinta-se à vontade para explorar ainda mais os recursos do Aspose.Cells para realizar outras manipulações em seus arquivos Excel.

### Perguntas frequentes (FAQ)

#### 1. Como posso instalar o Aspose.Cells for .NET no meu sistema?
Para instalar o Aspose.Cells for .NET, você precisa baixar o pacote de instalação do site oficial do Aspose e seguir as instruções fornecidas na documentação.

#### 2. Este método funciona com todas as versões do Excel?
Sim, o método de configuração de cabeçalhos e rodapés com Aspose.Cells for .NET funciona com todas as versões suportadas do Excel.

#### 3. Posso personalizar ainda mais cabeçalhos e rodapés?
Sim, Aspose.Cells oferece uma ampla gama de recursos para personalizar cabeçalhos e rodapés, incluindo posicionamento de texto, cor, fonte, números de página e muito mais.

#### 4. Como posso adicionar informações dinâmicas aos cabeçalhos e rodapés?
Você pode usar variáveis especiais e códigos de formatação para adicionar informações dinâmicas, como data atual, hora, nome do arquivo, número da página, etc., aos cabeçalhos e rodapés.

#### 5. Posso remover cabeçalhos e rodapés depois de configurá-los?
 Sim, você pode remover cabeçalhos e rodapés usando o`ClearHeaderFooter` método do`PageSetup` objeto. Isso restaurará os cabeçalhos e rodapés padrão.