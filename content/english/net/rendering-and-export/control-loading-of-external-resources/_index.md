---
title: Control External Resources in Excel to PDF in Aspose.Cells
linktitle: Control External Resources in Excel to PDF in Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/rendering-and-export/control-loading-of-external-resources/
---

## Complete Source Code
```csharp
using System.IO;

using System.Drawing;
using System.Drawing.Imaging;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using Aspose.Cells.Rendering;
using System;

namespace Aspose.Cells.Examples.CSharp.Rendering
{
    public class ControlLoadingOfExternalResourcesInExcelToPDF
    {
        // ExStart:1
        //Implement IStreamProvider
        class MyStreamProvider : IStreamProvider
        {
            public void CloseStream(StreamProviderOptions options)
            {
                System.Diagnostics.Debug.WriteLine("-----Close Stream-----");
            }

            public void InitStream(StreamProviderOptions options)
            {
                string sourceDir = "Your Document Directory";

                System.Diagnostics.Debug.WriteLine("-----Init Stream-----");

                //Read the new image in a memory stream and assign it to Stream property
                byte[] bts = File.ReadAllBytes(sourceDir + "newPdfSaveOptions_StreamProvider.png");
                MemoryStream ms = new MemoryStream(bts);
                options.Stream = ms;
            }
        }

        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load source Excel file containing external image
            Workbook wb = new Workbook(sourceDir + "samplePdfSaveOptions_StreamProvider.xlsx");

            //Specify Pdf Save Options - Stream Provider
            PdfSaveOptions opts = new PdfSaveOptions();
            opts.OnePagePerSheet = true;

            wb.Settings.StreamProvider = new MyStreamProvider();

            //Save the workbook to Pdf
            wb.Save(outputDir + "outputPdfSaveOptions_StreamProvider.pdf", opts);

            Console.WriteLine("ControlLoadingOfExternalResourcesInExcelToPDF executed successfully.\r\n");
        }
        // ExEnd:1
    }

}

```
