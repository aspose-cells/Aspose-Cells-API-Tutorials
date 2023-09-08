---
title: Configuración de protección avanzada para la hoja de cálculo de Excel
linktitle: Configuración de protección avanzada para la hoja de cálculo de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Proteja sus archivos de Excel configurando configuraciones de protección avanzadas con Aspose.Cells para .NET.
type: docs
weight: 10
url: /es/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
En este tutorial, lo guiaremos a través de los pasos para establecer configuraciones de protección avanzadas para una hoja de cálculo de Excel utilizando la biblioteca Aspose.Cells para .NET. Siga las instrucciones a continuación para completar esta tarea.

## Paso 1: preparación

Asegúrese de haber instalado Aspose.Cells para .NET y creado un proyecto C# en su entorno de desarrollo integrado (IDE) preferido.

## Paso 2: establezca la ruta del directorio de documentos

 Declarar un`dataDir` variable e inicialícela con la ruta a su directorio de documentos. Por ejemplo :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Asegúrate de reemplazar`"YOUR_DOCUMENTS_DIRECTORY"` con la ruta real a su directorio.

## Paso 3: cree una secuencia de archivos para abrir el archivo de Excel

 Crear un`FileStream` objeto que contiene el archivo Excel a abrir:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Asegúrate de tener el archivo Excel.`book1.xls` en su directorio de documentos o especifique el nombre y la ubicación del archivo correcto.

## Paso 4: cree una instancia de un objeto Libro de trabajo y abra el archivo Excel

 Utilizar el`Workbook`clase de Aspose.Cells para crear una instancia de un objeto Libro de trabajo y abrir el archivo Excel especificado a través de la secuencia de archivos:

```csharp
Workbook excel = new Workbook(fstream);
```

## Paso 5: acceda a la primera hoja de trabajo

Navegue a la primera hoja de trabajo del archivo de Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Paso 6: Establecer la configuración de protección de la hoja de trabajo

Utilice las propiedades del objeto Hoja de trabajo para establecer la configuración de protección de la hoja de trabajo según sea necesario. Por ejemplo :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Establezca otras configuraciones de protección según sea necesario...
```

## Paso 7: guarde el archivo de Excel modificado

 Guarde el archivo Excel modificado utilizando el`Save` método del objeto Libro de trabajo:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Asegúrese de especificar la ruta y el nombre de archivo deseados para el archivo de salida.

## Paso 8: cierre la secuencia de archivos

Una vez guardado, cierre la secuencia de archivos para liberar todos los recursos asociados:

```csharp
fstream.Close();
```
	
### Código fuente de muestra para la configuración de protección avanzada para la hoja de cálculo de Excel usando Aspose.Cells para .NET 
```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una secuencia de archivos que contenga el archivo de Excel que se abrirá
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Crear instancias de un objeto de libro de trabajo
// Abrir el archivo de Excel a través de la secuencia de archivos
Workbook excel = new Workbook(fstream);
// Accediendo a la primera hoja de trabajo en el archivo de Excel
Worksheet worksheet = excel.Worksheets[0];
// Restringir a los usuarios la eliminación de columnas de la hoja de trabajo
worksheet.Protection.AllowDeletingColumn = false;
// Restringir a los usuarios para que eliminen una fila de la hoja de trabajo
worksheet.Protection.AllowDeletingRow = false;
// Restringir a los usuarios la edición del contenido de la hoja de trabajo
worksheet.Protection.AllowEditingContent = false;
// Restringir a los usuarios la edición de objetos de la hoja de trabajo
worksheet.Protection.AllowEditingObject = false;
// Restringir a los usuarios la edición de escenarios de la hoja de trabajo
worksheet.Protection.AllowEditingScenario = false;
//Restringir a los usuarios para filtrar
worksheet.Protection.AllowFiltering = false;
// Permitir a los usuarios formatear celdas de la hoja de trabajo
worksheet.Protection.AllowFormattingCell = true;
// Permitir a los usuarios formatear filas de la hoja de trabajo
worksheet.Protection.AllowFormattingRow = true;
// Permitir a los usuarios insertar columnas en la hoja de trabajo
worksheet.Protection.AllowFormattingColumn = true;
// Permitir a los usuarios insertar hipervínculos en la hoja de trabajo
worksheet.Protection.AllowInsertingHyperlink = true;
// Permitir a los usuarios insertar filas en la hoja de trabajo
worksheet.Protection.AllowInsertingRow = true;
// Permitir a los usuarios seleccionar celdas bloqueadas de la hoja de trabajo
worksheet.Protection.AllowSelectingLockedCell = true;
// Permitir a los usuarios seleccionar celdas desbloqueadas de la hoja de trabajo
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Permitir a los usuarios ordenar
worksheet.Protection.AllowSorting = true;
// Permitir a los usuarios usar tablas dinámicas en la hoja de trabajo
worksheet.Protection.AllowUsingPivotTable = true;
// Guardar el archivo Excel modificado
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Cerrar el flujo de archivos para liberar todos los recursos
fstream.Close();
```

## Conclusión

¡Enhorabuena! Ahora ha aprendido cómo establecer configuraciones de protección avanzadas para una hoja de cálculo de Excel usando Aspose.Cells para .NET. Utilice este conocimiento para proteger sus archivos de Excel y restringir las acciones del usuario.

### Preguntas frecuentes

#### P: ¿Cómo puedo crear un nuevo proyecto de C# en mi IDE?

R: Los pasos para crear un nuevo proyecto de C# pueden variar según el IDE que esté utilizando. Consulte la documentación de su IDE para obtener instrucciones detalladas.

#### P: ¿Es posible establecer configuraciones de protección personalizadas distintas a las mencionadas en el tutorial?

R: Sí, Aspose.Cells ofrece una amplia gama de configuraciones de protección que puede personalizar según sus necesidades específicas. Consulte la documentación de Aspose.Cells para obtener más detalles.

#### P: ¿Cuál es el formato de archivo utilizado para guardar el archivo de Excel modificado en el código de muestra?

R: En el código de muestra, el archivo de Excel modificado se guarda en formato Excel 97-2003 (.xls). Puede elegir otros formatos admitidos por Aspose.Cells si es necesario.

#### P: ¿Cómo puedo acceder a otras hojas de trabajo en el archivo de Excel?

 R: Puede acceder a otras hojas de trabajo usando el índice o el nombre de la hoja, por ejemplo:`Worksheet worksheet = excel.Worksheets[1];` o`Worksheet worksheet = excel.Worksheets[" SheetName"];`.