---
title: Copiar hoja de trabajo de Excel
linktitle: Copiar hoja de trabajo de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Copie una hoja de cálculo de Excel a otra con Aspose.Cells para .NET.
type: docs
weight: 20
url: /es/net/excel-copy-worksheet/excel-copy-worksheet/
---

En esta guía, explicaremos cómo copiar una hoja de cálculo de Excel usando la biblioteca Aspose.Cells para .NET. Le proporcionaremos el código fuente de C# y le guiaremos por los pasos necesarios para completar esta tarea. Al final, te mostraremos el resultado esperado. Siga las instrucciones a continuación para comenzar.

## Paso 1: preparación

Antes de comenzar, asegúrese de haber instalado Aspose.Cells para .NET y creado un proyecto C# en su entorno de desarrollo integrado (IDE) preferido. También asegúrese de tener una copia del archivo de Excel que desea manipular.

## Paso 2: importar las bibliotecas necesarias

 En su archivo fuente de C#, importe las bibliotecas necesarias desde Aspose.Cells usando el`using` directiva:

```csharp
using Aspose.Cells;
```

## Paso 3: establece la ruta del archivo

 Declarar un`dataDir` variable e inicialícela con el directorio que contiene su archivo de Excel. Por ejemplo :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Asegúrate de reemplazar`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` con la ruta real a su directorio.

## Paso 4: cargue el archivo de Excel existente

 Utilizar el`Workbook` clase de Aspose.Cells para abrir el archivo de Excel existente. Utilizar el`InputPath` variable para especificar la ruta del archivo:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Asegúrate de haber reemplazado`"book1.xls"` con el nombre real de su archivo de Excel.

## Paso 5: copie la hoja de trabajo

 Ahora copiaremos la hoja de trabajo existente a una nueva hoja de trabajo. Utilizar el`Worksheets` propiedad de la`Workbook` objeto para acceder a la colección de hojas de trabajo:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Luego usa el`AddCopy` método para copiar la hoja de trabajo especificada. Por ejemplo, para copiar "Hoja1":

```csharp
sheets.AddCopy("Sheet1");
```

## Paso 6: guarde el archivo de Excel

 Utilizar el`Save` método de la`Workbook` objeto para guardar los cambios en un nuevo archivo:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Asegúrese de especificar la ruta y el nombre de archivo deseados para el archivo de salida.

### Código fuente de muestra para copiar hoja de trabajo de Excel usando Aspose.Cells para .NET 

```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Abra un archivo de Excel existente.
Workbook wb = new Workbook(InputPath);
// Cree un objeto Hojas de trabajo con referencia a
// las hojas del Cuaderno de Trabajo.
WorksheetCollection sheets = wb.Worksheets;
// Copiar datos a una nueva hoja desde una existente
// hoja dentro del Libro de Trabajo.
sheets.AddCopy("Sheet1");
// Guarde el archivo de Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Conclusión

¡Enhorabuena! Ahora ha aprendido cómo copiar una hoja de cálculo de Excel usando Aspose.Cells para .NET. Esta guía paso a paso mostró cómo importar las bibliotecas necesarias, cargar un archivo de Excel existente, copiar la hoja de trabajo y guardar el archivo modificado. No dude en utilizar este método en sus propios proyectos para manipular archivos de Excel de manera eficiente.

### Preguntas frecuentes

#### P. ¿Aspose.Cells es compatible con otros lenguajes de programación?

A. Sí, Aspose.Cells admite múltiples lenguajes de programación, incluidos C#, Java, Python y muchos más.

#### P. ¿Puedo copiar una hoja de cálculo a otro libro de Excel?

A.  Sí, puedes usar el`AddCopy` Método para copiar una hoja de cálculo a otro libro de Excel.

#### P. ¿Aspose.Cells conserva las fórmulas y el formato al copiar la hoja de trabajo?

A. Sí, Aspose.Cells conserva fórmulas, formato y otras propiedades al copiar una hoja de trabajo.

#### P. ¿Aspose.Cells requiere una licencia para uso comercial?

A. Sí, Aspose.Cells es un producto comercial y requiere la compra de una licencia para uso comercial. Puede encontrar más información sobre licencias en el sitio web oficial de Aspose.