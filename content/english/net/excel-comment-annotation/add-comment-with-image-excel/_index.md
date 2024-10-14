---
title: Add a Comment with Image in Excel
linktitle: Add a Comment with Image in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-comment-annotation/add-comment-with-image-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Comments
{
    public class AddImageToComment
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

            // Instantiate a Workbook
            Workbook workbook = new Workbook();

            // Get a reference of comments collection with the first sheet
            CommentCollection comments = workbook.Worksheets[0].Comments;

            // Add a comment to cell A1
            int commentIndex = comments.Add(0, 0);
            Comment comment = comments[commentIndex];
            comment.Note = "First note.";
            comment.Font.Name = "Times New Roman";

            // Load an image into stream
            Bitmap bmp = new Bitmap(dataDir + "logo.jpg");
            MemoryStream ms = new MemoryStream();
            bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Png);

            // Set image data to the shape associated with the comment
            comment.CommentShape.Fill.ImageData = ms.ToArray();

            // Save the workbook
            workbook.Save(dataDir + "book1.out.xlsx", Aspose.Cells.SaveFormat.Xlsx);
            // ExEnd:1

            
        }
    }
}

```
