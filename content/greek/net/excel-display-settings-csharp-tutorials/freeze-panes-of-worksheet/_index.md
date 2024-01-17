---
title: Πάγωμα υαλοπινάκων του φύλλου εργασίας
linktitle: Πάγωμα υαλοπινάκων του φύλλου εργασίας
second_title: Aspose.Cells for .NET API Reference
description: Χειριστείτε εύκολα τα παράθυρα παγώματος του φύλλου εργασίας του Excel με το Aspose.Cells για .NET.
type: docs
weight: 70
url: /el/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
Σε αυτό το σεμινάριο, θα σας δείξουμε πώς να κλειδώνετε τα παράθυρα σε ένα φύλλο εργασίας του Excel χρησιμοποιώντας τον πηγαίο κώδικα C# με το Aspose.Cells για .NET. Ακολουθήστε τα παρακάτω βήματα για να έχετε το επιθυμητό αποτέλεσμα.

## Βήμα 1: Εισαγάγετε τις απαραίτητες βιβλιοθήκες

Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.Cells για .NET και εισαγάγετε τις απαραίτητες βιβλιοθήκες στο έργο σας C#.

```csharp
using Aspose.Cells;
```

## Βήμα 2: Ορίστε τη διαδρομή καταλόγου και ανοίξτε το αρχείο Excel

 Ορίστε τη διαδρομή προς τον κατάλογο που περιέχει το αρχείο σας Excel και, στη συνέχεια, ανοίξτε το αρχείο δημιουργώντας στιγμιότυπο α`Workbook` αντικείμενο.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Βήμα 3: Μεταβείτε στο υπολογιστικό φύλλο και εφαρμόστε τις ρυθμίσεις κλειδώματος παραθύρου

 Μεταβείτε στο πρώτο φύλλο εργασίας στο αρχείο Excel χρησιμοποιώντας το`Worksheet` αντικείμενο. Στη συνέχεια χρησιμοποιήστε το`FreezePanes` μέθοδος εφαρμογής των ρυθμίσεων κλειδώματος παραθύρου.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Στο παραπάνω παράδειγμα, τα παράθυρα είναι κλειδωμένα στο κελί στη σειρά 3 και στη στήλη 2.

## Βήμα 4: Αποθήκευση αλλαγών

 Αφού κάνετε τις απαραίτητες αλλαγές, αποθηκεύστε το τροποποιημένο αρχείο Excel χρησιμοποιώντας το`Save` μέθοδος του`Workbook` αντικείμενο.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Δείγμα πηγαίου κώδικα για Freeze Panes Of Worksheet χρησιμοποιώντας Aspose.Cells για .NET 

```csharp
//Η διαδρομή προς τον κατάλογο εγγράφων.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Δημιουργία ροής αρχείων που περιέχει το αρχείο Excel που πρόκειται να ανοίξει
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Δημιουργία αντικειμένου βιβλίου εργασίας
// Άνοιγμα του αρχείου Excel μέσω της ροής αρχείων
Workbook workbook = new Workbook(fstream);
// Πρόσβαση στο πρώτο φύλλο εργασίας στο αρχείο Excel
Worksheet worksheet = workbook.Worksheets[0];
// Εφαρμογή ρυθμίσεων παγώματος τζαμιών
worksheet.FreezePanes(3, 2, 3, 2);
// Αποθήκευση του τροποποιημένου αρχείου Excel
workbook.Save(dataDir + "output.xls");
// Κλείσιμο της ροής αρχείων για να ελευθερωθούν όλοι οι πόροι
fstream.Close();
```

## συμπέρασμα

Αυτός ο οδηγός βήμα προς βήμα σάς έδειξε πώς να κλειδώνετε τα παράθυρα σε ένα υπολογιστικό φύλλο Excel χρησιμοποιώντας το Aspose.Cells για .NET. Χρησιμοποιώντας τον παρεχόμενο πηγαίο κώδικα C#, μπορείτε εύκολα να προσαρμόσετε τις ρυθμίσεις κλειδώματος παραθύρου για καλύτερη οργάνωση και οπτικοποίηση των δεδομένων σας σε αρχεία Excel.

### Συχνές Ερωτήσεις (FAQ)

#### Τι είναι το Aspose.Cells για .NET;

Το Aspose.Cells για .NET είναι μια ισχυρή βιβλιοθήκη για το χειρισμό αρχείων Excel σε εφαρμογές .NET.

#### Πώς μπορώ να εγκαταστήσω το Aspose.Cells για .NET;

 Για να εγκαταστήσετε το Aspose.Cells για .NET, πρέπει να κάνετε λήψη του σχετικού πακέτου από[Aspose Releases](https://releases/aspose.com/cells/net/) και προσθέστε το στο έργο σας .NET.

#### Πώς να κλειδώσετε τα παράθυρα σε ένα φύλλο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET;

 Μπορείτε να χρησιμοποιήσετε το`FreezePanes` μέθοδος του`Worksheet` αντικείμενο να κλειδώσει τα παράθυρα ενός φύλλου εργασίας. Καθορίστε τα κελιά που θα κλειδωθούν παρέχοντας δείκτες σειρών και στηλών.

#### Μπορώ να προσαρμόσω τις ρυθμίσεις κλειδώματος παραθύρου με το Aspose.Cells για .NET;

 Ναι, χρησιμοποιώντας το`FreezePanes` μέθοδο, μπορείτε να καθορίσετε ποια κελιά θα κλειδωθούν ανάλογα με τις ανάγκες, παρέχοντας τους κατάλληλους δείκτες σειρών και στηλών.