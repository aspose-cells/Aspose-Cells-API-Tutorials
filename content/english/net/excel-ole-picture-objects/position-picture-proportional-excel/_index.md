---
title: Position Picture (Proportional) in Excel
linktitle: Position Picture (Proportional) in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/excel-ole-picture-objects/position-picture-proportional-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Pictures.PositioningPictures
{
    public class ProportionalPositioning
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

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Adding a new worksheet to the Workbook object
            int sheetIndex = workbook.Worksheets.Add();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[sheetIndex];

            // Adding a picture at the location of a cell whose row and column indices
            // Are 5 in the worksheet. It is "F6" cell
            int pictureIndex = worksheet.Pictures.Add(5, 5, dataDir + "logo.jpg");

            // Accessing the newly added picture
            Aspose.Cells.Drawing.Picture picture = worksheet.Pictures[pictureIndex];

            // Positioning the picture proportional to row height and colum width
            picture.UpperDeltaX = 200;
            picture.UpperDeltaY = 200;

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
