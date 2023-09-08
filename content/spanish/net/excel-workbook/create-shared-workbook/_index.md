---
title: Crear libro de trabajo compartido
linktitle: Crear libro de trabajo compartido
second_title: Referencia de API de Aspose.Cells para .NET
description: Cree un libro de trabajo compartido de Excel con Aspose.Cells para .NET para permitir la colaboración de datos simultánea.
type: docs
weight: 70
url: /es/net/excel-workbook/create-shared-workbook/
---
En este tutorial, lo guiaremos a través del código fuente de C# proporcionado que le permitirá crear un libro de trabajo compartido usando Aspose.Cells para .NET. Siga los pasos a continuación para realizar esta operación.

## Paso 1: configurar el directorio de salida

```csharp
// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

En este primer paso, definimos el directorio de salida donde se guardará el libro compartido.

## Paso 2: crear un objeto de libro de trabajo

```csharp
// Crear un objeto de libro de trabajo
Workbook wb = new Workbook();
```

Estamos creando un nuevo objeto Libro de trabajo que representará nuestro libro de Excel.

## Paso 3: habilite el uso compartido de libros

```csharp
// compartir el libro de trabajo
wb.Settings.Shared = true;
```

 Habilitamos la función para compartir el libro configurando el`Shared` propiedad del objeto Libro de trabajo para`true`.

## Paso 4: guarde el libro compartido

```csharp
// Guarde el libro compartido
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Guardamos el libro compartido especificando la ruta y el nombre del archivo de salida.

### Código fuente de muestra para crear un libro de trabajo compartido usando Aspose.Cells para .NET 
```csharp
//Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
//Crear objeto de libro de trabajo
Workbook wb = new Workbook();
//Comparte el libro de trabajo
wb.Settings.Shared = true;
//Guarde el libro de trabajo compartido
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Conclusión

¡Enhorabuena! Aprendió a crear un libro de trabajo compartido usando Aspose.Cells para .NET. El libro compartido puede ser utilizado por varios usuarios simultáneamente para colaborar en los datos. Experimente con sus propios datos y explore más a fondo las funciones de Aspose.Cells para crear libros de Excel potentes y personalizados.

### Preguntas frecuentes

#### P: ¿Qué es un libro compartido?

R: Un libro compartido es un libro de Excel que varios usuarios pueden utilizar simultáneamente para colaborar en los datos. Cada usuario puede realizar cambios en el libro y otros usuarios verán las actualizaciones en tiempo real.

#### P: ¿Cómo habilitar el uso compartido de un libro de trabajo en Aspose.Cells para .NET?

 R: Para habilitar el uso compartido de un libro de trabajo en Aspose.Cells para .NET, debe configurar el`Shared` propiedad del objeto Libro de trabajo para`true`. Esto permitirá a los usuarios trabajar en el libro simultáneamente.

#### P: ¿Puedo restringir los permisos de usuario en un libro compartido?

R: Sí, puede restringir los permisos de usuario en un libro compartido utilizando las funciones de seguridad de Excel. Puede establecer permisos específicos para cada usuario, como la capacidad de editar, solo lectura, etc.

#### P: ¿Cómo puedo compartir el libro con otros usuarios?

R: Una vez que haya creado el libro compartido, puede compartirlo con otros usuarios enviándoles el archivo de Excel. Otros usuarios podrán abrir el archivo y trabajar en él simultáneamente.

#### P: ¿Se admiten todas las funciones de Excel en un libro compartido?

R: La mayoría de las funciones de Excel son compatibles con un libro compartido. Sin embargo, algunas funciones avanzadas, como macros y complementos, pueden tener limitaciones o restricciones cuando se utilizan en un libro compartido.