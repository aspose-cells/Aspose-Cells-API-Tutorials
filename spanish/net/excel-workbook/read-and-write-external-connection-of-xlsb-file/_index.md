---
title: Leer y escribir conexión externa de archivo XLSB
linktitle: Leer y escribir conexión externa de archivo XLSB
second_title: Referencia de API de Aspose.Cells para .NET
description: Aprenda a leer y modificar las conexiones externas de un archivo XLSB utilizando Aspose.Cells para .NET.
type: docs
weight: 130
url: /es/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Leer y escribir conexiones externas en un archivo XLSB es esencial para manipular datos de fuentes externas en sus libros de Excel. Con Aspose.Cells para .NET puede leer y escribir fácilmente conexiones externas siguiendo los siguientes pasos:

## Paso 1: especificar el directorio de origen y el directorio de salida

Primero, debe especificar el directorio de origen donde se encuentra el archivo XLSB que contiene la conexión externa, así como el directorio de salida donde desea guardar el archivo modificado. He aquí cómo hacerlo usando Aspose.Cells:

```csharp
// directorio fuente
string sourceDir = RunExamples.Get_SourceDirectory();

// Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
```

## Paso 2: Cargue el archivo Excel XLSB de origen

A continuación, debe cargar el archivo Excel XLSB de origen en el que desea realizar operaciones de lectura y escritura de conexión externa. Aquí hay un código de muestra:

```csharp
// Cargue el archivo Excel XLSB de origen
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Paso 3: Leer y modificar la conexión externa

Después de cargar el archivo, puede acceder a la primera conexión externa que en realidad es una conexión de base de datos. Puede leer y modificar varias propiedades de la conexión externa. Así es cómo:

```csharp
// Lea la primera conexión externa que es una conexión de base de datos
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Mostrar el nombre de conexión de la base de datos, el comando y la información de conexión
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Modificar el nombre de la conexión.
dbCon.Name = "NewCustomer";
```

## Paso 4: guarde el archivo Excel XLSB de salida

Una vez que haya realizado los cambios necesarios, puede guardar el archivo XLSB de Excel modificado en el directorio de salida especificado. Aquí está cómo hacerlo:

```csharp
// Guarde el archivo Excel XLSB de salida
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Código fuente de muestra para la conexión externa de lectura y escritura del archivo XLSB usando Aspose.Cells para .NET 
```csharp
//directorio de origen
string sourceDir = RunExamples.Get_SourceDirectory();
//Directorio de salida
string outputDir = RunExamples.Get_OutputDirectory();
//Cargue el archivo fuente Excel Xlsb
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Lea la primera conexión externa que en realidad es una conexión DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Imprima el nombre, el comando y la información de conexión de la conexión DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Modificar el nombre de la conexión
dbCon.Name = "NewCust";
//Guarde el archivo Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Conclusión

Leer y escribir conexiones externas en un archivo XLSB le permite manipular datos de fuentes externas en sus libros de Excel. Con Aspose.Cells para .NET, puede acceder fácilmente a conexiones externas, leer y modificar información de conexión y guardar cambios. Experimente con sus propios archivos XLSB y aproveche el poder de las conexiones externas en sus aplicaciones de Excel.

### preguntas frecuentes

#### P: ¿Qué es una conexión externa en un archivo XLSB?
    
R: Una conexión externa en un archivo XLSB hace referencia a una conexión establecida con una fuente de datos externa, como una base de datos. Le permite importar datos desde esta fuente externa al libro de Excel.

#### P: ¿Puedo tener varias conexiones externas en un archivo XLSB?
     
R: Sí, puede tener varias conexiones externas en un archivo XLSB. Puede administrarlos individualmente accediendo a cada objeto de conexión.

#### P: ¿Cómo puedo leer los detalles de una conexión externa en un archivo XLSB con Aspose.Cells?
     
R: Puede usar la funcionalidad proporcionada por Aspose.Cells para acceder a las propiedades de una conexión externa, como el nombre de la conexión, el comando asociado y la información de la conexión.

#### P: ¿Es posible modificar una conexión externa en un archivo XLSB con Aspose.Cells?
     
R: Sí, puede modificar las propiedades de una conexión externa, como el nombre de la conexión, para satisfacer sus necesidades específicas. Aspose.Cells proporciona métodos para realizar estos cambios.

#### P: ¿Cómo puedo guardar los cambios realizados en una conexión externa en un archivo XLSB con Aspose.Cells?
     
R: Una vez que haya realizado los cambios necesarios en una conexión externa, simplemente puede guardar el archivo XLSB de Excel modificado utilizando el método adecuado proporcionado por Aspose.Cells.