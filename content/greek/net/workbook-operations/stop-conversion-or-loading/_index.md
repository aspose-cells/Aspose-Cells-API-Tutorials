---
title: Διακοπή μετατροπής ή φόρτωσης χρησιμοποιώντας την οθόνη διακοπής
linktitle: Διακοπή μετατροπής ή φόρτωσης χρησιμοποιώντας την οθόνη διακοπής
second_title: Aspose.Cells .NET Excel Processing API
description: Μάθετε να διακόπτετε τη μετατροπή βιβλίου εργασίας στο Aspose.Cells για .NET χρησιμοποιώντας την Παρακολούθηση Διακοπής, με λεπτομερή, βήμα προς βήμα εκμάθηση.
type: docs
weight: 26
url: /el/net/workbook-operations/stop-conversion-or-loading/
---
## Εισαγωγή
Η εργασία με μεγάλα αρχεία Excel συχνά περιλαμβάνει μακρές διαδικασίες που μπορεί να καταναλώσουν χρόνο και πόρους. Τι θα γινόταν όμως αν μπορούσατε να σταματήσετε τη διαδικασία μετατροπής στα μέσα του δρόμου όταν συνειδητοποιήσετε ότι κάτι χρειάζεται αλλαγή; Το Aspose.Cells για .NET διαθέτει μια δυνατότητα που ονομάζεται Παρακολούθηση Διακοπής, η οποία σας επιτρέπει να διακόψετε τη μετατροπή ενός βιβλίου εργασίας σε άλλη μορφή, όπως το PDF. Αυτό μπορεί να είναι σωτήριο, ειδικά όταν εργάζεστε με σημαντικά αρχεία δεδομένων. Σε αυτόν τον οδηγό, θα δούμε πώς μπορείτε να διακόψετε τη διαδικασία μετατροπής χρησιμοποιώντας το Interrupt Monitor στο Aspose.Cells για .NET.
## Προαπαιτούμενα
Πριν βουτήξετε, βεβαιωθείτε ότι έχετε στη θέση τους τα εξής:
1.  Aspose.Cells για .NET - Κάντε λήψη του[εδώ](https://releases.aspose.com/cells/net/).
2. .NET Development Environment - Όπως το Visual Studio.
3. Βασικές γνώσεις προγραμματισμού C# - Η εξοικείωση με τη σύνταξη της C# θα σας βοηθήσει να ακολουθήσετε.
## Εισαγωγή πακέτων
Για να ξεκινήσουμε, ας εισάγουμε τα απαραίτητα πακέτα. Αυτές οι εισαγωγές περιλαμβάνουν:
- Aspose.Cells: Η κύρια βιβλιοθήκη για το χειρισμό αρχείων Excel.
- System.Threading: Για τη διαχείριση νημάτων, όπως αυτό το παράδειγμα θα εκτελέσει δύο παράλληλες διεργασίες.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using System.IO;
```
Ας αναλύσουμε τη διαδικασία σε λεπτομερή βήματα. Κάθε βήμα θα σας βοηθήσει να κατανοήσετε τη σημασία της ρύθμισης και της χρήσης της Παρακολούθησης Διακοπής για τη διαχείριση της μετατροπής βιβλίου εργασίας του Excel.
## Βήμα 1: Δημιουργήστε τον κατάλογο κλάσης και ορίστε την έξοδο
Πρώτον, χρειαζόμαστε μια κλάση για να ενσωματώσουμε τις συναρτήσεις μας, μαζί με έναν κατάλογο όπου θα αποθηκευτεί το αρχείο εξόδου.
```csharp
class StopConversionOrLoadingUsingInterruptMonitor
{
    static string outputDir = "Your Document Directory";
}
```
 Αντικαθιστώ`"Your Document Directory"` με την πραγματική διαδρομή όπου θέλετε να αποθηκευτεί το αρχείο PDF.
## Βήμα 2: Δημιουργήστε την οθόνη διακοπής
Στη συνέχεια, δημιουργήστε ένα αντικείμενο InterruptMonitor. Αυτή η οθόνη θα βοηθήσει στον έλεγχο της διαδικασίας ρυθμίζοντας τη δυνατότητα διακοπής της σε οποιοδήποτε δεδομένο σημείο.
```csharp
InterruptMonitor im = new InterruptMonitor();
```
Αυτή η οθόνη διακοπής θα προσαρτηθεί στο βιβλίο εργασίας μας, επιτρέποντάς μας να διαχειριζόμαστε τη διαδικασία μετατροπής.
## Βήμα 3: Ρυθμίστε το βιβλίο εργασίας για μετατροπή
Τώρα, ας δημιουργήσουμε ένα αντικείμενο βιβλίου εργασίας, ας αντιστοιχίσουμε το InterruptMonitor σε αυτό και, στη συνέχεια, αποκτήστε πρόσβαση στο πρώτο φύλλο εργασίας για να εισαγάγετε κάποιο δείγμα κειμένου.
```csharp
void CreateWorkbookAndConvertItToPdfFormat()
{
    Workbook wb = new Workbook();
    wb.InterruptMonitor = im;
    Worksheet ws = wb.Worksheets[0];
    Cell cell = ws.Cells["J1000000"];
    cell.PutValue("This is text.");
}
```
Ο παραπάνω κώδικας δημιουργεί ένα βιβλίο εργασίας, ορίζει το InterruptMonitor για αυτό και τοποθετεί κείμενο σε ένα μακρινό κελί (`J1000000`). Η τοποθέτηση κειμένου σε αυτή τη θέση κελιού διασφαλίζει ότι η επεξεργασία του βιβλίου εργασίας θα είναι πιο χρονοβόρα, δίνοντας στο InterruptMonitor αρκετό χρόνο για να παρέμβει.
## Βήμα 4: Αποθηκεύστε το βιβλίο εργασίας ως PDF και χειριστείτε τη διακοπή
 Τώρα, ας προσπαθήσουμε να αποθηκεύσουμε το βιβλίο εργασίας ως PDF. Θα χρησιμοποιήσουμε α`try-catch` μπλοκ για να χειριστεί οποιαδήποτε διακοπή που μπορεί να προκύψει.
```csharp
try
{
    wb.Save(outputDir + "output_InterruptMonitor.pdf");
}
catch (Aspose.Cells.CellsException ex)
{
    Console.WriteLine("Process Interrupted - Message: " + ex.Message);
}
```
Εάν η διαδικασία διακοπεί, η εξαίρεση θα την καταλάβει και θα εμφανίσει ένα κατάλληλο μήνυμα. Διαφορετικά, το βιβλίο εργασίας θα αποθηκευτεί ως PDF.
## Βήμα 5: Διακοπή της διαδικασίας μετατροπής
 Το κύριο χαρακτηριστικό εδώ είναι η δυνατότητα διακοπής της διαδικασίας. Θα προσθέσουμε μια καθυστέρηση χρήσης`Thread.Sleep` και μετά καλέστε το`Interrupt()` μέθοδος διακοπής της μετατροπής μετά από 10 δευτερόλεπτα.
```csharp
void WaitForWhileAndThenInterrupt()
{
    Thread.Sleep(1000 * 10);
    im.Interrupt();
}
```
Αυτή η καθυστέρηση δίνει στο βιβλίο εργασίας χρόνο να ξεκινήσει τη μετατροπή σε PDF προτού σταλεί το σήμα διακοπής.
## Βήμα 6: Εκτελέστε τα νήματα ταυτόχρονα
Για να συνδυάσουμε τα πάντα, πρέπει να ξεκινήσουμε και τις δύο λειτουργίες σε ξεχωριστά νήματα. Με αυτόν τον τρόπο, η μετατροπή του βιβλίου εργασίας και η αναμονή διακοπής μπορούν να συμβούν ταυτόχρονα.
```csharp
public void TestRun()
{
    ThreadStart ts1 = new ThreadStart(this.CreateWorkbookAndConvertItToPdfFormat);
    Thread t1 = new Thread(ts1);
    t1.Start();
    ThreadStart ts2 = new ThreadStart(this.WaitForWhileAndThenInterrupt);
    Thread t2 = new Thread(ts2);
    t2.Start();
    t1.Join();
    t2.Join();
}
```
 Εκτελείται ο παραπάνω κώδικας`CreateWorkbookAndConvertItToPdfFormat` και`WaitForWhileAndThenInterrupt` σε παράλληλα νήματα, ενώνοντάς τα μόλις ολοκληρωθούν και οι δύο διεργασίες.
## Βήμα 7: Τελική εκτέλεση
 Τέλος, θα προσθέσουμε ένα`Run()` μέθοδο εκτέλεσης του κώδικα.
```csharp
public static void Run()
{
    new StopConversionOrLoadingUsingInterruptMonitor().TestRun();
    Console.WriteLine("StopConversionOrLoadingUsingInterruptMonitor executed successfully.");
}
```
 Αυτό`Run` μέθοδος είναι το σημείο εισόδου για την έναρξη και την παρατήρηση της διακοπής στη δράση.
## Σύναψη
Σε αυτό το σεμινάριο, εξερευνήσαμε τον τρόπο διακοπής της διαδικασίας μετατροπής στο Aspose.Cells για .NET. Το Interrupt Monitor είναι ένα χρήσιμο εργαλείο όταν εργάζεστε με μεγάλα αρχεία Excel, επιτρέποντάς σας να διακόπτετε τις διαδικασίες χωρίς να περιμένετε να ολοκληρωθούν. Αυτό είναι ιδιαίτερα χρήσιμο σε σενάρια όπου ο χρόνος και οι πόροι είναι πολύτιμοι και απαιτείται γρήγορη ανατροφοδότηση.
## Συχνές ερωτήσεις
### Τι είναι μια οθόνη διακοπής στο Aspose.Cells για .NET;  
Η Παρακολούθηση Διακοπής σάς επιτρέπει να διακόψετε τη μετατροπή ενός βιβλίου εργασίας ή να φορτώσετε τη διαδικασία εν μέρει.
### Μπορώ να χρησιμοποιήσω το Interrupt Monitor για άλλες μορφές εκτός από το PDF;  
Ναι, μπορείτε επίσης να διακόψετε τις μετατροπές σε άλλες υποστηριζόμενες μορφές.
### Πώς επηρεάζει το Thread.Sleep() το χρόνο διακοπής;  
Η Thread.Sleep() δημιουργεί μια καθυστέρηση πριν από την ενεργοποίηση της διακοπής, δίνοντας χρόνο για να ξεκινήσει η μετατροπή.
### Μπορώ να διακόψω τη διαδικασία πριν από 10 δευτερόλεπτα;  
 Ναι, τροποποιήστε την καθυστέρηση`WaitForWhileAndThenInterrupt()` σε μικρότερο χρονικό διάστημα.
### Η διαδικασία διακοπής θα επηρεάσει την απόδοση;  
Ο αντίκτυπος είναι ελάχιστος και είναι εξαιρετικά επωφελής για τη διαχείριση μακροχρόνιων διαδικασιών.
 Για περισσότερες πληροφορίες, ανατρέξτε στο[Aspose.Cells for .NET Documentation](https://reference.aspose.com/cells/net/) . Εάν χρειάζεστε βοήθεια, ελέγξτε το[Φόρουμ υποστήριξης](https://forum.aspose.com/c/cells/9)ή πάρτε ένα[Δωρεάν δοκιμή](https://releases.aspose.com/).