---
title: Agregar extensión web
linktitle: Agregar extensión web
second_title: Referencia de API de Aspose.Cells para .NET
description: Agregue fácilmente una extensión web a sus libros de Excel con Aspose.Cells para .NET.
type: docs
weight: 40
url: /es/net/excel-workbook/add-web-extension/
---
En este tutorial paso a paso, explicaremos el código fuente C# proporcionado que le permitirá agregar una extensión web usando Aspose.Cells para .NET. Siga los pasos a continuación para agregar una extensión web a su libro de Excel.

## Paso 1: configurar el directorio de salida

```csharp
// Directorio de salida
string outDir = RunExamples.Get_OutputDirectory();
```

En este primer paso, definimos el directorio de salida donde se guardará el libro de Excel modificado.

## Paso 2: crear un nuevo libro de trabajo

```csharp
// Crear un nuevo libro de trabajo
Workbook workbook = new Workbook();
```

Aquí estamos creando un nuevo libro de Excel usando el`Workbook` clase de Aspose.Cells.

## Paso 3: acceda a la colección de extensiones web

```csharp
// Accede a la colección de extensiones web.
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Accedemos a la colección de extensiones web del libro de Excel usando el`WebExtensions` propiedad de la`Worksheets` objeto.

## Paso 4: agrega una nueva extensión web

```csharp
// Agregar una nueva extensión web
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Estamos agregando una nueva extensión web a la colección de extensiones. Definimos el ID de referencia, el nombre de la tienda y el tipo de tienda de la extensión.

## Paso 5: acceda a la colección del panel de tareas de la extensión web

```csharp
// Acceda a la colección del panel de tareas de la extensión web
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Accedemos a la colección de paneles de tareas de Excel Workbook Web Extension usando el`WebExtensionTaskPanes` propiedad de la`Worksheets` objeto.

## Paso 6: agregue un nuevo panel de tareas

```csharp
// Agregar un nuevo panel de tareas
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Estamos agregando un nuevo panel de tareas a la colección de paneles de tareas. Configuramos la visibilidad del panel, su estado de acoplamiento y la extensión web asociada.

## Paso 7: guarde y cierre el libro de trabajo

```csharp
// Guarde y cierre el libro de trabajo.
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Guardamos el libro de trabajo modificado en el directorio de salida especificado y luego lo cerramos.

### Código fuente de muestra para Agregar extensión web usando Aspose.Cells para .NET 
```csharp
//Directorio fuente
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

## Conclusión

¡Enhorabuena! Ahora ha aprendido cómo agregar una extensión web usando Aspose.Cells para .NET. Experimente con el código y explore funciones adicionales de Aspose.Cells para aprovechar al máximo la manipulación de extensiones web en sus libros de Excel.

## Preguntas frecuentes

#### P: ¿Qué es una extensión web en un libro de Excel?

R: Una extensión web en un libro de Excel es un componente que le permite agregar funcionalidad adicional a Excel mediante la integración de aplicaciones web. Puede ofrecer funciones interactivas, paneles personalizados, integraciones externas y más.

#### P: ¿Cómo agregar una extensión web al libro de Excel con Aspose.Cells?

 R: Para agregar una extensión web a un libro de Excel con Aspose.Cells, puede seguir los pasos proporcionados en nuestra guía paso a paso. Utilizar el`WebExtensionCollection` y`WebExtensionTaskPaneCollection` clases para agregar y configurar la extensión web y el panel de tareas asociado.

#### P: ¿Qué información se requiere para agregar una extensión web?

R: Al agregar una extensión web, debe proporcionar el ID de SKU de la extensión, el nombre de la tienda y el tipo de tienda. Esta información ayuda a identificar y cargar la extensión correctamente.

#### P: ¿Puedo agregar varias extensiones web a un solo libro de Excel?

 R: Sí, puede agregar varias extensiones web a un solo libro de Excel. Utilizar el`Add` método de la colección de extensiones web para agregar cada extensión y luego asociarlas con los paneles de tareas correspondientes.