---
title: Implementar el tamaño de papel personalizado de la hoja de trabajo para la representación
linktitle: Implementar el tamaño de papel personalizado de la hoja de trabajo para la representación
second_title: Referencia de API de Aspose.Cells para .NET
description: Guía paso a paso para implementar un tamaño de hoja de cálculo personalizado con Aspose.Cells para .NET. Establezca las dimensiones, agregue un mensaje y guárdelo como PDF.
type: docs
weight: 50
url: /es/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Implementar un tamaño personalizado para su hoja de trabajo puede ser muy útil cuando desea crear un documento PDF con un tamaño específico. En este tutorial, aprenderemos a usar Aspose.Cells para .NET para establecer un tamaño personalizado para una hoja de trabajo y luego guardar el documento como PDF.

## Paso 1: Crear la carpeta de salida

Antes de comenzar, debe crear una carpeta de salida donde se guardará el archivo PDF generado. Puede usar la ruta que desee para su carpeta de salida.

```csharp
// Directorios de salida
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Asegúrese de especificar la ruta correcta a su carpeta de salida.

## Paso 2: Creación del objeto Libro de trabajo

Para comenzar, debe crear un objeto Workbook usando Aspose.Cells. Este objeto representa su hoja de cálculo.

```csharp
// Crear el objeto Libro de trabajo
Workbook wb = new Workbook();
```

## Paso 3: Acceso a la primera hoja de trabajo

Después de crear el objeto Libro de trabajo, puede acceder a la primera hoja de trabajo dentro de él.

```csharp
// Acceso a la primera ficha
Worksheet ws = wb.Worksheets[0];
```

## Paso 4: Configuración del tamaño de la hoja de cálculo personalizada

 Ahora puede configurar el tamaño de la hoja de trabajo personalizado usando`CustomPaperSize(width, height)` método de la clase PageSetup.

```csharp
// Establecer el tamaño de la hoja de trabajo personalizado (en pulgadas)
ws.PageSetup.CustomPaperSize(6, 4);
```

En este ejemplo, hemos establecido el tamaño de la hoja de trabajo en 6 pulgadas de ancho y 4 pulgadas de alto.

## Paso 5: Acceso a la celda B4

Después de eso, podemos acceder a una celda específica en la hoja de trabajo. En este caso, accederemos a la celda B4.

```csharp
// Acceso a la celda B4
Cell b4 = ws.Cells["B4"];
```

## Paso 6: Agregar el mensaje en la celda B4

 Ahora podemos agregar un mensaje a la celda B4 usando el`PutValue(value)` método.

```csharp
// Agrega el mensaje en la celda B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

En este ejemplo, agregamos el mensaje "Tamaño de página PDF: 6,00" x 4,00" en la celda B4.

## Paso 7: Guardar la hoja de trabajo en formato PDF

 Finalmente, podemos guardar la hoja de trabajo en formato PDF usando el`Save(filePath)` método del objeto Workbook.

```csharp
// Guarde la hoja de trabajo en formato PDF
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Especifique la ruta deseada al archivo PDF generado, utilizando la carpeta de salida creada anteriormente.

### Ejemplo de código fuente para implementar el tamaño de papel personalizado de la hoja de trabajo para renderizar usando Aspose.Cells para .NET 
```csharp
//Directorio de salida
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Crear objeto de libro de trabajo
Workbook wb = new Workbook();
//Acceder a la primera hoja de trabajo
Worksheet ws = wb.Worksheets[0];
//Establecer el tamaño de papel personalizado en unidades de pulgadas
ws.PageSetup.CustomPaperSize(6, 4);
//Acceder a la celda B4
Cell b4 = ws.Cells["B4"];
//Agrega el mensaje en la celda B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Guardar el libro de trabajo en formato pdf
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Conclusiones

En este tutorial, aprendió a implementar el tamaño personalizado de una hoja de trabajo usando Aspose.Cells para .NET. Puede usar estos pasos para establecer dimensiones específicas para sus hojas de trabajo y luego guardar los documentos en formato PDF. Esperamos que esta guía haya sido útil para comprender el proceso de implementación de un tamaño de hoja de cálculo personalizado.

### Preguntas frecuentes (FAQ)

#### Pregunta 1: ¿Puedo personalizar aún más el diseño de la hoja de cálculo?

Sí, Aspose.Cells ofrece muchas opciones para personalizar el diseño de su hoja de trabajo. Puede establecer dimensiones personalizadas, orientación de página, márgenes, encabezados y pies de página, y mucho más.

#### Pregunta 2: ¿Qué otros formatos de salida admite Aspose.Cells?

Aspose.Cells admite muchos formatos de salida diferentes, incluidos PDF, XLSX, XLS, CSV, HTML, TXT y muchos más. Puede elegir el formato de salida deseado según sus necesidades.