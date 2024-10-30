---
title: Use Formula Parameter in Smart Marker Field Aspose.Cells
linktitle: Use Formula Parameter in Smart Marker Field Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/smart-markers-dynamic-data/formula-parameter-smart-marker/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Data;

namespace Aspose.Cells.Examples.CSharp.SmartMarkers
{
    public class UsingFormulaParameterInSmartMarkerField
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Create a datatable and add column named TestFormula
            DataTable dt = new DataTable();
            dt.Columns.Add("TestFormula");

            //Create first row with formula (which basically concatenates three strings)
            DataRow dr = dt.NewRow();
            dr["TestFormula"] = "=\"01-This \" & \"is \" & \"concatenation\"";
            dt.Rows.Add(dr);

            //Create second row like above
            dr = dt.NewRow();
            dr["TestFormula"] = "=\"02-This \" & \"is \" & \"concatenation\"";
            dt.Rows.Add(dr);

            //Create third row like above
            dr = dt.NewRow();
            dr["TestFormula"] = "=\"03-This \" & \"is \" & \"concatenation\"";
            dt.Rows.Add(dr);

            //Create fourth row like above
            dr = dt.NewRow();
            dr["TestFormula"] = "=\"04-This \" & \"is \" & \"concatenation\"";
            dt.Rows.Add(dr);

            //Create fifth row like above
            dr = dt.NewRow();
            dr["TestFormula"] = "=\"05-This \" & \"is \" & \"concatenation\"";
            dt.Rows.Add(dr);

            //Set the name of the data table
            dt.TableName = "MyDataSource";

            //Create a workbook
            Workbook wb = new Workbook();

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Put the smart marker field with formula parameter in cell A1
            ws.Cells["A1"].PutValue("&=MyDataSource.TestFormula(Formula)");

            //Create workbook designer, set data source and process it
            WorkbookDesigner wd = new WorkbookDesigner(wb);
            wd.SetDataSource(dt);
            wd.Process();

            //Save the workbook in xlsx format
            wb.Save(outputDir + "outputUsingFormulaParameterInSmartMarkerField.xlsx");

            Console.WriteLine("UsingFormulaParameterInSmartMarkerField executed successfully.\r\n");
        }
    }
}
```
