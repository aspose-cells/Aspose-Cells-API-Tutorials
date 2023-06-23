---
title: Permitir apóstrofe inicial
linktitle: Permitir apóstrofe inicial
second_title: Referencia de API de Aspose.Cells para .NET
description: Permita el apóstrofe inicial en los libros de trabajo de Excel con Aspose.Cells para .NET.
type: docs
weight: 60
url: /es/net/excel-workbook/allow-leading-apostrophe/
---
En este tutorial paso a paso, explicaremos el código fuente de C# provisto que le permitirá permitir el uso de un apóstrofo inicial en un libro de Excel usando Aspose.Cells para .NET. Siga los pasos a continuación para realizar esta operación.

## Paso 1: Establecer directorios de origen y salida

```csharp
// directorio fuente
string sourceDir = RunExamples.Get_SourceDirectory();
// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

En este primer paso, definimos los directorios de origen y salida para los archivos de Excel.

## Paso 2: Crea una instancia de un objeto WorkbookDesigner

```csharp
// Crear una instancia de un objeto WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Creamos una instancia del`WorkbookDesigner` clase de Aspose.Cells.

## Paso 3: Cargue el libro de Excel

```csharp
//Cargar el libro de Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Cargamos el libro de trabajo de Excel desde el archivo especificado y deshabilitamos la conversión automática de los apóstrofes iniciales al estilo de texto.

## Paso 4: establecer la fuente de datos

```csharp
// Definir la fuente de datos para el libro de trabajo del diseñador
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Definimos una lista de objetos de datos y usamos el`SetDataSource` para establecer el origen de datos del libro de trabajo del diseñador.

## Paso 5: Procesar marcadores inteligentes

```csharp
// Procesar marcadores inteligentes
designer. Process();
```

 usamos el`Process` método para procesar marcadores inteligentes en el libro de trabajo del diseñador.

## Paso 6: guarde el libro de Excel modificado

```csharp
// Guarde el libro de Excel modificado
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Guardamos el libro de Excel modificado con los cambios realizados.

### Ejemplo de código fuente para Permitir apóstrofe inicial usando Aspose.Cells para .NET 
```csharp
//directorio de origen
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Crear una instancia de un objeto WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Abra una hoja de cálculo de diseñador que contenga marcadores inteligentes
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Establecer la fuente de datos para la hoja de cálculo del diseñador
designer.SetDataSource("sampleData", list);
// Procesar los marcadores inteligentes
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Conclusión

¡Felicidades! Aprendió a permitir el uso de un apóstrofo inicial en un libro de Excel usando Aspose.Cells para .NET. Experimente con sus propios datos para personalizar aún más sus libros de Excel.

### preguntas frecuentes

#### P: ¿Qué es el permiso de apóstrofe inicial en un libro de Excel?

R: Permitir el apóstrofo inicial en un libro de Excel permite que los datos que comienzan con un apóstrofe se muestren correctamente sin convertirlos a un estilo de texto. Esto es útil cuando desea mantener el apóstrofo como parte de los datos.

#### P: ¿Por qué necesito desactivar la conversión automática de apóstrofes iniciales?

R: Al deshabilitar la conversión automática de comillas principales, puede conservar su uso tal como está en sus datos. Esto evita cualquier modificación no deseada de los datos al abrir o manipular el libro de Excel.

#### P: ¿Cómo configurar la fuente de datos en el libro de trabajo del diseñador?

 R: Para establecer la fuente de datos en el libro de trabajo del diseñador, puede usar el`SetDataSource` método que especifica el nombre de la fuente de datos y una lista de los objetos de datos correspondientes.

#### P: ¿Permitir el apóstrofe inicial afecta a otros datos en el libro de Excel?

R: No, permitir el apóstrofo inicial solo afecta a los datos que comienzan con un apóstrofe. Otros datos en el libro de Excel permanecen sin cambios.

#### P: ¿Puedo usar esta función con otros formatos de archivo de Excel?

R: Sí, puede usar esta función con otros formatos de archivo de Excel compatibles con Aspose.Cells, como .xls, .xlsm, etc.