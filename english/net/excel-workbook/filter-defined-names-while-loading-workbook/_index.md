---
title: Filter Defined Names While Loading Workbook
linktitle: Filter Defined Names While Loading Workbook
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 100
url: /net/excel-workbook/filter-defined-names-while-loading-workbook/
---
### Sample source code for Filter Defined Names While Loading Workbook using Aspose.Cells for .NET 
```csharp
            //Specify the load options
            LoadOptions opts = new LoadOptions();
            //We do not want to load defined names
            opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
            //Load the workbook
            Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
            //Save the output Excel file, it will break the formula in C1
            wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
            Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```