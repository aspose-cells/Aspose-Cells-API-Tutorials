---
title: Ενημέρωση στοιχείου τύπου Power Query
linktitle: Ενημέρωση στοιχείου τύπου Power Query
second_title: Aspose.Cells for .NET API Reference
description: Μάθετε πώς να ενημερώνετε τα στοιχεία τύπου Power Query σε αρχεία Excel χρησιμοποιώντας το Aspose.Cells για .NET.
type: docs
weight: 160
url: /el/net/excel-workbook/update-power-query-formula-item/
---
Η ενημέρωση ενός στοιχείου τύπου Power Query είναι μια συνηθισμένη λειτουργία κατά την εργασία με δεδομένα σε αρχεία Excel. Με το Aspose.Cells για .NET, μπορείτε εύκολα να ενημερώσετε ένα στοιχείο τύπου Power Query ακολουθώντας αυτά τα βήματα:

## Βήμα 1: Καθορίστε τους καταλόγους προέλευσης και εξόδου

Αρχικά, πρέπει να καθορίσετε τον κατάλογο προέλευσης όπου βρίσκεται το αρχείο Excel που περιέχει τους τύπους Power Query προς ενημέρωση, καθώς και τον κατάλογο εξόδου όπου θέλετε να αποθηκεύσετε το τροποποιημένο αρχείο. Δείτε πώς μπορείτε να το κάνετε χρησιμοποιώντας το Aspose.Cells:

```csharp
// κατάλογος πηγής
string SourceDir = RunExamples.Get_SourceDirectory();

// Κατάλογο εξόδου
string outputDir = RunExamples.Get_OutputDirectory();
```

## Βήμα 2: Φορτώστε το βιβλίο εργασίας του Excel προέλευσης

Στη συνέχεια, πρέπει να φορτώσετε το βιβλίο εργασίας του Excel προέλευσης στο οποίο θέλετε να ενημερώσετε το στοιχείο τύπου Power Query. Δείτε πώς να το κάνετε:

```csharp
// Φορτώστε το βιβλίο εργασίας του Excel προέλευσης
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Βήμα 3: Περιήγηση και ενημέρωση στοιχείων τύπου Power Query

Μετά τη φόρτωση του βιβλίου εργασίας, μπορείτε να πλοηγηθείτε στη συλλογή τύπων Power Query και να περιηγηθείτε σε κάθε τύπο και τα στοιχεία του. Σε αυτό το παράδειγμα, αναζητούμε το στοιχείο τύπου με το όνομα "Πηγή" και ενημερώνουμε την τιμή του. Ακολουθεί δείγμα κώδικα για την ενημέρωση ενός στοιχείου τύπου Power Query:

```csharp
// Πρόσβαση στη συλλογή τύπων Power Query
DataMashup mashupData = workbook.DataMashup;

// Κάντε βρόχο στους τύπους του Power Query και στα στοιχεία τους
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Βήμα 4: Αποθηκεύστε το βιβλίο εργασίας του Excel εξόδου

Αφού ενημερώσετε το στοιχείο τύπου Power Query, μπορείτε να αποθηκεύσετε το τροποποιημένο βιβλίο εργασίας του Excel στον καθορισμένο κατάλογο εξόδου. Δείτε πώς να το κάνετε:

```csharp
// Αποθηκεύστε το βιβλίο εργασίας του Excel εξόδου
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Δείγμα πηγαίου κώδικα για Ενημέρωση στοιχείου τύπου Power Query χρησιμοποιώντας Aspose.Cells για .NET 
```csharp
// Κατάλογοι εργασίας
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Αποθηκεύστε το βιβλίο εργασίας εξόδου.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## συμπέρασμα

Η ενημέρωση στοιχείων τύπου Power Query είναι μια βασική λειτουργία όταν χρησιμοποιείτε το Aspose.Cells για τον χειρισμό και την επεξεργασία δεδομένων σε αρχεία Excel. Ακολουθώντας τα βήματα που δίνονται παραπάνω, μπορείτε εύκολα να ενημερώσετε στοιχεία τύπου

### Συχνές ερωτήσεις

#### Ε: Τι είναι το Power Query στο Excel;
     
Α: Το Power Query είναι μια δυνατότητα στο Excel που βοηθά στη συλλογή, μετατροπή και φόρτωση δεδομένων από διαφορετικές πηγές. Προσφέρει ισχυρά εργαλεία για τον καθαρισμό, τον συνδυασμό και την αναμόρφωση δεδομένων πριν τα εισαγάγετε στο Excel.

#### Ε: Πώς μπορώ να ξέρω εάν ένα στοιχείο τύπου Power Query ενημερώθηκε με επιτυχία;
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Ε: Μπορώ να ενημερώσω πολλά στοιχεία τύπου Power Query ταυτόχρονα;
    
Α: Ναι, μπορείτε να πραγματοποιήσετε βρόχο μέσω της συλλογής στοιχείων τύπου Power Query και να ενημερώσετε πολλά στοιχεία σε έναν μόνο βρόχο, ανάλογα με τις συγκεκριμένες ανάγκες σας.

#### Ε: Υπάρχουν άλλες λειτουργίες που μπορώ να εκτελέσω σε τύπους Power Query με το Aspose.Cells;
    
Α: Ναι, το Aspose.Cells προσφέρει μια πλήρη γκάμα δυνατοτήτων για εργασία με τύπους Power Query, συμπεριλαμβανομένης της δημιουργίας, διαγραφής, αντιγραφής και αναζήτησης τύπων σε βιβλίο εργασίας του Excel.