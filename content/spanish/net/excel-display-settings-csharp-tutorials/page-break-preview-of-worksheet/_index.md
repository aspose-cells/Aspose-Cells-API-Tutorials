---
title: Vista previa de salto de página de la hoja de trabajo
linktitle: Vista previa de salto de página de la hoja de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Guía paso a paso para mostrar una vista previa de salto de página de la hoja de trabajo usando Aspose.Cells para .NET.
type: docs
weight: 110
url: /es/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
En este tutorial, explicaremos cómo mostrar la vista previa del salto de página de una hoja de trabajo usando Aspose.Cells para .NET. Siga estos pasos para obtener el resultado deseado:

## Paso 1: configurar el entorno

Asegúrese de haber instalado Aspose.Cells para .NET y configurar su entorno de desarrollo. Además, asegúrese de tener una copia del archivo de Excel en el que desea mostrar la vista previa del salto de página.

## Paso 2: Importe las dependencias necesarias

Agregue las directivas necesarias para usar las clases de Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Paso 3: inicialización del código

Comience inicializando la ruta al directorio que contiene sus documentos de Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Paso 4: abrir el archivo Excel

 Crear un`FileStream` objeto que contiene el archivo Excel a abrir:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Crear una instancia de`Workbook` objeto y abra el archivo de Excel usando la secuencia de archivos:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Paso 5: acceder a la hoja de cálculo

Navegue a la primera hoja de trabajo del archivo de Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Paso 6: Mostrar la vista previa paginada

Habilite la vista previa página por página para la hoja de cálculo:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Paso 7: Guardar cambios

Guarde los cambios realizados en el archivo de Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Paso 8: cerrar la secuencia de archivos

Cierre la secuencia de archivos para liberar todos los recursos:

```csharp
fstream.Close();
```

### Código fuente de muestra para la vista previa de salto de página de la hoja de trabajo usando Aspose.Cells para .NET 
```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una secuencia de archivos que contenga el archivo de Excel que se abrirá
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Crear instancias de un objeto de libro de trabajo
// Abrir el archivo de Excel a través de la secuencia de archivos
Workbook workbook = new Workbook(fstream);
// Accediendo a la primera hoja de trabajo en el archivo de Excel
Worksheet worksheet = workbook.Worksheets[0];
// Mostrar la hoja de trabajo en la vista previa de salto de página
worksheet.IsPageBreakPreview = true;
// Guardar el archivo Excel modificado
workbook.Save(dataDir + "output.xls");
// Cerrar el flujo de archivos para liberar todos los recursos
fstream.Close();
```

## Conclusión

En este tutorial, aprendió cómo mostrar la vista previa del salto de página de una hoja de trabajo usando Aspose.Cells para .NET. Siguiendo los pasos descritos, podrá controlar fácilmente la apariencia y el diseño de sus archivos de Excel.

### Preguntas frecuentes (FAQ)

#### ¿Qué es Aspose.Cells para .NET?

Aspose.Cells para .NET es una biblioteca de software popular para manipular archivos de Excel en aplicaciones .NET.

#### ¿Puedo mostrar la vista previa página por página de una hoja de trabajo específica en lugar de toda la hoja de trabajo?

Sí, usando Aspose.Cells puede habilitar la vista previa de salto de página para una hoja de trabajo específica accediendo al objeto Hoja de trabajo correspondiente.

#### ¿Aspose.Cells admite otras funciones de edición de archivos de Excel?

Sí, Aspose.Cells ofrece una amplia gama de funciones para editar y manipular archivos de Excel, como agregar datos, formatear, crear gráficos, etc.

#### ¿Aspose.Cells solo funciona con archivos de Excel en formato .xls?

No, Aspose.Cells admite varios formatos de archivos de Excel, incluidos .xls y .xlsx.
	