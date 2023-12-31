---
title: Obtener dimensiones de página
linktitle: Obtener dimensiones de página
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda cómo recuperar dimensiones de página en Excel usando Aspose.Cells para .NET. Guía paso a paso con código fuente en C#.
type: docs
weight: 40
url: /es/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells para .NET es una poderosa biblioteca que permite a los desarrolladores trabajar con archivos de Microsoft Excel mediante programación. Ofrece una amplia gama de funciones para manipular documentos de Excel, incluida la capacidad de obtener dimensiones de página. En este tutorial, lo guiaremos a través de los pasos para recuperar las dimensiones de la página usando Aspose.Cells para .NET.

## Paso 1: crear una instancia de la clase Libro de trabajo

Para comenzar, necesitamos crear una instancia de la clase Libro de trabajo, que representa el libro de Excel. Esto se puede lograr usando el siguiente código:

```csharp
Workbook book = new Workbook();
```

## Paso 2: acceder a la hoja de cálculo

A continuación, debemos navegar a la hoja de trabajo del libro donde queremos configurar las dimensiones de la página. En este ejemplo, supongamos que queremos trabajar con la primera hoja de trabajo. Podemos acceder a él mediante el siguiente código:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Paso 3: establezca el tamaño del papel en A2 e imprima el ancho y alto en pulgadas

Ahora estableceremos el tamaño del papel en A2 e imprimiremos el ancho y alto de la página en pulgadas. Esto se puede lograr usando el siguiente código:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Paso 4: establezca el tamaño del papel en A3 e imprima el ancho y alto en pulgadas

A continuación, configuraremos el tamaño del papel en A3 e imprimiremos el ancho y alto de la página en pulgadas. Aquí está el código correspondiente:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Paso 5: establezca el tamaño del papel en A4 e imprima el ancho y alto en pulgadas

Ahora configuraremos el tamaño del papel en A4 e imprimiremos el ancho y alto de la página en pulgadas. Aquí está el código:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Paso 6: establezca el tamaño del papel en Carta e imprima el ancho y el alto en pulgadas

Finalmente, configuraremos el tamaño del papel en Carta e imprimiremos el ancho y alto de la página en pulgadas. Aquí está el código:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Código fuente de muestra para Obtener dimensiones de página usando Aspose.Cells para .NET 
```csharp
// Crear una instancia de la clase Libro de trabajo
Workbook book = new Workbook();
// Acceder a la primera hoja de trabajo
Worksheet sheet = book.Worksheets[0];
// Establezca el tamaño del papel en A2 e imprima el ancho y alto del papel en pulgadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Establezca el tamaño del papel en A3 e imprima el ancho y alto del papel en pulgadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Establezca el tamaño del papel en A4 e imprima el ancho y alto del papel en pulgadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Establezca el tamaño del papel en Carta e imprima el ancho y alto del papel en pulgadas
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Conclusión

¡Enhorabuena! Aprendió a recuperar dimensiones de página usando Aspose.Cells para .NET. Esta función puede resultar útil cuando necesita realizar operaciones específicas basadas en las dimensiones de la página en sus archivos de Excel.

No olvide explorar más a fondo la documentación de Aspose.Cells para descubrir todas las potentes funciones que ofrece.

### Preguntas frecuentes

#### 1. ¿Qué otros tamaños de papel admite Aspose.Cells para .NET?

Aspose.Cells para .NET admite una variedad de tamaños de papel, incluidos A1, A5, B4, B5, Executive, Legal, Letter y muchos más. Puede consultar la documentación para obtener la lista completa de tamaños de papel admitidos.

#### 2. ¿Puedo configurar dimensiones de página personalizadas con Aspose.Cells para .NET?

Sí, puede establecer dimensiones de página personalizadas especificando el ancho y alto deseados. Aspose.Cells ofrece total flexibilidad para personalizar las dimensiones de la página según sus necesidades.

#### 3. ¿Puedo obtener las dimensiones de la página en unidades distintas a pulgadas?

Sí, Aspose.Cells para .NET le permite obtener dimensiones de página en diferentes unidades, incluidas pulgadas, centímetros, milímetros y puntos.

#### 4. ¿Aspose.Cells para .NET admite otras funciones de edición de configuraciones de página?

Sí, Aspose.Cells ofrece una gama completa de funciones para editar la configuración de la página, incluida la configuración de márgenes, orientación, encabezados y pies de página, etc.