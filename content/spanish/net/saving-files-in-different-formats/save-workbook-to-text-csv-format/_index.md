---
title: Guardar libro de trabajo en formato de texto CSV
linktitle: Guardar libro de trabajo en formato de texto CSV
second_title: API de procesamiento de Excel Aspose.Cells .NET
description: Aprenda a convertir sin esfuerzo libros de Excel al formato CSV con Aspose.Cells en este completo tutorial paso a paso diseñado para desarrolladores de .NET.
type: docs
weight: 17
url: /es/net/saving-files-in-different-formats/save-workbook-to-text-csv-format/
---
## Introducción
Al trabajar con datos, el formato que elija puede determinar realmente la facilidad con la que podrá trabajar con ellos. Entre los formatos más comunes para manejar datos tabulares se encuentra CSV (valores separados por comas). Si es un desarrollador que trabaja con archivos de Excel y necesita convertir libros de trabajo a formato CSV, Aspose.Cells para .NET es una biblioteca fantástica que simplifica esta tarea. En este tutorial, desglosaremos los pasos para convertir un libro de trabajo de Excel a un formato de texto CSV sin problemas.
## Prerrequisitos
Antes de comenzar, asegurémonos de que tienes todo listo para comenzar:
1. Conocimientos básicos de C# y .NET: dado que escribiremos código en C#, es esencial estar familiarizado con el lenguaje y el marco .NET.
2. Biblioteca Aspose.Cells: asegúrese de tener instalada la biblioteca Aspose.Cells para .NET en su entorno de desarrollo. Puede descargarla[aquí](https://releases.aspose.com/cells/net/).
3. Visual Studio o cualquier entorno de desarrollo integrado (IDE) de C#: necesitará un entorno de desarrollo integrado (IDE) para escribir y ejecutar su código. Visual Studio es una opción popular.
4. Libro de trabajo de Excel: prepare un libro de trabajo de Excel de muestra (por ejemplo, "book1.xls") que contenga algunos datos para probar la conversión.
## Importar paquetes
Ahora que hemos cubierto nuestros requisitos previos, el primer paso del proceso es importar los paquetes necesarios. En su proyecto de C#, debe incluir el siguiente espacio de nombres en la parte superior de su archivo de código:
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
Estos espacios de nombres le darán acceso a las clases y métodos necesarios para trabajar con archivos de Excel y administrar flujos de memoria.
## Paso 1: Definir la ruta al directorio de documentos
El primer paso de nuestro proceso es definir dónde se almacenan nuestros documentos (libros de Excel). Esto es fundamental, ya que permite que nuestro programa sepa dónde encontrar los archivos que necesita procesar. 
```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";
```
 Asegúrese de reemplazar`"Your Document Directory"` con la ruta real donde se encuentra el archivo "book1.xls". Puede ser un directorio de su computadora o una ruta a un servidor.
## Paso 2: Cargue su libro de trabajo de origen
A continuación, debemos cargar el libro de Excel que se convertirá al formato CSV.
```csharp
// Cargue su libro de trabajo de origen
Workbook workbook = new Workbook(dataDir + "book1.xls");
```
 El`Workbook` La clase de la biblioteca Aspose.Cells permite manipular y acceder a los libros de Excel. Al pasar la ruta del archivo, cargamos el libro especificado para su procesamiento.
## Paso 3: Inicializar una matriz de bytes para los datos del libro de trabajo
Antes de comenzar a convertir el libro de trabajo a CSV, necesitamos inicializar una matriz de bytes vacía que eventualmente contendrá todos los datos de la hoja de trabajo.
```csharp
// Matriz de 0 bytes
byte[] workbookData = new byte[0];
```
Esta matriz de bytes combinará los datos de cada hoja de trabajo en una única estructura que podremos escribir en un archivo más tarde.
## Paso 4: Configurar las opciones para guardar texto
Ahora, configuremos las opciones para guardar el formato de texto. Puedes elegir delimitadores personalizados o utilizar tabulaciones.
```csharp
// Opciones para guardar texto. Puedes utilizar cualquier tipo de separador.
TxtSaveOptions opts = new TxtSaveOptions();
opts.Separator = '\t'; // Establecer la pestaña como separador
```
 En este ejemplo, usamos un carácter de tabulación como separador. Puedes reemplazarlo`'\t'` con cualquier carácter que desees, como una coma (`,`), dependiendo de cómo quieras formatear tu CSV.
## Paso 5: Iterar a través de cada hoja de trabajo
 A continuación, iteraremos a través de todas las hojas de trabajo dentro del libro de trabajo, guardando cada una en nuestro`workbookData` matriz, pero primero debe seleccionar en qué hoja de trabajo trabajar.
```csharp
// Copiar cada dato de la hoja de trabajo en formato de texto dentro de la matriz de datos del libro de trabajo
for (int idx = 0; idx < workbook.Worksheets.Count; idx++)
{
    // Guardar la hoja de cálculo activa en formato de texto
    MemoryStream ms = new MemoryStream();
    workbook.Worksheets.ActiveSheetIndex = idx;
    workbook.Save(ms, opts);
```
 El bucle recorre cada hoja de trabajo del libro.`ActiveSheetIndex` está configurado de manera que cada vez que pasemos por el bucle, guardemos la hoja de cálculo actual. Los resultados se guardarán en la memoria mediante un`MemoryStream`.
## Paso 6: Recuperar datos de la hoja de cálculo
 Después de guardar una hoja de cálculo en el flujo de memoria, el siguiente paso es recuperar estos datos y agregarlos a nuestro`workbookData` formación.
```csharp
    // Guardar los datos de la hoja de cálculo en la matriz de datos de la hoja
    ms.Position = 0; // Restablecer la posición del flujo de memoria
    byte[] sheetData = ms.ToArray(); // Obtener la matriz de bytes
```
`ms.Position = 0;` restablece la posición para leer después de escribir. Luego, usamos`ToArray()` para convertir el flujo de memoria en una matriz de bytes que contiene los datos de la hoja de trabajo.
## Paso 7: Combinar datos de la hoja de cálculo
 Ahora, combinaremos los datos de cada hoja de trabajo en una sola.`workbookData` matriz inicializada anteriormente.
```csharp
    // Combine los datos de esta hoja de trabajo en la matriz de datos del libro de trabajo
    byte[] combinedArray = new byte[workbookData.Length + sheetData.Length];
    Array.Copy(workbookData, 0, combinedArray, 0, workbookData.Length);
    Array.Copy(sheetData, 0, combinedArray, workbookData.Length, sheetData.Length);
    workbookData = combinedArray;
}
```
Creamos una nueva matriz lo suficientemente grande como para contener los datos del libro de trabajo existente y los datos de la nueva hoja de trabajo. Luego copiamos los datos existentes y nuevos en esta matriz combinada para su uso posterior.
## Paso 8: Guardar todos los datos del libro de trabajo en un archivo
 Finalmente, con todos los datos combinados en nuestro`workbookData` matriz, podemos guardar esta matriz en una ruta de archivo especificada.
```csharp
//Guardar todos los datos del libro de trabajo en un archivo
File.WriteAllBytes(dataDir + "out.txt", workbookData);
```
`WriteAllBytes` toma la matriz de bytes combinada y la escribe en un archivo de texto llamado "out.txt" en el directorio especificado.
## Conclusión
¡Y ya está! Ha convertido con éxito un libro de Excel a formato CSV con Aspose.Cells para .NET. Este proceso no solo es eficiente, sino que también permite manipular fácilmente los datos de Excel para realizar análisis o informes posteriores. Ahora puede automatizar sus tareas de procesamiento de datos o incluso integrar esta funcionalidad en aplicaciones más grandes.
## Preguntas frecuentes
### ¿Puedo utilizar diferentes delimitadores para el archivo CSV?
 Sí, puedes cambiar el`opts.Separator` a cualquier carácter que desees, como comas o barras verticales.
### ¿Aspose.Cells es de uso gratuito?
 Aspose.Cells no es gratuito, pero puedes obtener una prueba gratuita[aquí](https://releases.aspose.com/).
### ¿En qué tipos de formatos puedo guardar además de CSV?
Aspose.Cells permite guardar en múltiples formatos, incluidos XLSX, PDF y más.
### ¿Puedo procesar archivos grandes de Excel usando Aspose.Cells?
Sí, Aspose.Cells está diseñado para manejar archivos grandes de manera eficiente, pero el rendimiento puede depender de los recursos del sistema.
### ¿Dónde puedo encontrar documentación más detallada?
Puede encontrar documentación completa y ejemplos en su[sitio de referencia](https://reference.aspose.com/cells/net/).