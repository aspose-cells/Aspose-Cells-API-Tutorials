---
title: Read and Write External Connection of XLSB File
linktitle: Read and Write External Connection of XLSB File
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 24
url: /net/workbook-operations/read-and-write-external-connection/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    class ReadAndWriteExternalConnectionOfXLSBFile
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

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
        }
    }
}

```
