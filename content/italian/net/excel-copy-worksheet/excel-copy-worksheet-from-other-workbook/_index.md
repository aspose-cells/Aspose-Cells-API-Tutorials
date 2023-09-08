---
title: Copia foglio di lavoro Excel da un'altra cartella di lavoro
linktitle: Copia foglio di lavoro Excel da un'altra cartella di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Copia facilmente un foglio di lavoro Excel da una cartella di lavoro a un'altra utilizzando Aspose.Cells per .NET.
type: docs
weight: 10
url: /it/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
In questo tutorial, ti guideremo attraverso i passaggi per copiare un foglio di lavoro Excel da un'altra cartella di lavoro utilizzando la libreria Aspose.Cells per .NET. Seguire le istruzioni riportate di seguito per completare questa attività.

## Passaggio 1: preparazione

Prima di iniziare, assicurati di aver installato Aspose.Cells per .NET e di aver creato un progetto C# nel tuo ambiente di sviluppo integrato (IDE) preferito.

## Passaggio 2: impostare il percorso della directory del documento

 Dichiarare a`dataDir` variabile e inizializzala con il percorso della directory dei documenti. Per esempio :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIRECTORY"` con il percorso effettivo della directory.

## Passaggio 3: crea una nuova cartella di lavoro Excel

 Usa il`Workbook` classe da Aspose.Cells per creare una nuova cartella di lavoro di Excel:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Passaggio 4: ottieni il primo foglio di lavoro nella cartella di lavoro

Passare al primo foglio di lavoro nella cartella di lavoro utilizzando l'indice 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Passaggio 5: aggiungi dati alle righe di intestazione (A1:A4)

 Usare un`for` loop per aggiungere dati alle righe di intestazione (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Passaggio 6: aggiungere dati dettagliati (A5:A999)

 Usane un altro`for` ciclo per aggiungere dati dettagliati (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Passaggio 7: imposta le opzioni di layout

 Imposta le opzioni di impostazione della pagina per il foglio di lavoro utilizzando`PageSetup` oggetto:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Passaggio 8: crea un'altra cartella di lavoro Excel

Crea un'altra cartella di lavoro di Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Passaggio 9: ottieni il primo foglio di lavoro dalla seconda cartella di lavoro

Passare al primo foglio di lavoro nella seconda cartella di lavoro:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Passaggio 10: assegnare un nome al foglio di lavoro

dare un nome al fuoco

isola di calcolo:

```csharp
ws1.Name = "MySheet";
```

## Passaggio 11: copiare i dati dal primo foglio di lavoro della prima cartella di lavoro al primo foglio di lavoro della seconda cartella di lavoro

Copia i dati dal primo foglio di lavoro della prima cartella di lavoro al primo foglio di lavoro della seconda cartella di lavoro:

```csharp
ws1.Copy(ws0);
```

## Passaggio 12: salva il file Excel

Salvare il file Excel:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Assicurati di specificare il percorso e il nome file desiderati per il file di output.

### Codice sorgente di esempio per copiare il foglio di lavoro di Excel da un'altra cartella di lavoro utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crea una nuova cartella di lavoro.
Workbook excelWorkbook0 = new Workbook();
// Ottieni il primo foglio di lavoro nel libro.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Inserisci alcuni dati nelle righe di intestazione (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Inserisci alcuni dati dettagliati (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Definire un oggetto pagesetup in base al primo foglio di lavoro.
PageSetup pagesetup = ws0.PageSetup;
// Le prime cinque righe si ripetono in ogni pagina...
// Può essere visto nell'anteprima di stampa.
pagesetup.PrintTitleRows = "$1:$5";
// Crea un'altra cartella di lavoro.
Workbook excelWorkbook1 = new Workbook();
// Ottieni il primo foglio di lavoro nel libro.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Assegna un nome al foglio di lavoro.
ws1.Name = "MySheet";
// Copia i dati dal primo foglio di lavoro della prima cartella di lavoro nel file
// primo foglio di lavoro del secondo quaderno di esercizi.
ws1.Copy(ws0);
// Salva il file Excel.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Conclusione

Congratulazioni! Ora hai imparato come copiare un foglio di lavoro Excel da un'altra cartella di lavoro utilizzando Aspose.Cells per .NET. Sentiti libero di utilizzare questo metodo nei tuoi progetti per manipolare in modo efficiente i file Excel.

### Domande frequenti

#### D. Quali librerie sono necessarie per utilizzare Aspose.Cells per .NET?

A. Per utilizzare Aspose.Cells per .NET, è necessario includere la libreria Aspose.Cells nel progetto. Assicurati di aver fatto riferimento correttamente a questa libreria nel tuo ambiente di sviluppo integrato (IDE).

#### D. Aspose.Cells supporta altri formati di file Excel, come XLSX?

A. Sì, Aspose.Cells supporta vari formati di file Excel tra cui XLSX, XLS, CSV, HTML e molti altri. È possibile manipolare questi formati di file utilizzando le funzionalità di Aspose.Cells per .NET.

#### D. Posso personalizzare le opzioni di layout durante la copia del foglio di lavoro?

A.  Sì, puoi personalizzare le opzioni di impostazione della pagina quando copi il foglio di lavoro utilizzando le proprietà del file`PageSetup` oggetto. È possibile specificare intestazioni di pagina, piè di pagina, margini, orientamenti, ecc.