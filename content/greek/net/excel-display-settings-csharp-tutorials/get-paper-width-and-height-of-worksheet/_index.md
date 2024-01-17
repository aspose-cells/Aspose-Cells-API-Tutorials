---
title: Λάβετε το πλάτος του χαρτιού και το ύψος του φύλλου εργασίας
linktitle: Λάβετε το πλάτος του χαρτιού και το ύψος του φύλλου εργασίας
second_title: Aspose.Cells for .NET API Reference
description: Δημιουργήστε έναν οδηγό βήμα προς βήμα για να εξηγήσετε τον ακόλουθο πηγαίο κώδικα C# για να λάβετε το πλάτος και το ύψος του χαρτιού ενός υπολογιστικού φύλλου χρησιμοποιώντας το Aspose.Cells για .NET.
type: docs
weight: 80
url: /el/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
Σε αυτό το σεμινάριο, θα σας οδηγήσουμε βήμα προς βήμα για να εξηγήσετε τον ακόλουθο πηγαίο κώδικα C# για να λάβετε το πλάτος και το ύψος του χαρτιού ενός φύλλου εργασίας χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθήστε τα παρακάτω βήματα:

## Βήμα 1: Δημιουργήστε το βιβλίο εργασίας
 Ξεκινήστε δημιουργώντας ένα νέο βιβλίο εργασίας χρησιμοποιώντας το`Workbook` τάξη:

```csharp
Workbook wb = new Workbook();
```

## Βήμα 2: Πρόσβαση στο πρώτο φύλλο εργασίας
 Στη συνέχεια, μεταβείτε στο πρώτο φύλλο εργασίας του βιβλίου εργασίας χρησιμοποιώντας το`Worksheet` τάξη:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Βήμα 3: Ορίστε το μέγεθος χαρτιού σε A2 και εμφανίστε το πλάτος και το ύψος του χαρτιού σε ίντσες
 Χρησιμοποιήστε το`PaperSize` ιδιοκτησία του`PageSetup` Αντικείμενο να ορίσετε το μέγεθος χαρτιού σε A2 και, στη συνέχεια, χρησιμοποιήστε το`PaperWidth` και`PaperHeight` ιδιότητες για να πάρετε το πλάτος και το ύψος του χαρτιού αντίστοιχα. Εμφανίστε αυτές τις τιμές χρησιμοποιώντας το`Console.WriteLine` μέθοδος:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Βήμα 4: Επαναλάβετε τα βήματα για άλλα μεγέθη χαρτιού
Επαναλάβετε τα προηγούμενα βήματα, αλλάζοντας το μέγεθος χαρτιού σε A3, A4 και Letter και, στη συνέχεια, εμφανίζοντας τις τιμές πλάτους και ύψους χαρτιού για κάθε μέγεθος:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Δείγμα πηγαίου κώδικα για Λήψη πλάτους χαρτιού και ύψους φύλλου εργασίας χρησιμοποιώντας Aspose.Cells για .NET 

```csharp
//Δημιουργία βιβλίου εργασίας
Workbook wb = new Workbook();
//Πρόσβαση στο πρώτο φύλλο εργασίας
Worksheet ws = wb.Worksheets[0];
//Ρυθμίστε το μέγεθος χαρτιού σε A2 και εκτυπώστε το πλάτος και το ύψος του χαρτιού σε ίντσες
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ρυθμίστε το μέγεθος χαρτιού σε A3 και εκτυπώστε το πλάτος και το ύψος του χαρτιού σε ίντσες
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ρυθμίστε το μέγεθος χαρτιού σε A4 και εκτυπώστε το πλάτος και το ύψος του χαρτιού σε ίντσες
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Ρυθμίστε το μέγεθος χαρτιού σε Letter και εκτυπώστε το πλάτος και το ύψος του χαρτιού σε ίντσες
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## συμπέρασμα

Μάθατε πώς να χρησιμοποιείτε το Aspose.Cells για .NET για να λαμβάνετε το πλάτος και το ύψος του χαρτιού ενός υπολογιστικού φύλλου. Αυτή η δυνατότητα μπορεί να είναι χρήσιμη για τη διαμόρφωση και την ακριβή διάταξη των εγγράφων σας στο Excel.

### Συχνές Ερωτήσεις (FAQ)

#### Τι είναι το Aspose.Cells για .NET;

Το Aspose.Cells for .NET είναι μια ισχυρή βιβλιοθήκη για το χειρισμό και την επεξεργασία αρχείων Excel σε εφαρμογές .NET. Προσφέρει πολλές δυνατότητες για τη δημιουργία, την τροποποίηση, τη μετατροπή και την ανάλυση αρχείων Excel.

#### Πώς μπορώ να αποκτήσω το μέγεθος χαρτιού ενός υπολογιστικού φύλλου με το Aspose.Cells για .NET;

 Μπορείτε να χρησιμοποιήσετε το`PageSetup` τάξη των`Worksheet` αντικείμενο πρόσβασης στο μέγεθος χαρτιού. Χρησιμοποιήστε το`PaperSize` ιδιότητα για να ορίσετε το μέγεθος χαρτιού και το`PaperWidth` και`PaperHeight` ιδιότητες για να πάρετε το πλάτος και το ύψος του χαρτιού αντίστοιχα.

#### Ποια μεγέθη χαρτιού υποστηρίζει το Aspose.Cells για .NET;

Το Aspose.Cells για .NET υποστηρίζει ένα ευρύ φάσμα μεγεθών χαρτιού που χρησιμοποιούνται συνήθως, όπως A2, A3, A4 και Letter, καθώς και πολλά άλλα προσαρμοσμένα μεγέθη.

#### Μπορώ να προσαρμόσω το μέγεθος χαρτιού ενός υπολογιστικού φύλλου με το Aspose.Cells για .NET;

 Ναι, μπορείτε να ορίσετε ένα προσαρμοσμένο μέγεθος χαρτιού καθορίζοντας τις ακριβείς διαστάσεις πλάτους και ύψους χρησιμοποιώντας το`PaperWidth` και`PaperHeight` ιδιότητες του`PageSetup` τάξη.