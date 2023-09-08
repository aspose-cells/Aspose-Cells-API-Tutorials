---
title: Actualizar elemento de fórmula de Power Query
linktitle: Actualizar elemento de fórmula de Power Query
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a actualizar elementos de fórmula de Power Query en archivos de Excel usando Aspose.Cells para .NET.
type: docs
weight: 160
url: /es/net/excel-workbook/update-power-query-formula-item/
---
Actualizar un elemento de fórmula de Power Query es una operación común cuando se trabaja con datos en archivos de Excel. Con Aspose.Cells para .NET, puede actualizar fácilmente un elemento de fórmula de Power Query siguiendo estos pasos:

## Paso 1: especificar los directorios de origen y de salida

Primero, debe especificar el directorio de origen donde se encuentra el archivo de Excel que contiene las fórmulas de Power Query para actualizar, así como el directorio de salida donde desea guardar el archivo modificado. Aquí se explica cómo hacerlo usando Aspose.Cells:

```csharp
// directorio fuente
string SourceDir = RunExamples.Get_SourceDirectory();

// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

## Paso 2: cargue el libro de Excel de origen

A continuación, debe cargar el libro de Excel de origen en el que desea actualizar el elemento de fórmula de Power Query. He aquí cómo hacerlo:

```csharp
// Cargue el libro de Excel de origen
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Paso 3: Examinar y actualizar los elementos de la fórmula de Power Query

Después de cargar el libro, puede navegar a la colección de fórmulas de Power Query y explorar cada fórmula y sus elementos. En este ejemplo, buscamos el elemento de fórmula con el nombre "Fuente" y actualizamos su valor. A continuación se muestra un código de ejemplo para actualizar un elemento de fórmula de Power Query:

```csharp
// Acceder a la colección de fórmulas de Power Query
DataMashup mashupData = workbook.DataMashup;

// Recorrer las fórmulas de Power Query y sus elementos
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Paso 4: guarde el libro de Excel de salida

Una vez que haya actualizado el elemento de fórmula de Power Query, puede guardar el libro de Excel modificado en el directorio de salida especificado. He aquí cómo hacerlo:

```csharp
// Guarde el libro de Excel de salida
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Código fuente de muestra para actualizar el elemento de fórmula de Power Query usando Aspose.Cells para .NET 
```csharp
// Directorios de trabajo
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Guarde el libro de trabajo de salida.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Conclusión

La actualización de los elementos de la fórmula de Power Query es una operación esencial cuando se utiliza Aspose.Cells para manipular y procesar datos en archivos de Excel. Siguiendo los pasos indicados anteriormente, puede actualizar fácilmente los elementos de la fórmula

### Preguntas frecuentes

#### P: ¿Qué es Power Query en Excel?
     
R: Power Query es una característica de Excel que ayuda a recopilar, transformar y cargar datos de diferentes fuentes. Ofrece herramientas poderosas para limpiar, combinar y remodelar datos antes de importarlos a Excel.

#### P: ¿Cómo sé si un elemento de fórmula de Power Query se actualizó correctamente?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### P: ¿Puedo actualizar varios elementos de fórmula de Power Query a la vez?
    
R: Sí, puede recorrer la colección de elementos de la fórmula de Power Query y actualizar varios elementos en un solo bucle, según sus necesidades específicas.

#### P: ¿Hay otras operaciones que pueda realizar en fórmulas de Power Query con Aspose.Cells?
    
R: Sí, Aspose.Cells ofrece una gama completa de funciones para trabajar con fórmulas de Power Query, incluida la creación, eliminación, copia y búsqueda de fórmulas en un libro de Excel.