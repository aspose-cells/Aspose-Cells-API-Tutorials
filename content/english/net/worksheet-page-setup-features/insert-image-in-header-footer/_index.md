---
title: Insert Image in Header Footer of Worksheet
linktitle: Insert Image in Header Footer of Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/worksheet-page-setup-features/insert-image-in-header-footer/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class InsertImageInHeaderFooter
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a Workbook object
            Workbook workbook = new Workbook();

            // Creating a string variable to store the url of the logo/picture
            string logo_url = dataDir + "aspose-logo.jpg";

            // Declaring a FileStream object
            FileStream inFile;

            // Declaring a byte array
            byte[] binaryData;

            // Creating the instance of the FileStream object to open the logo/picture in the stream
            inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);

            // Instantiating the byte array of FileStream object's size
            binaryData = new Byte[inFile.Length];

            // Reads a block of bytes from the stream and writes data in a given buffer of byte array.
            long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);

            // Creating a PageSetup object to get the page settings of the first worksheet of the workbook
            PageSetup pageSetup = workbook.Worksheets[0].PageSetup;

            // Setting the logo/picture in the central section of the page header
            pageSetup.SetHeaderPicture(1, binaryData);

            // Setting the script for the logo/picture
            pageSetup.SetHeader(1, "&G");

            // Setting the Sheet's name in the right section of the page header with the script
            pageSetup.SetHeader(2, "&A");

            // Saving the workbook
            workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");

            //Closing the FileStream object
            inFile.Close();       
            // ExEnd:1
        }
    }
}

```
