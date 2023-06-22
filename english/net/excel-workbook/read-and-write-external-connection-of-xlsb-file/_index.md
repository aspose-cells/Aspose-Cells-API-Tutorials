---
title: Read And Write External Connection Of XLSB File
linktitle: Read And Write External Connection Of XLSB File
second_title: Aspose.Cells for .NET API Reference
description: Learn how to read and modify the external connections of an XLSB file using Aspose.Cells for .NET.
type: docs
weight: 130
url: /net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Reading and writing external connections to an XLSB file is essential for manipulating data from external sources in your Excel workbooks. With Aspose.Cells for .NET you can easily read and write external connections using the following steps:

## Step 1: Specify source directory and output directory

First, you must specify the source directory where the XLSB file containing the external connection is located, as well as the output directory where you want to save the modified file. Here's how to do it using Aspose.Cells:

```csharp
// source directory
string sourceDir = RunExamples.Get_SourceDirectory();

// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

## Step 2: Load the source Excel XLSB file

Next, you need to load the source Excel XLSB file on which you want to perform external connection read and write operations. Here is a sample code:

```csharp
// Load the source Excel XLSB file
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Step 3: Read and modify the external connection

After loading the file, you can access the first external connection which is actually a database connection. You can read and modify various properties of the external connection. Here's how:

```csharp
// Read the first external connection which is a database connection
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Display the database connection name, command, and connection information
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Modify the name of the connection
dbCon.Name = "NewCustomer";
```

## Step 4: Save the output Excel XLSB file

Once you have made the necessary changes, you can save the modified Excel XLSB file to the specified output directory. Here's how to do it:

```csharp
// Save the output Excel XLSB file
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Sample source code for Read And Write External Connection Of XLSB File using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
//Output directory
string outputDir = RunExamples.Get_OutputDirectory();
//Load the source Excel Xlsb file
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Read the first external connection which is actually a DB-Connection
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Print the Name, Command and Connection Info of the DB-Connection
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Modify the Connection Name
dbCon.Name = "NewCust";
//Save the Excel Xlsb file
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Conclusion

Reading and writing external connections to an XLSB file allows you to manipulate data from external sources in your Excel workbooks. With Aspose.Cells for .NET, you can easily access external connections, read and modify connection information, and save changes. Experiment with your own XLSB files and harness the power of external connections in your Excel applications.

### FAQs

#### Q: What is an external connection in an XLSB file?
    
	 A: An external connection in an XLSB file refers to a connection established with an external data source such as a database. It allows you to import data from this external source into the Excel workbook.

#### Q: Can I have multiple external connections in an XLSB file?
     
	 A: Yes, you can have multiple external connections in an XLSB file. You can manage them individually by accessing each connection object.

#### Q: How can I read the details of an external connection in an XLSB file with Aspose.Cells?
     
	 A: You can use the functionality provided by Aspose.Cells to access properties of an external connection, such as connection name, associated command, and connection information.

#### Q: Is it possible to modify an external connection in an XLSB file with Aspose.Cells?
     
	 A: Yes, you can modify the properties of an external connection, such as the connection name, to meet your specific needs. Aspose.Cells provides methods to make these changes.

#### Q: How can I save changes made to an external connection to an XLSB file with Aspose.Cells?
     
	 A: Once you have made the necessary changes to an external connection, you can simply save the modified Excel XLSB file using the appropriate method provided by Aspose.Cells.
