---
title: Password Protect Or Unprotect Shared Workbook
linktitle: Password Protect Or Unprotect Shared Workbook
second_title: Aspose.Cells for .NET API Reference
description: Learn how to password protect or unprotect a shared workbook using Aspose.Cells for .NET.
type: docs
weight: 120
url: /net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Protecting a shared workbook with a password is important to ensure data privacy. With Aspose.Cells for .NET, you can easily protect or unprotect a shared workbook using passwords. Follow the steps below to get the desired results:

## Step 1: Specify output directory

First, you need to specify the output directory where the protected Excel file will be saved. Here's how to do it using Aspose.Cells:

```csharp
// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

## Step 2: Create an empty Excel file

Then you can create an empty Excel file on which you want to apply protection or unprotection. Here is a sample code:

```csharp
// Create an empty Excel workbook
Workbook wb = new Workbook();
```

## Step 3: Protect or unprotect the shared workbook

After creating the workbook, you can protect or unprotect the shared workbook by specifying the appropriate password. Here's how:

```csharp
// Protect the shared workbook with a password
wb.ProtectSharedWorkbook("1234");

// Uncomment this line to unprotect the shared workbook
// wb.UnprotectSharedWorkbook("1234");
```

## Step 4: Save the output Excel file

Once you apply protection or unprotection, you can save the protected Excel file to the specified output directory. Here's how to do it:

```csharp
// Save the output Excel file
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Sample source code for Password Protect Or Unprotect Shared Workbook using Aspose.Cells for .NET 
```csharp
//Output directory
string outputDir = RunExamples.Get_OutputDirectory();
//Create empty Excel file
Workbook wb = new Workbook();
//Protect the Shared Workbook with Password
wb.ProtectSharedWorkbook("1234");
//Uncomment this line to Unprotect the Shared Workbook
//wb.UnprotectSharedWorkbook("1234");
//Save the output Excel file
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusion

Protecting or unprotecting a shared workbook with a password is essential to ensure data security. With Aspose.Cells for .NET you can easily add this functionality to your Excel files. By following the steps in this guide, you can effectively protect or unprotect your shared workbooks using passwords. Experiment with your own Excel files and be sure to maintain the security of your sensitive data.

### FAQs

#### Q: What types of protection can I apply to a workbook shared with Aspose.Cells?
    
	 A: With Aspose.Cells, you can protect a shared workbook by specifying a password to prevent unauthorized access, modification or deletion of data.

#### Q: Can I protect a shared workbook without specifying a password?
    
	 A: Yes, you can protect a shared workbook without specifying a password. However, it is recommended to use a strong password for better security.

#### Q: How can I unprotect a workbook shared with Aspose.Cells?
    
	 A: To unprotect a shared workbook, you must specify the same password that was used when protecting the workbook. This allows the protection to be removed and the data to be freely accessed.

#### Q: Does protecting a shared workbook affect the features and formulas in the workbook?
    
	 A: When you protect a shared workbook, users can still access features and formulas present in the workbook. Protection only affects structural changes to the workbook.
