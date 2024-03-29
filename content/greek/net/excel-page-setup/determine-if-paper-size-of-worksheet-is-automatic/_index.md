---
title: Προσδιορίστε εάν το μέγεθος χαρτιού του φύλλου εργασίας είναι αυτόματο
linktitle: Προσδιορίστε εάν το μέγεθος χαρτιού του φύλλου εργασίας είναι αυτόματο
second_title: Aspose.Cells for .NET API Reference
description: Μάθετε πώς να προσδιορίζετε εάν το μέγεθος χαρτιού ενός υπολογιστικού φύλλου είναι αυτόματο με το Aspose.Cells για .NET.
type: docs
weight: 20
url: /el/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
Σε αυτό το άρθρο, θα σας οδηγήσουμε βήμα προς βήμα για να εξηγήσετε τον ακόλουθο πηγαίο κώδικα C#: Προσδιορίστε εάν το μέγεθος χαρτιού ενός φύλλου εργασίας είναι αυτόματο χρησιμοποιώντας το Aspose.Cells για .NET. Θα χρησιμοποιήσουμε τη βιβλιοθήκη Aspose.Cells για .NET για να εκτελέσουμε αυτήν τη λειτουργία. Ακολουθήστε τα παρακάτω βήματα για να προσδιορίσετε εάν το μέγεθος χαρτιού ενός φύλλου εργασίας είναι αυτόματο.

## Βήμα 1: Φόρτωση βιβλίων εργασίας
Το πρώτο βήμα είναι να φορτώσετε τα βιβλία εργασίας. Θα έχουμε δύο βιβλία εργασίας: ένα με απενεργοποιημένο το αυτόματο μέγεθος χαρτιού και το άλλο με ενεργοποιημένο το αυτόματο μέγεθος χαρτιού. Ακολουθεί ο κώδικας για τη φόρτωση των βιβλίων εργασίας:

```csharp
// κατάλογος πηγής
string sourceDir = "YOUR_SOURCE_DIR";
// Κατάλογο εξόδου
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Τοποθετήστε το πρώτο βιβλίο εργασίας με απενεργοποιημένο το αυτόματο μέγεθος χαρτιού
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Τοποθετήστε δεύτερο βιβλίο εργασίας με ενεργοποιημένο το αυτόματο μέγεθος χαρτιού
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Βήμα 2: Πρόσβαση σε υπολογιστικά φύλλα
Τώρα που φορτώσαμε τα βιβλία εργασίας, πρέπει να έχουμε πρόσβαση στα φύλλα εργασίας, ώστε να μπορούμε να ελέγξουμε το αυτόματο μέγεθος χαρτιού. Θα πάμε στο πρώτο φύλλο εργασίας από τα δύο βιβλία εργασίας. Εδώ είναι ο κωδικός πρόσβασης:

```csharp
//Μεταβείτε στο πρώτο φύλλο εργασίας του πρώτου βιβλίου εργασίας
Worksheet ws11 = wb1.Worksheets[0];

// Μεταβείτε στο πρώτο φύλλο εργασίας του δεύτερου βιβλίου εργασίας
Worksheet ws12 = wb2.Worksheets[0];
```

## Βήμα 3: Ελέγξτε το αυτόματο μέγεθος χαρτιού
 Σε αυτό το βήμα, θα ελέγξουμε αν το μέγεθος του φύλλου εργασίας είναι αυτόματο. Θα χρησιμοποιήσουμε το`PageSetup.IsAutomaticPaperSize` ιδιοκτησίας για να λάβετε αυτές τις πληροφορίες. Στη συνέχεια θα εμφανίσουμε το αποτέλεσμα. Εδώ είναι ο κωδικός για αυτό:

```csharp
// Εμφανίστε την ιδιότητα IsAutomaticPaperSize του πρώτου φύλλου εργασίας στο πρώτο βιβλίο εργασίας
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Εμφανίστε την ιδιότητα IsAutomaticPaperSize του πρώτου φύλλου εργασίας στο δεύτερο βιβλίο εργασίας
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Δείγμα πηγαίου κώδικα για Προσδιορισμός εάν το μέγεθος χαρτιού του φύλλου εργασίας είναι αυτόματο χρησιμοποιώντας το Aspose.Cells για .NET 
```csharp
//Κατάλογος πηγής
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Κατάλογο εξόδου
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Τοποθετήστε το πρώτο βιβλίο εργασίας με αυτόματο μέγεθος χαρτιού false
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Τοποθετήστε το δεύτερο βιβλίο εργασίας με αυτόματο μέγεθος χαρτιού true
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Πρόσβαση στο πρώτο φύλλο εργασίας και των δύο βιβλίων εργασίας
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Εκτυπώστε την ιδιότητα PageSetup.IsAutomaticPaperSize και των δύο φύλλων εργασίας
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## συμπέρασμα
Σε αυτό το άρθρο, μάθαμε πώς να προσδιορίζουμε εάν το μέγεθος χαρτιού ενός φύλλου εργασίας είναι αυτόματο χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθήσαμε τα ακόλουθα βήματα: φόρτωση των βιβλίων εργασίας,

πρόσβαση σε υπολογιστικά φύλλα και αυτόματος έλεγχος μεγέθους χαρτιού. Τώρα μπορείτε να χρησιμοποιήσετε αυτή τη γνώση για να προσδιορίσετε εάν το μέγεθος χαρτιού των υπολογιστικών φύλλων σας είναι αυτόματο.

### Συχνές ερωτήσεις

#### Ε: Πώς μπορώ να φορτώσω βιβλία εργασίας με το Aspose.Cells για .NET;

Α: Μπορείτε να φορτώσετε βιβλία εργασίας χρησιμοποιώντας την κλάση Βιβλίο εργασίας από τη βιβλιοθήκη Aspose.Cells. Χρησιμοποιήστε τη μέθοδο Workbook.Load για να φορτώσετε ένα βιβλίο εργασίας από ένα αρχείο.

#### Ε: Μπορώ να ελέγξω το αυτόματο μέγεθος χαρτιού για άλλα υπολογιστικά φύλλα;

Α: Ναι, μπορείτε να ελέγξετε το αυτόματο μέγεθος χαρτιού για οποιοδήποτε φύλλο εργασίας αποκτώντας πρόσβαση στην ιδιότητα PageSetup.IsAutomaticPaperSize του αντίστοιχου αντικειμένου φύλλου εργασίας.

#### Ε: Πώς μπορώ να αλλάξω το αυτόματο μέγεθος χαρτιού ενός υπολογιστικού φύλλου;

Α: Για να αλλάξετε το αυτόματο μέγεθος χαρτιού ενός φύλλου εργασίας, μπορείτε να χρησιμοποιήσετε την ιδιότητα PageSetup.IsAutomaticPaperSize και να την ορίσετε στην επιθυμητή τιμή (true ή false).

#### Ε: Ποιες άλλες δυνατότητες προσφέρει το Aspose.Cells για .NET;

Α: Το Aspose.Cells για .NET προσφέρει πολλές δυνατότητες για εργασία με υπολογιστικά φύλλα, όπως δημιουργία, τροποποίηση και μετατροπή βιβλίων εργασίας, καθώς και χειρισμό δεδομένων, τύπων και μορφοποίησης.