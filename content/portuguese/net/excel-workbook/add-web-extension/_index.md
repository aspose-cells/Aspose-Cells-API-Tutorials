---
title: Adicionar extensão da web
linktitle: Adicionar extensão da web
second_title: Referência da API Aspose.Cells para .NET
description: Adicione facilmente extensão da web às suas pastas de trabalho do Excel com Aspose.Cells for .NET.
type: docs
weight: 40
url: /pt/net/excel-workbook/add-web-extension/
---
Neste tutorial passo a passo, explicaremos o código-fonte C# fornecido que permitirá adicionar uma extensão da web usando Aspose.Cells for .NET. Siga as etapas abaixo para adicionar uma extensão da web à sua pasta de trabalho do Excel.

## Etapa 1: definir o diretório de saída

```csharp
// Diretório de saída
string outDir = RunExamples.Get_OutputDirectory();
```

Nesta primeira etapa, definimos o diretório de saída onde a pasta de trabalho modificada do Excel será salva.

## Etapa 2: crie uma nova pasta de trabalho

```csharp
// Crie uma nova pasta de trabalho
Workbook workbook = new Workbook();
```

Aqui estamos criando uma nova pasta de trabalho do Excel usando o`Workbook` classe de Aspose.Cells.

## Etapa 3: acesse a coleção de extensões da Web

```csharp
// Acesse a coleção de extensões da web
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Acessamos a coleção de extensões da web da pasta de trabalho do Excel usando o`WebExtensions` propriedade do`Worksheets` objeto.

## Etapa 4: adicione uma nova extensão da web

```csharp
// Adicione uma nova extensão da web
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Estamos adicionando uma nova extensão da web à coleção de extensões. Definimos o ID de referência, o nome da loja e o tipo de loja da extensão.

## Etapa 5: acesse a coleção do painel de tarefas de extensão da Web

```csharp
// Acesse a coleção do painel de tarefas da extensão da web
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Acessamos a coleção de painéis de tarefas Excel Workbook Web Extension usando o`WebExtensionTaskPanes` propriedade do`Worksheets` objeto.

## Etapa 6: adicionar um novo painel de tarefas

```csharp
// Adicione um novo painel de tarefas
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Estamos adicionando um novo painel de tarefas à coleção de painéis de tarefas. Definimos a visibilidade do painel, seu estado de encaixe e a extensão da web associada.

## Etapa 7: salve e feche a pasta de trabalho

```csharp
// Salve e feche a pasta de trabalho
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Salvamos a pasta de trabalho modificada no diretório de saída especificado e a fechamos.

### Exemplo de código-fonte para adicionar extensão da Web usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Conclusão

Parabéns! Agora você aprendeu como adicionar uma extensão da web usando Aspose.Cells for .NET. Experimente o código e explore recursos adicionais do Aspose.Cells para aproveitar ao máximo a manipulação de extensões da web em suas pastas de trabalho do Excel.

## Perguntas frequentes

#### P: O que é uma extensão da web em uma pasta de trabalho do Excel?

R: Uma extensão da web em uma pasta de trabalho do Excel é um componente que permite adicionar funcionalidades adicionais ao Excel integrando aplicativos da web. Ele pode oferecer recursos interativos, painéis personalizados, integrações externas e muito mais.

#### P: Como adicionar extensão da web à pasta de trabalho do Excel com Aspose.Cells?

 R: Para adicionar uma extensão da web a uma pasta de trabalho do Excel com Aspose.Cells, você pode seguir as etapas fornecidas em nosso guia passo a passo. Use o`WebExtensionCollection` e`WebExtensionTaskPaneCollection` classes para adicionar e configurar a extensão da web e o painel de tarefas associado.

#### P: Quais informações são necessárias para adicionar uma extensão da web?

R: Ao adicionar uma extensão da web, você deve fornecer o ID do SKU da extensão, o nome da loja e o tipo de loja. Essas informações ajudam a identificar e carregar a extensão corretamente.

#### P: Posso adicionar várias extensões da Web a uma única pasta de trabalho do Excel?

 R: Sim, você pode adicionar várias extensões da Web a uma única pasta de trabalho do Excel. Use o`Add` da coleção de extensões da web para adicionar cada extensão e associá-las aos painéis de tarefas correspondentes.