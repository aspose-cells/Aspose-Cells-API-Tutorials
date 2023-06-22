---
title: Update Power Query Formula Item
linktitle: Update Power Query Formula Item
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 160
url: /net/excel-workbook/update-power-query-formula-item/
---
### Sample source code for Update Power Query Formula Item using Aspose.Cells for .NET 
```csharp
            // Working directories
            string SourceDir = RunExamples.Get_SourceDirectory();
            string outputDir = RunExamples.Get_OutputDirectory();
            Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
            DataMashup mashupData = workbook.DataMashup;
            foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
            {
                foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
                {
                    if (item.Name == "Source")
                    {
                        item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
                    }
                }
            }
            // Save the output workbook.
            workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
            Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```