---
title: Create List Object in Excel using Aspose.Cells
linktitle: Create List Object in Excel using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/tables-and-lists/creating-list-object/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Tables
{
    public class CreatingListObject
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Create a Workbook object.
            // Open a template excel file.
            Workbook workbook = new Workbook(dataDir + "book1.xls");

            // Get the List objects collection in the first worksheet.
            Aspose.Cells.Tables.ListObjectCollection listObjects = workbook.Worksheets[0].ListObjects;

            // Add a List based on the data source range with headers on.
            listObjects.Add(1, 1, 7, 5, true);

            // Show the total row for the List.
            listObjects[0].ShowTotals = true;

            // Calculate the total of the last (5th ) list column.

            listObjects[0].ListColumns[4].TotalsCalculation = Aspose.Cells.Tables.TotalsCalculation.Sum;

            // Save the excel file.
            workbook.Save(dataDir + "output.xls");
            // ExEnd:1

        }
    }
}

```
