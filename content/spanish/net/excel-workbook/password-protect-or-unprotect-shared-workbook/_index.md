---
title: Proteger con contraseña o desproteger el libro de trabajo compartido
linktitle: Proteger con contraseña o desproteger el libro de trabajo compartido
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a proteger o desproteger con contraseña un libro compartido usando Aspose.Cells para .NET.
type: docs
weight: 120
url: /es/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Proteger un libro compartido con una contraseña es importante para garantizar la privacidad de los datos. Con Aspose.Cells para .NET, puede proteger o desproteger fácilmente un libro compartido mediante contraseñas. Siga los pasos a continuación para obtener los resultados deseados:

## Paso 1: especificar el directorio de salida

Primero, debe especificar el directorio de salida donde se guardará el archivo Excel protegido. Aquí se explica cómo hacerlo usando Aspose.Cells:

```csharp
// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

## Paso 2: cree un archivo de Excel vacío

Luego puede crear un archivo de Excel vacío al que desea aplicar protección o desprotección. Aquí hay un código de muestra:

```csharp
// Crear un libro de Excel vacío
Workbook wb = new Workbook();
```

## Paso 3: proteger o desproteger el libro compartido

Después de crear el libro, puede proteger o desproteger el libro compartido especificando la contraseña adecuada. Así es cómo:

```csharp
// Proteger el libro compartido con una contraseña
wb.ProtectSharedWorkbook("1234");

// Descomentar esta línea para desproteger el libro compartido
// wb.UnprotectSharedWorkbook("1234");
```

## Paso 4: guarde el archivo Excel de salida

Una vez que aplique la protección o desprotección, puede guardar el archivo de Excel protegido en el directorio de salida especificado. He aquí cómo hacerlo:

```csharp
// Guarde el archivo Excel de salida
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Código fuente de muestra para proteger o desproteger un libro de trabajo compartido con contraseña usando Aspose.Cells para .NET 
```csharp
//Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
//Crear un archivo Excel vacío
Workbook wb = new Workbook();
//Proteja el libro compartido con contraseña
wb.ProtectSharedWorkbook("1234");
//Descomentar esta línea para desproteger el libro compartido
//wb.UnprotectSharedWorkbook("1234");
//Guarde el archivo Excel de salida
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusión

Proteger o desproteger un libro compartido con una contraseña es esencial para garantizar la seguridad de los datos. Con Aspose.Cells para .NET puede agregar fácilmente esta funcionalidad a sus archivos de Excel. Si sigue los pasos de esta guía, puede proteger o desproteger eficazmente sus libros compartidos mediante contraseñas. Experimente con sus propios archivos de Excel y asegúrese de mantener la seguridad de sus datos confidenciales.

### Preguntas frecuentes

#### P: ¿Qué tipos de protección puedo aplicar a un libro compartido con Aspose.Cells?
    
R: Con Aspose.Cells, puede proteger un libro compartido especificando una contraseña para evitar el acceso no autorizado, la modificación o la eliminación de datos.

#### P: ¿Puedo proteger un libro compartido sin especificar una contraseña?
    
R: Sí, puede proteger un libro compartido sin especificar una contraseña. Sin embargo, se recomienda utilizar una contraseña segura para mayor seguridad.

#### P: ¿Cómo puedo desproteger un libro compartido con Aspose.Cells?
    
R: Para desproteger un libro compartido, debe especificar la misma contraseña que utilizó al proteger el libro. Esto permite eliminar la protección y acceder libremente a los datos.

#### P: ¿La protección de un libro compartido afecta las características y fórmulas del libro?
    
R: Cuando protege un libro compartido, los usuarios aún pueden acceder a las funciones y fórmulas presentes en el libro. La protección solo afecta los cambios estructurales en el libro de trabajo.