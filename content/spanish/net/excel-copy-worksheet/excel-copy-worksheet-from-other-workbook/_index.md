---
title: Copiar hoja de trabajo de Excel desde otro libro de trabajo
linktitle: Copiar hoja de trabajo de Excel desde otro libro de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Copie fácilmente una hoja de cálculo de Excel de un libro a otro usando Aspose.Cells para .NET.
type: docs
weight: 10
url: /es/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
En este tutorial, lo guiaremos a través de los pasos para copiar una hoja de cálculo de Excel desde otro libro usando la biblioteca Aspose.Cells para .NET. Siga las instrucciones a continuación para completar esta tarea.

## Paso 1: preparación

Antes de comenzar, asegúrese de haber instalado Aspose.Cells para .NET y creado un proyecto C# en su entorno de desarrollo integrado (IDE) preferido.

## Paso 2: establezca la ruta del directorio de documentos

 Declarar un`dataDir` variable e inicialícela con la ruta a su directorio de documentos. Por ejemplo :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Asegúrate de reemplazar`"YOUR_DOCUMENTS_DIRECTORY"` con la ruta real a su directorio.

## Paso 3: cree un nuevo libro de Excel

 Utilizar el`Workbook` clase de Aspose.Cells para crear un nuevo libro de Excel:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Paso 4: obtenga la primera hoja de trabajo del libro de trabajo

Navegue a la primera hoja de trabajo del libro usando el índice 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Paso 5: agregar datos a las filas del encabezado (A1:A4)

 Usar una`for` bucle para agregar datos a las filas del encabezado (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Paso 6: Agregar datos detallados (A5:A999)

 usa otro`for` bucle para agregar datos detallados (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Paso 7: configurar las opciones de diseño

 Establezca las opciones de configuración de página para la hoja de trabajo usando el`PageSetup` objeto:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Paso 8: crea otro libro de Excel

Cree otro libro de Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Paso 9: obtenga la primera hoja de trabajo del segundo libro

Navegue a la primera hoja de trabajo en el segundo libro de trabajo:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Paso 10: nombre la hoja de trabajo

nombra el fuego

isla de cálculo:

```csharp
ws1.Name = "MySheet";
```

## Paso 11: copie los datos de la primera hoja de trabajo del primer libro a la primera hoja de trabajo del segundo libro

Copie los datos de la primera hoja de trabajo del primer libro a la primera hoja de trabajo del segundo libro:

```csharp
ws1.Copy(ws0);
```

## Paso 12: guarde el archivo de Excel

Guarde el archivo de Excel:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Asegúrese de especificar la ruta y el nombre de archivo deseados para el archivo de salida.

### Código fuente de muestra para copiar hoja de trabajo de Excel desde otro libro de trabajo usando Aspose.Cells para .NET 
```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Cree un nuevo libro de trabajo.
Workbook excelWorkbook0 = new Workbook();
// Obtenga la primera hoja de trabajo del libro.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Coloque algunos datos en las filas del encabezado (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Poner algunos datos de detalle (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Defina un objeto de configuración de página basado en la primera hoja de trabajo.
PageSetup pagesetup = ws0.PageSetup;
// Las primeras cinco filas se repiten en cada página...
// Se puede ver en la vista previa de impresión.
pagesetup.PrintTitleRows = "$1:$5";
// Crea otro libro de trabajo.
Workbook excelWorkbook1 = new Workbook();
// Obtenga la primera hoja de trabajo del libro.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Nombra la hoja de trabajo.
ws1.Name = "MySheet";
// Copie los datos de la primera hoja de trabajo del primer libro de trabajo en el
// primera hoja de trabajo del segundo libro de trabajo.
ws1.Copy(ws0);
// Guarde el archivo de Excel.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Conclusión

¡Enhorabuena! Ahora ha aprendido cómo copiar una hoja de cálculo de Excel desde otro libro usando Aspose.Cells para .NET. No dude en utilizar este método en sus propios proyectos para manipular archivos de Excel de manera eficiente.

### Preguntas frecuentes

#### P. ¿Qué bibliotecas se necesitan para usar Aspose.Cells para .NET?

A. Para utilizar Aspose.Cells para .NET, debe incluir la biblioteca Aspose.Cells en su proyecto. Asegúrese de haber hecho referencia a esta biblioteca correctamente en su entorno de desarrollo integrado (IDE).

#### P. ¿Aspose.Cells admite otros formatos de archivos de Excel, como XLSX?

A. Sí, Aspose.Cells admite varios formatos de archivos de Excel, incluidos XLSX, XLS, CSV, HTML y muchos más. Puede manipular estos formatos de archivo utilizando las funciones de Aspose.Cells para .NET.

#### P. ¿Puedo personalizar las opciones de diseño al copiar la hoja de trabajo?

A.  Sí, puede personalizar las opciones de configuración de página al copiar la hoja de trabajo usando las propiedades del`PageSetup` objeto. Puede especificar encabezados de página, pies de página, márgenes, orientaciones, etc.