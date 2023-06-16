---
title: Mostrar y ocultar barras de desplazamiento de la hoja de trabajo
linktitle: Mostrar y ocultar barras de desplazamiento de la hoja de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Muestre u oculte las barras de desplazamiento en la hoja de cálculo de Excel usando Aspose.Cells para .NET.
type: docs
weight: 50
url: /es/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
En este tutorial, le mostraremos cómo mostrar u ocultar las barras de desplazamiento verticales y horizontales en una hoja de cálculo de Excel utilizando el código fuente de C# con Aspose.Cells para .NET. Siga los pasos a continuación para obtener el resultado deseado.

## Paso 1: importa las bibliotecas necesarias

Asegúrese de haber instalado la biblioteca Aspose.Cells para .NET e importe las bibliotecas necesarias en su proyecto C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Paso 2: establezca la ruta del directorio y abra el archivo de Excel

 Establezca la ruta al directorio que contiene su archivo de Excel, luego abra el archivo creando una secuencia de archivos e instanciando un`Workbook` objeto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Paso 3: ocultar las barras de desplazamiento

 Utilizar el`IsVScrollBarVisible` y`IsHScrollBarVisible` propiedades de la`Workbook.Settings` objeto para ocultar las barras de desplazamiento vertical y horizontal de la hoja de trabajo.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Paso 4: Guardar cambios

 Una vez que haya realizado los cambios necesarios, guarde el archivo de Excel modificado utilizando el`Save` metodo de la`Workbook` objeto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Ejemplo de código fuente para Mostrar y ocultar barras de desplazamiento de la hoja de trabajo usando Aspose.Cells para .NET 

```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una secuencia de archivos que contenga el archivo de Excel que se abrirá
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Crear una instancia de un objeto Workbook
// Abrir el archivo de Excel a través de la secuencia de archivos
Workbook workbook = new Workbook(fstream);
// Ocultar la barra de desplazamiento vertical del archivo de Excel
workbook.Settings.IsVScrollBarVisible = false;
// Ocultar la barra de desplazamiento horizontal del archivo de Excel
workbook.Settings.IsHScrollBarVisible = false;
// Guardar el archivo de Excel modificado
workbook.Save(dataDir + "output.xls");
// Cerrar el flujo de archivos para liberar todos los recursos
fstream.Close();
```

### Conclusión

Esta guía paso a paso le mostró cómo mostrar u ocultar barras de desplazamiento verticales y horizontales en una hoja de cálculo de Excel usando Aspose.Cells para .NET. Con el código fuente de C# provisto, puede personalizar fácilmente la visualización de las barras de desplazamiento en sus archivos de Excel.

### Preguntas frecuentes (FAQ)

#### ¿Qué es Aspose.Cells para .NET?

Aspose.Cells for .NET es una poderosa biblioteca para manipular archivos de Excel en aplicaciones .NET.

#### ¿Cómo puedo instalar Aspose.Cells para .NET?

 Para instalar Aspose.Cells para .NET, debe descargar el paquete correspondiente de[Lanzamientos de Aspose](https://releases/aspose.com/cells/net/) y agréguelo a su proyecto .NET.

#### ¿Cómo puedo mostrar u ocultar las barras de desplazamiento en una hoja de cálculo de Excel con Aspose.Cells para .NET?

 Puedes usar el`IsVScrollBarVisible` y`IsHScrollBarVisible` propiedades de la`Workbook.Settings`objeto para mostrar u ocultar la barra de desplazamiento vertical y horizontal respectivamente en una hoja de cálculo de Excel.

#### ¿Qué otros formatos de archivo de Excel son compatibles con Aspose.Cells para .NET?

Aspose.Cells para .NET admite una variedad de formatos de archivo de Excel, como XLS, XLSX, CSV, HTML, PDF, etc.