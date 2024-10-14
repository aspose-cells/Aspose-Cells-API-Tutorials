---
title: Insert OLE Object into Excel
linktitle: Insert OLE Object into Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-ole-picture-objects/insert-ole-object-into-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.OLE
{
    public class InsertingOLEObjects
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Create directory if it is not already present.
            bool IsExists = System.IO.Directory.Exists(dataDir);
            if (!IsExists)
                System.IO.Directory.CreateDirectory(dataDir);

            // Instantiate a new Workbook.
            Workbook workbook = new Workbook();

            // Get the first worksheet.
            Worksheet sheet = workbook.Worksheets[0];

            // Define a string variable to store the image path.
            string ImageUrl = dataDir + "logo.jpg";

            // Get the picture into the streams.
            FileStream fs = File.OpenRead(ImageUrl);

            // Define a byte array.
            byte[] imageData = new Byte[fs.Length];

            // Obtain the picture into the array of bytes from streams.
            fs.Read(imageData, 0, imageData.Length);

            // Close the stream.
            fs.Close();

            // Get an excel file path in a variable.
            string path = dataDir + "book1.xls";

            // Get the file into the streams.
            fs = File.OpenRead(path);

            // Define an array of bytes.
            byte[] objectData = new Byte[fs.Length];

            // Store the file from streams.
            fs.Read(objectData, 0, objectData.Length);

            // Close the stream.
            fs.Close();

            // Add an Ole object into the worksheet with the image
            // Shown in MS Excel.
            sheet.OleObjects.Add(14, 3, 200, 220, imageData);

            // Set embedded ole object data.
            sheet.OleObjects[0].ObjectData = objectData;

            // Save the excel file
            workbook.Save(dataDir + "output.out.xls");
            // ExEnd:1

        }
    }
}

```
