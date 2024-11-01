---
title: Ομαδοποιήστε γραμμές και στήλες στο Excel με το Aspose.Cells
linktitle: Ομαδοποιήστε γραμμές και στήλες στο Excel με το Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: Μάθετε πώς να ομαδοποιείτε σειρές και στήλες στο Excel χρησιμοποιώντας το Aspose.Cells για .NET με αυτόν τον οδηγό βήμα προς βήμα.
type: docs
weight: 12
url: /el/net/row-and-column-management/grouping-rows-and-columns/
---
## Εισαγωγή
Εάν εργάζεστε με μεγάλα φύλλα Excel, γνωρίζετε πόσο σημαντικό είναι να διατηρείτε τα πάντα καλά οργανωμένα και φιλικά προς το χρήστη. Η ομαδοποίηση γραμμών και στηλών σάς βοηθά να δημιουργήσετε ενότητες, κάνοντας την πλοήγηση στα δεδομένα πολύ πιο ομαλή. Με το Aspose.Cells για .NET, μπορείτε εύκολα να ομαδοποιήσετε γραμμές και στήλες στο Excel μέσω προγραμματισμού, δίνοντάς σας τον πλήρη έλεγχο της διάταξης των αρχείων σας.
Σε αυτό το σεμινάριο, θα δούμε όλα όσα χρειάζεται να γνωρίζετε για να ρυθμίσετε, να ομαδοποιήσετε και να αποκρύψετε σειρές και στήλες σε ένα φύλλο Excel με Aspose.Cells για .NET. Στο τέλος, θα μπορείτε να χειρίζεστε αρχεία Excel σαν επαγγελματίας χωρίς καν να ανοίξετε το ίδιο το Excel. Είστε έτοιμοι να βουτήξετε;
## Προαπαιτούμενα
Προτού μεταβούμε στον κώδικα, ας βεβαιωθούμε ότι τα έχετε όλα ρυθμισμένα και έτοιμα:
1.  Aspose.Cells for .NET Library: Θα χρειαστείτε αυτή τη βιβλιοθήκη για να εργαστείτε με αρχεία Excel. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cells/net/).
2. Visual Studio: Αυτό το σεμινάριο χρησιμοποιεί το Visual Studio για παραδείγματα κώδικα.
3. Βασικές γνώσεις C#: Η εξοικείωση με C# και .NET είναι χρήσιμη.
4. Aspose License: Απαιτείται πληρωμένη ή προσωρινή άδεια για την αποφυγή περιορισμών αξιολόγησης. Λάβετε προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).
## Εισαγωγή πακέτων
Για να ξεκινήσετε, εισαγάγετε τον απαραίτητο χώρο ονομάτων Aspose.Cells, μαζί με βασικές βιβλιοθήκες .NET για χειρισμό αρχείων. 
```csharp
using System.IO;
using Aspose.Cells;
```
Ας αναλύσουμε κάθε μέρος του κώδικα, διευκολύνοντας την παρακολούθηση και την κατανόηση.
## Βήμα 1: Ρύθμιση του καταλόγου δεδομένων σας
Πρώτα πράγματα πρώτα, πρέπει να ορίσουμε τη διαδρομή προς το αρχείο Excel με το οποίο θα εργαστούμε. Αυτή είναι συνήθως μια τοπική διαδρομή, αλλά θα μπορούσε επίσης να είναι μια διαδρομή σε ένα δίκτυο.
```csharp
// Η διαδρομή προς τον κατάλογο εγγράφων.
string dataDir = "Your Document Directory";
```
 Εδώ, αντικαταστήστε`"Your Document Directory"` με την πραγματική διαδρομή προς τα αρχεία Excel. Αυτή η ρύθμιση βοηθά τον κώδικά σας να βρει τα αρχεία στα οποία χρειάζεται να εργαστεί.
## Βήμα 2: Δημιουργήστε μια ροή αρχείων για πρόσβαση στο αρχείο Excel
Το Aspose.Cells απαιτεί να ανοίξετε το αρχείο μέσω μιας ροής αρχείου. Αυτή η ροή διαβάζει και φορτώνει τα περιεχόμενα του αρχείου για επεξεργασία.
```csharp
// Δημιουργία ροής αρχείων που περιέχει το αρχείο Excel που πρόκειται να ανοίξει
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```
 Ανοίγει ο παραπάνω κωδικός`book1.xls` από τον καθορισμένο κατάλογο σας. Εάν το αρχείο δεν υπάρχει, φροντίστε να το δημιουργήσετε ή να αλλάξετε το όνομα του αρχείου.
## Βήμα 3: Φορτώστε το βιβλίο εργασίας με το Aspose.Cells
Τώρα, ας αρχικοποιήσουμε το βιβλίο εργασίας μέσω του Aspose.Cells. Αυτό το βήμα μας δίνει πρόσβαση στο αρχείο Excel, επιτρέποντας τον εύκολο χειρισμό.
```csharp
// Άνοιγμα του αρχείου Excel μέσω της ροής αρχείων
Workbook workbook = new Workbook(fstream);
```
 Μετά από αυτή τη γραμμή, το`workbook` αντικείμενο θα περιέχει όλα τα δεδομένα και τη δομή από το αρχείο Excel. Σκεφτείτε το σαν να έχετε φορτώσει ολόκληρο το υπολογιστικό φύλλο στη μνήμη.
## Βήμα 4: Πρόσβαση στο φύλλο εργασίας που θέλετε να τροποποιήσετε
Το Aspose.Cells αποθηκεύει κάθε φύλλο εργασίας στο βιβλίο εργασίας ως ξεχωριστό αντικείμενο. Εδώ, επιλέγουμε το πρώτο φύλλο εργασίας.
```csharp
// Πρόσβαση στο πρώτο φύλλο εργασίας στο αρχείο Excel
Worksheet worksheet = workbook.Worksheets[0];
```
Εάν χρειάζεστε ένα συγκεκριμένο φύλλο εργασίας, μπορείτε να τροποποιήσετε αυτήν τη γραμμή για να αποκτήσετε πρόσβαση σε αυτό με όνομα ή ευρετήριο.
## Βήμα 5: Ομαδοποιήστε τις γραμμές στο φύλλο εργασίας
Τώρα ήρθε η ώρα για το διασκεδαστικό μέρος — την ομαδοποίηση σειρών! Ας ομαδοποιήσουμε τις έξι πρώτες σειρές και ας τις κρύψουμε.
```csharp
// Ομαδοποίηση έξι πρώτων σειρών (από το 0 έως το 5) και η απόκρυψή τους περνώντας true
worksheet.Cells.GroupRows(0, 5, true);
```
Δείτε τι κάνει κάθε παράμετρος:
- 0, 5: Τα ευρετήρια έναρξης και λήξης για τις σειρές που θέλετε να ομαδοποιήσετε. Στο Excel, η ευρετηρίαση σειρών ξεκινά από το 0.
- true: Η ρύθμιση σε true αποκρύπτει τις ομαδοποιημένες σειρές.
Μόλις εκτελεστούν, οι σειρές από το 0 έως το 5 θα ομαδοποιηθούν και θα κρυφτούν από την προβολή.
## Βήμα 6: Ομαδοποιήστε στήλες στο φύλλο εργασίας
Όπως και με τις σειρές, μπορείτε να ομαδοποιήσετε στήλες για να δημιουργήσετε μια πιο καθαρή, πιο οργανωμένη διάταξη. Δείτε πώς να ομαδοποιήσετε τις τρεις πρώτες στήλες.
```csharp
// Ομαδοποίηση των τριών πρώτων στηλών (από το 0 έως το 2) και η απόκρυψή τους περνώντας true
worksheet.Cells.GroupColumns(0, 2, true);
```
Οι παράμετροι αυτής της συνάρτησης είναι:
- 0, 2: Το εύρος των στηλών προς ομαδοποίηση, όπου η ευρετηρίαση ξεκινά από το 0.
- true: Αυτή η παράμετρος κρύβει τις ομαδοποιημένες στήλες.
Οι επιλεγμένες στήλες σας (0 έως 2) θα εμφανίζονται πλέον ομαδοποιημένες και κρυφές στο αρχείο Excel.
## Βήμα 7: Αποθηκεύστε το τροποποιημένο αρχείο Excel
Αφού κάνουμε αλλαγές, ας αποθηκεύσουμε το αρχείο με νέο όνομα για να αποφύγουμε την αντικατάσταση του πρωτοτύπου.
```csharp
// Αποθήκευση του τροποποιημένου αρχείου Excel
workbook.Save(dataDir + "output.xls");
```
 Τώρα έχετε αποθηκεύσει με επιτυχία τις ομαδοποιημένες σειρές και στήλες σας σε`output.xls`. Μπορείτε να προσαρμόσετε το όνομα αρχείου όπως απαιτείται.
## Βήμα 8: Κλείστε τη ροή αρχείων σε δωρεάν πόρους
Τέλος, κλείστε τη ροή αρχείων για να απελευθερώσετε τυχόν πόρους. Εάν δεν το κάνετε αυτό, μπορεί να προκληθούν προβλήματα εάν χρειαστεί να αποκτήσετε ξανά πρόσβαση ή να τροποποιήσετε το αρχείο.
```csharp
// Κλείσιμο της ροής αρχείων για να ελευθερωθούν όλοι οι πόροι
fstream.Close();
```
Και τέλος! Τώρα έχετε ομαδοποιήσει σειρές και στήλες σε ένα αρχείο Excel χρησιμοποιώντας το Aspose.Cells για .NET.
## Σύναψη
Η ομαδοποίηση γραμμών και στηλών στο Excel με το Aspose.Cells για .NET είναι μια απλή διαδικασία που μπορεί να κάνει τα υπολογιστικά φύλλα σας πολύ πιο φιλικά και οργανωμένα. Με λίγες μόνο γραμμές κώδικα, έχετε κατακτήσει μια ισχυρή δυνατότητα που θα έκανε περισσότερα βήματα εάν γινόταν με μη αυτόματο τρόπο στο Excel. Επιπλέον, μπορείτε να αυτοματοποιήσετε αυτή τη διαδικασία σε πολλά αρχεία, εξοικονομώντας χρόνο και μειώνοντας τα σφάλματα. Αυτός ο οδηγός σάς έχει δείξει όλα τα βήματα που χρειάζεστε για να αναλάβετε τον έλεγχο των αρχείων σας Excel μέσω προγραμματισμού.
## Συχνές ερωτήσεις
### Μπορώ να ομαδοποιήσω σειρές και στήλες χωρίς να τις αποκρύψω;  
 Ναί! Απλά περάστε`false` ως τρίτη παράμετρος στο`GroupRows` ή`GroupColumns` μέθοδος.
### Τι γίνεται αν θέλω να καταργήσω την ομαδοποίηση σειρών ή στηλών;  
 Χρήση`worksheet.Cells.UngroupRows(startRow, endRow)` ή`worksheet.Cells.UngroupColumns(startColumn, endColumn)` να τους αποομαδοποιήσετε.
### Μπορώ να ομαδοποιήσω πολλαπλές περιοχές στο ίδιο φύλλο εργασίας;  
 Απολύτως. Καλέστε το`GroupRows` ή`GroupColumns`μέθοδο σε κάθε εύρος που θέλετε να ομαδοποιήσετε.
### Χρειάζομαι άδεια χρήσης για να χρησιμοποιήσω το Aspose.Cells για .NET;  
 Ναι, ενώ είναι διαθέσιμη μια δοκιμαστική έκδοση, θα χρειαστείτε άδεια για να ξεκλειδώσετε την πλήρη λειτουργικότητα. Μπορείτε να πάρετε μια προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).
### Μπορώ να ομαδοποιήσω σειρές και στήλες με λογική υπό όρους;  
Ναί! Μπορείτε να δημιουργήσετε ομαδοποίηση υπό όρους ενσωματώνοντας λογική στον κώδικά σας πριν από την ομαδοποίηση, ανάλογα με τα δεδομένα σε κάθε γραμμή ή στήλη.