---
title: Add Comments to Cells or Shapes in Excel
linktitle: Add Comments to Cells or Shapes in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-comment-annotation/add-comments-to-cells-or-shapes-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Comments
{
    public class AddingComment
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Create directory if it is not already present.
            bool IsExists = System.IO.Directory.Exists(dataDir);
            if (!IsExists)
                System.IO.Directory.CreateDirectory(dataDir);

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Adding a new worksheet to the Workbook object
            int sheetIndex = workbook.Worksheets.Add();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[sheetIndex];

            // Adding a comment to "F5" cell
            int commentIndex = worksheet.Comments.Add("F5");

            // Accessing the newly added comment
            Comment comment = worksheet.Comments[commentIndex];

            // Setting the comment note
            comment.Note = "Hello Aspose!";

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
