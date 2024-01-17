---
title: Εμφάνιση και απόκρυψη γραμμών κύλισης του φύλλου εργασίας
linktitle: Εμφάνιση και απόκρυψη γραμμών κύλισης του φύλλου εργασίας
second_title: Aspose.Cells for .NET API Reference
description: Εμφάνιση ή απόκρυψη γραμμών κύλισης στο φύλλο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET.
type: docs
weight: 50
url: /el/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
Σε αυτό το σεμινάριο, θα σας δείξουμε πώς να εμφανίζετε ή να αποκρύπτετε κάθετες και οριζόντιες γραμμές κύλισης σε ένα φύλλο εργασίας του Excel χρησιμοποιώντας τον πηγαίο κώδικα C# με το Aspose.Cells για .NET. Ακολουθήστε τα παρακάτω βήματα για να έχετε το επιθυμητό αποτέλεσμα.

## Βήμα 1: Εισαγάγετε τις απαραίτητες βιβλιοθήκες

Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.Cells για .NET και εισαγάγετε τις απαραίτητες βιβλιοθήκες στο έργο σας C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Βήμα 2: Ορίστε τη διαδρομή καταλόγου και ανοίξτε το αρχείο Excel

 Ορίστε τη διαδρομή προς τον κατάλογο που περιέχει το αρχείο σας Excel και, στη συνέχεια, ανοίξτε το αρχείο δημιουργώντας μια ροή αρχείου και δημιουργώντας ένα`Workbook` αντικείμενο.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Βήμα 3: Απόκρυψη γραμμών κύλισης

 Χρησιμοποιήστε το`IsVScrollBarVisible` και`IsHScrollBarVisible` ιδιότητες του`Workbook.Settings` αντικείμενο για απόκρυψη των κάθετων και οριζόντιων γραμμών κύλισης του φύλλου εργασίας.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Βήμα 4: Αποθήκευση αλλαγών

 Αφού κάνετε τις απαραίτητες αλλαγές, αποθηκεύστε το τροποποιημένο αρχείο Excel χρησιμοποιώντας το`Save` μέθοδος του`Workbook` αντικείμενο.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Δείγμα πηγαίου κώδικα για Εμφάνιση και Απόκρυψη γραμμών κύλισης φύλλου εργασίας χρησιμοποιώντας Aspose.Cells για .NET 

```csharp
//Η διαδρομή προς τον κατάλογο εγγράφων.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Δημιουργία ροής αρχείων που περιέχει το αρχείο Excel που πρόκειται να ανοίξει
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Δημιουργία αντικειμένου βιβλίου εργασίας
// Άνοιγμα του αρχείου Excel μέσω της ροής αρχείων
Workbook workbook = new Workbook(fstream);
// Απόκρυψη της κάθετης γραμμής κύλισης του αρχείου Excel
workbook.Settings.IsVScrollBarVisible = false;
// Απόκρυψη της οριζόντιας γραμμής κύλισης του αρχείου Excel
workbook.Settings.IsHScrollBarVisible = false;
// Αποθήκευση του τροποποιημένου αρχείου Excel
workbook.Save(dataDir + "output.xls");
// Κλείσιμο της ροής αρχείων για να ελευθερωθούν όλοι οι πόροι
fstream.Close();
```

### συμπέρασμα

Αυτός ο οδηγός βήμα προς βήμα σάς έδειξε πώς να εμφανίζετε ή να αποκρύπτετε κάθετες και οριζόντιες γραμμές κύλισης σε ένα υπολογιστικό φύλλο Excel χρησιμοποιώντας το Aspose.Cells για .NET. Χρησιμοποιώντας τον παρεχόμενο πηγαίο κώδικα C#, μπορείτε εύκολα να προσαρμόσετε την εμφάνιση των γραμμών κύλισης στα αρχεία σας Excel.

### Συχνές Ερωτήσεις (FAQ)

#### Τι είναι το Aspose.Cells για .NET;

Το Aspose.Cells για .NET είναι μια ισχυρή βιβλιοθήκη για το χειρισμό αρχείων Excel σε εφαρμογές .NET.

#### Πώς μπορώ να εγκαταστήσω το Aspose.Cells για .NET;

 Για να εγκαταστήσετε το Aspose.Cells για .NET, πρέπει να κάνετε λήψη του σχετικού πακέτου από[Aspose Releases](https://releases/aspose.com/cells/net/) και προσθέστε το στο έργο σας .NET.

#### Πώς μπορώ να εμφανίσω ή να αποκρύψω τις γραμμές κύλισης σε ένα υπολογιστικό φύλλο Excel με το Aspose.Cells για .NET;

 Μπορείτε να χρησιμοποιήσετε το`IsVScrollBarVisible` και`IsHScrollBarVisible` ιδιότητες του`Workbook.Settings` αντικείμενο για εμφάνιση ή απόκρυψη της κάθετης και της οριζόντιας γραμμής κύλισης αντίστοιχα σε ένα φύλλο εργασίας του Excel.

#### Ποιες άλλες μορφές αρχείων Excel υποστηρίζονται από το Aspose.Cells για .NET;

Το Aspose.Cells για .NET υποστηρίζει μια ποικιλία μορφών αρχείων Excel, όπως XLS, XLSX, CSV, HTML, PDF κ.λπ.