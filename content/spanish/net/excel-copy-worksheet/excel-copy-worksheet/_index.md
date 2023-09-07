---
title: Hoja de trabajo de copia de Excel
linktitle: Hoja de trabajo de copia de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Copie una hoja de cálculo de Excel a otra con Aspose.Cells para .NET.
type: docs
weight: 20
url: /es/net/excel-copy-worksheet/excel-copy-worksheet/
---

En esta guía, explicaremos cómo copiar una hoja de cálculo de Excel utilizando la biblioteca Aspose.Cells para .NET. Le proporcionaremos el código fuente de C# y lo guiaremos a través de los pasos necesarios para completar esta tarea. Al final, le mostraremos el resultado esperado. Siga las instrucciones a continuación para comenzar.

## Paso 1: Preparación

Antes de comenzar, asegúrese de haber instalado Aspose.Cells para .NET y creado un proyecto C# en su entorno de desarrollo integrado (IDE) preferido. También asegúrese de tener una copia del archivo de Excel que desea manipular.

## Paso 2: importa las bibliotecas requeridas

 En su archivo fuente de C#, importe las bibliotecas necesarias de Aspose.Cells usando el`using` directiva:

```csharp
using Aspose.Cells;
```

## Paso 3: establezca la ruta del archivo

 declarar un`dataDir` variable e inicialícelo con el directorio que contiene su archivo de Excel. Por ejemplo :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Asegúrese de reemplazar`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` con la ruta real a su directorio.

## Paso 4: Cargue el archivo de Excel existente

 Utilizar el`Workbook`class de Aspose.Cells para abrir el archivo de Excel existente. Utilizar el`InputPath` variable para especificar la ruta del archivo:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Asegúrese de haber reemplazado`"book1.xls"` con el nombre real de su archivo de Excel.

## Paso 5: Copie la hoja de trabajo

 Ahora copiaremos la hoja de trabajo existente a una nueva hoja de trabajo. Utilizar el`Worksheets` propiedad de la`Workbook` objeto para acceder a la colección de hojas de trabajo:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Luego usa el`AddCopy` para copiar la hoja de trabajo especificada. Por ejemplo, para copiar "Hoja1":

```csharp
sheets.AddCopy("Sheet1");
```

## Paso 6: Guarde el archivo de Excel

 Utilizar el`Save` metodo de la`Workbook` objeto para guardar los cambios en un nuevo archivo:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Asegúrese de especificar la ruta y el nombre de archivo deseados para el archivo de salida.

### Ejemplo de código fuente para la hoja de trabajo de copia de Excel usando Aspose.Cells para .NET 

```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Abra un archivo de Excel existente.
Workbook wb = new Workbook(InputPath);
// Cree un objeto Hojas de trabajo con referencia a
// las hojas del Cuaderno de Trabajo.
WorksheetCollection sheets = wb.Worksheets;
// Copiar datos a una nueva hoja desde una existente
// hoja dentro del Libro de trabajo.
sheets.AddCopy("Sheet1");
// Guarde el archivo de Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Conclusión

¡Felicidades! Ahora ha aprendido a copiar una hoja de cálculo de Excel utilizando Aspose.Cells para .NET. Esta guía paso a paso mostró cómo importar las bibliotecas necesarias, cargar un archivo de Excel existente, copiar la hoja de trabajo y guardar el archivo modificado. Siéntase libre de usar este método en sus propios proyectos para manipular eficientemente los archivos de Excel.

### preguntas frecuentes

#### P. ¿Es Aspose.Cells compatible con otros lenguajes de programación?

A. Sí, Aspose.Cells admite varios lenguajes de programación, incluidos C#, Java, Python y muchos más.

#### P. ¿Puedo copiar una hoja de cálculo a otro libro de Excel?

A.  Sí, puedes usar el`AddCopy` método para copiar una hoja de trabajo a otro libro de Excel.

#### P. ¿Aspose.Cells conserva las fórmulas y el formato al copiar la hoja de trabajo?

A. Sí, Aspose.Cells conserva fórmulas, formato y otras propiedades al copiar una hoja de cálculo.

#### P. ¿Aspose.Cells requiere una licencia para uso comercial?

A. Sí, Aspose.Cells es un producto comercial y requiere la compra de una licencia para uso comercial. Puede encontrar más información sobre licencias en el sitio web oficial de Aspose.