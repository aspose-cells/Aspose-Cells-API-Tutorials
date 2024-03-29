---
title: Προεπισκόπηση εκτύπωσης βιβλίου εργασίας
linktitle: Προεπισκόπηση εκτύπωσης βιβλίου εργασίας
second_title: Aspose.Cells for .NET API Reference
description: Μάθετε πώς να δημιουργείτε μια προεπισκόπηση εκτύπωσης ενός βιβλίου εργασίας χρησιμοποιώντας το Aspose.Cells για .NET.
type: docs
weight: 170
url: /el/net/excel-workbook/workbook-print-preview/
---
Η προεπισκόπηση εκτύπωσης ενός βιβλίου εργασίας είναι μια βασική δυνατότητα κατά την εργασία με αρχεία Excel με το Aspose.Cells για .NET. Μπορείτε εύκολα να δημιουργήσετε μια προεπισκόπηση εκτύπωσης ακολουθώντας αυτά τα βήματα:

## Βήμα 1: Καθορίστε τον κατάλογο προέλευσης

Αρχικά, πρέπει να καθορίσετε τον κατάλογο προέλευσης όπου βρίσκεται το αρχείο Excel που θέλετε να κάνετε προεπισκόπηση. Δείτε πώς να το κάνετε:

```csharp
// κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Βήμα 2: Φορτώστε το βιβλίο εργασίας

Στη συνέχεια, πρέπει να φορτώσετε το βιβλίο εργασίας του βιβλίου εργασίας από το καθορισμένο αρχείο Excel. Δείτε πώς να το κάνετε:

```csharp
// Φορτώστε το βιβλίο εργασίας του βιβλίου εργασίας
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Βήμα 3: Διαμορφώστε τις επιλογές εικόνας και εκτύπωσης

Πριν δημιουργήσετε την προεπισκόπηση εκτύπωσης, μπορείτε να διαμορφώσετε την εικόνα και τις επιλογές εκτύπωσης όπως απαιτείται. Σε αυτό το παράδειγμα, χρησιμοποιούμε τις προεπιλεγμένες επιλογές. Δείτε πώς να το κάνετε:

```csharp
// Επιλογές εικόνας και εκτύπωσης
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Βήμα 4: Δημιουργήστε την προεπισκόπηση εκτύπωσης του βιβλίου εργασίας

Τώρα μπορείτε να δημιουργήσετε την προεπισκόπηση εκτύπωσης του βιβλίου εργασίας του βιβλίου εργασίας χρησιμοποιώντας την κλάση WorkbookPrintingPreview. Δείτε πώς να το κάνετε:

```csharp
// Προεπισκόπηση εκτύπωσης του βιβλίου εργασίας
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Βήμα 5: Δημιουργήστε την προεπισκόπηση εκτύπωσης του φύλλου εργασίας

Εάν θέλετε να δημιουργήσετε την προεπισκόπηση εκτύπωσης ενός συγκεκριμένου φύλλου εργασίας, μπορείτε να χρησιμοποιήσετε την κλάση SheetPrintingPreview. Εδώ είναι ένα παράδειγμα:

```csharp
// Προεπισκόπηση εκτύπωσης του φύλλου εργασίας
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Δείγμα πηγαίου κώδικα για προεπισκόπηση εκτύπωσης βιβλίου εργασίας χρησιμοποιώντας Aspose.Cells για .NET 
```csharp
//Κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## συμπέρασμα

Η δημιουργία της προεπισκόπησης εκτύπωσης ενός βιβλίου εργασίας είναι μια ισχυρή δυνατότητα που προσφέρεται από το Aspose.Cells για .NET. Ακολουθώντας τα βήματα που δίνονται παραπάνω, μπορείτε εύκολα να κάνετε προεπισκόπηση του βιβλίου εργασίας του Excel και να λάβετε πληροφορίες σχετικά με τον αριθμό των σελίδων προς εκτύπωση.

### Συχνές ερωτήσεις

#### Ε: Πώς μπορώ να καθορίσω έναν διαφορετικό κατάλογο προέλευσης για να φορτώσω το Βιβλίο εργασίας μου;
    
 Α: Μπορείτε να χρησιμοποιήσετε το`Set_SourceDirectory` μέθοδος για τον καθορισμό διαφορετικού καταλόγου προέλευσης. Για παράδειγμα:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Ε: Μπορώ να προσαρμόσω τις επιλογές εικόνας και εκτύπωσης κατά τη δημιουργία της προεπισκόπησης εκτύπωσης;
    
 Α: Ναι, μπορείτε να προσαρμόσετε τις επιλογές εικόνας και εκτύπωσης αλλάζοντας τις ιδιότητες του`ImageOrPrintOptions` αντικείμενο. Για παράδειγμα, μπορείτε να ορίσετε την ανάλυση εικόνας, τη μορφή αρχείου εξόδου κ.λπ.

#### Ε: Είναι δυνατή η δημιουργία προεπισκόπησης εκτύπωσης για πολλά φύλλα εργασίας σε ένα βιβλίο εργασίας;
    
Α: Ναι, μπορείτε να επαναλάβετε τα διαφορετικά φύλλα εργασίας στο βιβλίο εργασίας και να δημιουργήσετε μια προεπισκόπηση εκτύπωσης για κάθε φύλλο χρησιμοποιώντας το`SheetPrintingPreview` τάξη.

#### Ε: Πώς μπορώ να αποθηκεύσω την προεπισκόπηση εκτύπωσης ως αρχείο εικόνας ή PDF;
    
 Α: Μπορείτε να χρησιμοποιήσετε`ToImage` ή`ToPdf` μέθοδος για`WorkbookPrintingPreview` ή`SheetPrintingPreview` αντικείμενο για αποθήκευση της προεπισκόπησης εκτύπωσης ως αρχείο εικόνας ή PDF.

#### Ε: Τι μπορώ να κάνω με την προεπισκόπηση εκτύπωσης μόλις δημιουργηθεί;
    
Α: Αφού δημιουργήσετε την προεπισκόπηση εκτύπωσης, μπορείτε να την προβάλετε στην οθόνη, να την αποθηκεύσετε ως εικόνα ή αρχείο PDF ή να τη χρησιμοποιήσετε για άλλες λειτουργίες, όπως αποστολή μέσω email ή εκτύπωση.
	