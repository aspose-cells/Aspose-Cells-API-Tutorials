---
title: Raggruppamento dei dati nelle tabelle pivot
linktitle: Raggruppamento dei dati nelle tabelle pivot
second_title: Aspose.Cells API di elaborazione Java Excel
description: Scopri come creare tabelle pivot in Excel utilizzando Aspose.Cells per Java. Automatizza il raggruppamento e l'analisi dei dati con esempi di codice sorgente.
type: docs
weight: 14
url: /it/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

Le tabelle pivot sono un potente strumento per analizzare e riepilogare i dati nei fogli di calcolo. Ti consentono di raggruppare e classificare i dati per ottenere informazioni preziose. In questo articolo esploreremo come raggruppare in modo efficace i dati nelle tabelle pivot utilizzando Aspose.Cells per Java, insieme ad esempi di codice sorgente.

## introduzione

Le tabelle pivot forniscono un modo flessibile per organizzare e riepilogare i dati provenienti da set di dati di grandi dimensioni. Ti consentono di creare visualizzazioni personalizzate dei tuoi dati raggruppandoli in categorie o gerarchie. Ciò può aiutarti a identificare più facilmente tendenze, modelli e valori anomali nei tuoi dati.

## Passaggio 1: crea una tabella pivot

Iniziamo creando una tabella pivot utilizzando Aspose.Cells per Java. Di seguito è riportato un esempio di come creare una tabella pivot da un file Excel di esempio.

```java
// Carica il file Excel
Workbook workbook = new Workbook("sample.xlsx");

// Accedi al foglio di lavoro contenente i dati
Worksheet worksheet = workbook.getWorksheets().get(0);

// Specificare l'intervallo di dati
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // Supponendo 20 righe di dati
sourceData.startColumn = 0;
sourceData.endColumn = 3; // Supponendo 4 colonne di dati

// Crea una tabella pivot in base all'intervallo di dati
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Ottieni la tabella pivot per indice
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Aggiungi campi a righe e colonne
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Aggiungi valori e applica l'aggregazione
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Salva il file Excel modificato
workbook.save("output.xlsx");
```

## Passaggio 2: raggruppare i dati

 In Aspose.Cells per Java, puoi raggruppare i dati all'interno della tabella pivot utilizzando il file`PivotField` classe. Ecco un esempio di come raggruppare un campo nella tabella pivot:

```java
// Accedi al campo "Prodotto" nella tabella pivot
PivotField productField = pivotTable.getPivotFields().get("Product");

//Raggruppare il campo "Prodotto" in base a un criterio specifico, ad esempio per lettera iniziale
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Salva il file Excel modificato con i dati raggruppati
workbook.save("output_grouped.xlsx");
```

## Passaggio 3: personalizza il raggruppamento

È possibile personalizzare ulteriormente le impostazioni di raggruppamento, ad esempio specificando intervalli di raggruppamento basati sulla data o regole di raggruppamento personalizzate. Ecco un esempio di personalizzazione del raggruppamento basato sulla data:

```java
// Accedi al campo "Data" nella tabella pivot (supponendo che si tratti di un campo data)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Raggruppare le date per mese
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Salva il file Excel modificato con il raggruppamento di date personalizzato
workbook.save("output_custom_grouping.xlsx");
```

## Conclusione

Raggruppare i dati in tabelle pivot è una tecnica preziosa per analizzare e riepilogare i dati in Excel e Aspose.Cells per Java semplifica l'automazione di questo processo. Con gli esempi di codice sorgente forniti, puoi creare tabelle pivot, personalizzare il raggruppamento e ottenere informazioni approfondite dai tuoi dati in modo efficiente.

## Domande frequenti

### 1. Qual è lo scopo delle tabelle pivot in Excel?

Le tabelle pivot in Excel vengono utilizzate per riepilogare e analizzare set di dati di grandi dimensioni. Ti consentono di creare visualizzazioni personalizzate dei tuoi dati, semplificando l'identificazione di modelli e tendenze.

### 2. Come posso personalizzare il raggruppamento dei dati in una tabella pivot?

 È possibile personalizzare il raggruppamento dei dati in una tabella pivot utilizzando il file`PivotField` classe in Aspose.Cells per Java. Ciò consente di specificare criteri di raggruppamento, come intervalli basati sulla data o regole personalizzate.

### 3. Posso automatizzare la creazione di tabelle pivot utilizzando Aspose.Cells per Java?

Sì, puoi automatizzare la creazione di tabelle pivot in Excel utilizzando Aspose.Cells per Java, come dimostrato negli esempi di codice sorgente forniti.