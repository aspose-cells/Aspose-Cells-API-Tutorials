---
title: Determinar si el tamaño de papel de la hoja de trabajo es automático
linktitle: Determinar si el tamaño de papel de la hoja de trabajo es automático
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a determinar si el tamaño de papel de una hoja de cálculo es automático con Aspose.Cells para .NET.
type: docs
weight: 20
url: /es/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
En este artículo, lo guiaremos paso a paso para explicar el siguiente código fuente de C#: Determine si el tamaño del papel de una hoja de trabajo es automático usando Aspose.Cells para .NET. Usaremos la biblioteca Aspose.Cells para .NET para realizar esta operación. Siga los pasos a continuación para determinar si el tamaño de papel de una hoja de cálculo es automático.

## Paso 1: Cargar libros de trabajo
El primer paso es cargar los libros de trabajo. Tendremos dos libros de trabajo: uno con el tamaño de papel automático deshabilitado y el otro con el tamaño de papel automático habilitado. Aquí está el código para cargar los libros de trabajo:

```csharp
// directorio fuente
string sourceDir = "YOUR_SOURCE_DIR";
// Directorio de salida
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Cargue el primer libro de trabajo con el tamaño de papel automático deshabilitado
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Cargue el segundo libro de trabajo con el tamaño de papel automático habilitado
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Paso 2: Acceso a hojas de cálculo
Ahora que hemos cargado los libros de trabajo, necesitamos acceder a las hojas de trabajo para poder verificar el tamaño de papel automático. Iremos a la primera hoja de trabajo de los dos libros de trabajo. Aquí está el código para acceder a él:

```csharp
//Ir a la primera hoja de trabajo del primer libro de trabajo
Worksheet ws11 = wb1.Worksheets[0];

// Ir a la primera hoja de trabajo del segundo libro de trabajo
Worksheet ws12 = wb2.Worksheets[0];
```

## Paso 3: Comprobar el tamaño de papel automático
 En este paso, comprobaremos si el tamaño del papel de la hoja de trabajo es automático. Usaremos el`PageSetup.IsAutomaticPaperSize` propiedad para obtener esta información. Luego mostraremos el resultado. Aquí está el código para eso:

```csharp
// Muestre la propiedad IsAutomaticPaperSize de la primera hoja de trabajo en el primer libro de trabajo
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Mostrar la propiedad IsAutomaticPaperSize de la primera hoja de trabajo en el segundo libro
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Ejemplo de código fuente para Determinar si el tamaño del papel de la hoja de trabajo es automático usando Aspose.Cells para .NET 
```csharp
//directorio de origen
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Directorio de salida
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Cargue el primer libro de trabajo con tamaño de papel automático falso
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Cargue el segundo libro de trabajo con tamaño de papel automático verdadero
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Acceder a la primera hoja de trabajo de ambos libros
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Imprima la propiedad PageSetup.IsAutomaticPaperSize de ambas hojas de trabajo
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Conclusión
En este artículo, aprendimos cómo determinar si el tamaño del papel de una hoja de trabajo es automático usando Aspose.Cells para .NET. Seguimos los siguientes pasos: cargar los libros de trabajo,

acceso a hojas de cálculo y comprobación automática del tamaño del papel. Ahora puede utilizar este conocimiento para determinar si el tamaño del papel de sus hojas de cálculo es automático.

### preguntas frecuentes

#### P: ¿Cómo puedo cargar libros de trabajo con Aspose.Cells para .NET?

R: Puede cargar libros de trabajo mediante la clase Workbook de la biblioteca Aspose.Cells. Utilice el método Workbook.Load para cargar un libro de trabajo desde un archivo.

#### P: ¿Puedo verificar el tamaño de papel automático para otras hojas de cálculo?

R: Sí, puede verificar el tamaño de papel automático para cualquier hoja de cálculo accediendo a la propiedad PageSetup.IsAutomaticPaperSize del objeto Hoja de cálculo correspondiente.

#### P: ¿Cómo puedo cambiar el tamaño de papel automático de una hoja de cálculo?

R: Para cambiar el tamaño de papel automático de una hoja de trabajo, puede usar la propiedad PageSetup.IsAutomaticPaperSize y establecerla en el valor deseado (verdadero o falso).

#### P: ¿Qué otras funciones ofrece Aspose.Cells para .NET?

R: Aspose.Cells para .NET ofrece muchas funciones para trabajar con hojas de cálculo, como la creación, modificación y conversión de libros de trabajo, así como la manipulación de datos, fórmulas y formateo.