---
title: Congelar paneles de hoja de trabajo
linktitle: Congelar paneles de hoja de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Manipule fácilmente los paneles congelados de la hoja de cálculo de Excel con Aspose.Cells para .NET.
type: docs
weight: 70
url: /es/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
En este tutorial, le mostraremos cómo bloquear paneles en una hoja de cálculo de Excel usando el código fuente de C# con Aspose.Cells para .NET. Siga los pasos a continuación para obtener el resultado deseado.

## Paso 1: Importe las bibliotecas necesarias

Asegúrese de haber instalado la biblioteca Aspose.Cells para .NET e importe las bibliotecas necesarias a su proyecto C#.

```csharp
using Aspose.Cells;
```

## Paso 2: establezca la ruta del directorio y abra el archivo de Excel

 Establezca la ruta al directorio que contiene su archivo de Excel, luego abra el archivo creando una instancia de`Workbook` objeto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Paso 3: vaya a la hoja de cálculo y aplique la configuración de bloqueo del panel

 Navegue a la primera hoja de trabajo en el archivo de Excel usando el`Worksheet` objeto. Luego usa el`FreezePanes` método para aplicar la configuración de bloqueo del panel.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

En el ejemplo anterior, los paneles están bloqueados en la celda de la fila 3 y la columna 2.

## Paso 4: guardar cambios

 Una vez que haya realizado los cambios necesarios, guarde el archivo de Excel modificado usando el`Save` método de la`Workbook` objeto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Código fuente de muestra para congelar paneles de hoja de trabajo usando Aspose.Cells para .NET 

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
// Aplicar la configuración de paneles congelados
worksheet.FreezePanes(3, 2, 3, 2);
// Guardar el archivo Excel modificado
workbook.Save(dataDir + "output.xls");
// Cerrar el flujo de archivos para liberar todos los recursos
fstream.Close();
```

## Conclusión

Esta guía paso a paso le mostró cómo bloquear paneles en una hoja de cálculo de Excel usando Aspose.Cells para .NET. Con el código fuente de C# proporcionado, puede personalizar fácilmente la configuración de bloqueo del panel para organizar y visualizar mejor sus datos en archivos de Excel.

### Preguntas frecuentes (FAQ)

#### ¿Qué es Aspose.Cells para .NET?

Aspose.Cells para .NET es una poderosa biblioteca para manipular archivos de Excel en aplicaciones .NET.

#### ¿Cómo puedo instalar Aspose.Cells para .NET?

 Para instalar Aspose.Cells para .NET, debe descargar el paquete correspondiente desde[Lanzamientos de Aspose](https://releases/aspose.com/cells/net/) y agréguelo a su proyecto .NET.

#### ¿Cómo bloquear paneles en una hoja de cálculo de Excel usando Aspose.Cells para .NET?

 Puedes usar el`FreezePanes` método de la`Worksheet` Objeto para bloquear los paneles de una hoja de trabajo. Especifique las celdas que desea bloquear proporcionando índices de filas y columnas.

#### ¿Puedo personalizar la configuración de bloqueo del panel con Aspose.Cells para .NET?

 Sí, usando el`FreezePanes` método, puede especificar qué celdas bloquear según sea necesario, proporcionando los índices de fila y columna adecuados.
