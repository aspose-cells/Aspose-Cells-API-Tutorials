---
title: Permitir al usuario editar rangos en la hoja de cálculo de Excel
linktitle: Permitir al usuario editar rangos en la hoja de cálculo de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Permita a los usuarios editar rangos específicos en una hoja de cálculo de Excel usando Aspose.Cells para .NET. Guía paso a paso con código fuente en C#.
type: docs
weight: 10
url: /es/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
En esta guía, le explicaremos cómo utilizar Aspose.Cells para .NET para permitir al usuario editar rangos específicos en una hoja de cálculo de Excel. Siga los pasos a continuación para realizar esta tarea.

## Paso 1: configurar el entorno

Asegúrese de haber configurado su entorno de desarrollo e instalado Aspose.Cells para .NET. Puede descargar la última versión de la biblioteca desde el sitio web oficial de Aspose.

## Paso 2: importar los espacios de nombres necesarios

En su proyecto C#, importe los espacios de nombres necesarios para trabajar con Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Paso 3: configurar la ruta al directorio de documentos

 Declarar un`dataDir` variable para especificar la ruta al directorio donde desea guardar el archivo de Excel generado:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Asegúrate de reemplazar`"YOUR_DOCUMENT_DIRECTORY"` con la ruta correcta en su sistema.

## Paso 4: crear un objeto de libro de trabajo

Cree una instancia de un nuevo objeto Libro de trabajo que represente el libro de Excel que desea crear:

```csharp
Workbook book = new Workbook();
```

## Paso 5: Acceso a la primera hoja de trabajo

Navegue a la primera hoja de trabajo del libro de Excel usando el siguiente código:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Paso 6: Recuperar rangos de modificación autorizados

 Obtenga la colección de rangos de edición permitidos usando el`AllowEditRanges` propiedad:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Paso 7: definir un rango protegido

 Defina un rango protegido usando el`Add` método de la`AllowEditRanges` recopilación:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Aquí hemos creado un rango protegido "r2" que se extiende desde la celda A1 hasta la celda C3.

## Paso 8: especificar la contraseña

 Especifique una contraseña para el rango protegido usando el`Password` propiedad:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Asegúrate de reemplazar`"YOUR_PASSWORD"` con la contraseña deseada.

## Paso 9: Proteger la hoja de trabajo

 Proteja la hoja de trabajo usando el`Protect` método de la`Worksheet` objeto:

```csharp
sheet.Protect(ProtectionType.All);
```

Esto protegerá la hoja de cálculo evitando cualquier modificación fuera de los rangos permitidos.

## Paso 10: Registrar el

  archivo Excel

 Guarde el archivo Excel generado usando el`Save` método de la`Workbook` objeto:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Asegúrese de especificar el nombre del archivo deseado y la ruta correcta.

### Código fuente de muestra para permitir al usuario editar rangos en una hoja de cálculo de Excel usando Aspose.Cells para .NET 
```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Cree un directorio si aún no está presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Crear una instancia de un nuevo libro de trabajo
Workbook book = new Workbook();
// Obtenga la primera hoja de trabajo (predeterminada)
Worksheet sheet = book.Worksheets[0];
// Obtenga Permitir rangos de edición
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

Ahora ha aprendido a utilizar Aspose.Cells para .NET para permitir al usuario editar rangos específicos en una hoja de cálculo de Excel. No dude en explorar más a fondo las funciones que ofrece Aspose.Cells para satisfacer sus necesidades específicas.


### Preguntas frecuentes

#### 1. ¿Cómo permitir que el usuario edite rangos específicos en una hoja de cálculo de Excel?

 Puedes usar el`ProtectedRangeCollection` clase para definir los rangos de modificación permitidos. Utilizar el`Add` Método para crear un nuevo rango protegido con las celdas deseadas.

#### 2. ¿Puedo establecer una contraseña para los rangos de modificación autorizados?

 Sí, puede especificar una contraseña utilizando el`Password` propiedad de la`ProtectedRange` objeto. Esto restringirá el acceso sólo a los usuarios con la contraseña.

#### 3. ¿Cómo protejo la hoja de cálculo una vez establecidos los rangos permitidos?

 Utilizar el`Protect` método de la`Worksheet` objeto para proteger la hoja de trabajo. Esto evitará cualquier cambio fuera de los rangos permitidos, posiblemente solicitando una contraseña si especificó una.