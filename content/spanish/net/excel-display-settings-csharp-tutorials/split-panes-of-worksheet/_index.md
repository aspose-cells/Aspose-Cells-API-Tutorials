---
title: Dividir paneles de hoja de trabajo
linktitle: Dividir paneles de hoja de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Guía paso a paso para dividir paneles en una hoja de cálculo de Excel usando Aspose.Cells para .NET.
type: docs
weight: 130
url: /es/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
En este tutorial, explicaremos cómo dividir paneles en una hoja de cálculo de Excel usando Aspose.Cells para .NET. Siga estos pasos para obtener el resultado deseado:

## Paso 1: configurar el entorno

Asegúrese de haber instalado Aspose.Cells para .NET y configurar su entorno de desarrollo. Además, asegúrese de tener una copia del archivo de Excel en el que desea dividir los paneles.

## Paso 2: Importe las dependencias necesarias

Agregue las directivas necesarias para usar las clases de Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Paso 3: inicialización del código

Comience inicializando la ruta al directorio que contiene sus documentos de Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Paso 4: abrir el archivo Excel

 Crear una instancia nueva`Workbook` objeto y abra el archivo Excel usando el`Open` método:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Paso 5: definir la celda activa

 Establezca la celda activa de la hoja de trabajo usando el`ActiveCell` propiedad:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Paso 6: División de las solapas

 Divida la ventana de la hoja de trabajo usando el`Split` método:

```csharp
book.Worksheets[0].Split();
```

## Paso 7: Guardar cambios

Guarde los cambios realizados en el archivo de Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Código fuente de muestra para paneles divididos de hoja de trabajo usando Aspose.Cells para .NET 

```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Cree una instancia de un nuevo libro de trabajo y abra un archivo de plantilla
Workbook book = new Workbook(dataDir + "Book1.xls");
// Establecer la celda activa
book.Worksheets[0].ActiveCell = "A20";
// Dividir la ventana de la hoja de trabajo
book.Worksheets[0].Split();
// Guarde el archivo de Excel
book.Save(dataDir + "output.xls");
```

## Conclusión

En este tutorial, aprendió cómo dividir paneles en una hoja de cálculo de Excel usando Aspose.Cells para .NET. Siguiendo los pasos descritos, podrá personalizar fácilmente la apariencia y el comportamiento de sus archivos de Excel.

### Preguntas frecuentes (FAQ)

#### ¿Qué es Aspose.Cells para .NET?

Aspose.Cells para .NET es una biblioteca de software popular para manipular archivos de Excel en aplicaciones .NET.

#### ¿Cómo puedo configurar la celda activa de una hoja de trabajo en Aspose.Cells?

 Puede configurar la celda activa usando el`ActiveCell`propiedad del objeto Hoja de trabajo.

#### ¿Puedo dividir sólo los paneles horizontales o verticales de la ventana de la hoja de trabajo?

 Sí, al usar Aspose.Cells solo puedes dividir paneles horizontales o verticales usando los métodos apropiados, como`SplitColumn` o`SplitRow`.

#### ¿Aspose.Cells solo funciona con archivos de Excel en formato .xls?

No, Aspose.Cells admite varios formatos de archivos de Excel, incluidos .xls y .xlsx.