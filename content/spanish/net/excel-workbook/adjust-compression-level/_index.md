---
title: Ajustar el nivel de compresión
linktitle: Ajustar el nivel de compresión
second_title: Referencia de API de Aspose.Cells para .NET
description: Reduzca el tamaño de sus libros de Excel ajustando el nivel de compresión con Aspose.Cells para .NET.
type: docs
weight: 50
url: /es/net/excel-workbook/adjust-compression-level/
---
En este tutorial paso a paso, explicaremos el código fuente C# proporcionado que le permitirá ajustar el nivel de compresión usando Aspose.Cells para .NET. Siga los pasos a continuación para ajustar el nivel de compresión en su libro de Excel.

## Paso 1: configurar los directorios de origen y de salida

```csharp
// directorio fuente
string sourceDir = RunExamples.Get_SourceDirectory();
// Directorio de salida
string outDir = RunExamples.Get_OutputDirectory();
```

En este primer paso, definimos los directorios de origen y salida de los archivos de Excel.

## Paso 2: cargar el libro de Excel

```csharp
// Cargue el libro de Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Cargamos el libro de Excel desde el archivo especificado usando el`Workbook` clase de Aspose.Cells.

## Paso 3: configurar las opciones de copia de seguridad

```csharp
// Definir opciones de respaldo
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Creamos una instancia del`XlsbSaveOptions` clase para configurar las opciones de guardado.

## Paso 4: Ajuste el nivel de compresión (Nivel 1)

```csharp
// Ajustar el nivel de compresión (Nivel 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Ajustamos el nivel de compresión configurando`CompressionType` a`Level1`. Luego guardamos el libro de Excel con esta opción de compresión especificada.

## Paso 5: Ajuste el nivel de compresión (Nivel 6)

```csharp
// Ajustar el nivel de compresión (Nivel 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Repetimos el proceso para ajustar el nivel de compresión a`Level6` y guarde el libro de Excel con esta opción.

## Paso 6: Ajuste el nivel de compresión (Nivel 9)

```csharp
// Ajustar el nivel de compresión (Nivel 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Repetimos el proceso una última vez para ajustar el nivel de compresión a`Level9` y guarde el libro de Excel con esta opción.

### Código fuente de muestra para ajustar el nivel de compresión usando Aspose.Cells para .NET 
```csharp
//Directorio fuente
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Conclusión

¡Enhorabuena! Aprendió a ajustar el nivel de compresión en un libro de Excel usando Aspose.Cells para .NET. Experimente con diferentes niveles de compresión para encontrar el que mejor se adapte a sus necesidades.

### Preguntas frecuentes

#### P: ¿Qué es la compresión en un libro de Excel?

R: La compresión en un libro de Excel es un proceso de reducción del tamaño del archivo mediante el uso de algoritmos de compresión. Esto reduce el espacio de almacenamiento requerido y mejora el rendimiento al cargar y manipular el archivo.

#### P: ¿Qué niveles de compresión están disponibles con Aspose.Cells?

R: Con Aspose.Cells, puede ajustar el nivel de compresión de 1 a 9. Cuanto mayor sea el nivel de compresión, menor será el tamaño del archivo, pero también puede aumentar el tiempo de procesamiento.

#### P: ¿Cómo elijo el nivel de compresión correcto para mi libro de Excel?

R: La elección del nivel de compresión depende de sus necesidades específicas. Si desea la máxima compresión y el tiempo de procesamiento no es un problema, puede optar por el nivel 9. Si prefiere un compromiso entre el tamaño del archivo y el tiempo de procesamiento, puede elegir un nivel intermedio.

#### P: ¿La compresión afecta la calidad de los datos en el libro de Excel?

R: No, la compresión no afecta la calidad de los datos en el libro de Excel. Simplemente reduce el tamaño del archivo utilizando técnicas de compresión sin alterar los datos en sí.

#### P: ¿Puedo ajustar el nivel de compresión después de guardar el archivo de Excel?

R: No, una vez que guarde el archivo de Excel con un nivel de compresión específico, no podrá ajustar el nivel de compresión más adelante. Deberá guardar el archivo nuevamente con el nuevo nivel de compresión si desea modificarlo.