---
title: Opciones de Ajustar a páginas de Excel
linktitle: Opciones de Ajustar a páginas de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a ajustar páginas automáticamente en una hoja de cálculo de Excel con Aspose.Cells para .NET.
type: docs
weight: 30
url: /es/net/excel-page-setup/fit-to-excel-pages-options/
---
En este artículo, lo guiaremos paso a paso para explicar el siguiente código fuente de C#: Ajuste a las opciones de páginas de Excel usando Aspose.Cells para .NET. Usaremos la biblioteca Aspose.Cells para .NET para realizar esta operación. Siga los pasos a continuación para configurar el ajuste a las páginas en Excel.

## Paso 1: crear un libro de trabajo
El primer paso es crear un libro de trabajo. Vamos a instanciar un objeto Workbook. Aquí está el código para crear un libro de trabajo:

```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Crear una instancia de un objeto Workbook
Workbook workbook = new Workbook();
```

## Paso 2: Acceso a la hoja de trabajo
Ahora que hemos creado el libro de trabajo, necesitamos navegar a la primera hoja de trabajo. Usaremos el índice 0 para acceder a la primera hoja. Aquí está el código para acceder a él:

```csharp
// Acceso a la primera hoja de trabajo en el libro de trabajo
Worksheet worksheet = workbook.Worksheets[0];
```

## Paso 3: Configuración del ajuste a las páginas
 En este paso, configuraremos el ajuste a las páginas de la hoja de trabajo. Usaremos el`FitToPagesTall` y`FitToPagesWide` propiedades de la`PageSetup` objeto para especificar el número deseado de páginas para la altura y el ancho de la hoja de trabajo. Aquí está el código para eso:

```csharp
// Configure el número de páginas para la altura de la hoja de trabajo
worksheet.PageSetup.FitToPagesTall = 1;

// Configure el número de páginas para el ancho de la hoja de trabajo
worksheet.PageSetup.FitToPagesWide = 1;
```

## Paso 4: Guardar el libro de trabajo
 Ahora que hemos configurado el ajuste a las páginas, podemos guardar el libro de trabajo. Usaremos el`Save` método del objeto Workbook para esto. Aquí está el código para guardar el libro de trabajo:

```csharp
// Guardar el libro de trabajo
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Ejemplo de código fuente para las opciones de Ajustar a páginas de Excel usando Aspose.Cells para .NET 
```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una instancia de un objeto Workbook
Workbook workbook = new Workbook();
// Acceso a la primera hoja de trabajo en el archivo de Excel
Worksheet worksheet = workbook.Worksheets[0];
// Establecer el número de páginas a las que se extenderá la longitud de la hoja de trabajo
worksheet.PageSetup.FitToPagesTall = 1;
//Establecer el número de páginas a las que se extenderá el ancho de la hoja de trabajo
worksheet.PageSetup.FitToPagesWide = 1;
// Guarde el libro de trabajo.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Conclusión
En este artículo, aprendimos cómo configurar el ajuste a las páginas en Excel usando Aspose.Cells para .NET. Pasamos por los siguientes pasos: crear el libro de trabajo, acceder a la hoja de trabajo, configurar el ajuste a las páginas y guardar el libro de trabajo. Ahora puede usar este conocimiento para ajustar sus hojas de cálculo a las páginas deseadas.

### preguntas frecuentes

P: ¿Cómo puedo instalar Aspose.Cells para .NET?

R: Para instalar Aspose.Cells para .NET, puede usar el administrador de paquetes NuGet en Visual Studio. Busque el paquete "Aspose.Cells" e instálelo en su proyecto.

P: ¿Puedo ajustar páginas tanto de alto como de ancho?

 R: Sí, puede ajustar tanto el alto como el ancho de la hoja de trabajo usando el`FitToPagesTall` y`FitToPagesWide` propiedades. Puede especificar el número deseado de páginas para cada dimensión.

P: ¿Cómo puedo personalizar las opciones de Ajustar a las páginas?

R: Además de especificar el número de páginas, también puede personalizar otras opciones de ajuste a las páginas, como la escala de la hoja de trabajo, la orientación del papel, los márgenes y más. Utilice las propiedades disponibles en el`PageSetup` objeto para esto.

P: ¿Puedo usar Aspose.Cells para .NET para procesar libros de trabajo existentes?

R: Sí, puede usar Aspose.Cells para .NET para abrir y editar libros de trabajo existentes. Puede acceder a hojas de trabajo, celdas, fórmulas, estilos y otros elementos del libro de trabajo para realizar varias operaciones.