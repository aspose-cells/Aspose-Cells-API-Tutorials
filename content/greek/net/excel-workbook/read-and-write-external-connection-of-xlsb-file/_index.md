---
title: Διαβάστε και γράψτε την εξωτερική σύνδεση του αρχείου XLSB
linktitle: Διαβάστε και γράψτε την εξωτερική σύνδεση του αρχείου XLSB
second_title: Aspose.Cells for .NET API Reference
description: Μάθετε πώς να διαβάζετε και να τροποποιείτε τις εξωτερικές συνδέσεις ενός αρχείου XLSB χρησιμοποιώντας το Aspose.Cells για .NET.
type: docs
weight: 130
url: /el/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Η ανάγνωση και η εγγραφή εξωτερικών συνδέσεων σε ένα αρχείο XLSB είναι απαραίτητη για τον χειρισμό δεδομένων από εξωτερικές πηγές στα βιβλία εργασίας του Excel. Με το Aspose.Cells για .NET μπορείτε εύκολα να διαβάσετε και να γράψετε εξωτερικές συνδέσεις ακολουθώντας τα παρακάτω βήματα:

## Βήμα 1: Καθορίστε τον κατάλογο προέλευσης και τον κατάλογο εξόδου

Αρχικά, πρέπει να καθορίσετε τον κατάλογο προέλευσης όπου βρίσκεται το αρχείο XLSB που περιέχει την εξωτερική σύνδεση, καθώς και τον κατάλογο εξόδου όπου θέλετε να αποθηκεύσετε το τροποποιημένο αρχείο. Δείτε πώς μπορείτε να το κάνετε χρησιμοποιώντας το Aspose.Cells:

```csharp
// κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();

// Κατάλογο εξόδου
string outputDir = RunExamples.Get_OutputDirectory();
```

## Βήμα 2: Φορτώστε το αρχείο προέλευσης Excel XLSB

Στη συνέχεια, πρέπει να φορτώσετε το αρχείο προέλευσης Excel XLSB στο οποίο θέλετε να εκτελέσετε λειτουργίες ανάγνωσης και εγγραφής εξωτερικής σύνδεσης. Εδώ είναι ένα δείγμα κώδικα:

```csharp
// Φορτώστε το αρχείο προέλευσης Excel XLSB
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Βήμα 3: Διαβάστε και τροποποιήστε την εξωτερική σύνδεση

Μετά τη φόρτωση του αρχείου, μπορείτε να αποκτήσετε πρόσβαση στην πρώτη εξωτερική σύνδεση που είναι στην πραγματικότητα μια σύνδεση βάσης δεδομένων. Μπορείτε να διαβάσετε και να τροποποιήσετε διάφορες ιδιότητες της εξωτερικής σύνδεσης. Δείτε πώς:

```csharp
// Διαβάστε την πρώτη εξωτερική σύνδεση που είναι μια σύνδεση βάσης δεδομένων
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Εμφάνιση του ονόματος σύνδεσης της βάσης δεδομένων, της εντολής και των πληροφοριών σύνδεσης
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Τροποποιήστε το όνομα της σύνδεσης
dbCon.Name = "NewCustomer";
```

## Βήμα 4: Αποθηκεύστε το αρχείο εξόδου Excel XLSB

Αφού κάνετε τις απαραίτητες αλλαγές, μπορείτε να αποθηκεύσετε το τροποποιημένο αρχείο Excel XLSB στον καθορισμένο κατάλογο εξόδου. Δείτε πώς να το κάνετε:

```csharp
// Αποθηκεύστε το αρχείο εξόδου Excel XLSB
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Δείγμα πηγαίου κώδικα για ανάγνωση και εγγραφή εξωτερικής σύνδεσης αρχείου XLSB χρησιμοποιώντας Aspose.Cells για .NET 
```csharp
//Κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
//Κατάλογο εξόδου
string outputDir = RunExamples.Get_OutputDirectory();
//Φορτώστε το αρχείο προέλευσης Excel Xlsb
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Διαβάστε την πρώτη εξωτερική σύνδεση που είναι στην πραγματικότητα μια σύνδεση DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Εκτυπώστε το όνομα, την εντολή και τις πληροφορίες σύνδεσης της σύνδεσης DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Τροποποιήστε το όνομα σύνδεσης
dbCon.Name = "NewCust";
//Αποθηκεύστε το αρχείο Xlsb του Excel
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## συμπέρασμα

Η ανάγνωση και η εγγραφή εξωτερικών συνδέσεων σε ένα αρχείο XLSB σάς επιτρέπει να χειρίζεστε δεδομένα από εξωτερικές πηγές στα βιβλία εργασίας του Excel. Με το Aspose.Cells για .NET, μπορείτε εύκολα να αποκτήσετε πρόσβαση σε εξωτερικές συνδέσεις, να διαβάσετε και να τροποποιήσετε πληροφορίες σύνδεσης και να αποθηκεύσετε αλλαγές. Πειραματιστείτε με τα δικά σας αρχεία XLSB και αξιοποιήστε τη δύναμη των εξωτερικών συνδέσεων στις εφαρμογές σας Excel.

### Συχνές ερωτήσεις

#### Ε: Τι είναι μια εξωτερική σύνδεση σε ένα αρχείο XLSB;
    
Α: Μια εξωτερική σύνδεση σε ένα αρχείο XLSB αναφέρεται σε μια σύνδεση που έχει δημιουργηθεί με μια εξωτερική πηγή δεδομένων, όπως μια βάση δεδομένων. Σας επιτρέπει να εισάγετε δεδομένα από αυτήν την εξωτερική πηγή στο βιβλίο εργασίας του Excel.

#### Ε: Μπορώ να έχω πολλές εξωτερικές συνδέσεις σε ένα αρχείο XLSB;
     
Α: Ναι, μπορείτε να έχετε πολλές εξωτερικές συνδέσεις σε ένα αρχείο XLSB. Μπορείτε να τα διαχειριστείτε μεμονωμένα, έχοντας πρόσβαση σε κάθε αντικείμενο σύνδεσης.

#### Ε: Πώς μπορώ να διαβάσω τις λεπτομέρειες μιας εξωτερικής σύνδεσης σε ένα αρχείο XLSB με το Aspose.Cells;
     
Α: Μπορείτε να χρησιμοποιήσετε τη λειτουργικότητα που παρέχεται από το Aspose.Cells για να αποκτήσετε πρόσβαση σε ιδιότητες μιας εξωτερικής σύνδεσης, όπως όνομα σύνδεσης, σχετική εντολή και πληροφορίες σύνδεσης.

#### Ε: Είναι δυνατή η τροποποίηση μιας εξωτερικής σύνδεσης σε ένα αρχείο XLSB με το Aspose.Cells;
     
Α: Ναι, μπορείτε να τροποποιήσετε τις ιδιότητες μιας εξωτερικής σύνδεσης, όπως το όνομα της σύνδεσης, για να καλύψετε τις συγκεκριμένες ανάγκες σας. Το Aspose.Cells παρέχει μεθόδους για να κάνετε αυτές τις αλλαγές.

#### Ε: Πώς μπορώ να αποθηκεύσω τις αλλαγές που έγιναν σε μια εξωτερική σύνδεση σε ένα αρχείο XLSB με το Aspose.Cells;
     
Α: Αφού κάνετε τις απαραίτητες αλλαγές σε μια εξωτερική σύνδεση, μπορείτε απλώς να αποθηκεύσετε το τροποποιημένο αρχείο Excel XLSB χρησιμοποιώντας την κατάλληλη μέθοδο που παρέχεται από το Aspose.Cells.