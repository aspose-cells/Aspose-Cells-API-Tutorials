---
title: Establecer encabezados y pies de página de Excel
linktitle: Establecer encabezados y pies de página de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a configurar encabezados y pies de página en Excel usando Aspose.Cells para .NET.
type: docs
weight: 100
url: /es/net/excel-page-setup/set-excel-headers-and-footers/
---

En este tutorial, le mostraremos paso a paso cómo configurar encabezados y pies de página en Excel usando Aspose.Cells para .NET. Usaremos el código fuente C# para ilustrar el proceso.

## Paso 1: configurar el entorno

Asegúrese de tener Aspose.Cells para .NET instalado en su máquina. También cree un nuevo proyecto en su entorno de desarrollo preferido.

## Paso 2: importar las bibliotecas necesarias

En su archivo de código, importe las bibliotecas necesarias para trabajar con Aspose.Cells. Aquí está el código correspondiente:

```csharp
using Aspose.Cells;
```

## Paso 3: configurar el directorio de datos

Configure el directorio de datos donde desea guardar el archivo de Excel modificado. Utilice el siguiente código:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Asegúrese de especificar la ruta completa del directorio.

## Paso 4: crear el libro y la hoja de trabajo

Cree un nuevo objeto Libro de trabajo y navegue hasta la primera hoja de trabajo del libro usando el siguiente código:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Esto creará un libro vacío con una hoja de trabajo y proporcionará acceso al objeto PageSetup de esa hoja de trabajo.

## Paso 5: configurar encabezados

 Configure los encabezados de la hoja de cálculo usando el`SetHeader` métodos del objeto PageSetup. Aquí hay un código de muestra:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Esto establecerá el nombre de la hoja de trabajo, la fecha y hora actuales y el nombre del archivo en los encabezados respectivamente.

## Paso 6: Definir pies de página

 Establezca pies de página de hojas de cálculo usando el`SetFooter` métodos del objeto PageSetup. Aquí hay un código de muestra:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Esto establecerá respectivamente una cadena de texto, el número de página actual y el número total de páginas en los pies de página.

## Paso 7: guardar el libro de trabajo modificado

Guarde el libro modificado usando el siguiente código:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Esto guardará el libro modificado en el directorio de datos especificado.

### Código fuente de muestra para establecer encabezados y pies de página de Excel usando Aspose.Cells para .NET 
```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear instancias de un objeto de libro de trabajo
Workbook excel = new Workbook();
// Obteniendo la referencia del PageSetup de la hoja de trabajo
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Configurar el nombre de la hoja de trabajo en la sección izquierda del encabezado
pageSetup.SetHeader(0, "&A");
//Configuración de la fecha y hora actuales en la sección central del encabezado
// y cambiando la fuente del encabezado
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Configurar el nombre del archivo actual en la sección derecha del encabezado y cambiar el
// fuente del encabezado
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Establecer una cadena en la sección izquierda del pie de página y cambiar la fuente
// de una parte de esta cadena ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Configurar el número de página actual en la sección central del pie de página
pageSetup.SetFooter(1, "&P");
// Configurar el recuento de páginas en la sección derecha del pie de página
pageSetup.SetFooter(2, "&N");
// Guarde el libro de trabajo.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Conclusión

Ahora ha aprendido cómo configurar encabezados y pies de página en Excel usando Aspose.Cells para .NET. Este tutorial lo guió a través de cada paso del proceso, desde configurar el entorno hasta guardar el libro modificado. No dude en explorar más a fondo las funciones de Aspose.Cells para realizar más manipulaciones en sus archivos de Excel.

### Preguntas frecuentes (FAQ)

#### 1. ¿Cómo puedo instalar Aspose.Cells para .NET en mi sistema?
Para instalar Aspose.Cells para .NET, debe descargar el paquete de instalación del sitio web oficial de Aspose y seguir las instrucciones proporcionadas en la documentación.

#### 2. ¿Este método funciona con todas las versiones de Excel?
Sí, el método para configurar encabezados y pies de página con Aspose.Cells para .NET funciona con todas las versiones compatibles de Excel.

#### 3. ¿Puedo personalizar aún más los encabezados y pies de página?
Sí, Aspose.Cells ofrece una amplia gama de funciones para personalizar encabezados y pies de página, incluida la ubicación del texto, el color, la fuente, los números de página y más.

#### 4. ¿Cómo puedo agregar información dinámica a los encabezados y pies de página?
Puede utilizar variables especiales y códigos de formato para agregar información dinámica, como fecha, hora actual, nombre de archivo, número de página, etc., a los encabezados y pies de página.

#### 5. ¿Puedo eliminar encabezados y pies de página después de configurarlos?
 Sí, puedes eliminar encabezados y pies de página usando el`ClearHeaderFooter` método de la`PageSetup` objeto. Esto restaurará los encabezados y pies de página predeterminados.