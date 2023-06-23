---
title: Especificar autor mientras se protege contra escritura el libro de Excel
linktitle: Especificar autor mientras se protege contra escritura el libro de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a proteger y personalizar sus libros de Excel con Aspose.Cells para .NET. Tutorial paso a paso en C#.
type: docs
weight: 30
url: /es/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

En este tutorial, le mostraremos cómo especificar el autor al proteger contra escritura un libro de Excel usando la biblioteca Aspose.Cells para .NET.

## Paso 1: Preparando el ambiente

Antes de comenzar, asegúrese de tener Aspose.Cells para .NET instalado en su máquina. Descargue la biblioteca del sitio web oficial de Aspose y siga las instrucciones de instalación proporcionadas.

## Paso 2: Configuración de los directorios de origen y salida

En el código fuente proporcionado, debe especificar los directorios de origen y salida. Modificar el`sourceDir` y`outputDir` variables reemplazando "SU DIRECTORIO DE FUENTE" y "SU DIRECTORIO DE SALIDA" con las respectivas rutas absolutas en su máquina.

```csharp
// directorio de origen
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Directorio de salida
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Paso 3: crear un libro de Excel vacío

Para comenzar, creamos un objeto Workbook que representa un libro de Excel vacío.

```csharp
// Crear libro de trabajo vacío.
Workbook wb = new Workbook();
```

## Paso 4: Protección contra escritura con contraseña

 A continuación, especificamos una contraseña para proteger contra escritura el libro de Excel usando el`WriteProtection.Password` propiedad del objeto Workbook.

```csharp
// Libro de protección contra escritura con contraseña.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Paso 5: Especificación del autor

 Ahora especificamos el autor del libro de Excel usando el`WriteProtection.Author` propiedad del objeto Workbook.

```csharp
// Especifique el autor mientras escribe el libro de trabajo de protección.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Paso 6: Copia de seguridad del libro de Excel protegido

 Una vez especificada la protección contra escritura y el autor, podemos guardar el libro de Excel en el formato XLSX usando el`Save()` método.

```csharp
// Guarde el libro de trabajo en formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Ejemplo de código fuente para especificar el autor mientras se protege contra escritura el libro de Excel con Aspose.Cells para .NET 
```csharp
//directorio de origen
string sourceDir = "YOUR SOURCE DIRECTORY";

//Directorio de salida
string outputDir = "YOUR OUTPUT DIRECTORY";

// Crear libro de trabajo vacío.
Workbook wb = new Workbook();

// Libro de protección contra escritura con contraseña.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Especifique el autor mientras escribe el libro de trabajo de protección.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Guarde el libro de trabajo en formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Conclusión

¡Felicidades! Ahora ha aprendido cómo especificar el autor al proteger contra escritura un libro de Excel con Aspose.Cells para .NET. Puede aplicar estos pasos a sus propios proyectos para proteger y personalizar sus libros de Excel.

Siéntase libre de explorar más a fondo las características de Aspose.Cells para .NET para operaciones más avanzadas en archivos de Excel.

## preguntas frecuentes

#### P: ¿Puedo proteger contra escritura un libro de Excel sin especificar una contraseña?

 R: Sí, puede usar el objeto Workbook`WriteProtect()` método sin especificar una contraseña para proteger contra escritura un libro de Excel. Esto restringirá los cambios al libro de trabajo sin requerir una contraseña.

#### P: ¿Cómo elimino la protección contra escritura de un libro de Excel?

 R: Para eliminar la protección contra escritura de un libro de Excel, puede usar el`Unprotect()` método del objeto Hoja de trabajo o el`RemoveWriteProtection()` del objeto Workbook, según su caso de uso específico. .

#### P: Olvidé la contraseña para proteger mi libro de Excel. Qué puedo hacer ?

R: Si olvidó la contraseña para proteger su libro de Excel, no puede eliminarla directamente. Sin embargo, puede intentar usar herramientas especializadas de terceros que brindan funciones de recuperación de contraseña para archivos de Excel protegidos.

#### P: ¿Es posible especificar varios autores al proteger contra escritura un libro de Excel?

R: No, la biblioteca Aspose.Cells para .NET permite especificar un solo autor al proteger contra escritura un libro de Excel. Si desea especificar varios autores, deberá considerar soluciones personalizadas manipulando directamente el archivo de Excel.