---
title: Αντιγραφή ρυθμίσεων ρύθμισης σελίδας από άλλο φύλλο εργασίας
linktitle: Αντιγραφή ρυθμίσεων ρύθμισης σελίδας από άλλο φύλλο εργασίας
second_title: Aspose.Cells for .NET API Reference
description: Μάθετε πώς να αντιγράφετε τις ρυθμίσεις διαμόρφωσης σελίδας από ένα υπολογιστικό φύλλο σε άλλο χρησιμοποιώντας το Aspose.Cells για .NET. Ένας βήμα προς βήμα οδηγός για τη βελτιστοποίηση της χρήσης αυτής της βιβλιοθήκης.
type: docs
weight: 10
url: /el/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Σε αυτό το άρθρο, θα σας οδηγήσουμε βήμα προς βήμα για να εξηγήσετε τον ακόλουθο πηγαίο κώδικα C#: Αντιγράψτε τις ρυθμίσεις διαμόρφωσης σελίδας από άλλο υπολογιστικό φύλλο χρησιμοποιώντας το Aspose.Cells για .NET. Θα χρησιμοποιήσουμε τη βιβλιοθήκη Aspose.Cells για .NET για να εκτελέσουμε αυτήν τη λειτουργία. Εάν θέλετε να αντιγράψετε τις ρυθμίσεις ρύθμισης σελίδας από το ένα φύλλο εργασίας στο άλλο, ακολουθήστε τα παρακάτω βήματα.

## Βήμα 1: Δημιουργία του βιβλίου εργασίας
Το πρώτο βήμα είναι να δημιουργήσετε ένα βιβλίο εργασίας. Στην περίπτωσή μας, θα χρησιμοποιήσουμε την κλάση Βιβλίο εργασίας που παρέχεται από τη βιβλιοθήκη Aspose.Cells. Εδώ είναι ο κώδικας για τη δημιουργία ενός βιβλίου εργασίας:

```csharp
Workbook wb = new Workbook();
```

## Βήμα 2: Προσθήκη φύλλων εργασίας δοκιμής
Αφού δημιουργήσουμε το βιβλίο εργασίας, πρέπει να προσθέσουμε δοκιμαστικά φύλλα εργασίας. Σε αυτό το παράδειγμα, θα προσθέσουμε δύο φύλλα εργασίας. Εδώ είναι ο κώδικας για την προσθήκη δύο φύλλων εργασίας:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Βήμα 3: Πρόσβαση σε φύλλα εργασίας
Τώρα που προσθέσαμε τα φύλλα εργασίας, πρέπει να έχουμε πρόσβαση σε αυτά για να μπορούμε να αλλάξουμε τις ρυθμίσεις τους. Θα έχουμε πρόσβαση στα φύλλα εργασίας "TestSheet1" και "TestSheet2" χρησιμοποιώντας τα ονόματά τους. Εδώ είναι ο κωδικός πρόσβασης:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Βήμα 4: Ρύθμιση μεγέθους χαρτιού
 Σε αυτό το βήμα, θα ορίσουμε το μέγεθος χαρτιού του φύλλου εργασίας "TestSheet1". Θα χρησιμοποιήσουμε το`PageSetup.PaperSize` ιδιότητα για να ορίσετε το μέγεθος του χαρτιού. Για παράδειγμα, θα ορίσουμε το μέγεθος χαρτιού σε "PaperA3ExtraTransverse". Εδώ είναι ο κωδικός για αυτό:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Βήμα 5: Αντιγραφή ρυθμίσεων ρύθμισης σελίδας
Τώρα θα αντιγράψουμε τις ρυθμίσεις διαμόρφωσης σελίδας από το φύλλο εργασίας "TestSheet1" στο "TestSheet2". Θα χρησιμοποιήσουμε το`PageSetup.Copy` μέθοδο εκτέλεσης αυτής της λειτουργίας. Εδώ είναι ο κωδικός για αυτό:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Βήμα 6: Εκτύπωση μεγεθών χαρτιού
 Αφού αντιγράψουμε τις ρυθμίσεις ρύθμισης σελίδας, θα εκτυπώσουμε τα μεγέθη χαρτιού των δύο φύλλων εργασίας. Θα το χρησιμοποιησουμε`Console.WriteLine` για να εμφανίσετε τα μεγέθη χαρτιού. Εδώ είναι ο κωδικός για αυτό:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Δείγμα πηγαίου κώδικα για Ρυθμίσεις ρύθμισης αντιγραφής σελίδας από άλλο φύλλο εργασίας χρησιμοποιώντας Aspose.Cells για .NET 
```csharp
//Δημιουργία βιβλίου εργασίας
Workbook wb = new Workbook();
//Προσθέστε δύο φύλλα εργασίας δοκιμής
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Πρόσβαση και στα δύο φύλλα εργασίας ως TestSheet1 και TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Ορίστε το Μέγεθος χαρτιού του TestSheet1 σε PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Εκτυπώστε το Μέγεθος χαρτιού και των δύο φύλλων εργασίας
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Αντιγράψτε το PageSetup από TestSheet1 στο TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Εκτυπώστε το Μέγεθος χαρτιού και των δύο φύλλων εργασίας
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## συμπέρασμα
Σε αυτό το άρθρο, μάθαμε πώς να αντιγράψουμε τις ρυθμίσεις διαμόρφωσης σελίδας από το ένα φύλλο εργασίας στο άλλο χρησιμοποιώντας το Aspose.Cells για .NET. Πραγματοποιήσαμε τα ακόλουθα βήματα: δημιουργία του βιβλίου εργασίας, προσθήκη δοκιμαστικών φύλλων εργασίας, πρόσβαση στα φύλλα εργασίας, ρύθμιση μεγέθους χαρτιού, αντιγραφή των ρυθμίσεων ρύθμισης σελίδας και εκτύπωση μεγεθών χαρτιού. Τώρα μπορείτε να χρησιμοποιήσετε αυτή τη γνώση για να αντιγράψετε τις ρυθμίσεις διαμόρφωσης σελίδας στα δικά σας έργα.

### Συχνές ερωτήσεις

#### Ε: Μπορώ να αντιγράψω τις ρυθμίσεις διαμόρφωσης σελίδας μεταξύ διαφορετικών παρουσιών βιβλίου εργασίας;

 Α: Ναι, μπορείτε να αντιγράψετε τις ρυθμίσεις ρύθμισης σελίδας μεταξύ διαφορετικών παρουσιών βιβλίου εργασίας χρησιμοποιώντας το`PageSetup.Copy` μέθοδος της βιβλιοθήκης Aspose.Cells.

#### Ε: Μπορώ να αντιγράψω άλλες ρυθμίσεις ρύθμισης σελίδας, όπως προσανατολισμό ή περιθώρια;

 Α: Ναι, μπορείτε να αντιγράψετε άλλες ρυθμίσεις ρύθμισης σελίδας χρησιμοποιώντας το`PageSetup.Copy` μέθοδος με τις κατάλληλες επιλογές. Για παράδειγμα, μπορείτε να αντιγράψετε τον προσανατολισμό χρησιμοποιώντας`CopyOptions.Orientation` και περιθώρια χρησιμοποιώντας`CopyOptions.Margins`.

#### Ε: Πώς μπορώ να ξέρω ποιες επιλογές είναι διαθέσιμες για το μέγεθος χαρτιού;

Α: Μπορείτε να ελέγξετε την Αναφορά API βιβλιοθήκης Aspose.Cells για διαθέσιμες επιλογές για το μέγεθος χαρτιού. Υπάρχει ένα enum που ονομάζεται`PaperSizeType` που παραθέτει τα διάφορα υποστηριζόμενα μεγέθη χαρτιού.

#### Ε: Πώς μπορώ να κατεβάσω τη βιβλιοθήκη Aspose.Cells για .NET;

 Α: Μπορείτε να κάνετε λήψη της βιβλιοθήκης Aspose.Cells για .NET από[Aspose Releases](https://releases.aspose.com/cells/net). Υπάρχουν διαθέσιμες δωρεάν δοκιμαστικές εκδόσεις, καθώς και άδειες επί πληρωμή για εμπορική χρήση.

#### Ε: Η βιβλιοθήκη Aspose.Cells υποστηρίζει άλλες γλώσσες προγραμματισμού;

Α: Ναι, η βιβλιοθήκη Aspose.Cells υποστηρίζει πολλές γλώσσες προγραμματισμού, όπως C#, Java, Python και πολλές άλλες.