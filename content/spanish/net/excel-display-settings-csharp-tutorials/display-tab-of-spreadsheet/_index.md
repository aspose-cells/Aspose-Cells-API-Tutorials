---
title: Mostrar ficha de hoja de cálculo
linktitle: Mostrar ficha de hoja de cálculo
second_title: Referencia de API de Aspose.Cells para .NET
description: Muestre una pestaña de hoja de cálculo de Excel usando Aspose.Cells para .NET.
type: docs
weight: 60
url: /es/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
En este tutorial, le mostraremos cómo mostrar la pestaña de una hoja de cálculo de Excel utilizando el código fuente de C# con Aspose.Cells para .NET. Siga los pasos a continuación para obtener el resultado deseado.

## Paso 1: importa las bibliotecas necesarias

Asegúrese de haber instalado la biblioteca Aspose.Cells para .NET e importe las bibliotecas necesarias en su proyecto C#.

```csharp
using Aspose.Cells;
```

## Paso 2: establezca la ruta del directorio y abra el archivo de Excel

 Establezca la ruta al directorio que contiene su archivo de Excel, luego abra el archivo instanciando un`Workbook` objeto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Paso 3: Mostrar la pestaña de la hoja de trabajo

 Utilizar el`ShowTabs` propiedad de la`Workbook.Settings` objeto para mostrar la pestaña de la hoja de cálculo de Excel.

```csharp
workbook.Settings.ShowTabs = true;
```

## Paso 4: Guardar cambios

 Una vez que haya realizado los cambios necesarios, guarde el archivo de Excel modificado utilizando el`Save` metodo de la`Workbook` objeto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Ejemplo de código fuente para la pestaña Mostrar de la hoja de cálculo usando Aspose.Cells para .NET 

```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una instancia de un objeto Workbook
// Abriendo el archivo de Excel
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Ocultar las pestañas del archivo de Excel
workbook.Settings.ShowTabs = true;
// Guardar el archivo de Excel modificado
workbook.Save(dataDir + "output.xls");
```

### Conclusión

Esta guía paso a paso le mostró cómo mostrar la pestaña de una hoja de cálculo de Excel usando Aspose.Cells para .NET. Con el código fuente de C# provisto, puede personalizar fácilmente la visualización de las pestañas en sus archivos de Excel.

### Preguntas frecuentes (FAQ)

#### ¿Qué es Aspose.Cells para .NET?

Aspose.Cells for .NET es una poderosa biblioteca para manipular archivos de Excel en aplicaciones .NET.

#### ¿Cómo puedo instalar Aspose.Cells para .NET?

 Para instalar Aspose.Cells para .NET, debe descargar el paquete correspondiente de[Lanzamientos de Aspose](https://releases/aspose.com/cells/net/) y agréguelo a su proyecto .NET.

#### ¿Cómo mostrar la pestaña de una hoja de cálculo de Excel usando Aspose.Cells para .NET?

 Puedes usar el`ShowTabs` propiedad de la`Workbook.Settings` objeto y establecerlo en`true` para mostrar la pestaña de la hoja de trabajo.

#### ¿Qué otros formatos de archivo de Excel son compatibles con Aspose.Cells para .NET?

Aspose.Cells para .NET admite una variedad de formatos de archivo de Excel, como XLS, XLSX, CSV, HTML, PDF, etc.
