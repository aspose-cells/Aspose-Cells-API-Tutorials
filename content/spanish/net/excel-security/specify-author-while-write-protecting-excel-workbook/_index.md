---
title: Especifique el autor mientras escribe y protege el libro de Excel
linktitle: Especifique el autor mientras escribe y protege el libro de Excel
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda cómo proteger y personalizar sus libros de Excel usando Aspose.Cells para .NET. Tutorial paso a paso en C#.
type: docs
weight: 30
url: /es/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

En este tutorial, le mostraremos cómo especificar el autor al proteger contra escritura un libro de Excel usando la biblioteca Aspose.Cells para .NET.

## Paso 1: Preparar el entorno

Antes de comenzar, asegúrese de tener Aspose.Cells para .NET instalado en su máquina. Descargue la biblioteca del sitio web oficial de Aspose y siga las instrucciones de instalación proporcionadas.

## Paso 2: configurar los directorios de origen y de salida

En el código fuente proporcionado, debe especificar los directorios de origen y de salida. Modificar el`sourceDir` y`outputDir` variables reemplazando "SU DIRECTORIO DE FUENTE" y "SU DIRECTORIO DE SALIDA" con las respectivas rutas absolutas en su máquina.

```csharp
// Directorio fuente
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Directorio de salida
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Paso 3: crear un libro de Excel vacío

Para comenzar, creamos un objeto Libro de trabajo que representa un libro de Excel vacío.

```csharp
// Cree un libro de trabajo vacío.
Workbook wb = new Workbook();
```

## Paso 4: protección contra escritura con contraseña

 A continuación, especificamos una contraseña para proteger contra escritura el libro de Excel usando el`WriteProtection.Password` propiedad del objeto Libro de trabajo.

```csharp
// Libro de trabajo protegido contra escritura con contraseña.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Paso 5: especificación del autor

 Ahora especificamos el autor del libro de Excel usando el`WriteProtection.Author` propiedad del objeto Libro de trabajo.

```csharp
// Especifique el autor mientras escribe el libro de protección.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Paso 6: Copia de seguridad del libro de Excel protegido

 Una vez especificada la protección contra escritura y el autor, podemos guardar el libro de Excel en formato XLSX usando el`Save()` método.

```csharp
// Guarde el libro en formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Código fuente de muestra para Especificar autor mientras se escribe Proteger el libro de Excel usando Aspose.Cells para .NET 
```csharp
//Directorio fuente
string sourceDir = "YOUR SOURCE DIRECTORY";

//Directorio de salida
string outputDir = "YOUR OUTPUT DIRECTORY";

// Cree un libro de trabajo vacío.
Workbook wb = new Workbook();

// Libro de trabajo protegido contra escritura con contraseña.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Especifique el autor mientras escribe el libro de protección.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Guarde el libro en formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Conclusión

¡Enhorabuena! Ahora ha aprendido cómo especificar el autor al proteger contra escritura un libro de Excel con Aspose.Cells para .NET. Puede aplicar estos pasos a sus propios proyectos para proteger y personalizar sus libros de Excel.

No dude en explorar más a fondo las funciones de Aspose.Cells para .NET para realizar operaciones más avanzadas en archivos de Excel.

## Preguntas frecuentes

#### P: ¿Puedo proteger contra escritura un libro de Excel sin especificar una contraseña?

 R: Sí, puedes usar el objeto Libro de trabajo.`WriteProtect()` método sin especificar una contraseña para proteger contra escritura un libro de Excel. Esto restringirá los cambios en el libro sin requerir una contraseña.

#### P: ¿Cómo elimino la protección contra escritura de un libro de Excel?

 R: Para eliminar la protección contra escritura de un libro de Excel, puede usar el`Unprotect()` método del objeto Hoja de trabajo o el`RemoveWriteProtection()` método del objeto Workbook, dependiendo de su caso de uso específico. .

#### P: Olvidé la contraseña para proteger mi libro de Excel. Qué puedo hacer ?

R: Si olvidó la contraseña para proteger su libro de Excel, no podrá eliminarla directamente. Sin embargo, puede intentar utilizar herramientas especializadas de terceros que proporcionen funciones de recuperación de contraseña para archivos de Excel protegidos.

#### P: ¿Es posible especificar varios autores al proteger contra escritura un libro de Excel?

R: No, la biblioteca Aspose.Cells para .NET permite especificar un único autor al proteger contra escritura un libro de Excel. Si desea especificar varios autores, deberá considerar soluciones personalizadas manipulando directamente el archivo de Excel.