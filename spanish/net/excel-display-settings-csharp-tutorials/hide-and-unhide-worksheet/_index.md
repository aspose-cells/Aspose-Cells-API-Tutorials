---
title: Ocultar y mostrar hoja de trabajo
linktitle: Ocultar y mostrar hoja de trabajo
second_title: Referencia de API de Aspose.Cells para .NET
description: Una poderosa biblioteca para trabajar con archivos de Excel, incluida la creación, modificación y manipulación de datos.
type: docs
weight: 90
url: /es/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
En este tutorial, lo guiaremos paso a paso para explicar el siguiente código fuente de C# que se usa para ocultar y mostrar una hoja de trabajo usando Aspose.Cells para .NET. Siga los pasos a continuación:

## Paso 1: Preparando el ambiente

Antes de comenzar, asegúrese de tener Aspose.Cells para .NET instalado en su sistema. Si aún no lo tiene instalado, puede descargarlo del sitio web oficial de Aspose. Una vez instalado, puede crear un nuevo proyecto en su entorno de desarrollo integrado (IDE) preferido.

## Paso 2: importa los espacios de nombres requeridos

En su archivo fuente de C#, agregue los espacios de nombres necesarios para usar las características de Aspose.Cells. Agregue las siguientes líneas al principio de su archivo:

```csharp
using Aspose.Cells;
using System.IO;
```

## Paso 3: Cargue el archivo de Excel

Antes de ocultar o mostrar una hoja de trabajo, debe cargar el archivo de Excel en su aplicación. Asegúrese de tener el archivo de Excel que desea usar en el mismo directorio que su proyecto. Use el siguiente código para cargar el archivo de Excel:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Asegúrese de reemplazar "RUTA A SU DIRECTORIO DE DOCUMENTOS" con la ruta real al directorio que contiene su archivo de Excel.

## Paso 4: Accede a la hoja de cálculo

Una vez que se carga el archivo de Excel, puede navegar a la hoja de trabajo que desea ocultar o mostrar. Utilice el siguiente código para acceder a la primera hoja de cálculo del archivo:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Paso 5: ocultar la hoja de trabajo

 Ahora que ha accedido a la hoja de trabajo, puede ocultarla usando el`IsVisible` propiedad. Use el siguiente código para ocultar la primera hoja de trabajo en el archivo:

```csharp
worksheet. IsVisible = false;
```

## Paso 6: Vuelva a mostrar la hoja de trabajo

 Si desea volver a mostrar la hoja de trabajo previamente oculta, puede usar el mismo código cambiando el valor de la`IsVisible` propiedad. Utilice el siguiente código para volver a mostrar la primera hoja de cálculo:

```csharp
worksheet. IsVisible = true;
```

## Paso 7: Guardar cambios

Una vez tú

  ha ocultado o mostrado la hoja de trabajo según sea necesario, debe guardar los cambios en el archivo de Excel. Use el siguiente código para guardar los cambios:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Asegúrese de especificar la ruta de salida correcta para guardar el archivo de Excel modificado.

### Ejemplo de código fuente para Ocultar y mostrar la hoja de trabajo usando Aspose.Cells para .NET 

```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una secuencia de archivos que contenga el archivo de Excel que se abrirá
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Creación de instancias de un objeto de libro de trabajo con la apertura del archivo de Excel a través de la secuencia de archivos
Workbook workbook = new Workbook(fstream);
// Acceso a la primera hoja de trabajo en el archivo de Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ocultar la primera hoja de trabajo del archivo de Excel
worksheet.IsVisible = false;
// Muestra la primera hoja de cálculo del archivo de Excel
//Hoja de trabajo.IsVisible = verdadero;
// Guardar el archivo de Excel modificado en formato predeterminado (es decir, Excel 2003)
workbook.Save(dataDir + "output.out.xls");
// Cerrar el flujo de archivos para liberar todos los recursos
fstream.Close();
```

## Conclusión

¡Felicidades! Ha aprendido a ocultar y mostrar una hoja de cálculo con Aspose.Cells para .NET. Ahora puede usar esta función para controlar la visibilidad de sus hojas de cálculo en sus archivos de Excel.

### Preguntas frecuentes (FAQ)

#### ¿Cómo puedo instalar Aspose.Cells para .NET?

 Puede instalar Aspose.Cells para .NET descargando el paquete NuGet correspondiente de[Lanzamientos de Aspose](https://releases/aspose.com/cells/net/) y agregarlo a su proyecto de Visual Studio.

#### ¿Cuál es la versión mínima requerida de .NET Framework para usar Aspose.Cells para .NET?

Aspose.Cells para .NET admite .NET Framework 2.0 y versiones posteriores.

#### ¿Puedo abrir y editar archivos de Excel existentes con Aspose.Cells para .NET?

Sí, puede abrir y editar archivos de Excel existentes con Aspose.Cells para .NET. Puede acceder a hojas de trabajo, celdas, fórmulas y otros elementos del archivo de Excel.

#### ¿Aspose.Cells para .NET admite la generación de informes y la exportación a otros formatos de archivo?

Sí, Aspose.Cells para .NET admite la generación y exportación de informes a formatos como PDF, HTML, CSV, TXT, etc.

#### ¿La modificación del archivo de Excel es permanente?

Sí, la edición del archivo de Excel es permanente una vez que lo guarda. Asegúrese de guardar una copia de seguridad antes de realizar cambios en el archivo original.