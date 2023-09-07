---
title: Agregar firma digital a un archivo de Excel ya firmado
linktitle: Agregar firma digital a un archivo de Excel ya firmado
second_title: Referencia de API de Aspose.Cells para .NET
description: Agregue fácilmente firmas digitales a archivos de Excel existentes con Aspose.Cells para .NET.
type: docs
weight: 30
url: /es/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
En esta guía paso a paso, explicaremos el código fuente de C# provisto que le permitirá agregar una firma digital a un archivo de Excel ya firmado usando Aspose.Cells para .NET. Siga los pasos a continuación para agregar una nueva firma digital a un archivo de Excel existente.

## Paso 1: Establecer directorios de origen y salida

```csharp
// directorio fuente
string sourceDir = RunExamples.Get_SourceDirectory();

// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

En este primer paso, definimos los directorios de origen y salida que se utilizarán para cargar el archivo de Excel existente y guardar el archivo con la nueva firma digital.

## Paso 2: Cargue el archivo de Excel existente

```csharp
// Cargue el libro de Excel ya firmado
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Aquí cargamos el archivo de Excel ya firmado usando el`Workbook` clase de Aspose.Cells.

## Paso 3: Crear la colección de firmas digitales

```csharp
// Crear la colección de firmas digitales
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Creamos una nueva colección de firmas digitales utilizando el`DigitalSignatureCollection` clase.

## Paso 4: Crear un nuevo certificado

```csharp
// Crear un nuevo certificado
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Aquí creamos un nuevo certificado a partir del archivo y la contraseña proporcionados.

## Paso 5: agregue una nueva firma digital a la colección

```csharp
// Crear una nueva firma digital
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Añade la firma digital a la colección.
dsCollection.Add(signature);
```

 Creamos una nueva firma digital usando el`DigitalSignature` class y agréguelo a la colección de firmas digitales.

## Paso 6: agregue la colección de firmas digitales al libro de trabajo

```csharp
//Agregar la colección de firmas digitales al libro de trabajo
workbook.AddDigitalSignature(dsCollection);
```

 Agregamos la colección de firmas digitales al libro de Excel existente usando el`AddDigitalSignature()` método.

## Paso 7: Guarde y cierre el libro de trabajo

```csharp
// Guarde el libro y ciérrelo.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Guardamos el libro de trabajo con la nueva firma digital en el directorio de salida especificado, luego lo cerramos y liberamos los recursos asociados.

### Ejemplo de código fuente para Agregar firma digital a un archivo de Excel ya firmado usando Aspose.Cells para .NET 
```csharp
//directorio de origen
string sourceDir = RunExamples.Get_SourceDirectory();
//Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
//Archivo de certificado y su contraseña
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Cargue el libro de trabajo que ya está firmado digitalmente para agregar una nueva firma digital
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Crear la colección de firmas digitales
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Crear nuevo certificado
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Cree una nueva firma digital y agréguela a la colección de firmas digitales
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Agregue una colección de firmas digitales dentro del libro de trabajo
workbook.AddDigitalSignature(dsCollection);
//Guarde el libro y deséchelo.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Conclusión

¡Felicidades! Ahora ha aprendido cómo agregar una firma digital a un archivo de Excel ya firmado usando Aspose.Cells para .NET. Las firmas digitales agregan una capa adicional de seguridad a sus archivos de Excel, lo que garantiza su autenticidad e integridad.

### Preguntas frecuentes

#### P: ¿Qué es Aspose.Cells para .NET?

R: Aspose.Cells para .NET es una potente biblioteca de clases que permite a los desarrolladores de .NET crear, modificar, convertir y manipular archivos de Excel con facilidad.

#### P: ¿Qué es una firma digital en un archivo de Excel?

R: Una firma digital en un archivo de Excel es una marca electrónica que garantiza la autenticidad, integridad y origen del documento. Se utiliza para verificar que el archivo no ha sido modificado desde que se firmó y proviene de una fuente confiable.

#### P: ¿Cuáles son los beneficios de agregar una firma digital a un archivo de Excel?

R: Agregar una firma digital a un archivo de Excel brinda varios beneficios, incluida la protección contra cambios no autorizados, asegurando la integridad de los datos, autenticando al autor del documento y brindando confianza en la información que contiene.

#### P: ¿Puedo agregar varias firmas digitales a un archivo de Excel?

R: Sí, Aspose.Cells le permite agregar varias firmas digitales a un archivo de Excel. Puede crear una colección de firmas digitales y agregarlas al archivo en una sola operación.

#### P: ¿Cuáles son los requisitos para agregar una firma digital a un archivo de Excel?

R: Para agregar una firma digital a un archivo de Excel, necesita un certificado digital válido que se utilizará para firmar el documento. Asegúrese de tener el certificado y la contraseña correctos antes de agregar la firma digital.