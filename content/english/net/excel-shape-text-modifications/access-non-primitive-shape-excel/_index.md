---
title: Access Non-Primitive Shape in Excel
linktitle: Access Non-Primitive Shape in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/excel-shape-text-modifications/access-non-primitive-shape-excel/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Collections;
using System;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects
{
    public class AccessNonPrimitiveShape
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            Workbook workbook = new Workbook(dataDir + "NonPrimitiveShape.xlsx");

            Worksheet worksheet = workbook.Worksheets[0];

            // Accessing the user defined shape
            Shape shape = worksheet.Shapes[0];

            if (shape.AutoShapeType == AutoShapeType.NotPrimitive)
            {
                // Access shape's data
                ShapePathCollection shapePathCollection = shape.Paths;

                // Access information of indvidual path
                foreach (ShapePath shapePath in shapePathCollection)
                {
                    // Access path segment list
                    ShapeSegmentPathCollection pathSegments = shapePath.PathSegementList;

                    // Access individual path segment
                    foreach (ShapeSegmentPath pathSegment in pathSegments)
                    {
                        // Gets the points in path segment
                        ShapePathPointCollection segmentPoints = pathSegment.Points;

                        foreach (ShapePathPoint pathPoint in segmentPoints)
                        {
                            Console.WriteLine("X: " + pathPoint.X + ", Y: " + pathPoint.Y);
                        }
                    }
                }
            }
            // ExEnd:1
        }
    }
}
```
