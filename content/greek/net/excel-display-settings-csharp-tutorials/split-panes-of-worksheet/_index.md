---
title: Διαίρεση υαλοπινάκων του φύλλου εργασίας
linktitle: Διαίρεση υαλοπινάκων του φύλλου εργασίας
second_title: Aspose.Cells for .NET API Reference
description: Οδηγός βήμα προς βήμα για τη διαίρεση των πλαισίων σε ένα φύλλο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET.
type: docs
weight: 130
url: /el/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
Σε αυτό το σεμινάριο, θα εξηγήσουμε πώς να χωρίσετε τα παράθυρα σε ένα φύλλο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθήστε αυτά τα βήματα για να έχετε το επιθυμητό αποτέλεσμα:

## Βήμα 1: Ρύθμιση περιβάλλοντος

Βεβαιωθείτε ότι έχετε εγκαταστήσει το Aspose.Cells για .NET και έχετε ρυθμίσει το περιβάλλον ανάπτυξης. Επίσης, βεβαιωθείτε ότι έχετε ένα αντίγραφο του αρχείου Excel στο οποίο θέλετε να χωρίσετε τα παράθυρα.

## Βήμα 2: Εισαγάγετε τις απαραίτητες εξαρτήσεις

Προσθέστε τις απαραίτητες οδηγίες για να χρησιμοποιήσετε τις κλάσεις από το Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Βήμα 3: Αρχικοποίηση κώδικα

Ξεκινήστε αρχικοποιώντας τη διαδρομή προς τον κατάλογο που περιέχει τα έγγραφά σας Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Βήμα 4: Άνοιγμα του αρχείου Excel

 Δημιουργήστε ένα νέο`Workbook` αντικείμενο και ανοίξτε το αρχείο Excel χρησιμοποιώντας το`Open` μέθοδος:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Βήμα 5: Ορίστε το ενεργό κελί

 Ορίστε το ενεργό κελί του φύλλου εργασίας χρησιμοποιώντας το`ActiveCell` ιδιοκτησία:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Βήμα 6: Διαίρεση των πτερυγίων

 Διαχωρίστε το παράθυρο του φύλλου εργασίας χρησιμοποιώντας το`Split` μέθοδος:

```csharp
book.Worksheets[0].Split();
```

## Βήμα 7: Αποθήκευση αλλαγών

Αποθηκεύστε τις αλλαγές που έγιναν στο αρχείο Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Δείγμα πηγαίου κώδικα για Split Panes Of Worksheet χρησιμοποιώντας Aspose.Cells για .NET 

```csharp
//Η διαδρομή προς τον κατάλογο εγγράφων.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Δημιουργήστε ένα νέο βιβλίο εργασίας και ανοίξτε ένα αρχείο προτύπου
Workbook book = new Workbook(dataDir + "Book1.xls");
// Ρυθμίστε το ενεργό κελί
book.Worksheets[0].ActiveCell = "A20";
// Διαχωρίστε το παράθυρο του φύλλου εργασίας
book.Worksheets[0].Split();
// Αποθηκεύστε το αρχείο excel
book.Save(dataDir + "output.xls");
```

## συμπέρασμα

Σε αυτό το σεμινάριο, μάθατε πώς να χωρίζετε τα παράθυρα σε ένα φύλλο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθώντας τα βήματα που περιγράφονται, μπορείτε εύκολα να προσαρμόσετε την εμφάνιση και τη συμπεριφορά των αρχείων σας Excel.

### Συχνές Ερωτήσεις (FAQ)

#### Τι είναι το Aspose.Cells για .NET;

Το Aspose.Cells για .NET είναι μια δημοφιλής βιβλιοθήκη λογισμικού για το χειρισμό αρχείων Excel σε εφαρμογές .NET.

#### Πώς μπορώ να ορίσω το ενεργό κελί ενός φύλλου εργασίας στο Aspose.Cells;

 Μπορείτε να ορίσετε το ενεργό κελί χρησιμοποιώντας το`ActiveCell`ιδιότητα του αντικειμένου φύλλου εργασίας.

#### Μπορώ να χωρίσω μόνο τα οριζόντια ή κατακόρυφα τμήματα του παραθύρου του φύλλου εργασίας;

 Ναι, χρησιμοποιώντας το Aspose.Cells μπορείτε να χωρίσετε μόνο οριζόντια ή κάθετα παράθυρα χρησιμοποιώντας τις κατάλληλες μεθόδους όπως π.χ`SplitColumn` ή`SplitRow`.

#### Το Aspose.Cells λειτουργεί μόνο με αρχεία Excel σε μορφή .xls;

Όχι, το Aspose.Cells υποστηρίζει διάφορες μορφές αρχείων Excel, συμπεριλαμβανομένων των .xls και .xlsx.