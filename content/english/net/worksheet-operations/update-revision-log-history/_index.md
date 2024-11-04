---
title: Update Revision Log History in Shared Workbook
linktitle: Update Revision Log History in Shared Workbook
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 26
url: /net/worksheet-operations/update-revision-log-history/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class UpdateDaysPreservingHistoryOfRevisionLogsInSharedWorkbook 
    {
        public static void Run()
        {
            //Output directory
            string outputDir = "Your Document Directory";

            //Create empty workbook
            Workbook wb = new Workbook();

            //Share the workbook
            wb.Settings.Shared = true;

            //Update DaysPreservingHistory of RevisionLogs
            wb.Worksheets.RevisionLogs.DaysPreservingHistory = 7;

            //Save the workbook
            wb.Save(outputDir + "outputShared_DaysPreservingHistory.xlsx");

            Console.WriteLine("UpdateDaysPreservingHistoryOfRevisionLogsInSharedWorkbook executed successfully.");
        }
    }
}

```
