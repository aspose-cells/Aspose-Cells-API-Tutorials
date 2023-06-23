---
title: Create Shared Workbook
linktitle: Create Shared Workbook
second_title: Aspose.Cells for .NET API Reference
description: Create an Excel shared workbook with Aspose.Cells for .NET to enable concurrent data collaboration.
type: docs
weight: 70
url: /net/excel-workbook/create-shared-workbook/
---
In this tutorial, we will walk you through the provided C# source code that will allow you to create a shared workbook using Aspose.Cells for .NET. Follow the steps below to perform this operation.

## Step 1: Set output directory

```csharp
// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

In this first step, we define the output directory where the shared workbook will be saved.

## Step 2: Create a Workbook Object

```csharp
// Create a Workbook object
Workbook wb = new Workbook();
```

We are creating a new Workbook object that will represent our Excel workbook.

## Step 3: Enable Workbook Sharing

```csharp
// Share the workbook
wb.Settings.Shared = true;
```

We enable the workbook's sharing feature by setting the `Shared` property of the Workbook object to `true`.

## Step 4: Save the shared workbook

```csharp
// Save the shared workbook
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

We save the shared workbook by specifying the path and name of the output file.

### Sample source code for Create Shared Workbook using Aspose.Cells for .NET 
```csharp
//Output directory
string outputDir = RunExamples.Get_OutputDirectory();
//Create Workbook object
Workbook wb = new Workbook();
//Share the Workbook
wb.Settings.Shared = true;
//Save the Shared Workbook
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Conclusion

Congratulation ! You learned how to create a shared workbook using Aspose.Cells for .NET. The shared workbook can be used by multiple users simultaneously to collaborate on data. Experiment with your own data and further explore the features of Aspose.Cells to create powerful and personalized Excel workbooks.

### FAQs

#### Q: What is a shared workbook?

A: A shared workbook is an Excel workbook that can be used simultaneously by multiple users to collaborate on data. Each user can make changes to the workbook and other users will see updates in real time.

#### Q: How to enable sharing of a workbook in Aspose.Cells for .NET?

A: To enable sharing of a workbook in Aspose.Cells for .NET, you must set the `Shared` property of the Workbook object to `true`. This will allow users to work on the workbook simultaneously.

#### Q: Can I restrict user permissions in a shared workbook?

A: Yes, you can restrict user permissions in a shared workbook using Excel's security features. You can set specific permissions for each user, such as the ability to edit, read only, etc.

#### Q: How can I share the workbook with other users?

A: Once you have created the shared workbook, you can share it with other users by sending them the Excel file. Other users will be able to open the file and work on it simultaneously.

#### Q: Are all Excel features supported in a shared workbook?

A: Most Excel features are supported in a shared workbook. However, some advanced features, such as macros and add-ins, may have limitations or restrictions when used in a shared workbook.
