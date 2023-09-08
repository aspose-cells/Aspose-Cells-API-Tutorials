---
title: Extraer el archivo Mol incrustado
linktitle: Extraer el archivo Mol incrustado
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda cómo extraer fácilmente archivos MOL incrustados de un libro de Excel usando Aspose.Cells para .NET.
type: docs
weight: 90
url: /es/net/excel-workbook/extract-embedded-mol-file/
---
En este tutorial, le explicaremos paso a paso cómo extraer un archivo MOL incrustado de un libro de Excel utilizando la biblioteca Aspose.Cells para .NET. Aprenderá a explorar las hojas del libro, extraer los objetos OLE correspondientes y guardar los archivos MOL extraídos. Siga los pasos a continuación para completar esta tarea con éxito.

## Paso 1: definir los directorios de origen y de salida
Primero, necesitamos definir los directorios de origen y de salida en nuestro código. Estos directorios indican dónde se encuentra el libro de Excel de origen y dónde se guardarán los archivos MOL extraídos. Aquí está el código correspondiente:

```csharp
// Directorios
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Asegúrese de especificar las rutas adecuadas según sea necesario.

## Paso 2: cargar el libro de Excel
El siguiente paso es cargar el libro de Excel que contiene los objetos OLE y archivos MOL incrustados. Aquí está el código para cargar el libro de trabajo:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Asegúrese de especificar correctamente el nombre del archivo fuente en el código.

## Paso 3: recorre las hojas y extrae los archivos MOL
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

Este código recorre cada hoja del libro de trabajo, recupera los objetos OLE y guarda los archivos MOL extraídos en el directorio de salida.

### Código fuente de muestra para extraer archivo Mol incrustado usando Aspose.Cells para .NET 
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
¡Enhorabuena! Ha aprendido cómo extraer un archivo MOL incrustado de un libro de Excel usando Aspose.Cells para .NET. Ahora puede aplicar este conocimiento para extraer archivos MOL de sus propios libros de Excel. No dude en explorar más a fondo la biblioteca Aspose.Cells y conocer sus otras potentes funciones.

### Preguntas frecuentes

#### P: ¿Qué es un archivo MOL?
 
R: Un archivo MOL es un formato de archivo que se utiliza para representar estructuras químicas en química computacional. Contiene información sobre átomos, enlaces y otras propiedades moleculares.

#### P: ¿Este método funciona con todos los tipos de archivos de Excel?

R: Sí, este método funciona con todos los tipos de archivos de Excel compatibles con Aspose.Cells.

#### P: ¿Puedo extraer varios archivos MOL a la vez?

R: Sí, puede extraer varios archivos MOL a la vez iterando a través de objetos OLE en cada hoja del libro.