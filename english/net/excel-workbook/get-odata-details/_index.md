---
title: Get Odata Details
linktitle: Get Odata Details
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 110
url: /net/excel-workbook/get-odata-details/
---
### Sample source code for Get Odata Details using Aspose.Cells for .NET 
```csharp
            // source directory
            string SourceDir = RunExamples.Get_SourceDirectory();
            Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
            PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
            foreach (PowerQueryFormula PQF in PQFcoll)
            {
                Console.WriteLine("Connection Name: " + PQF.Name);
                PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
                foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
                {
                    Console.WriteLine("Name: " + PQFI.Name);
                    Console.WriteLine("Value: " + PQFI.Value);
                }
            }
            Console.WriteLine("GetOdataDetails executed successfully.");
```