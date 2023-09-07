---
title: Proteger o desproteger con contraseña el libro de trabajo compartido
linktitle: Proteger o desproteger con contraseña el libro de trabajo compartido
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a proteger con contraseña o desproteger un libro de trabajo compartido con Aspose.Cells para .NET.
type: docs
weight: 120
url: /es/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Proteger un libro de trabajo compartido con una contraseña es importante para garantizar la privacidad de los datos. Con Aspose.Cells para .NET, puede proteger o desproteger fácilmente un libro de trabajo compartido mediante contraseñas. Siga los pasos a continuación para obtener los resultados deseados:

## Paso 1: especificar el directorio de salida

Primero, debe especificar el directorio de salida donde se guardará el archivo de Excel protegido. He aquí cómo hacerlo usando Aspose.Cells:

```csharp
// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

## Paso 2: crea un archivo de Excel vacío

Luego puede crear un archivo de Excel vacío en el que desea aplicar protección o desprotección. Aquí hay un código de muestra:

```csharp
// Crear un libro de Excel vacío
Workbook wb = new Workbook();
```

## Paso 3: proteger o desproteger el libro de trabajo compartido

Después de crear el libro de trabajo, puede proteger o desproteger el libro de trabajo compartido especificando la contraseña adecuada. Así es cómo:

```csharp
// Proteger el libro compartido con una contraseña
wb.ProtectSharedWorkbook("1234");

// Descomente esta línea para desproteger el libro de trabajo compartido
// wb.UnprotectSharedWorkbook("1234");
```

## Paso 4: guarde el archivo de salida de Excel

Una vez que aplica la protección o la desprotección, puede guardar el archivo de Excel protegido en el directorio de salida especificado. Aquí está cómo hacerlo:

```csharp
// Guarde el archivo de salida de Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Ejemplo de código fuente para proteger con contraseña o desproteger el libro de trabajo compartido usando Aspose.Cells para .NET 
```csharp
//Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
//Crear archivo de Excel vacío
Workbook wb = new Workbook();
//Proteger el libro de trabajo compartido con contraseña
wb.ProtectSharedWorkbook("1234");
//Descomente esta línea para desproteger el libro de trabajo compartido
//wb.UnprotectSharedWorkbook("1234");
//Guarde el archivo de salida de Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusión

Proteger o desproteger un libro de trabajo compartido con una contraseña es fundamental para garantizar la seguridad de los datos. Con Aspose.Cells for .NET puede agregar fácilmente esta funcionalidad a sus archivos de Excel. Si sigue los pasos de esta guía, puede proteger o desproteger de manera efectiva sus libros de trabajo compartidos mediante contraseñas. Experimente con sus propios archivos de Excel y asegúrese de mantener la seguridad de sus datos confidenciales.

### preguntas frecuentes

#### P: ¿Qué tipos de protección puedo aplicar a un libro de trabajo compartido con Aspose.Cells?
    
R: Con Aspose.Cells, puede proteger un libro de trabajo compartido especificando una contraseña para evitar el acceso no autorizado, la modificación o la eliminación de datos.

#### P: ¿Puedo proteger un libro de trabajo compartido sin especificar una contraseña?
    
R: Sí, puede proteger un libro de trabajo compartido sin especificar una contraseña. Sin embargo, se recomienda utilizar una contraseña segura para mayor seguridad.

#### P: ¿Cómo puedo desproteger un libro de trabajo compartido con Aspose.Cells?
    
R: Para desproteger un libro de trabajo compartido, debe especificar la misma contraseña que utilizó para proteger el libro de trabajo. Esto permite eliminar la protección y acceder libremente a los datos.

#### P: ¿La protección de un libro de trabajo compartido afecta las características y fórmulas del libro de trabajo?
    
R: Cuando protege un libro de trabajo compartido, los usuarios aún pueden acceder a las funciones y fórmulas presentes en el libro de trabajo. La protección solo afecta a los cambios estructurales en el libro de trabajo.