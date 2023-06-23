---
title: Vista previa de impresión del libro
linktitle: Vista previa de impresión del libro
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a generar una vista previa de impresión de un libro de trabajo con Aspose.Cells para .NET.
type: docs
weight: 170
url: /es/net/excel-workbook/workbook-print-preview/
---
La vista previa de impresión de un libro de trabajo es una característica esencial cuando se trabaja con archivos de Excel con Aspose.Cells para .NET. Puede generar fácilmente una vista previa de impresión siguiendo estos pasos:

## Paso 1: especificar el directorio de origen

Primero, debe especificar el directorio de origen donde se encuentra el archivo de Excel que desea obtener una vista previa. Aquí está cómo hacerlo:

```csharp
// directorio fuente
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Paso 2: Cargue el libro de trabajo

Luego, debe cargar el libro de trabajo Workbook desde el archivo de Excel especificado. Aquí está cómo hacerlo:

```csharp
// Cargue el libro de trabajo Workbook
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Paso 3: Configure las opciones de imagen e impresión

Antes de generar la vista previa de impresión, puede configurar la imagen y las opciones de impresión según sea necesario. En este ejemplo, estamos usando las opciones predeterminadas. Aquí está cómo hacerlo:

```csharp
// Opciones de imagen e impresión
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Paso 4: Genere la vista previa de impresión del libro de trabajo

Ahora puede generar la vista previa de impresión del libro de Workbook utilizando la clase WorkbookPrintingPreview. Aquí está cómo hacerlo:

```csharp
// Imprimir vista previa del libro
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Paso 5: Genere la vista previa de impresión de la hoja de trabajo

Si desea generar la vista previa de impresión de una hoja de trabajo específica, puede usar la clase SheetPrintingPreview. Aquí hay un ejemplo :

```csharp
// Imprimir vista previa de la hoja de trabajo
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Ejemplo de código fuente para la vista previa de impresión del libro usando Aspose.Cells para .NET 
```csharp
//directorio de origen
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Conclusión

La generación de la vista previa de impresión de un libro de trabajo es una característica poderosa que ofrece Aspose.Cells para .NET. Siguiendo los pasos anteriores, puede obtener fácilmente una vista previa de su libro de Excel y obtener información sobre la cantidad de páginas para imprimir.

### preguntas frecuentes

#### P: ¿Cómo puedo especificar un directorio de origen diferente para cargar mi libro de trabajo?
    
 R: Puede utilizar el`Set_SourceDirectory` método para especificar un directorio de origen diferente. Por ejemplo:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### P: ¿Puedo personalizar la imagen y las opciones de impresión al generar la vista previa de impresión?
    
 R: Sí, puede personalizar las opciones de imagen e impresión cambiando las propiedades de la`ImageOrPrintOptions` objeto. Por ejemplo, puede configurar la resolución de la imagen, el formato del archivo de salida, etc.

#### P: ¿Es posible generar una vista previa de impresión para varias hojas de trabajo en un libro de trabajo?
    
R: Sí, puede iterar sobre las diferentes hojas de trabajo en el Libro de trabajo y generar una vista previa de impresión para cada hoja usando el`SheetPrintingPreview` clase.

#### P: ¿Cómo guardo la vista previa de impresión como imagen o archivo PDF?
    
 R: Puedes usar`ToImage` o`ToPdf` método de`WorkbookPrintingPreview` o`SheetPrintingPreview` objeto para guardar la vista previa de impresión como imagen o archivo PDF.

#### P: ¿Qué puedo hacer con la vista previa de impresión una vez generada?
    
R: Una vez que haya generado la vista previa de impresión, puede verla en pantalla, guardarla como imagen o archivo PDF, o usarla para otras operaciones, como enviar por correo electrónico o imprimir.
	