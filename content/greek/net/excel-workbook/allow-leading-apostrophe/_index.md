---
title: Allow Leading Apostrophe
linktitle: Allow Leading Apostrophe
second_title: Aspose.Cells for .NET API Reference
description: Να επιτρέπεται η κύρια απόστροφη σε βιβλία εργασίας του Excel με το Aspose.Cells για .NET.
type: docs
weight: 60
url: /el/net/excel-workbook/allow-leading-apostrophe/
---
Σε αυτό το βήμα προς βήμα σεμινάριο, θα εξηγήσουμε τον παρεχόμενο πηγαίο κώδικα C# που θα σας επιτρέψει να επιτρέψετε τη χρήση μιας κύριας απόστροφης σε ένα βιβλίο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET. Ακολουθήστε τα παρακάτω βήματα για να εκτελέσετε αυτήν τη λειτουργία.

## Βήμα 1: Ορίστε καταλόγους πηγής και εξόδου

```csharp
// κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
// Κατάλογο εξόδου
string outputDir = RunExamples.Get_OutputDirectory();
```

Σε αυτό το πρώτο βήμα, ορίζουμε τους καταλόγους προέλευσης και εξόδου για τα αρχεία Excel.

## Βήμα 2: Δημιουργήστε ένα αντικείμενο WorkbookDesigner

```csharp
// Δημιουργήστε ένα αντικείμενο WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Δημιουργούμε ένα παράδειγμα του`WorkbookDesigner` τάξη από το Aspose.Cells.

## Βήμα 3: Φορτώστε το βιβλίο εργασίας του Excel

```csharp
// Φορτώστε το βιβλίο εργασίας του Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Φορτώνουμε το βιβλίο εργασίας του Excel από το καθορισμένο αρχείο και απενεργοποιούμε την αυτόματη μετατροπή των αρχικών αποστρόφων σε στυλ κειμένου.

## Βήμα 4: Ορίστε την πηγή δεδομένων

```csharp
// Καθορίστε την προέλευση δεδομένων για το βιβλίο εργασίας σχεδιαστή
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Ορίζουμε μια λίστα αντικειμένων δεδομένων και χρησιμοποιούμε το`SetDataSource` μέθοδος ορισμού της προέλευσης δεδομένων για το βιβλίο εργασίας σχεδιαστή.

## Βήμα 5: Επεξεργαστείτε τους έξυπνους δείκτες

```csharp
// Επεξεργαστείτε έξυπνους δείκτες
designer. Process();
```

 Χρησιμοποιούμε το`Process` μέθοδος επεξεργασίας έξυπνων δεικτών στο βιβλίο εργασίας σχεδιαστή.

## Βήμα 6: Αποθηκεύστε το τροποποιημένο βιβλίο εργασίας του Excel

```csharp
// Αποθηκεύστε το τροποποιημένο βιβλίο εργασίας του Excel
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Αποθηκεύουμε το τροποποιημένο βιβλίο εργασίας του Excel με τις αλλαγές που έγιναν.

### Δείγμα πηγαίου κώδικα για το Allow Leading Apostrophe χρησιμοποιώντας Aspose.Cells για .NET 
```csharp
//Κατάλογος πηγής
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Δημιουργία αντικειμένου WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Ανοίξτε ένα υπολογιστικό φύλλο σχεδιαστή που περιέχει έξυπνους δείκτες
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Ορίστε την πηγή δεδομένων για το υπολογιστικό φύλλο σχεδιαστή
designer.SetDataSource("sampleData", list);
// Επεξεργαστείτε τους έξυπνους δείκτες
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## συμπέρασμα

Συγχαρητήρια ! Μάθατε πώς να επιτρέπεται η χρήση μιας κύριας απόστροφης σε ένα βιβλίο εργασίας του Excel χρησιμοποιώντας το Aspose.Cells για .NET. Πειραματιστείτε με τα δικά σας δεδομένα για να προσαρμόσετε περαιτέρω τα βιβλία εργασίας σας στο Excel.

### Συχνές ερωτήσεις

#### Ε: Τι είναι η άδεια κύριας απόστροφης σε ένα βιβλίο εργασίας του Excel;

Α: Επιτρέποντας την αρχική απόστροφο σε ένα βιβλίο εργασίας του Excel, τα δεδομένα που ξεκινούν με μια απόστροφο να εμφανίζονται σωστά χωρίς να τα μετατρέπουν σε στυλ κειμένου. Αυτό είναι χρήσιμο όταν θέλετε να διατηρήσετε την απόστροφο ως μέρος των δεδομένων.

#### Ε: Γιατί πρέπει να απενεργοποιήσω την αυτόματη μετατροπή των αρχικών αποστρόφων;

Α: Απενεργοποιώντας την αυτόματη μετατροπή των κορυφαίων εισαγωγικών, μπορείτε να διατηρήσετε τη χρήση τους ως έχει στα δεδομένα σας. Αυτό αποφεύγει οποιαδήποτε ακούσια τροποποίηση των δεδομένων κατά το άνοιγμα ή τον χειρισμό του βιβλίου εργασίας του Excel.

#### Ε: Πώς να ορίσετε την πηγή δεδομένων στο βιβλίο εργασίας σχεδιαστή;

 Α: Για να ορίσετε την προέλευση δεδομένων στο βιβλίο εργασίας σχεδιαστή, μπορείτε να χρησιμοποιήσετε το`SetDataSource` μέθοδος που καθορίζει το όνομα της προέλευσης δεδομένων και μια λίστα με τα αντίστοιχα αντικείμενα δεδομένων.

#### Ε: Το να επιτρέπεται η κύρια απόστροφος επηρεάζει άλλα δεδομένα στο βιβλίο εργασίας του Excel;

Α: Όχι, επιτρέποντας την κύρια απόστροφο επηρεάζει μόνο δεδομένα που ξεκινούν με απόστροφο. Άλλα δεδομένα στο βιβλίο εργασίας του Excel παραμένουν αμετάβλητα.

#### Ε: Μπορώ να χρησιμοποιήσω αυτήν τη δυνατότητα με άλλες μορφές αρχείων Excel;

Α: Ναι, μπορείτε να χρησιμοποιήσετε αυτήν τη δυνατότητα με άλλες μορφές αρχείων Excel που υποστηρίζονται από το Aspose.Cells, όπως .xls, .xlsm κ.λπ.