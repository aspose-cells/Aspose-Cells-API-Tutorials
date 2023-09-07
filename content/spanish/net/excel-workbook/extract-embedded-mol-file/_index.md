---
title: Extraer archivo Mol incrustado
linktitle: Extraer archivo Mol incrustado
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a extraer fácilmente archivos MOL incrustados de un libro de Excel con Aspose.Cells para .NET.
type: docs
weight: 90
url: /es/net/excel-workbook/extract-embedded-mol-file/
---
En este tutorial, lo guiaremos paso a paso sobre cómo extraer un archivo MOL incrustado de un libro de Excel usando la biblioteca Aspose.Cells para .NET. Aprenderá a navegar por las hojas del libro de trabajo, extraer los objetos OLE correspondientes y guardar los archivos MOL extraídos. Siga los pasos a continuación para completar esta tarea con éxito.

## Paso 1: definir los directorios de origen y salida
Primero, necesitamos definir los directorios fuente y de salida en nuestro código. Estos directorios indican dónde se encuentra el libro de Excel de origen y dónde se guardarán los archivos MOL extraídos. Aquí está el código correspondiente:

```csharp
// directorios
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Asegúrese de especificar las rutas adecuadas según sea necesario.

## Paso 2: Cargar el libro de Excel
El siguiente paso es cargar el libro de trabajo de Excel que contiene los objetos OLE y los archivos MOL incrustados. Aquí está el código para cargar el libro de trabajo:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Asegúrese de especificar correctamente el nombre del archivo de origen en el código.

## Paso 3: recorrer las hojas y extraer los archivos MOL
Ahora recorreremos cada hoja del libro de trabajo y extraeremos los objetos OLE correspondientes, que contienen los archivos MOL. Aquí está el código correspondiente:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Este código recorre cada hoja del libro de trabajo, obtiene los objetos OLE y guarda los archivos MOL extraídos en el directorio de salida.

### Ejemplo de código fuente para Extraer archivo Mol incrustado usando Aspose.Cells para .NET 
```csharp
//directorios
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Conclusión
¡Felicidades! Ha aprendido a extraer un archivo MOL incrustado de un libro de Excel utilizando Aspose.Cells para .NET. Ahora puede aplicar este conocimiento para extraer archivos MOL de sus propios libros de Excel. Siéntase libre de explorar más la biblioteca de Aspose.Cells y aprender sobre sus otras características poderosas.

### preguntas frecuentes

#### P: ¿Qué es un archivo MOL?
 
R: Un archivo MOL es un formato de archivo que se utiliza para representar estructuras químicas en química computacional. Contiene información sobre átomos, enlaces y otras propiedades moleculares.

#### P: ¿Este método funciona con todos los tipos de archivos de Excel?

R: Sí, este método funciona con todos los tipos de archivos de Excel compatibles con Aspose.Cells.

#### P: ¿Puedo extraer varios archivos MOL a la vez?

R: Sí, puede extraer varios archivos MOL a la vez iterando a través de objetos OLE en cada hoja del libro de trabajo.