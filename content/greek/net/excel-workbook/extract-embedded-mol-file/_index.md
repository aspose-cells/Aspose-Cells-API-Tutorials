---
title: Εξαγωγή ενσωματωμένου αρχείου Mol
linktitle: Εξαγωγή ενσωματωμένου αρχείου Mol
second_title: Aspose.Cells for .NET API Reference
description: Μάθετε πώς να εξάγετε εύκολα ενσωματωμένα αρχεία MOL από ένα βιβλίο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET.
type: docs
weight: 90
url: /el/net/excel-workbook/extract-embedded-mol-file/
---
Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε βήμα προς βήμα πώς να εξαγάγετε ένα ενσωματωμένο αρχείο MOL από ένα βιβλίο εργασίας του Excel χρησιμοποιώντας τη βιβλιοθήκη Aspose.Cells για .NET. Θα μάθετε πώς να περιηγείστε στα φύλλα του βιβλίου εργασίας, να εξάγετε τα αντίστοιχα αντικείμενα OLE και να αποθηκεύετε τα εξαγόμενα αρχεία MOL. Ακολουθήστε τα παρακάτω βήματα για να ολοκληρώσετε με επιτυχία αυτήν την εργασία.

## Βήμα 1: Ορίστε τους καταλόγους προέλευσης και εξόδου
Αρχικά, πρέπει να ορίσουμε τους καταλόγους πηγής και εξόδου στον κώδικά μας. Αυτοί οι κατάλογοι υποδεικνύουν πού βρίσκεται το βιβλίο εργασίας του Excel προέλευσης και πού θα αποθηκευτούν τα εξαγόμενα αρχεία MOL. Εδώ είναι ο αντίστοιχος κωδικός:

```csharp
// καταλόγους
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Φροντίστε να καθορίσετε τις κατάλληλες διαδρομές όπως απαιτείται.

## Βήμα 2: Φόρτωση του βιβλίου εργασίας του Excel
Το επόμενο βήμα είναι να φορτώσετε το βιβλίο εργασίας του Excel που περιέχει τα ενσωματωμένα αντικείμενα OLE και αρχεία MOL. Εδώ είναι ο κώδικας για τη φόρτωση του βιβλίου εργασίας:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Βεβαιωθείτε ότι έχετε καθορίσει σωστά το όνομα του αρχείου προέλευσης στον κώδικα.

## Βήμα 3: Διασχίστε τα φύλλα και εξαγάγετε τα αρχεία MOL
Τώρα θα κάνουμε βρόχο σε κάθε φύλλο του βιβλίου εργασίας και θα εξαγάγουμε τα αντίστοιχα αντικείμενα OLE, τα οποία περιέχουν τα αρχεία MOL. Εδώ είναι ο αντίστοιχος κωδικός:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Αυτός ο κώδικας περνά μέσα από κάθε φύλλο στο βιβλίο εργασίας, ανακτά τα αντικείμενα OLE και αποθηκεύει τα εξαγόμενα αρχεία MOL στον κατάλογο εξόδου.

### Δείγμα πηγαίου κώδικα για Extract Embedded Mol File χρησιμοποιώντας Aspose.Cells για .NET 
```csharp
//καταλόγους
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## συμπέρασμα
Συγχαρητήρια ! Έχετε μάθει πώς να εξάγετε ένα ενσωματωμένο αρχείο MOL από ένα βιβλίο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET. Τώρα μπορείτε να εφαρμόσετε αυτή τη γνώση για να εξαγάγετε αρχεία MOL από τα δικά σας βιβλία εργασίας του Excel. Μη διστάσετε να εξερευνήσετε περαιτέρω τη βιβλιοθήκη Aspose.Cells και να μάθετε για τα άλλα ισχυρά χαρακτηριστικά της.

### Συχνές ερωτήσεις

#### Ε: Τι είναι ένα αρχείο MOL;
 
Α: Ένα αρχείο MOL είναι μια μορφή αρχείου που χρησιμοποιείται για την αναπαράσταση χημικών δομών στην υπολογιστική χημεία. Περιέχει πληροφορίες για άτομα, δεσμούς και άλλες μοριακές ιδιότητες.

#### Ε: Αυτή η μέθοδος λειτουργεί με όλους τους τύπους αρχείων Excel;

Α: Ναι, αυτή η μέθοδος λειτουργεί με όλους τους τύπους αρχείων Excel που υποστηρίζονται από το Aspose.Cells.

#### Ε: Μπορώ να εξαγάγω πολλά αρχεία MOL ταυτόχρονα;

Α: Ναι, μπορείτε να εξαγάγετε πολλά αρχεία MOL ταυτόχρονα κάνοντας επανάληψη μέσω αντικειμένων OLE σε κάθε φύλλο του βιβλίου εργασίας.