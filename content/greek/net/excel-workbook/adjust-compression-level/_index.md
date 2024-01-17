---
title: Ρυθμίστε το επίπεδο συμπίεσης
linktitle: Ρυθμίστε το επίπεδο συμπίεσης
second_title: Aspose.Cells for .NET API Reference
description: Μειώστε το μέγεθος των βιβλίων εργασίας του Excel προσαρμόζοντας το επίπεδο συμπίεσης με το Aspose.Cells για .NET.
type: docs
weight: 50
url: /el/net/excel-workbook/adjust-compression-level/
---
Σε αυτό το βήμα προς βήμα σεμινάριο, θα εξηγήσουμε τον παρεχόμενο πηγαίο κώδικα C# που θα σας επιτρέψει να προσαρμόσετε το επίπεδο συμπίεσης χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθήστε τα παρακάτω βήματα για να προσαρμόσετε το επίπεδο συμπίεσης στο βιβλίο εργασίας του Excel.

## Βήμα 1: Ορίστε καταλόγους πηγής και εξόδου

```csharp
// κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
// Κατάλογο εξόδου
string outDir = RunExamples.Get_OutputDirectory();
```

Σε αυτό το πρώτο βήμα, ορίζουμε τους καταλόγους προέλευσης και εξόδου για τα αρχεία Excel.

## Βήμα 2: Φορτώστε το βιβλίο εργασίας του Excel

```csharp
// Φορτώστε το βιβλίο εργασίας του Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Φορτώνουμε το βιβλίο εργασίας του Excel από το καθορισμένο αρχείο χρησιμοποιώντας το`Workbook` τάξη από το Aspose.Cells.

## Βήμα 3: Ορίστε επιλογές δημιουργίας αντιγράφων ασφαλείας

```csharp
// Καθορίστε τις επιλογές δημιουργίας αντιγράφων ασφαλείας
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Δημιουργούμε ένα παράδειγμα του`XlsbSaveOptions` τάξη για να ορίσετε τις επιλογές αποθήκευσης.

## Βήμα 4: Προσαρμόστε το επίπεδο συμπίεσης (Επίπεδο 1)

```csharp
// Ρυθμίστε το επίπεδο συμπίεσης (Επίπεδο 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Ρυθμίζουμε το επίπεδο συμπίεσης`CompressionType` προς την`Level1`. Στη συνέχεια αποθηκεύουμε το βιβλίο εργασίας του Excel με καθορισμένη αυτήν την επιλογή συμπίεσης.

## Βήμα 5: Προσαρμόστε το επίπεδο συμπίεσης (Επίπεδο 6)

```csharp
// Ρυθμίστε το επίπεδο συμπίεσης (Επίπεδο 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Επαναλαμβάνουμε τη διαδικασία για να ρυθμίσουμε το επίπεδο συμπίεσης`Level6` και αποθηκεύστε το βιβλίο εργασίας του Excel με αυτήν την επιλογή.

## Βήμα 6: Προσαρμόστε το επίπεδο συμπίεσης (Επίπεδο 9)

```csharp
// Ρυθμίστε το επίπεδο συμπίεσης (Επίπεδο 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Επαναλαμβάνουμε τη διαδικασία για τελευταία φορά για να ρυθμίσουμε το επίπεδο συμπίεσης`Level9` και αποθηκεύστε το βιβλίο εργασίας του Excel με αυτήν την επιλογή.

### Δείγμα πηγαίου κώδικα για Προσαρμογή επιπέδου συμπίεσης χρησιμοποιώντας Aspose.Cells για .NET 
```csharp
//Κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## συμπέρασμα

Συγχαρητήρια ! Μάθατε πώς να προσαρμόζετε το επίπεδο συμπίεσης σε ένα βιβλίο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET. Πειραματιστείτε με διαφορετικά επίπεδα συμπίεσης για να βρείτε αυτό που ταιριάζει καλύτερα στις ανάγκες σας.

### Συχνές ερωτήσεις

#### Ε: Τι είναι η συμπίεση σε ένα βιβλίο εργασίας του Excel;

Α: Η συμπίεση σε ένα βιβλίο εργασίας του Excel είναι μια διαδικασία μείωσης του μεγέθους του αρχείου χρησιμοποιώντας αλγόριθμους συμπίεσης. Αυτό μειώνει τον απαιτούμενο χώρο αποθήκευσης και βελτιώνει την απόδοση κατά τη φόρτωση και τον χειρισμό του αρχείου.

#### Ε: Ποια επίπεδα συμπίεσης είναι διαθέσιμα με το Aspose.Cells;

Α: Με το Aspose.Cells, μπορείτε να προσαρμόσετε το επίπεδο συμπίεσης από 1 έως 9. Όσο υψηλότερο είναι το επίπεδο συμπίεσης, τόσο μικρότερο θα είναι το μέγεθος του αρχείου, αλλά μπορεί επίσης να αυξήσει τον χρόνο επεξεργασίας.

#### Ε: Πώς μπορώ να επιλέξω το σωστό επίπεδο συμπίεσης για το βιβλίο εργασίας του Excel;

Α: Η επιλογή του επιπέδου συμπίεσης εξαρτάται από τις συγκεκριμένες ανάγκες σας. Εάν θέλετε η μέγιστη συμπίεση και ο χρόνος επεξεργασίας δεν είναι πρόβλημα, μπορείτε να πάτε στο επίπεδο 9. Εάν προτιμάτε έναν συμβιβασμό μεταξύ του μεγέθους του αρχείου και του χρόνου επεξεργασίας, μπορείτε να επιλέξετε ένα ενδιάμεσο επίπεδο.

#### Ε: Επηρεάζει η συμπίεση την ποιότητα των δεδομένων στο βιβλίο εργασίας του Excel;

Α: Όχι, η συμπίεση δεν επηρεάζει την ποιότητα των δεδομένων στο βιβλίο εργασίας του Excel. Απλώς μειώνει το μέγεθος του αρχείου χρησιμοποιώντας τεχνικές συμπίεσης χωρίς να αλλάζει τα ίδια τα δεδομένα.

#### Ε: Μπορώ να προσαρμόσω το επίπεδο συμπίεσης μετά την αποθήκευση του αρχείου Excel;

Α: Όχι, αφού αποθηκεύσετε το αρχείο Excel με ένα συγκεκριμένο επίπεδο συμπίεσης, δεν μπορείτε να προσαρμόσετε το επίπεδο συμπίεσης αργότερα. Θα χρειαστεί να αποθηκεύσετε ξανά το αρχείο με το νέο επίπεδο συμπίεσης εάν θέλετε να το τροποποιήσετε.