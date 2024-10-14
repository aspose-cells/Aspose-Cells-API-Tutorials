---
title: Reference Picture Cell in Excel
linktitle: Reference Picture Cell in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/excel-ole-picture-objects/reference-picture-cell-excel/
---

## Complete Source Code
```csharp
using System.IO;
using System;
using Aspose.Cells;
using Aspose.Cells.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Pictures
{
    public class PictureCellReference
    {
        public static void Run()
        {
            try
            {
                // ExStart:1
                // The path to the documents directory.
                string dataDir = "Your Document Directory";

                // Instantiate a new Workbook
                Workbook workbook = new Workbook();
                // Get the first worksheet's cells collection
                Cells cells = workbook.Worksheets[0].Cells;

                // Add string values to the cells
                cells["A1"].PutValue("A1");
                cells["C10"].PutValue("C10");

                // Add a blank picture to the D1 cell
                Picture pic = workbook.Worksheets[0].Shapes.AddPicture(0, 3, 10, 6, null);

                // Specify the formula that refers to the source range of cells
                pic.Formula = "A1:C10";

                // Update the shapes selected value in the worksheet
                workbook.Worksheets[0].Shapes.UpdateSelectedValue();

                // Save the Excel file.
                workbook.Save(dataDir + "output.out.xls");
                // ExEnd:1
            }
            catch (Exception ex)
            {
                Console.WriteLine(ex.Message);
            }
        }
    }
}

```
