---
title: Proteger fila en hoja de cálculo de Excel
linktitle: Proteger fila en hoja de cálculo de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Descubra en este tutorial cómo proteger las filas de una hoja de cálculo de Excel usando Aspose.Cells para .NET. Tutorial paso a paso en C#.
type: docs
weight: 60
url: /es/net/protect-excel-file/protect-row-in-excel-worksheet/
---
En este tutorial, veremos algo de código fuente de C# que utiliza la biblioteca Aspose.Cells para proteger filas en una hoja de cálculo de Excel. Revisaremos cada paso del código y explicaremos cómo funciona. Siga las instrucciones cuidadosamente para obtener los resultados deseados.

## Paso 1: requisitos previos

Antes de comenzar, asegúrese de haber instalado la biblioteca Aspose.Cells para .NET. Puede obtenerlo en el sitio web oficial de Aspose. También asegúrese de tener una versión reciente de Visual Studio o cualquier otro entorno de desarrollo de C#.

## Paso 2: importar los espacios de nombres necesarios

Para utilizar la biblioteca Aspose.Cells, necesitamos importar los espacios de nombres necesarios a nuestro código. Agregue las siguientes líneas en la parte superior de su archivo fuente de C#:

```csharp
using Aspose.Cells;
```

## Paso 3: crear un libro de Excel

En este paso, crearemos un nuevo libro de Excel. Utilice el siguiente código para crear un libro de Excel:

```csharp
// Ruta al directorio de documentos.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Cree un nuevo libro de trabajo.
Workbook wb = new Workbook();
```

 Asegúrate de reemplazar`"YOUR_DOCUMENTS_DIR"` con la ruta adecuada a su directorio de documentos.

## Paso 4: crear una hoja de cálculo

Ahora que hemos creado el libro de Excel, creemos una hoja de trabajo y obtengamos la primera hoja. Utilice el siguiente código:

```csharp
// Crea un objeto de hoja de cálculo y obtén la primera hoja.
Worksheet sheet = wb.Worksheets[0];
```

## Paso 5: Definir el estilo

En este paso, definiremos el estilo a aplicar a las filas de la hoja de cálculo. Utilice el siguiente código:

```csharp
// Definición del objeto de estilo.
Styling styling;
```

## Paso 6: bucle para desbloquear todas las columnas

Ahora recorreremos todas las columnas de la hoja de trabajo y las desbloquearemos. Utilice el siguiente código:

```csharp
// Recorra todas las columnas de la hoja de trabajo y desbloquéelas.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Paso 7: bloquear la primera línea

En este paso, bloquearemos la primera fila de la hoja de trabajo. Utilice el siguiente código:

```csharp
// Consigue el estilo de la primera línea.
style = sheet.Cells.Rows[0].Style;
// Bloquea el estilo.
style. IsLocked = true;
// Aplica el estilo a la primera línea.
sheet.Cells.ApplyRowStyle(0, style);
```

## Paso 8: Proteger la hoja de trabajo

Ahora que configuramos los estilos y bloqueamos las filas, protejamos la hoja de cálculo. Utilice el siguiente código:

```csharp
// Proteja la hoja de trabajo.
sheet.Protect(ProtectionType.All);
```

## Paso 9: guardar el archivo de Excel

Finalmente, guardaremos el archivo Excel modificado. Utilice el siguiente código:

```csharp
// Guarde el archivo de Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Asegúrese de especificar la ruta correcta para guardar el archivo de Excel modificado.

### Código fuente de muestra para Proteger fila en hoja de cálculo de Excel usando Aspose.Cells para .NET 
```csharp
//La ruta al directorio de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Cree un directorio si aún no está presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Cree un nuevo libro de trabajo.
Workbook wb = new Workbook();
// Cree un objeto de hoja de trabajo y obtenga la primera hoja.
Worksheet sheet = wb.Worksheets[0];
// Defina el objeto de estilo.
Style style;
// Defina el objeto styleflag.
StyleFlag flag;
// Recorra todas las columnas de la hoja de trabajo y desbloquéelas.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Obtén el estilo de la primera fila.
style = sheet.Cells.Rows[0].Style;
// Ciérralo.
style.IsLocked = true;
//Crea una instancia de la bandera.
flag = new StyleFlag();
// Establezca la configuración de bloqueo.
flag.Locked = true;
// Aplica el estilo a la primera fila.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Protege la sábana.
sheet.Protect(ProtectionType.All);
// Guarde el archivo de Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusión

¡Enhorabuena! Ahora tiene el código fuente de C# que le permite proteger filas en una hoja de cálculo de Excel utilizando la biblioteca Aspose.Cells para .NET. Asegúrese de seguir los pasos cuidadosamente y personalizar el código según sus necesidades específicas.

### Preguntas frecuentes (Preguntas frecuentes)

#### ¿Este código funciona con versiones recientes de Excel?

Sí, este código funciona con versiones recientes de Excel, incluidos archivos en formato Excel 2010 y superior.

#### ¿Puedo proteger sólo filas específicas en lugar de todas las filas de la hoja de cálculo?

Sí, puede modificar el código para especificar las filas específicas que desea proteger. Deberá ajustar el bucle y los índices en consecuencia.

#### ¿Cómo puedo desbloquear líneas bloqueadas nuevamente?

 Puedes usar el`IsLocked` método de la`Style` objeto para establecer el valor`false` y desbloquear las filas.

#### ¿Es posible proteger varias hojas de cálculo en el mismo libro de Excel?

Sí, puede repetir los pasos para crear una hoja de trabajo, configurar el estilo y proteger cada hoja de trabajo del libro.

#### ¿Cómo puedo cambiar la contraseña de protección de la hoja de cálculo?

 Puede cambiar la contraseña utilizando el`Protect` método y especificando una nueva contraseña como argumento.