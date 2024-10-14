---
title: Opening FODS Files
linktitle: Opening FODS Files
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/data-loading-and-parsing/opening-fods-files/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class OpeningFODSFiles
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();


            // Create a Workbook object and opening the file from its path
            Workbook workbook = new Workbook(sourceDir + "SampleFods.fods");

            Console.WriteLine("FODS file opened successfully!");

            // ExEnd:1
            }
          }
        }
            

```
