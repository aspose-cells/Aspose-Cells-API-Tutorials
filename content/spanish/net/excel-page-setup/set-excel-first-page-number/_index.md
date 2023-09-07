---
title: Establecer el número de la primera página de Excel
linktitle: Establecer el número de la primera página de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a configurar el número de la primera página en Excel usando Aspose.Cells para .NET.
type: docs
weight: 90
url: /es/net/excel-page-setup/set-excel-first-page-number/
---
En este tutorial, lo guiaremos a través de cómo configurar el número de la primera página en Excel usando Aspose.Cells para .NET. Usaremos el código fuente de C# para ilustrar el proceso.

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
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Esto creará un libro de trabajo vacío con una hoja de trabajo.

## Paso 5: Configurar el número de la primera página

Establezca el número de la primera página de las páginas de la hoja de trabajo usando el siguiente código:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Esto establecerá el número de la primera página en 2.

## Paso 6: guardar el libro de trabajo modificado

Guarde el libro de trabajo modificado usando el siguiente código:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Esto guardará el libro de trabajo modificado en el directorio de datos especificado.

### Ejemplo de código fuente para establecer el número de la primera página de Excel usando Aspose.Cells para .NET 
```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una instancia de un objeto Workbook
Workbook workbook = new Workbook();
// Acceso a la primera hoja de trabajo en el archivo de Excel
Worksheet worksheet = workbook.Worksheets[0];
// Establecer el número de la primera página de las páginas de la hoja de trabajo
worksheet.PageSetup.FirstPageNumber = 2;
// Guarde el libro de trabajo.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Conclusión

Ahora ha aprendido cómo establecer el número de la primera página en Excel usando Aspose.Cells para .NET. Este tutorial lo guió a través de cada paso del proceso, desde configurar el entorno hasta configurar el número de la primera página. Ahora puede usar este conocimiento para personalizar la numeración de páginas en sus archivos de Excel.

### Preguntas frecuentes

#### P1: ¿Puedo establecer un número de primera página diferente para cada hoja de trabajo?

 R1: Sí, puede establecer un número de primera página diferente para cada hoja de trabajo accediendo a la`FirstPageNumber`propiedad de la respectiva hoja de trabajo`PageSetup` objeto.

#### P2: ¿Cómo puedo verificar el número de la primera página de una hoja de cálculo existente?

 R2: Puede comprobar el número de la primera página de una hoja de cálculo existente accediendo a la`FirstPageNumber` propiedad de la`PageSetup` objeto correspondiente a esa hoja de cálculo.

#### P3: ¿La numeración de páginas siempre comienza desde 1 de forma predeterminada?

R3: Sí, la numeración de páginas comienza desde 1 de forma predeterminada en Excel. Sin embargo, puede usar el código que se muestra en este tutorial para establecer un número de primera página diferente.

#### P4: ¿Los cambios en el número de la primera página son permanentes en el archivo de Excel editado?

R4: Sí, los cambios realizados en el número de la primera página se guardan de forma permanente en el archivo de Excel modificado.

#### P5: ¿Funciona este método para todos los formatos de archivo de Excel, como .xls y .xlsx?

R5: Sí, este método funciona para todos los formatos de archivo de Excel compatibles con Aspose.Cells, incluidos .xls y .xlsx.