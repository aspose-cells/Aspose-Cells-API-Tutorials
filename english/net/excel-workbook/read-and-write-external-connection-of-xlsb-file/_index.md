---
title: Read And Write External Connection Of XLSB File
linktitle: Read And Write External Connection Of XLSB File
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 130
url: /net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
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