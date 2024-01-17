---
title: Προσθήκη ψηφιακής υπογραφής σε ένα ήδη υπογεγραμμένο αρχείο Excel
linktitle: Προσθήκη ψηφιακής υπογραφής σε ένα ήδη υπογεγραμμένο αρχείο Excel
second_title: Aspose.Cells for .NET API Reference
description: Προσθέστε εύκολα ψηφιακές υπογραφές σε υπάρχοντα αρχεία Excel με το Aspose.Cells για .NET.
type: docs
weight: 30
url: /el/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Σε αυτόν τον οδηγό βήμα προς βήμα, θα εξηγήσουμε τον παρεχόμενο πηγαίο κώδικα C# που θα σας επιτρέψει να προσθέσετε μια ψηφιακή υπογραφή σε ένα ήδη υπογεγραμμένο αρχείο Excel χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθήστε τα παρακάτω βήματα για να προσθέσετε μια νέα ψηφιακή υπογραφή σε ένα υπάρχον αρχείο Excel.

## Βήμα 1: Ορίστε καταλόγους πηγής και εξόδου

```csharp
// κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();

// Κατάλογο εξόδου
string outputDir = RunExamples.Get_OutputDirectory();
```

Σε αυτό το πρώτο βήμα, ορίζουμε τους καταλόγους προέλευσης και εξόδου που θα χρησιμοποιηθούν για τη φόρτωση του υπάρχοντος αρχείου Excel και την αποθήκευση του αρχείου με τη νέα ψηφιακή υπογραφή.

## Βήμα 2: Φορτώστε το υπάρχον αρχείο Excel

```csharp
// Φορτώστε το ήδη υπογεγραμμένο βιβλίο εργασίας του Excel
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Εδώ φορτώνουμε το ήδη υπογεγραμμένο αρχείο Excel χρησιμοποιώντας το`Workbook` κλάση Aspose.Κελιά.

## Βήμα 3: Δημιουργήστε τη συλλογή ψηφιακών υπογραφών

```csharp
// Δημιουργήστε τη συλλογή ψηφιακών υπογραφών
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Δημιουργούμε μια νέα συλλογή ψηφιακών υπογραφών χρησιμοποιώντας το`DigitalSignatureCollection` τάξη.

## Βήμα 4: Δημιουργήστε ένα νέο πιστοποιητικό

```csharp
// Δημιουργήστε ένα νέο πιστοποιητικό
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Εδώ δημιουργούμε ένα νέο πιστοποιητικό από το παρεχόμενο αρχείο και τον κωδικό πρόσβασης.

## Βήμα 5: Προσθέστε μια νέα ψηφιακή υπογραφή στη συλλογή

```csharp
// Δημιουργήστε μια νέα ψηφιακή υπογραφή
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Προσθέστε την ψηφιακή υπογραφή στη συλλογή
dsCollection.Add(signature);
```

 Δημιουργούμε μια νέα ψηφιακή υπογραφή χρησιμοποιώντας το`DigitalSignature` τάξη και προσθέστε το στη συλλογή ψηφιακών υπογραφών.

## Βήμα 6: Προσθέστε τη συλλογή ψηφιακών υπογραφών στο βιβλίο εργασίας

```csharp
//Προσθέστε τη συλλογή ψηφιακών υπογραφών στο βιβλίο εργασίας
workbook.AddDigitalSignature(dsCollection);
```

 Προσθέτουμε τη συλλογή ψηφιακών υπογραφών στο υπάρχον βιβλίο εργασίας του Excel χρησιμοποιώντας το`AddDigitalSignature()` μέθοδος.

## Βήμα 7: Αποθηκεύστε και κλείστε το βιβλίο εργασίας

```csharp
// Αποθηκεύστε το βιβλίο εργασίας και κλείστε το
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Αποθηκεύουμε το βιβλίο εργασίας με τη νέα ψηφιακή υπογραφή στον καθορισμένο κατάλογο εξόδου, το κλείνουμε και αποδεσμεύουμε τους σχετικούς πόρους.

### Δείγμα πηγαίου κώδικα για Προσθήκη ψηφιακής υπογραφής σε ένα ήδη υπογεγραμμένο αρχείο Excel χρησιμοποιώντας το Aspose.Cells για .NET 
```csharp
//Κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
//Κατάλογο εξόδου
string outputDir = RunExamples.Get_OutputDirectory();
//Το αρχείο πιστοποιητικού και ο κωδικός πρόσβασής του
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Φορτώστε το βιβλίο εργασίας που είναι ήδη ψηφιακά υπογεγραμμένο για να προσθέσετε νέα ψηφιακή υπογραφή
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Δημιουργήστε τη συλλογή ψηφιακών υπογραφών
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Δημιουργία νέου πιστοποιητικού
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Δημιουργήστε νέα ψηφιακή υπογραφή και προσθέστε τη στη συλλογή ψηφιακών υπογραφών
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Προσθέστε συλλογή ψηφιακών υπογραφών μέσα στο βιβλίο εργασίας
workbook.AddDigitalSignature(dsCollection);
//Αποθηκεύστε το βιβλίο εργασίας και απορρίψτε το.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## συμπέρασμα

Συγχαρητήρια ! Τώρα έχετε μάθει πώς να προσθέτετε μια ψηφιακή υπογραφή σε ένα ήδη υπογεγραμμένο αρχείο Excel χρησιμοποιώντας το Aspose.Cells για .NET. Οι ψηφιακές υπογραφές προσθέτουν ένα επιπλέον επίπεδο ασφάλειας στα αρχεία σας Excel, διασφαλίζοντας την αυθεντικότητα και την ακεραιότητά τους.

### FAQS

#### Ε: Τι είναι το Aspose.Cells για .NET;

Α: Το Aspose.Cells για .NET είναι μια ισχυρή βιβλιοθήκη κλάσεων που επιτρέπει στους προγραμματιστές .NET να δημιουργούν, να τροποποιούν, να μετατρέπουν και να χειρίζονται αρχεία Excel με ευκολία.

#### Ε: Τι είναι η ψηφιακή υπογραφή σε ένα αρχείο Excel;

Α: Η ψηφιακή υπογραφή σε ένα αρχείο Excel είναι ένα ηλεκτρονικό σήμα που εγγυάται τη γνησιότητα, την ακεραιότητα και την προέλευση του εγγράφου. Χρησιμοποιείται για την επαλήθευση ότι το αρχείο δεν έχει τροποποιηθεί από τότε που υπογράφηκε και προέρχεται από αξιόπιστη πηγή.

#### Ε: Ποια είναι τα οφέλη από την προσθήκη ψηφιακής υπογραφής σε ένα αρχείο Excel;

Α: Η προσθήκη ψηφιακής υπογραφής σε ένα αρχείο Excel παρέχει πολλά πλεονεκτήματα, όπως προστασία από μη εξουσιοδοτημένες αλλαγές, διασφάλιση της ακεραιότητας των δεδομένων, έλεγχος ταυτότητας του συντάκτη του εγγράφου και παροχή εμπιστοσύνης στις πληροφορίες που περιέχει.

#### Ε: Μπορώ να προσθέσω πολλές ψηφιακές υπογραφές σε ένα αρχείο Excel;

Α: Ναι, το Aspose.Cells σάς επιτρέπει να προσθέσετε πολλές ψηφιακές υπογραφές σε ένα αρχείο Excel. Μπορείτε να δημιουργήσετε μια συλλογή ψηφιακών υπογραφών και να τις προσθέσετε στο αρχείο με μία λειτουργία.

#### Ε: Ποιες είναι οι απαιτήσεις για την προσθήκη ψηφιακής υπογραφής σε αρχείο Excel;

Α: Για να προσθέσετε μια ψηφιακή υπογραφή σε ένα αρχείο Excel, χρειάζεστε ένα έγκυρο ψηφιακό πιστοποιητικό που θα χρησιμοποιηθεί για την υπογραφή του εγγράφου. Βεβαιωθείτε ότι έχετε το σωστό πιστοποιητικό και κωδικό πρόσβασης πριν προσθέσετε την ψηφιακή υπογραφή.