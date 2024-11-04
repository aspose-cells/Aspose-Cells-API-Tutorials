---
title: Read Threaded Comments in Worksheet
linktitle: Read Threaded Comments in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 22
url: /net/worksheet-operations/read-threaded-comments/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class ReadThreadedComments
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            Workbook workbook = new Workbook(sourceDir + "ThreadedCommentsSample.xlsx");

            //Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Get Threaded Comments
            ThreadedCommentCollection threadedComments = worksheet.Comments.GetThreadedComments("A1");

            foreach (ThreadedComment comment in threadedComments)
            {
                Console.WriteLine("Comment: " + comment.Notes);
                Console.WriteLine("Author: " + comment.Author.Name);
            }
            // ExEnd:1

            Console.WriteLine("ReadThreadedComments executed successfully.");
        }
    }
}

```
