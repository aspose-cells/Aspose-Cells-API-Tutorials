---
title: Excluir planilha do Excel por nome Tutorial C#
linktitle: Excluir planilha do Excel por nome
second_title: Referência da API Aspose.Cells para .NET
description: Exclua facilmente uma planilha específica do Excel por nome usando Aspose.Cells for .NET. Tutorial detalhado com exemplos de código.
type: docs
weight: 40
url: /pt/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-name-csharp-tutorial/
---
Neste tutorial, iremos guiá-lo passo a passo para explicar o código-fonte C# abaixo, que pode excluir uma planilha do Excel usando Aspose.Cells for .NET usando seu nome. Incluiremos código de amostra para cada etapa para ajudá-lo a entender o processo em detalhes.

## Etapa 1: definir o diretório de documentos

Para começar, você precisa definir o caminho do diretório onde seu arquivo Excel está localizado. Substitua “SEU DIRETÓRIO DE DOCUMENTOS” no código pelo caminho real do seu arquivo Excel.

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Etapa 2: crie um fluxo de arquivos e abra o arquivo Excel

 Em seguida, você precisa criar um fluxo de arquivos e abrir o arquivo Excel usando o`FileStream` aula.

```csharp
// Crie um fluxo de arquivos contendo o arquivo Excel para abrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Etapa 3: instanciar um objeto de pasta de trabalho

 Depois de abrir o arquivo Excel, você precisa instanciar um`Workbook`objeto. Este objeto representa a pasta de trabalho do Excel e oferece vários métodos e propriedades para manipular a pasta de trabalho.

```csharp
// Instanciar um objeto Workbook
// Abra o arquivo Excel por meio do fluxo de arquivos
Workbook workbook = new Workbook(fstream);
```

## Etapa 4: excluir uma planilha por nome

 Para remover uma planilha de seu nome, você pode usar o`RemoveAt()` método do`Worksheets` objeto do`Workbook` objeto. O nome da planilha que deseja excluir deve ser passado como parâmetro.

```csharp
// Exclua uma planilha usando seu nome de planilha
workbook.Worksheets.RemoveAt("Sheet1");
```

## Etapa 5: salve a pasta de trabalho

 Depois de excluir a planilha, você pode salvar a pasta de trabalho do Excel modificada usando o`Save()` método do`Workbook` objeto.

```csharp
// Salve a pasta de trabalho do Excel
workbook.Save(dataDir + "output.out.xls");
```


### Exemplo de código-fonte para Excluir planilha do Excel por nome Tutorial C# usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Criando um fluxo de arquivos contendo o arquivo Excel a ser aberto
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciando um objeto Workbook
// Abrindo o arquivo Excel por meio do fluxo de arquivos
Workbook workbook = new Workbook(fstream);
// Removendo uma planilha usando seu nome de planilha
workbook.Worksheets.RemoveAt("Sheet1");
// Salvar pasta de trabalho
workbook.Save(dataDir + "output.out.xls");
```

## Conclusão

Neste tutorial, abordamos o processo passo a passo de exclusão de uma planilha do Excel por nome usando Aspose.Cells for .NET. Seguindo os exemplos de código e as explicações fornecidas, agora você deve ter um bom entendimento de como executar essa tarefa em seus aplicativos C#. Aspose.Cells for .NET oferece um conjunto abrangente de recursos para trabalhar com arquivos Excel, permitindo manipular facilmente planilhas e dados relacionados.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca poderosa que permite aos desenvolvedores criar, manipular e converter arquivos Excel em seus aplicativos .NET. Oferece uma ampla gama de recursos para trabalhar com planilhas, células, fórmulas, estilos e muito mais.

#### Como posso instalar o Aspose.Cells para .NET?

Para instalar o Aspose.Cells for .NET, você pode baixar o pacote de instalação em Aspose Releases (https://releases.aspose.com/cells/net) e siga as instruções fornecidas. Você precisará de uma licença válida para usar a biblioteca em seus aplicativos.

#### Posso excluir várias planilhas de uma vez?

Sim, você pode excluir várias planilhas usando Aspose.Cells for .NET. Você pode simplesmente repetir a etapa de exclusão para cada planilha que deseja excluir.

#### Como posso saber se uma planilha existe antes de excluí-la?

 Antes de excluir uma planilha, você pode verificar se ela existe usando o`Contains()` método do`Worksheets` objeto do`Workbook` objeto. Este método toma o nome da planilha como parâmetro e retorna`true` se a planilha existir, caso contrário ela retorna`false`.

#### É possível recuperar uma planilha excluída?

Infelizmente, depois que uma planilha é excluída, ela não pode ser recuperada diretamente do arquivo Excel. É recomendável criar um backup do seu arquivo Excel antes de excluir uma planilha para evitar perda de dados.