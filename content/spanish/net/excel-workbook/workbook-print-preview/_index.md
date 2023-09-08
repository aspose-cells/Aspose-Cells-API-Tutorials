---
title: Vista previa de impresión del libro de trabajo
linktitle: Vista previa de impresión del libro de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a generar una vista previa de impresión de un libro usando Aspose.Cells para .NET.
type: docs
weight: 170
url: /es/net/excel-workbook/workbook-print-preview/
---
La vista previa de impresión de un libro de trabajo es una característica esencial cuando se trabaja con archivos de Excel con Aspose.Cells para .NET. Puede generar fácilmente una vista previa de impresión siguiendo estos pasos:

## Paso 1: especificar el directorio de origen

Primero, debe especificar el directorio de origen donde se encuentra el archivo de Excel que desea obtener una vista previa. He aquí cómo hacerlo:

```csharp
// directorio fuente
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Paso 2: cargue el libro de trabajo

Luego, debe cargar el libro de trabajo desde el archivo de Excel especificado. He aquí cómo hacerlo:

```csharp
// Cargar el libro de trabajo
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Paso 3: configurar las opciones de imagen e impresión

Antes de generar la vista previa de impresión, puede configurar la imagen y las opciones de impresión según sea necesario. En este ejemplo, estamos usando las opciones predeterminadas. He aquí cómo hacerlo:

```csharp
// Opciones de imagen e impresión
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Paso 4: genere la vista previa de impresión del libro

Ahora puede generar la vista previa de impresión del libro de trabajo utilizando la clase WorkbookPrintingPreview. He aquí cómo hacerlo:

```csharp
// Vista previa de impresión del libro de trabajo
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Paso 5: genere la vista previa de impresión de la hoja de trabajo

Si desea generar la vista previa de impresión de una hoja de trabajo específica, puede utilizar la clase SheetPrintingPreview. Aquí hay un ejemplo :

```csharp
// Vista previa de impresión de la hoja de trabajo
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Código fuente de muestra para la vista previa de impresión del libro de trabajo usando Aspose.Cells para .NET 
```csharp
//Directorio fuente
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

Generar la vista previa de impresión de un libro de trabajo es una característica poderosa que ofrece Aspose.Cells para .NET. Si sigue los pasos indicados anteriormente, puede obtener fácilmente una vista previa de su libro de Excel y obtener información sobre la cantidad de páginas que desea imprimir.

### Preguntas frecuentes

#### P: ¿Cómo puedo especificar un directorio de origen diferente para cargar mi libro de trabajo?
    
 R: Puedes usar el`Set_SourceDirectory` método para especificar un directorio de origen diferente. Por ejemplo:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### P: ¿Puedo personalizar la imagen y las opciones de impresión al generar la vista previa de impresión?
    
 R: Sí, puede personalizar las opciones de imagen e impresión cambiando las propiedades del`ImageOrPrintOptions` objeto. Por ejemplo, puede configurar la resolución de la imagen, el formato del archivo de salida, etc.

#### P: ¿Es posible generar una vista previa de impresión para varias hojas de trabajo en un libro de trabajo?
    
R: Sí, puede iterar sobre las diferentes hojas de trabajo en el Libro de trabajo y generar una vista previa de impresión para cada hoja usando el`SheetPrintingPreview` clase.

#### P: ¿Cómo guardo la vista previa de impresión como una imagen o un archivo PDF?
    
 R: Puedes usar`ToImage` o`ToPdf` método de`WorkbookPrintingPreview` o`SheetPrintingPreview` objeto para guardar la vista previa de impresión como imagen o archivo PDF.

#### P: ¿Qué puedo hacer con la vista previa de impresión una vez generada?
    
R: Una vez que haya generado la vista previa de impresión, podrá verla en pantalla, guardarla como una imagen o archivo PDF, o utilizarla para otras operaciones como enviar por correo electrónico o imprimir.
	