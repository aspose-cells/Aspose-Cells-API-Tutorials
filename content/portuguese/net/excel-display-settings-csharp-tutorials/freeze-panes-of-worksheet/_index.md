---
title: Congelar painéis da planilha
linktitle: Congelar painéis da planilha
second_title: Referência da API Aspose.Cells para .NET
description: Manipule facilmente painéis congelados de planilhas do Excel com Aspose.Cells for .NET.
type: docs
weight: 70
url: /pt/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
Neste tutorial, mostraremos como bloquear painéis em uma planilha do Excel usando código-fonte C# com Aspose.Cells for .NET. Siga as etapas abaixo para obter o resultado desejado.

## Passo 1: Importe as bibliotecas necessárias

Certifique-se de ter instalado a biblioteca Aspose.Cells para .NET e importe as bibliotecas necessárias para o seu projeto C#.

```csharp
using Aspose.Cells;
```

## Etapa 2: definir o caminho do diretório e abrir o arquivo Excel

 Defina o caminho para o diretório que contém seu arquivo Excel e abra o arquivo instanciando um`Workbook` objeto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Etapa 3: vá para a planilha e aplique as configurações de bloqueio do painel

 Navegue até a primeira planilha do arquivo Excel usando o`Worksheet` objeto. Então use o`FreezePanes` método para aplicar as configurações de bloqueio do painel.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

No exemplo acima, os painéis estão bloqueados na célula da linha 3 e da coluna 2.

## Etapa 4: salvar alterações

 Depois de fazer as alterações necessárias, salve o arquivo Excel modificado usando o`Save` método do`Workbook` objeto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exemplo de código-fonte para congelar painéis de planilha usando Aspose.Cells for .NET 

```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Criando um fluxo de arquivos contendo o arquivo Excel a ser aberto
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciando um objeto Workbook
// Abrindo o arquivo Excel por meio do fluxo de arquivos
Workbook workbook = new Workbook(fstream);
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = workbook.Worksheets[0];
// Aplicando configurações de painéis congelados
worksheet.FreezePanes(3, 2, 3, 2);
// Salvando o arquivo Excel modificado
workbook.Save(dataDir + "output.xls");
// Fechando o fluxo de arquivos para liberar todos os recursos
fstream.Close();
```

## Conclusão

Este guia passo a passo mostrou como bloquear painéis em uma planilha do Excel usando Aspose.Cells for .NET. Usando o código-fonte C# fornecido, você pode personalizar facilmente as configurações de bloqueio do painel para organizar e visualizar melhor seus dados em arquivos Excel.

### Perguntas frequentes (FAQ)

#### O que é Aspose.Cells para .NET?

Aspose.Cells for .NET é uma biblioteca poderosa para manipular arquivos Excel em aplicativos .NET.

#### Como posso instalar o Aspose.Cells para .NET?

 Para instalar o Aspose.Cells for .NET, você precisa baixar o pacote relevante em[Aspose Lançamentos](https://releases/aspose.com/cells/net/) e adicione-o ao seu projeto .NET.

#### Como bloquear painéis em uma planilha do Excel usando Aspose.Cells for .NET?

 Você pode usar o`FreezePanes` método do`Worksheet` objeto para bloquear os painéis de uma planilha. Especifique as células a serem bloqueadas fornecendo índices de linhas e colunas.

#### Posso personalizar as configurações de bloqueio do painel com Aspose.Cells for .NET?

 Sim, usando o`FreezePanes` método, você pode especificar quais células bloquear conforme necessário, fornecendo os índices de linha e coluna apropriados.
