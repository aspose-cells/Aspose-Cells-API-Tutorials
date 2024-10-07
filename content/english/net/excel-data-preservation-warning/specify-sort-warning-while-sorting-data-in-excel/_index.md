---
title: Specify Sort Warning While Sorting Data in Excel
linktitle: Specify Sort Warning While Sorting Data in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-data-preservation-warning/specify-sort-warning-while-sorting-data-in-excel/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class SpecifyingSortWarningWhileSortingData
    {
        public static void Run()
        {
            //ExStart:SpecifyingSortWarningWhileSortingData

            //The path to the documents directory.
            string dataDir = "Your Document Directory";

            //Create workbook.
            Workbook workbook = new Workbook(dataDir + "sampleSortAsNumber.xlsx");

            //Access first worksheet.
            Worksheet worksheet = workbook.Worksheets[0];

            //Create your cell area.
            CellArea ca = CellArea.CreateCellArea("A1", "A20");

            //Create your sorter.
            DataSorter sorter = workbook.DataSorter;

            //Find the index, since we want to sort by column A, so we should know the index for sorter.
            int idx = CellsHelper.ColumnNameToIndex("A");

            //Add key in sorter, it will sort in Ascending order.
            sorter.AddKey(idx, SortOrder.Ascending);
            sorter.SortAsNumber = true;

            //Perform sort.
            sorter.Sort(worksheet.Cells, ca);

            //Save the output workbook.
            workbook.Save(dataDir + "outputSortAsNumber.xlsx");

            //ExEnd:SpecifyingSortWarningWhileSortingData
        }
    }
}
```
