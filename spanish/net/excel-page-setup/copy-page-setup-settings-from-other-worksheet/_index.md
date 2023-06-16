---
title: Copiar configuración de configuración de página desde otra hoja de cálculo
linktitle: Copiar configuración de configuración de página desde otra hoja de cálculo
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a copiar los ajustes de configuración de la página de una hoja de cálculo a otra usando Aspose.Cells para .NET. Una guía paso a paso para optimizar el uso de esta biblioteca.
type: docs
weight: 10
url: /es/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
En este artículo, lo guiaremos paso a paso para explicar el siguiente código fuente de C#: Copie los ajustes de configuración de la página desde otra hoja de cálculo usando Aspose.Cells para .NET. Usaremos la biblioteca Aspose.Cells para .NET para realizar esta operación. Si desea copiar la configuración de configuración de página de una hoja de trabajo a otra, siga los pasos a continuación.

## Paso 1: Creación del libro de trabajo
El primer paso es crear un libro de trabajo. En nuestro caso, usaremos la clase Workbook proporcionada por la biblioteca Aspose.Cells. Aquí está el código para crear un libro de trabajo:

```csharp
Workbook wb = new Workbook();
```

## Paso 2: agregar hojas de trabajo de prueba
Después de crear el libro de trabajo, necesitamos agregar hojas de trabajo de prueba. En este ejemplo, agregaremos dos hojas de trabajo. Aquí está el código para agregar dos hojas de trabajo:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Paso 3: Acceso a las hojas de trabajo
Ahora que hemos agregado las hojas de trabajo, necesitamos acceder a ellas para poder cambiar su configuración. Accederemos a las hojas de trabajo "TestSheet1" y "TestSheet2" utilizando sus nombres. Aquí está el código para acceder a él:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Paso 4: Configuración del tamaño del papel
 En este paso, estableceremos el tamaño de papel de la hoja de trabajo "TestSheet1". Usaremos el`PageSetup.PaperSize` propiedad para establecer el tamaño del papel. Por ejemplo, estableceremos el tamaño del papel en "PaperA3ExtraTransverse". Aquí está el código para eso:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Paso 5: Copia de la configuración de configuración de página
 Ahora copiaremos los ajustes de configuración de la página de la hoja de trabajo "TestSheet1" a "TestSheet2". Usaremos el`PageSetup.Copy` método para realizar esta operación. Aquí está el código para eso:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Paso 6: Tamaños de papel de impresión
 Después de copiar la configuración de configuración de la página, imprimiremos los tamaños de papel de las dos hojas de trabajo. Usaremos`Console.WriteLine` para mostrar los tamaños de papel. Aquí está el código para eso:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Ejemplo de código fuente para Copiar configuración de configuración de página desde otra hoja de trabajo usando Aspose.Cells para .NET 
```csharp
//Crear libro de trabajo
Workbook wb = new Workbook();
//Agregar dos hojas de trabajo de prueba
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Acceda a ambas hojas de trabajo como TestSheet1 y TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Establezca el tamaño de papel de TestSheet1 en PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Imprima el tamaño de papel de ambas hojas de trabajo
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Copie PageSetup de TestSheet1 a TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Imprima el tamaño de papel de ambas hojas de trabajo
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Conclusión
En este artículo, aprendimos cómo copiar los ajustes de configuración de la página de una hoja de trabajo a otra usando Aspose.Cells para .NET. Realizamos los siguientes pasos: crear el libro de trabajo, agregar hojas de trabajo de prueba, acceder a las hojas de trabajo, configurar el tamaño del papel, copiar la configuración de configuración de página e imprimir tamaños de papel. Ahora puede usar este conocimiento para copiar los ajustes de configuración de la página en sus propios proyectos.

### preguntas frecuentes

P: ¿Puedo copiar los ajustes de configuración de la página entre diferentes instancias del libro de trabajo?

 R: Sí, puede copiar la configuración de configuración de la página entre diferentes instancias del libro de trabajo usando el`PageSetup.Copy` método de la biblioteca Aspose.Cells.

P: ¿Puedo copiar otras configuraciones de configuración de página, como la orientación o los márgenes?

 R: Sí, puede copiar otras configuraciones de configuración de página usando el`PageSetup.Copy` método con las opciones apropiadas. Por ejemplo, puede copiar la orientación usando`CopyOptions.Orientation` y márgenes utilizando`CopyOptions.Margins`.

P: ¿Cómo sé qué opciones están disponibles para el tamaño del papel?

 R: Puede consultar la referencia de la API de la biblioteca Aspose.Cells para conocer las opciones disponibles para el tamaño del papel. Hay una enumeración llamada`PaperSizeType` que enumera los diferentes tamaños de papel admitidos.

P: ¿Cómo puedo descargar la biblioteca Aspose.Cells para .NET?

 R: Puede descargar la biblioteca Aspose.Cells para .NET desde[Lanzamientos de Aspose](https://releases.aspose.com/cells/net). Hay versiones de prueba gratuitas disponibles, así como licencias pagas para uso comercial.

P: ¿La biblioteca Aspose.Cells admite otros lenguajes de programación?

R: Sí, la biblioteca Aspose.Cells admite varios lenguajes de programación, incluidos C#, Java, Python y muchos más.