---
title: Establecer el número de primera página de Excel
linktitle: Establecer el número de primera página de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a configurar el número de la primera página en Excel usando Aspose.Cells para .NET.
type: docs
weight: 90
url: /es/net/excel-page-setup/set-excel-first-page-number/
---
En este tutorial, le explicaremos cómo configurar el número de la primera página en Excel usando Aspose.Cells para .NET. Usaremos el código fuente C# para ilustrar el proceso.

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
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Esto creará un libro vacío con una hoja de trabajo.

## Paso 5: Establecer el número de la primera página

Establezca el número de la primera página de las páginas de la hoja de trabajo usando el siguiente código:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Esto establecerá el número de la primera página en 2.

## Paso 6: guardar el libro de trabajo modificado

Guarde el libro modificado usando el siguiente código:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Esto guardará el libro modificado en el directorio de datos especificado.

### Código fuente de muestra para establecer el número de primera página de Excel usando Aspose.Cells para .NET 
```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear instancias de un objeto de libro de trabajo
Workbook workbook = new Workbook();
// Accediendo a la primera hoja de trabajo en el archivo de Excel
Worksheet worksheet = workbook.Worksheets[0];
// Configurar el número de la primera página de las páginas de la hoja de trabajo
worksheet.PageSetup.FirstPageNumber = 2;
// Guarde el libro de trabajo.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Conclusión

Ahora ha aprendido cómo configurar el número de la primera página en Excel usando Aspose.Cells para .NET. Este tutorial lo guió a través de cada paso del proceso, desde la configuración del entorno hasta la configuración del número de la primera página. Ahora puede utilizar este conocimiento para personalizar la numeración de páginas en sus archivos de Excel.

### Preguntas frecuentes

#### P1: ¿Puedo establecer un número de primera página diferente para cada hoja de trabajo?

 R1: Sí, puede establecer un número de primera página diferente para cada hoja de trabajo accediendo a`FirstPageNumber`propiedad de la hoja de trabajo respectiva`PageSetup` objeto.

#### P2: ¿Cómo puedo verificar el número de la primera página de una hoja de cálculo existente?

 R2: Puede verificar el número de la primera página de una hoja de trabajo existente accediendo a`FirstPageNumber` propiedad de la`PageSetup` objeto correspondiente a esa hoja de trabajo.

#### P3: ¿La numeración de páginas siempre comienza desde 1 de forma predeterminada?

R3: Sí, la numeración de páginas comienza desde 1 de forma predeterminada en Excel. Sin embargo, puede utilizar el código que se muestra en este tutorial para establecer un número de primera página diferente.

#### P4: ¿Los cambios en el número de la primera página son permanentes en el archivo de Excel editado?

R4: Sí, los cambios realizados en el número de la primera página se guardan permanentemente en el archivo de Excel modificado.

#### P5: ¿Este método funciona para todos los formatos de archivos de Excel, como .xls y .xlsx?

R5: Sí, este método funciona para todos los formatos de archivos de Excel compatibles con Aspose.Cells, incluidos .xls y .xlsx.