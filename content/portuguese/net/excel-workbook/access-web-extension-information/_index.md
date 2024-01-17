---
title: Acesse informações de extensão da web
linktitle: Acesse informações de extensão da web
second_title: Referência da API Aspose.Cells para .NET
description: Acesse informações de extensão da web com Aspose.Cells for .NET.
type: docs
weight: 10
url: /pt/net/excel-workbook/access-web-extension-information/
---
acesso às informações de extensões da web é um recurso essencial ao desenvolver aplicativos usando Aspose.Cells for .NET. Neste guia passo a passo, explicaremos o código-fonte C# fornecido que permitirá que você acesse informações de extensão da web usando Aspose.Cells for .NET. Também forneceremos uma conclusão e uma resposta em formato Markdown para facilitar o entendimento. Siga as etapas abaixo para obter informações valiosas sobre extensões da web.

## Etapa 1: definir o diretório de origem

```csharp
// diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
```

Nesta primeira etapa definimos o diretório fonte que será utilizado para carregar o arquivo Excel contendo as informações da extensão web.

## Passo 2: Carregue o arquivo Excel

```csharp
// Carregue o arquivo Excel de exemplo
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

Aqui carregamos o arquivo Excel de amostra que contém as informações da extensão da web que queremos recuperar.

## Etapa 3: acessar informações na janela de tarefas da extensão da web

```csharp
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach(WebExtensionTaskPane taskPane in taskPanes)
{
Console.WriteLine("Width: " + taskPane.Width);
Console.WriteLine("Is visible: " + taskPane.IsVisible);
Console.WriteLine("Is locked: " + taskPane.IsLocked);
Console.WriteLine("Docking State: " + taskPane.DockState);
Console.WriteLine("Store Name: " + taskPane.WebExtension.Reference.StoreName);
Console.WriteLine("Store type: " + taskPane.WebExtension.Reference.StoreType);
Console.WriteLine("Web Extension ID: " + taskPane.WebExtension.Id);
}
```

Nesta etapa acessamos as informações de cada janela de tarefas de extensão web presente no arquivo Excel. Exibimos diferentes propriedades, como largura, visibilidade, estado de bloqueio, estado inicial, nome da loja, tipo de loja e ID da extensão da web.

## Etapa 4: mostrar mensagem de sucesso

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

Por fim, exibimos uma mensagem indicando que as informações da extensão web foram acessadas com sucesso.

### Exemplo de código-fonte para acessar informações de extensão da Web usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
//Carregar arquivo Excel de amostra
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach (WebExtensionTaskPane taskPane in taskPanes)
{
	Console.WriteLine("Width: " + taskPane.Width);
	Console.WriteLine("IsVisible: " + taskPane.IsVisible);
	Console.WriteLine("IsLocked: " + taskPane.IsLocked);
	Console.WriteLine("DockState: " + taskPane.DockState);
	Console.WriteLine("StoreName: " + taskPane.WebExtension.Reference.StoreName);
	Console.WriteLine("StoreType: " + taskPane.WebExtension.Reference.StoreType);
	Console.WriteLine("WebExtension.Id: " + taskPane.WebExtension.Id);
}
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

## Conclusão

Neste tutorial, aprendemos como acessar informações de extensões da web usando Aspose.Cells for .NET. Seguindo as etapas fornecidas, você poderá extrair facilmente informações da janela de tarefas de uma extensão da web para um arquivo Excel.


### Perguntas frequentes

#### P: O que é Aspose.Cells para .NET?

R: Aspose.Cells for .NET é uma biblioteca de classes poderosa que permite aos desenvolvedores .NET criar, modificar, converter e manipular arquivos Excel com facilidade.

#### P: O Aspose.Cells oferece suporte a outras linguagens de programação?

R: Sim, Aspose.Cells oferece suporte a várias linguagens de programação como C#, VB.NET, Java, PHP, Python, etc.

#### P: Posso usar Aspose.Cells em projetos comerciais?

R: Sim, Aspose.Cells é uma biblioteca comercial e pode ser usada em projetos comerciais de acordo com o contrato de licença.

#### P: Existe documentação adicional sobre Aspose.Cells?

R: Sim, você pode verificar a documentação completa do Aspose.Cells no site oficial do Aspose para obter mais informações e recursos.