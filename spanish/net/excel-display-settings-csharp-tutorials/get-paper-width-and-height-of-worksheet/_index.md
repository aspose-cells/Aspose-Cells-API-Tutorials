---
title: Obtenga el ancho y la altura del papel de la hoja de trabajo
linktitle: Obtenga el ancho y la altura del papel de la hoja de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Cree una guía paso a paso para explicar el siguiente código fuente de C# para obtener el ancho y el alto del papel de una hoja de cálculo usando Aspose.Cells para .NET.
type: docs
weight: 80
url: /es/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
En este tutorial, lo guiaremos paso a paso para explicar el siguiente código fuente de C# para obtener el ancho y el alto del papel de una hoja de trabajo usando Aspose.Cells para .NET. Siga los pasos a continuación:

## Paso 1: Crear el libro de trabajo
 Comience por crear un nuevo libro de trabajo usando el`Workbook` clase:

```csharp
Workbook wb = new Workbook();
```

## Paso 2: Acceda a la primera hoja de trabajo
 A continuación, navegue a la primera hoja de trabajo en el libro de trabajo usando el`Worksheet` clase:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Paso 3: establezca el tamaño del papel en A2 y muestre el ancho y la altura del papel en pulgadas
 Utilizar el`PaperSize` propiedad de la`PageSetup` objeto para establecer el tamaño del papel en A2 y, a continuación, utilice el`PaperWidth` y`PaperHeight` properties para obtener el ancho y alto del papel respectivamente. Muestre estos valores usando el`Console.WriteLine` método:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Paso 4: repita los pasos para otros tamaños de papel
Repita los pasos anteriores, cambiando el tamaño del papel a A3, A4 y Carta, y luego muestre los valores de ancho y alto del papel para cada tamaño:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Ejemplo de código fuente para obtener el ancho y el alto del papel de la hoja de trabajo usando Aspose.Cells para .NET 

```csharp
//Crear libro de trabajo
Workbook wb = new Workbook();
//Acceder a la primera hoja de trabajo
Worksheet ws = wb.Worksheets[0];
//Establezca el tamaño del papel en A2 e imprima el ancho y la altura del papel en pulgadas
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Establezca el tamaño del papel en A3 e imprima el ancho y la altura del papel en pulgadas
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Establezca el tamaño del papel en A4 e imprima el ancho y la altura del papel en pulgadas
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Establezca el tamaño del papel en Carta e imprima el ancho y alto del papel en pulgadas
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Conclusión

Aprendió a usar Aspose.Cells para .NET para obtener el ancho y el alto del papel de una hoja de cálculo. Esta característica puede ser útil para la configuración y el diseño preciso de sus documentos de Excel.

### Preguntas frecuentes (FAQ)

#### ¿Qué es Aspose.Cells para .NET?

Aspose.Cells for .NET es una poderosa biblioteca para manipular y procesar archivos de Excel en aplicaciones .NET. Ofrece muchas funciones para crear, modificar, convertir y analizar archivos de Excel.

#### ¿Cómo puedo obtener el tamaño de papel de una hoja de cálculo con Aspose.Cells para .NET?

 Puedes usar el`PageSetup` clase de la`Worksheet` objeto para acceder al tamaño del papel. Utilizar el`PaperSize` propiedad para establecer el tamaño del papel y el`PaperWidth` y`PaperHeight` properties para obtener el ancho y alto del papel respectivamente.

#### ¿Qué tamaños de papel admite Aspose.Cells para .NET?

Aspose.Cells para .NET admite una amplia gama de tamaños de papel de uso común, como A2, A3, A4 y Carta, así como muchos otros tamaños personalizados.

#### ¿Puedo personalizar el tamaño del papel de una hoja de cálculo con Aspose.Cells para .NET?

Sí, puede configurar un tamaño de papel personalizado especificando las dimensiones exactas de ancho y alto usando el`PaperWidth` y`PaperHeight` propiedades de la`PageSetup` clase.