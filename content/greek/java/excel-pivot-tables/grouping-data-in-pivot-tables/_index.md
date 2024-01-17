---
title: Ομαδοποίηση δεδομένων σε συγκεντρωτικούς πίνακες
linktitle: Ομαδοποίηση δεδομένων σε συγκεντρωτικούς πίνακες
second_title: Aspose.Cells Java Excel Processing API
description: Μάθετε πώς να δημιουργείτε συγκεντρωτικούς πίνακες στο Excel χρησιμοποιώντας το Aspose.Cells για Java. Αυτοματοποιήστε την ομαδοποίηση και ανάλυση δεδομένων με παραδείγματα πηγαίου κώδικα.
type: docs
weight: 14
url: /el/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

Οι συγκεντρωτικοί πίνακες είναι ένα ισχυρό εργαλείο για την ανάλυση και τη σύνοψη δεδομένων σε υπολογιστικά φύλλα. Σας επιτρέπουν να ομαδοποιήσετε και να κατηγοριοποιήσετε δεδομένα για να αποκτήσετε πολύτιμες πληροφορίες. Σε αυτό το άρθρο, θα διερευνήσουμε πώς να ομαδοποιήσετε αποτελεσματικά δεδομένα σε συγκεντρωτικούς πίνακες χρησιμοποιώντας το Aspose.Cells για Java, μαζί με παραδείγματα πηγαίου κώδικα.

## Εισαγωγή

Οι συγκεντρωτικοί πίνακες παρέχουν έναν ευέλικτο τρόπο οργάνωσης και σύνοψης δεδομένων από μεγάλα σύνολα δεδομένων. Σας επιτρέπουν να δημιουργήσετε προσαρμοσμένες προβολές των δεδομένων σας ομαδοποιώντας τα σε κατηγορίες ή ιεραρχίες. Αυτό μπορεί να σας βοηθήσει να εντοπίσετε πιο εύκολα τάσεις, μοτίβα και ακραίες τιμές στα δεδομένα σας.

## Βήμα 1: Δημιουργήστε έναν Συγκεντρωτικό Πίνακα

Ας ξεκινήσουμε δημιουργώντας έναν συγκεντρωτικό πίνακα χρησιμοποιώντας το Aspose.Cells για Java. Παρακάτω είναι ένα παράδειγμα του τρόπου δημιουργίας ενός συγκεντρωτικού πίνακα από ένα δείγμα αρχείου Excel.

```java
// Φορτώστε το αρχείο Excel
Workbook workbook = new Workbook("sample.xlsx");

// Πρόσβαση στο φύλλο εργασίας που περιέχει τα δεδομένα
Worksheet worksheet = workbook.getWorksheets().get(0);

// Καθορίστε το εύρος δεδομένων
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // Υποθέτοντας 20 σειρές δεδομένων
sourceData.startColumn = 0;
sourceData.endColumn = 3; // Υποθέτοντας 4 στήλες δεδομένων

// Δημιουργήστε έναν συγκεντρωτικό πίνακα με βάση το εύρος δεδομένων
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Λάβετε τον συγκεντρωτικό πίνακα ανά ευρετήριο
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Προσθήκη πεδίων σε γραμμές και στήλες
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Προσθέστε τιμές και εφαρμόστε τη συγκέντρωση
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Αποθηκεύστε το τροποποιημένο αρχείο Excel
workbook.save("output.xlsx");
```

## Βήμα 2: Ομαδικά δεδομένα

 Στο Aspose.Cells για Java, μπορείτε να ομαδοποιήσετε δεδομένα εντός του συγκεντρωτικού πίνακα χρησιμοποιώντας το`PivotField` τάξη. Ακολουθεί ένα παράδειγμα του τρόπου ομαδοποίησης ενός πεδίου στον συγκεντρωτικό πίνακα:

```java
// Πρόσβαση στο πεδίο "Προϊόν" στον συγκεντρωτικό πίνακα
PivotField productField = pivotTable.getPivotFields().get("Product");

//Ομαδοποιήστε το πεδίο "Προϊόν" με ένα συγκεκριμένο κριτήριο, π.χ. με αρχικό γράμμα
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Αποθηκεύστε το τροποποιημένο αρχείο Excel με ομαδοποιημένα δεδομένα
workbook.save("output_grouped.xlsx");
```

## Βήμα 3: Προσαρμογή της Ομαδοποίησης

Μπορείτε να προσαρμόσετε περαιτέρω τις ρυθμίσεις ομαδοποίησης, όπως τον καθορισμό διαστημάτων ομαδοποίησης βάσει ημερομηνίας ή προσαρμοσμένων κανόνων ομαδοποίησης. Ακολουθεί ένα παράδειγμα προσαρμογής ομαδοποίησης βάσει ημερομηνίας:

```java
// Πρόσβαση στο πεδίο "Ημερομηνία" στον συγκεντρωτικό πίνακα (υποθέτοντας ότι πρόκειται για πεδίο ημερομηνίας)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Ημερομηνίες ομάδας ανά μήνες
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Αποθηκεύστε το τροποποιημένο αρχείο Excel με προσαρμοσμένη ομαδοποίηση ημερομηνιών
workbook.save("output_custom_grouping.xlsx");
```

## συμπέρασμα

Η ομαδοποίηση δεδομένων σε συγκεντρωτικούς πίνακες είναι μια πολύτιμη τεχνική για την ανάλυση και τη σύνοψη δεδομένων στο Excel και το Aspose.Cells για Java διευκολύνει την αυτοματοποίηση αυτής της διαδικασίας. Με τα παρεχόμενα παραδείγματα πηγαίου κώδικα, μπορείτε να δημιουργήσετε συγκεντρωτικούς πίνακες, να προσαρμόσετε την ομαδοποίηση και να αποκτήσετε αποτελεσματικά πληροφορίες από τα δεδομένα σας.

## Συχνές ερωτήσεις

### 1. Ποιος είναι ο σκοπός των συγκεντρωτικών πινάκων στο Excel;

Οι συγκεντρωτικοί πίνακες στο Excel χρησιμοποιούνται για τη σύνοψη και την ανάλυση μεγάλων συνόλων δεδομένων. Σας επιτρέπουν να δημιουργείτε προσαρμοσμένες προβολές των δεδομένων σας, διευκολύνοντας τον εντοπισμό μοτίβων και τάσεων.

### 2. Πώς μπορώ να προσαρμόσω την ομαδοποίηση δεδομένων σε έναν συγκεντρωτικό πίνακα;

 Μπορείτε να προσαρμόσετε την ομαδοποίηση δεδομένων σε έναν συγκεντρωτικό πίνακα χρησιμοποιώντας το`PivotField` κλάση στο Aspose.Cells για Java. Αυτό σας επιτρέπει να καθορίσετε κριτήρια ομαδοποίησης, όπως διαστήματα βάσει ημερομηνίας ή προσαρμοσμένους κανόνες.

### 3. Μπορώ να αυτοματοποιήσω τη δημιουργία συγκεντρωτικών πινάκων χρησιμοποιώντας το Aspose.Cells για Java;

Ναι, μπορείτε να αυτοματοποιήσετε τη δημιουργία συγκεντρωτικών πινάκων στο Excel χρησιμοποιώντας το Aspose.Cells για Java, όπως φαίνεται στα παρεχόμενα παραδείγματα πηγαίου κώδικα.