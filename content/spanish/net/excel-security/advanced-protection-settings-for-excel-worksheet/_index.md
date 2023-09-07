---
title: Configuración de protección avanzada para la hoja de cálculo de Excel
linktitle: Configuración de protección avanzada para la hoja de cálculo de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Proteja sus archivos de Excel configurando la configuración de protección avanzada con Aspose.Cells para .NET.
type: docs
weight: 10
url: /es/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
En este tutorial, lo guiaremos a través de los pasos para establecer la configuración de protección avanzada para una hoja de cálculo de Excel usando la biblioteca Aspose.Cells para .NET. Siga las instrucciones a continuación para completar esta tarea.

## Paso 1: Preparación

Asegúrese de haber instalado Aspose.Cells para .NET y creado un proyecto C# en su entorno de desarrollo integrado (IDE) preferido.

## Paso 2: establezca la ruta del directorio del documento

 declarar un`dataDir` variable e inicialícelo con la ruta a su directorio de documentos. Por ejemplo :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Asegúrese de reemplazar`"YOUR_DOCUMENTS_DIRECTORY"` con la ruta real a su directorio.

## Paso 3: Cree una secuencia de archivos para abrir el archivo de Excel

 Crear un`FileStream` objeto que contiene el archivo de Excel para abrir:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Asegúrate de tener el archivo de Excel`book1.xls` en su directorio de documentos o especifique el nombre de archivo y la ubicación correctos.

## Paso 4: crea una instancia de un objeto Workbook y abre el archivo de Excel

 Utilizar el`Workbook`class de Aspose.Cells para instanciar un objeto Workbook y abrir el archivo de Excel especificado a través de la secuencia de archivos:

```csharp
Workbook excel = new Workbook(fstream);
```

## Paso 5: Acceda a la primera hoja de trabajo

Navegue a la primera hoja de cálculo del archivo de Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Paso 6: Establecer la configuración de protección de la hoja de trabajo

Utilice las propiedades del objeto de la hoja de trabajo para establecer la configuración de protección de la hoja de trabajo según sea necesario. Por ejemplo :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Establezca otras configuraciones de protección según sea necesario...
```

## Paso 7: Guarde el archivo de Excel modificado

 Guarde el archivo de Excel modificado usando el`Save` método del objeto Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Asegúrese de especificar la ruta y el nombre de archivo deseados para el archivo de salida.

## Paso 8: Cierra el flujo de archivos

Una vez guardado, cierre el flujo de archivos para liberar todos los recursos asociados:

```csharp
fstream.Close();
```
	
### Ejemplo de código fuente para la configuración de protección avanzada para la hoja de cálculo de Excel con Aspose.Cells para .NET 
```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear una secuencia de archivos que contenga el archivo de Excel que se abrirá
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Crear una instancia de un objeto Workbook
// Abrir el archivo de Excel a través de la secuencia de archivos
Workbook excel = new Workbook(fstream);
// Acceso a la primera hoja de trabajo en el archivo de Excel
Worksheet worksheet = excel.Worksheets[0];
// Restricción de usuarios para eliminar columnas de la hoja de cálculo
worksheet.Protection.AllowDeletingColumn = false;
// Restricción de usuarios para eliminar filas de la hoja de cálculo
worksheet.Protection.AllowDeletingRow = false;
// Restricción de usuarios para editar contenidos de la hoja de trabajo
worksheet.Protection.AllowEditingContent = false;
// Restricción de usuarios para editar objetos de la hoja de cálculo
worksheet.Protection.AllowEditingObject = false;
// Restricción de usuarios para editar escenarios de la hoja de trabajo
worksheet.Protection.AllowEditingScenario = false;
//Restricción de usuarios para filtrar
worksheet.Protection.AllowFiltering = false;
// Permitir a los usuarios dar formato a las celdas de la hoja de cálculo
worksheet.Protection.AllowFormattingCell = true;
// Permitir a los usuarios formatear filas de la hoja de cálculo
worksheet.Protection.AllowFormattingRow = true;
// Permitir a los usuarios insertar columnas en la hoja de cálculo
worksheet.Protection.AllowFormattingColumn = true;
// Permitir a los usuarios insertar hipervínculos en la hoja de trabajo
worksheet.Protection.AllowInsertingHyperlink = true;
// Permitir a los usuarios insertar filas en la hoja de cálculo
worksheet.Protection.AllowInsertingRow = true;
// Permitir a los usuarios seleccionar celdas bloqueadas de la hoja de trabajo
worksheet.Protection.AllowSelectingLockedCell = true;
// Permitir a los usuarios seleccionar celdas desbloqueadas de la hoja de cálculo
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Permitir que los usuarios ordenen
worksheet.Protection.AllowSorting = true;
// Permitir a los usuarios usar tablas dinámicas en la hoja de trabajo
worksheet.Protection.AllowUsingPivotTable = true;
// Guardar el archivo de Excel modificado
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Cerrar el flujo de archivos para liberar todos los recursos
fstream.Close();
```

## Conclusión

¡Felicidades! Ahora ha aprendido a establecer la configuración de protección avanzada para una hoja de cálculo de Excel utilizando Aspose.Cells para .NET. Utilice este conocimiento para proteger sus archivos de Excel y restringir las acciones del usuario.

### preguntas frecuentes

#### P: ¿Cómo puedo crear un nuevo proyecto de C# en mi IDE?

R: Los pasos para crear un nuevo proyecto de C# pueden variar según el IDE que esté utilizando. Consulte la documentación de su IDE para obtener instrucciones detalladas.

#### P: ¿Es posible establecer configuraciones de protección personalizadas distintas a las mencionadas en el tutorial?

R: Sí, Aspose.Cells ofrece una amplia gama de configuraciones de protección que puede personalizar según sus necesidades específicas. Consulte la documentación de Aspose.Cells para obtener más detalles.

#### P: ¿Cuál es el formato de archivo utilizado para guardar el archivo de Excel modificado en el código de muestra?

R: En el código de ejemplo, el archivo de Excel modificado se guarda en formato Excel 97-2003 (.xls). Puede elegir otros formatos compatibles con Aspose.Cells si es necesario.

#### P: ¿Cómo puedo acceder a otras hojas de trabajo en el archivo de Excel?

 R: Puede acceder a otras hojas de trabajo utilizando el índice o el nombre de la hoja, por ejemplo:`Worksheet worksheet = excel.Worksheets[1];` o`Worksheet worksheet = excel.Worksheets[" SheetName"];`.