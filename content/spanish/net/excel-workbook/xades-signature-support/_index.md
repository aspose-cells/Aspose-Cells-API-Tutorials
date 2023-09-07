---
title: Soporte de la firma Xades
linktitle: Soporte de la firma Xades
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a agregar una firma Xades a un archivo de Excel usando Aspose.Cells para .NET.
type: docs
weight: 190
url: /es/net/excel-workbook/xades-signature-support/
---
En este artículo, lo guiaremos paso a paso para explicar el código fuente de C# a continuación, que trata sobre la compatibilidad con la firma Xades utilizando la biblioteca Aspose.Cells para .NET. Descubrirá cómo usar esta biblioteca para agregar una firma digital Xades a un archivo de Excel. También le proporcionaremos una descripción general del proceso de firma y su ejecución. Siga los pasos a continuación para obtener resultados concluyentes.

## Paso 1: definir los directorios de origen y salida
Para comenzar, necesitamos definir los directorios fuente y de salida en nuestro código. Estos directorios indican dónde se encuentran los archivos de origen y dónde se guardará el archivo de salida. Aquí está el código correspondiente:

```csharp
// directorio de origen
string sourceDir = RunExamples.Get_SourceDirectory();
// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

Asegúrese de adaptar las rutas de directorio según sea necesario.

## Paso 2: Cargar el libro de Excel
El siguiente paso es cargar el libro de Excel en el que queremos añadir la firma digital Xades. Aquí está el código para cargar el libro de trabajo:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Asegúrese de especificar correctamente el nombre del archivo de origen en el código.

## Paso 3: Configuración de la firma digital
Ahora configuraremos la firma digital de Xades proporcionando la información necesaria. Debemos especificar el archivo PFX que contiene el certificado digital, así como la contraseña asociada. Aquí está el código correspondiente:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Asegúrese de reemplazar "pfxPassword" con su contraseña real y "pfxFile" con la ruta al archivo PFX.

## Paso 4: Agregar la firma digital
Ahora que hemos configurado la firma digital, podemos agregarla al libro de Excel. Aquí está el código correspondiente:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Este paso agrega la firma digital Xades al libro de Excel.

## Paso 5: Guardar el libro de trabajo con la firma
Finalmente, guardamos el libro de Excel con la firma digital añadida. Aquí está el código correspondiente:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Asegúrese de adaptar el nombre del archivo de salida según sus necesidades.

### Ejemplo de código fuente para Xades Signature Support usando Aspose.Cells para .NET 
```csharp
//directorio de origen
string sourceDir = RunExamples.Get_SourceDirectory();
//Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Conclusión
¡Felicidades! Ha aprendido a usar la biblioteca Aspose.Cells para .NET para agregar una firma digital Xades a un archivo de Excel. Siguiendo los pasos proporcionados en este artículo, podrá implementar esta funcionalidad en sus propios proyectos. Siéntase libre de experimentar más con la biblioteca y descubra otras características poderosas que ofrece.

### preguntas frecuentes

#### P: ¿Qué es Xades?

R: Xades es un estándar de firma electrónica avanzada que se utiliza para garantizar la integridad y autenticidad de los documentos digitales.

#### P: ¿Puedo usar otros tipos de firmas digitales con Aspose.Cells?

R: Sí, Aspose.Cells también admite otros tipos de firmas digitales, como las firmas XMLDSig y las firmas PKCS#7.

#### P: ¿Puedo aplicar una firma a otros tipos de archivos que no sean archivos de Excel?
 
R: Sí, Aspose.Cells también permite aplicar firmas digitales a otros tipos de archivos compatibles, como archivos de Word, PDF y PowerPoint.