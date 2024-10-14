---
title: Replace Tag with Text in TextBox in Excel
linktitle: Replace Tag with Text in TextBox in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-shape-text-modifications/replace-tag-text-textbox-excel/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects
{
    class ReplaceTagWithTextInTextBox
    { 
        //Source directory
        static string sourceDir = RunExamples.Get_SourceDirectory();

        //Output directory
        static string outputDir = RunExamples.Get_OutputDirectory();

        public static void Main()
        {
            // ExStart:1
            Workbook wb = new Workbook(sourceDir + "sampleReplaceTagWithText.xlsx");
            string tag = "TAG_2$TAG_1";
            string replace = "1$ys";

            for (int i = 0; i < tag.Split('$').Length; i++)
            {
                sheetReplace(wb, "<" + tag.Split('$')[i] + ">", replace.Split('$')[i]);
            }
            PdfSaveOptions opts = new PdfSaveOptions();

            wb.Save(outputDir + "outputReplaceTagWithText.pdf", opts);
            // ExEnd:1
            Console.WriteLine("ReplaceTagWithTextInTextBox executed successfully.");
        }
        // ExStart:2
        public static void sheetReplace(Workbook workbook, string sFind, string sReplace)
        {
            string finding = sFind;

            foreach (Worksheet sheet in workbook.Worksheets)
            {
                sheet.Replace(finding, sReplace);

                for (int j = 0; j < 3; j++)
                {

                    if (sheet.PageSetup.GetHeader(j) != null)

                        sheet.PageSetup.SetHeader(j, sheet.PageSetup.GetHeader(j).Replace(finding, sReplace));

                    if (sheet.PageSetup.GetFooter(j) != null)

                        sheet.PageSetup.SetFooter(j, sheet.PageSetup.GetFooter(j).Replace(finding, sReplace));

                }

            }

            foreach (Worksheet sheet in workbook.Worksheets)
            {

                sFind = sFind.Replace("<", "&lt;");
                sFind = sFind.Replace(">", "&gt;");

                foreach (Aspose.Cells.Drawing.TextBox mytextbox in sheet.TextBoxes)
                {


                    if (mytextbox.HtmlText != null)
                    {
                        if (mytextbox.HtmlText.IndexOf(sFind) >= 0)
                        {
                            mytextbox.HtmlText = mytextbox.HtmlText.Replace(sFind, sReplace);
                        }
                    }
                }
            }
        }
        // ExEnd:2
    }
}

```
