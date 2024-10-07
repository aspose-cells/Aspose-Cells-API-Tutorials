---
title: Sort Data in a Column with Custom Sort List in Excel
linktitle: Sort Data in a Column with Custom Sort List in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-data-sorting-exporting/sort-data-in-a-column-with-custom-sort-list-in-excel/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class SortDataInColumnWithCustomSortList 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory"();

            //Output directory
            string outputDir = "Your Document Directory"();

            //Load the source Excel file
            Workbook wb = new Workbook(sourceDir + "sampleSortData_CustomSortList.xlsx");

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Specify cell area - sort from A1 to A40
            CellArea ca = CellArea.CreateCellArea("A1", "A40");

            //Create Custom Sort list
            string[] customSortList = new string[] { "USA,US", "Brazil,BR", "China,CN", "Russia,RU", "Canada,CA" };

            //Add Key for Column A, Sort it in Ascending Order with Custom Sort List
            wb.DataSorter.AddKey(0, SortOrder.Ascending, customSortList);
            wb.DataSorter.Sort(ws.Cells, ca);

            //Save the output Excel file
            wb.Save(outputDir + "outputSortData_CustomSortList.xlsx");

            Console.WriteLine("SortDataInColumnWithCustomSortList executed successfully.\r\n");
        }
    }
}
```
