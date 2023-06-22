---
title: Regex Replace
linktitle: Regex Replace
second_title: Aspose.Cells for .NET API Reference
description: Learn how to perform Regex replacement in Excel files using Aspose.Cells for .NET.
type: docs
weight: 140
url: /net/excel-workbook/regex-replace/
---
Text replacement based on regular expressions (Regex) is a common task when manipulating data in Excel files. With Aspose.Cells for .NET, you can easily perform a Regex replacement by following these steps:

## Step 1: Specify source directory and output directory

First of all, you must specify the source directory where the Excel file containing the data to be replaced is located, as well as the output directory where you want to save the modified file. Here's how to do it using Aspose.Cells:

```csharp
// source directory
string sourceDir = RunExamples.Get_SourceDirectory();

// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

## Step 2: Load the source Excel file

Next, you need to load the source Excel file on which you want to perform the Regex replacement. Here's how to do it:

```csharp
// Load the source Excel file
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## Step 3: Perform Regex Replacement

After uploading the file, you can set replacement options, including case sensitivity and exact cell content matching. Here is sample code to perform the Regex replacement:

```csharp
// Set replacement options
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Define that the search key is a regular expression
replace. RegexKey = true;

// Perform Regex replacement
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Step 4: Save the output Excel file

Once the Regex replacement is done, you can save the modified Excel file to the specified output directory. Here's how to do it:

```csharp
// Save the output Excel file
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Sample source code for Regex Replace using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
//Output directory
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Set to true to indicate that the searched key is regex
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Conclusion

Regex replacement is a powerful technique for dynamically modifying data in an Excel file. With Aspose.Cells for .NET, you can easily perform a Regex replacement by following the steps outlined above. Experiment with your own regular expressions and take advantage of the flexibility offered by Aspose.Cells.

### FAQs

#### Q: What is Regex Replacement?
    
	 A: Regex replacement is a technique used to replace text patterns based on regular expressions in an Excel file. This allows for quick and accurate changes to the data.

#### Q: Is Regex replacement case sensitive?
    
	 A: No, with Aspose.Cells you can specify whether the Regex replacement should be case sensitive or not. You have full control over this feature.

#### Q: How can I specify an exact match of cell content when replacing Regex?
    
	 A: Aspose.Cells allows you to define whether the Regex replacement should exactly match the cell content or not. You can adjust this option according to your needs.

#### Q: Can I use advanced regular expressions when replacing Regex with Aspose.Cells?
    
	 A: Yes, Aspose.Cells supports advanced regular expressions, allowing you to perform complex and sophisticated replacements in your Excel files.

#### Q: How can I check if the Regex replacement was successful?
    
	 A: After performing the Regex replacement, you can verify if the operation was successful by checking the output and ensuring that the output Excel file was created correctly.
	