---
title: Stop Conversion or Loading using Interrupt Monitor
linktitle: Stop Conversion or Loading using Interrupt Monitor
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 26
url: /net/workbook-operations/stop-conversion-or-loading/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using System.IO;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    class StopConversionOrLoadingUsingInterruptMonitor
    {
        //Output directory
        static string outputDir = "Your Document Directory";

        //Create InterruptMonitor object
        InterruptMonitor im = new InterruptMonitor();

        //This function will create workbook and convert it to Pdf format
        void CreateWorkbookAndConvertItToPdfFormat()
        {
            //Create a workbook object
            Workbook wb = new Workbook();

            //Assign it InterruptMonitor object
            wb.InterruptMonitor = im;

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Access cell J1000000 and add some text inside it.
            Cell cell = ws.Cells["J1000000"];
            cell.PutValue("This is text.");

            try
            {
                //Save the workbook to Pdf format
                wb.Save(outputDir + "output_InterruptMonitor.pdf");
            }
            catch (Aspose.Cells.CellsException ex)
            {
                Console.WriteLine("Process Interrupted - Message: " + ex.Message);
            }

        }

        //This function will interrupt the conversion process after 10s
        void WaitForWhileAndThenInterrupt()
        {
            Thread.Sleep(1000 * 10);
            im.Interrupt();
        }

        public void TestRun()
        {
            ThreadStart ts1 = new ThreadStart(this.CreateWorkbookAndConvertItToPdfFormat);
            Thread t1 = new Thread(ts1);
            t1.Start();

            ThreadStart ts2 = new ThreadStart(this.WaitForWhileAndThenInterrupt);
            Thread t2 = new Thread(ts2);
            t2.Start();

            t1.Join();
            t2.Join();
        }

      
        public static void Run()
        {
            new StopConversionOrLoadingUsingInterruptMonitor().TestRun();

            Console.WriteLine("StopConversionOrLoadingUsingInterruptMonitor executed successfully.");
        }
    }

}

```
