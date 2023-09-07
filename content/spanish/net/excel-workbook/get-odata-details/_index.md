---
title: Obtener detalles de Odata
linktitle: Obtener detalles de Odata
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a recuperar detalles de OData de un libro de Excel con Aspose.Cells para .NET.
type: docs
weight: 110
url: /es/net/excel-workbook/get-odata-details/
---
El uso de OData es común cuando se trata de recuperar datos estructurados de fuentes de datos externas. Con Aspose.Cells para .NET, puede recuperar fácilmente los detalles de OData de un libro de Excel. Siga los pasos a continuación para obtener los resultados deseados:

## Paso 1: especificar el directorio de origen

Primero, debe especificar el directorio de origen donde se encuentra el archivo de Excel que contiene los detalles de OData. He aquí cómo hacerlo usando Aspose.Cells:

```csharp
// directorio fuente
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Paso 2: Cargue el libro de trabajo

Una vez que se especifica el directorio de origen, puede cargar el libro de Excel desde el archivo. Aquí hay un código de muestra:

```csharp
// Cargar el libro de trabajo
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## Paso 3: obtenga los detalles de OData

Después de cargar el libro de trabajo, puede acceder a los detalles de OData mediante la colección PowerQueryFormulas. Así es cómo:

```csharp
// Recuperar la colección de fórmulas de Power Query
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Recorra cada fórmula de Power Query
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Recuperar la colección de elementos de fórmula de Power Query
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Iterar a través de cada elemento de fórmula de Power Query
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Ejemplo de código fuente para Obtener detalles de Odata usando Aspose.Cells para .NET 
```csharp
// directorio fuente
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## Conclusión

Recuperar detalles de OData de un libro de Excel ahora es fácil con Aspose.Cells para .NET. Si sigue los pasos descritos en esta guía, podrá acceder a los datos de OData y procesarlos de manera eficiente. Experimente con sus propios archivos de Excel que contengan detalles de OData y aproveche al máximo esta potente característica.

### preguntas frecuentes

#### P: ¿Aspose.Cells admite otras fuentes de datos además de OData?
    
R: Sí, Aspose.Cells admite múltiples fuentes de datos, como bases de datos SQL, archivos CSV, servicios web, etc.

#### P: ¿Cómo puedo usar los detalles de OData recuperados en mi aplicación?
    
R: Una vez que haya recuperado los detalles de OData usando Aspose.Cells, puede usarlos para el análisis de datos, la generación de informes o cualquier otra manipulación en su aplicación.

#### P: ¿Puedo filtrar u ordenar datos de OData cuando los recupero con Aspose.Cells?
    
R: Sí, Aspose.Cells ofrece funciones avanzadas para filtrar, ordenar y manipular datos de OData para satisfacer sus necesidades específicas.

#### P: ¿Puedo automatizar el proceso de recuperación de detalles de OData con Aspose.Cells?
    
R: Sí, puede automatizar el proceso de recuperación de detalles de OData integrando Aspose.Cells en sus flujos de trabajo o usando scripts de programación.