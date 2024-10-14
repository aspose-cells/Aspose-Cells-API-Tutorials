---
title: Αλλάξτε τη στοίχιση κελιών του Excel χωρίς απώλεια μορφοποίησης
linktitle: Αλλάξτε τη στοίχιση κελιών του Excel χωρίς απώλεια μορφοποίησης
second_title: Aspose.Cells .NET Excel Processing API
description: Μάθετε πώς μπορείτε να αλλάξετε τη στοίχιση κελιών του Excel χωρίς να χάσετε τη μορφοποίηση χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθήστε τον αναλυτικό μας οδηγό βήμα προς βήμα για απρόσκοπτο έλεγχο.
type: docs
weight: 10
url: /el/net/excel-data-alignment-formatting/change-cells-alignment-in-excel-without-losing-existing-formatting/
---
## Εισαγωγή

Η διαχείριση αρχείων Excel μπορεί μερικές φορές να μοιάζει σαν να πλοηγείστε σε έναν λαβύρινθο, ειδικά όταν πρόκειται για τη διατήρηση της μορφοποίησης, ενώ κάνετε ουσιαστικές προσαρμογές, όπως η αλλαγή στοίχισης κελιών. Εάν έχετε προσπαθήσει ποτέ να τροποποιήσετε την ευθυγράμμιση των κελιών στο Excel μόνο για να διαπιστώσετε ότι η μορφοποίηση διαταράσσεται, δεν είστε οι μόνοι! Σε αυτό το σεμινάριο, θα εμβαθύνουμε στον τρόπο αλλαγής της ευθυγράμμισης των κελιών του Excel χωρίς απώλεια μορφοποίησης, χρησιμοποιώντας το Aspose.Cells για .NET. Ας σηκώσουμε τα μανίκια και ας ξεκινήσουμε!

## Προαπαιτούμενα

Πριν βουτήξουμε στην πραγματική κωδικοποίηση, είναι σημαντικό να βεβαιωθείτε ότι έχετε ρυθμίσει τα πάντα σωστά. Εδώ είναι τι θα χρειαστείτε:

1. Visual Studio: Βεβαιωθείτε ότι έχετε εγκαταστήσει το Visual Studio (οποιαδήποτε έκδοση που υποστηρίζει .NET) στον υπολογιστή σας.
2.  Aspose.Cells για .NET: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης Aspose.Cells από[Ο ιστότοπος του Aspose](https://releases.aspose.com/cells/net/).
3. Βασικές γνώσεις C#: Λίγη εξοικείωση με τον προγραμματισμό C# θα σας φανεί χρήσιμη καθώς θα εργαζόμαστε σε ένα πλαίσιο C#.
4. Δείγμα αρχείου Excel: Για επίδειξη, ετοιμάστε ένα δείγμα αρχείου Excel (π.χ.`sampleChangeCellsAlignmentAndKeepExistingFormatting.xlsx`) που περιέχει κάποια αρχική μορφοποίηση κελιών.

## Εισαγωγή πακέτων

Το πρώτο βήμα για τη χρήση του Aspose.Cells για .NET είναι να συμπεριλάβετε τους απαραίτητους χώρους ονομάτων στο έργο σας. Δείτε πώς:

### Ανοίξτε το έργο σας

Ανοίξτε το Visual Studio και δημιουργήστε ένα νέο έργο C# (η εφαρμογή κονσόλας θα λειτουργήσει μια χαρά).

### Προσθήκη αναφοράς στο Aspose.Cells

- Κάντε δεξί κλικ στο έργο σας στην Εξερεύνηση λύσεων.
- Επιλέξτε "Διαχείριση πακέτων NuGet".
-  Αναζήτηση για`Aspose.Cells` και εγκαταστήστε το.

### Εισαγάγετε τους απαιτούμενους χώρους ονομάτων

Στην κορυφή του αρχείου C#, προσθέστε τα ακόλουθα χρησιμοποιώντας οδηγίες:

```csharp
using Aspose.Cells;
using Aspose.Cells.Drawing;
using Aspose.Cells.Tables;
```

Αυτό θα σας επιτρέψει να χρησιμοποιήσετε απρόσκοπτα τις κλάσεις και τις μεθόδους που παρέχονται από τη βιβλιοθήκη Aspose.Cells.

Τώρα που έχουμε ταξινομήσει τις προϋποθέσεις μας και εισάγουμε τα πακέτα, ας αναλύσουμε τη διαδικασία αλλαγής της ευθυγράμμισης των κελιών βήμα προς βήμα.

## Βήμα 1: Ρυθμίστε τους καταλόγους προέλευσης και εξόδου

Για να ξεκινήσετε, πρέπει να ορίσετε πού αποθηκεύεται το αρχείο Excel και πού θέλετε να το αποθηκεύσετε μετά την επεξεργασία.

```csharp
// Κατάλογος πηγής
string sourceDir = "Your Document Directory\\"; // Αντικαταστήστε τον με τον πραγματικό σας κατάλογο

// Κατάλογος εξόδου
string outputDir = "Your Document Directory\\"; // Αντικαταστήστε τον με τον πραγματικό σας κατάλογο
```

 Αυτός ο κώδικας ορίζει τις διαδρομές για τα αρχεία εισόδου και εξόδου. Φροντίστε να αντικαταστήσετε`"Your Document Directory\\"` με την πραγματική διαδρομή στον υπολογιστή σας.

## Βήμα 2: Φορτώστε το δείγμα αρχείου Excel

Στη συνέχεια, θα θέλετε να φορτώσετε το δείγμα αρχείου Excel στην εφαρμογή.

```csharp
// Φορτώστε δείγμα αρχείου Excel που περιέχει κελιά με μορφοποίηση.
Workbook wb = new Workbook(sourceDir + "sampleChangeCellsAlignmentAndKeepExistingFormatting.xlsx");
```

Αυτή η γραμμή κώδικα χρησιμοποιεί την κλάση Βιβλίο εργασίας για να φορτώσει το υπάρχον αρχείο Excel, ώστε να μπορούμε να χειριστούμε τα περιεχόμενά του.

## Βήμα 3: Πρόσβαση στο επιθυμητό φύλλο εργασίας

Μετά τη φόρτωση του βιβλίου εργασίας, αποκτήστε πρόσβαση στο φύλλο εργασίας που θέλετε να χειριστείτε. Τα αρχεία Excel μπορεί να έχουν πολλά φύλλα, επομένως βεβαιωθείτε ότι στοχεύετε το σωστό.

```csharp
// Πρόσβαση στο πρώτο φύλλο εργασίας.
Worksheet ws = wb.Worksheets[0];
```

Αυτό το παράδειγμα έχει πρόσβαση στο πρώτο φύλλο εργασίας. Εάν τα δεδομένα σας βρίσκονται σε διαφορετικό φύλλο, προσαρμόστε ανάλογα το ευρετήριο.

## Βήμα 4: Δημιουργήστε μια σειρά κελιών

Προσδιορίστε ποια κελιά θέλετε να αλλάξετε δημιουργώντας μια περιοχή. Αυτή η επιλογή θα επικεντρωθεί σε ένα καθορισμένο εύρος, όπως "B2:D7".

```csharp
// Δημιουργία εύρους κελιών.
Range rng = ws.Cells.CreateRange("B2:D7");
```

Αυτό το εύρος θα μας επιτρέψει να εφαρμόσουμε τις νέες ρυθμίσεις ευθυγράμμισης απευθείας σε αυτά τα κελιά.

## Βήμα 5: Δημιουργήστε και προσαρμόστε ένα αντικείμενο στυλ

Τώρα, πρέπει να ορίσουμε τα στυλ ευθυγράμμισης που θέλουμε να εφαρμόσουμε.

```csharp
// Δημιουργία αντικειμένου στυλ.
Style st = wb.CreateStyle();

// Ρυθμίστε την οριζόντια και κάθετη στοίχιση στο κέντρο.
st.HorizontalAlignment = TextAlignmentType.Center;
st.VerticalAlignment = TextAlignmentType.Center;
```

Εδώ, δημιουργείται ένα νέο αντικείμενο Style και ορίζουμε τόσο τις οριζόντιες όσο και τις κάθετες στοίχιση στο κέντρο. Αυτό είναι που θα βοηθήσει στην ακριβή ευθυγράμμιση του κειμένου στα επιλεγμένα κελιά.

## Βήμα 6: Ρύθμιση σημαιών στυλ

Η ρύθμιση των σημαιών στυλ παίζει κρίσιμο ρόλο στη διασφάλιση ότι εφαρμόζονται οι αλλαγές στυλ σας. 

```csharp
// Δημιουργία αντικειμένου σημαίας στυλ.
StyleFlag flag = new StyleFlag();

// Ορίστε τις ευθυγραμμίσεις σημαιών στυλ true. Είναι μια κρίσιμη δήλωση.
flag.Alignments = true;
```

 Ρυθμίζοντας το`Alignments` ιδιοκτησία του StyleFlag να`true`, λέτε στο Aspose.Cells να εφαρμόσει σωστά τα στυλ ευθυγράμμισης.

## Βήμα 7: Εφαρμόστε το στυλ στην περιοχή κελιών

Έχοντας τα στυλ και τις σημαίες σας στη θέση τους, ήρθε η ώρα να εφαρμόσετε αυτά τα στυλ στο εύρος των κελιών:

```csharp
// Εφαρμόστε στυλ σε εύρος κελιών.
rng.ApplyStyle(st, flag);
```

Αυτό το βήμα αλλάζει αποτελεσματικά τη στοίχιση όλων των κελιών εντός αυτού του εύρους, διατηρώντας ταυτόχρονα οποιαδήποτε υπάρχουσα μορφοποίηση.

## Βήμα 8: Αποθηκεύστε το βιβλίο εργασίας

Τέλος, θα θέλετε να αποθηκεύσετε τις αλλαγές σας σε ένα νέο αρχείο, ώστε να διατηρήσετε ανέπαφο το πρωτότυπο.

```csharp
// Αποθηκεύστε το βιβλίο εργασίας σε μορφή XLSX.
wb.Save(outputDir + "outputChangeCellsAlignmentAndKeepExistingFormatting.xlsx", SaveFormat.Xlsx);
```

Αυτή η γραμμή αποθηκεύει το βιβλίο εργασίας, μαζί με τις αλλαγές στοίχισης, στον κατάλογο εξόδου που καθορίστηκε προηγουμένως.

## Βήμα 9: Ειδοποίηση επιτυχίας

Μετά την αποθήκευση του αρχείου, είναι ωραίο να σχολιάσετε ότι όλα λειτούργησαν όπως αναμενόταν!

```csharp
Console.WriteLine("ChangeCellsAlignmentAndKeepExistingFormatting executed successfully.");
```

Αυτό το μήνυμα εμφανίζεται στην κονσόλα εάν η λειτουργία σας ολοκληρωθεί χωρίς προβλήματα.

## Σύναψη

Η αλλαγή της στοίχισης κελιών στο Excel διατηρώντας ανέπαφη την υπάρχουσα μορφοποίηση είναι μια απρόσκοπτη διαδικασία με το Aspose.Cells για .NET. Ακολουθώντας αυτά τα βήματα, μπορείτε να απλοποιήσετε τη διαχείριση του Excel στις εφαρμογές σας και να αποφύγετε τον πονοκέφαλο της απώλειας πολύτιμης μορφοποίησης. Είτε δημιουργείτε αναφορές είτε διαχειρίζεστε ροές δεδομένων, η εκμάθηση αυτής της ικανότητας μπορεί να αλλάξει το παιχνίδι!

## Συχνές ερωτήσεις

### Μπορεί το Aspose.Cells να χειριστεί μεγάλα αρχεία Excel;
Απολύτως! Είναι βελτιστοποιημένο για απόδοση και μπορεί να επεξεργαστεί αποτελεσματικά μεγάλα αρχεία.

### Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.Cells;
 Ναί! Μπορείτε να κατεβάσετε μια δωρεάν δοκιμή από τον ιστότοπο[Δωρεάν δοκιμή](https://releases.aspose.com/).

### Ποιες γλώσσες προγραμματισμού υποστηρίζει το Aspose.Cells;
Το Aspose.Cells υποστηρίζει κυρίως .NET, Java και πολλές άλλες γλώσσες μέσω αντίστοιχων βιβλιοθηκών.

### Πώς μπορώ να λάβω υποστήριξη για το Aspose.Cells;
 Για τυχόν απορίες ή ζητήματα που σχετίζονται με την υποστήριξη, επισκεφθείτε τη διεύθυνση[φόρουμ υποστήριξης](https://forum.aspose.com/c/cells/9).

### Μπορώ να εφαρμόσω πολλά στυλ ταυτόχρονα;
Ναι, μπορείτε να δημιουργήσετε πολλά αντικείμενα στυλ και να τα εφαρμόσετε διαδοχικά ή υπό όρους, όπως απαιτείται.