---
title: Establecer encabezados y pies de página de Excel
linktitle: Establecer encabezados y pies de página de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a configurar encabezados y pies de página en Excel usando Aspose.Cells para .NET.
type: docs
weight: 100
url: /es/net/excel-page-setup/set-excel-headers-and-footers/
---

En este tutorial, le mostraremos paso a paso cómo configurar encabezados y pies de página en Excel usando Aspose.Cells para .NET. Usaremos el código fuente de C# para ilustrar el proceso.

## Paso 1: Configuración del entorno

Asegúrese de tener Aspose.Cells para .NET instalado en su máquina. También cree un nuevo proyecto en su entorno de desarrollo preferido.

## Paso 2: importa las bibliotecas necesarias

En su archivo de código, importe las bibliotecas necesarias para trabajar con Aspose.Cells. Aquí está el código correspondiente:

```csharp
using Aspose.Cells;
```

## Paso 3: establecer el directorio de datos

Establezca el directorio de datos donde desea guardar el archivo de Excel modificado. Usa el siguiente código:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Asegúrese de especificar la ruta completa del directorio.

## Paso 4: Crear el libro de trabajo y la hoja de trabajo

Cree un nuevo objeto Libro de trabajo y navegue a la primera hoja de trabajo en el libro de trabajo usando el siguiente código:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Esto creará un libro de trabajo vacío con una hoja de trabajo y brindará acceso al objeto PageSetup de esa hoja de trabajo.

## Paso 5: Configuración de encabezados

 Configure los encabezados de la hoja de cálculo usando el`SetHeader` métodos del objeto PageSetup. Aquí hay un código de muestra:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Esto establecerá el nombre de la hoja de trabajo, la fecha y hora actuales y el nombre del archivo en los encabezados, respectivamente.

## Paso 6: Definición de pies de página

 Configure los pies de página de la hoja de cálculo con el`SetFooter` métodos del objeto PageSetup. Aquí hay un código de muestra:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Esto establecerá respectivamente una cadena de texto, el número de página actual y el número total de páginas en los pies de página.

## Paso 7: guardar el libro de trabajo modificado

Guarde el libro de trabajo modificado usando el siguiente código:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Esto guardará el libro de trabajo modificado en el directorio de datos especificado.

### Ejemplo de código fuente para establecer encabezados y pies de página de Excel usando Aspose.Cells para .NET 
```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una instancia de un objeto Workbook
Workbook excel = new Workbook();
// Obtención de la referencia del PageSetup de la hoja de cálculo
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Establecer el nombre de la hoja de trabajo en la sección izquierda del encabezado
pageSetup.SetHeader(0, "&A");
//Configuración de la fecha actual y la hora actual en la sección central del encabezado
// y cambiando la fuente del encabezado
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Establecer el nombre del archivo actual en la sección derecha del encabezado y cambiar el
// fuente del encabezado
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Establecer una cadena en la sección izquierda del pie de página y cambiar la fuente
// de una parte de esta cadena ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Configuración del número de página actual en la sección central del pie de página
pageSetup.SetFooter(1, "&P");
// Configuración del recuento de páginas en la sección derecha del pie de página
pageSetup.SetFooter(2, "&N");
// Guarde el libro de trabajo.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Conclusión

Ahora ha aprendido cómo configurar encabezados y pies de página en Excel usando Aspose.Cells para .NET. Este tutorial lo guió a través de cada paso del proceso, desde configurar el entorno hasta guardar el libro de trabajo modificado. Siéntase libre de explorar más a fondo las características de Aspose.Cells para realizar más manipulaciones en sus archivos de Excel.

### Preguntas frecuentes (FAQ)

#### 1. ¿Cómo puedo instalar Aspose.Cells para .NET en mi sistema?
Para instalar Aspose.Cells para .NET, debe descargar el paquete de instalación del sitio web oficial de Aspose y seguir las instrucciones proporcionadas en la documentación.

#### 2. ¿Funciona este método con todas las versiones de Excel?
Sí, el método de configuración de encabezados y pies de página con Aspose.Cells para .NET funciona con todas las versiones compatibles de Excel.

#### 3. ¿Puedo personalizar aún más los encabezados y pies de página?
Sí, Aspose.Cells ofrece una amplia gama de funciones para personalizar encabezados y pies de página, incluida la ubicación del texto, el color, la fuente, los números de página y más.

#### 4. ¿Cómo puedo agregar información dinámica a los encabezados y pies de página?
Puede usar variables especiales y códigos de formato para agregar información dinámica, como la fecha actual, la hora, el nombre del archivo, el número de página, etc., a los encabezados y pies de página.

#### 5. ¿Puedo eliminar encabezados y pies de página después de configurarlos?
 Sí, puede eliminar encabezados y pies de página usando el`ClearHeaderFooter` metodo de la`PageSetup` objeto. Esto restaurará los encabezados y pies de página predeterminados.