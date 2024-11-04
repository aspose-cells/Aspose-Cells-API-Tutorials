---
title: Edit Threaded Comments in Worksheet
linktitle: Edit Threaded Comments in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/worksheet-operations/edit-threaded-comments/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class EditThreadedComments
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";
            string outDir = "Your Document Directory";

            Workbook workbook = new Workbook(sourceDir + "ThreadedCommentsSample.xlsx");

            //Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Get Threaded Comment
            ThreadedComment comment = worksheet.Comments.GetThreadedComments("A1")[0];
            comment.Notes = "Updated Comment";

            workbook.Save(outDir + "EditThreadedComments.xlsx");
            // ExEnd:1

            Console.WriteLine("EditThreadedComments executed successfully.");
        }
    }
}

```
