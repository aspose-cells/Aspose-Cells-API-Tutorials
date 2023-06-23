---
title: Permitir al usuario editar rangos en la hoja de cálculo de Excel
linktitle: Permitir al usuario editar rangos en la hoja de cálculo de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Permita que los usuarios editen rangos específicos en una hoja de cálculo de Excel usando Aspose.Cells para .NET. Guía paso a paso con código fuente en C#.
type: docs
weight: 10
url: /es/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
En esta guía, lo guiaremos a través de cómo usar Aspose.Cells para .NET para permitir que el usuario edite rangos específicos en una hoja de cálculo de Excel. Siga los pasos a continuación para realizar esta tarea.

## Paso 1: Configuración del entorno

Asegúrese de haber configurado su entorno de desarrollo e instalado Aspose.Cells para .NET. Puede descargar la última versión de la biblioteca desde el sitio web oficial de Aspose.

## Paso 2: importa los espacios de nombres requeridos

En su proyecto de C#, importe los espacios de nombres necesarios para trabajar con Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Paso 3: Configuración de la ruta al directorio de documentos

 declarar un`dataDir` variable para especificar la ruta al directorio donde desea guardar el archivo de Excel generado:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Asegúrese de reemplazar`"YOUR_DOCUMENT_DIRECTORY"` con la ruta correcta en su sistema.

## Paso 4: crear un objeto de libro de trabajo

Cree una instancia de un nuevo objeto Libro de trabajo que represente el libro de trabajo de Excel que desea crear:

```csharp
Workbook book = new Workbook();
```

## Paso 5: Acceso a la primera hoja de trabajo

Navegue a la primera hoja de trabajo en el libro de Excel usando el siguiente código:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Paso 6: Recuperación de rangos de modificación autorizados

 Obtenga la colección de rangos de edición permitidos usando el`AllowEditRanges` propiedad:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Paso 7: Definir un rango protegido

 Defina un rango protegido usando el`Add` metodo de la`AllowEditRanges` recopilación:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Aquí hemos creado un rango protegido "r2" que se extiende desde la celda A1 hasta la celda C3.

## Paso 8: Especificación de la contraseña

 Especifique una contraseña para el rango protegido usando el`Password` propiedad:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Asegúrese de reemplazar`"YOUR_PASSWORD"` con la contraseña deseada.

## Paso 9: Proteger la hoja de trabajo

 Proteja la hoja de trabajo usando el`Protect` metodo de la`Worksheet` objeto:

```csharp
sheet.Protect(ProtectionType.All);
```

Esto protegerá la hoja de cálculo evitando cualquier modificación fuera de los rangos permitidos.

## Paso 10: Registrar el

  archivo Excel

 Guarde el archivo de Excel generado usando el`Save` metodo de la`Workbook` objeto:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Asegúrese de especificar el nombre de archivo deseado y la ruta correcta.

### Ejemplo de código fuente para Permitir que el usuario edite rangos en la hoja de cálculo de Excel usando Aspose.Cells para .NET 
```csharp
// La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crear directorio si aún no está presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Crear una instancia de un nuevo libro de trabajo
Workbook book = new Workbook();
// Obtener la primera hoja de cálculo (predeterminada)
Worksheet sheet = book.Worksheets[0];
// Obtener Permitir rangos de edición
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Definir rango protegido
ProtectedRange proteced_range;
// Crear el rango
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Especifique la contraseña
proteced_range.Password = "123";
// proteger la hoja
sheet.Protect(ProtectionType.All);
// Guarde el archivo de Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusión

Ahora ha aprendido a usar Aspose.Cells para .NET para permitir que el usuario edite rangos específicos en una hoja de cálculo de Excel. Siéntase libre de explorar más a fondo las funciones que ofrece Aspose.Cells para satisfacer sus necesidades específicas.


### preguntas frecuentes

#### 1. ¿Cómo permitir que el usuario edite rangos específicos en la hoja de cálculo de Excel?

 Puedes usar el`ProtectedRangeCollection` class para definir los rangos de modificación permitidos. Utilizar el`Add` para crear un nuevo rango protegido con las celdas deseadas.

#### 2. ¿Puedo establecer una contraseña para rangos de modificación autorizados?

 Sí, puede especificar una contraseña utilizando el`Password` propiedad de la`ProtectedRange` objeto. Esto restringirá el acceso solo a los usuarios con la contraseña.

#### 3. ¿Cómo protejo la hoja de cálculo una vez que se establecen los rangos permitidos?

 Utilizar el`Protect` metodo de la`Worksheet` objeto para proteger la hoja de cálculo. Esto evitará cualquier cambio fuera de los rangos permitidos, posiblemente solicitando una contraseña si especificó una.