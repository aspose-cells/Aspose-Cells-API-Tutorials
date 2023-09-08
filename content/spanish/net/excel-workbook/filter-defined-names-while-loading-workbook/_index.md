---
title: Filtrar nombres definidos mientras se carga el libro de trabajo
linktitle: Filtrar nombres definidos mientras se carga el libro de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a filtrar nombres definidos al cargar un libro de Excel con Aspose.Cells para .NET.
type: docs
weight: 100
url: /es/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Cuando se trabaja con libros de Excel en una aplicación .NET, a menudo es necesario filtrar los datos durante la carga. Aspose.Cells para .NET es una poderosa biblioteca para manipular fácilmente libros de Excel. En esta guía, le mostraremos cómo filtrar los nombres definidos al cargar un libro usando Aspose.Cells para .NET. Siga estos sencillos pasos para obtener los resultados deseados:

## Paso 1: especificar las opciones de carga

Primero, debe especificar las opciones de carga para definir el comportamiento de carga del libro. En nuestro caso, queremos ignorar los nombres establecidos al cargar. Aquí se explica cómo hacerlo usando Aspose.Cells:

```csharp
// Especifica opciones de carga
LoadOptions opts = new LoadOptions();

// No cargar nombres definidos
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Paso 2: cargue el libro de trabajo

Una vez configuradas las opciones de carga, puede cargar el libro de Excel desde el archivo fuente. Asegúrese de especificar la ruta del archivo correcta. Aquí hay un código de muestra:

```csharp
// Cargar el libro de trabajo
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Paso 3: guarde el libro filtrado

Después de cargar el libro, puede realizar otras operaciones o ediciones según sea necesario. Luego puede guardar el libro filtrado en un archivo de salida. Así es cómo:

```csharp
// Guarde el libro de Excel filtrado
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Código fuente de muestra para filtrar nombres definidos mientras se carga el libro de trabajo usando Aspose.Cells para .NET 
```csharp
//Especificar las opciones de carga
LoadOptions opts = new LoadOptions();
//No queremos cargar nombres definidos
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Cargar el libro de trabajo
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Guarde el archivo Excel de salida, romperá la fórmula en C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Conclusión

Filtrar nombres definidos al cargar un libro de Excel puede ser fundamental para muchas aplicaciones. Aspose.Cells para .NET facilita esta tarea al proporcionar opciones flexibles para cargar y filtrar datos. Si sigue los pasos de esta guía, podrá filtrar eficazmente los nombres definidos y lograr los resultados deseados en sus libros de Excel.


### Preguntas frecuentes

#### P: ¿Aspose.Cells admite otros lenguajes de programación además de C#?
    
R: Sí, Aspose.Cells es una biblioteca multiplataforma que admite muchos lenguajes de programación como Java, Python, C.++y muchos más.

#### P: ¿Puedo filtrar otros tipos de datos al cargar un libro con Aspose.Cells?
    
R: Sí, Aspose.Cells ofrece una variedad de opciones de filtrado de datos que incluyen fórmulas, estilos, macros, etc.

#### P: ¿Aspose.Cells conserva el formato y las propiedades del libro original?
    
R: Sí, Aspose.Cells conserva el formato, los estilos, las fórmulas y otras propiedades del libro original cuando se trabaja con archivos de Excel.