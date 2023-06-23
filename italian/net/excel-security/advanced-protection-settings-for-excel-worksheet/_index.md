---
title: Impostazioni di protezione avanzate per foglio di lavoro Excel
linktitle: Impostazioni di protezione avanzate per foglio di lavoro Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Proteggi i tuoi file Excel impostando impostazioni di protezione avanzate con Aspose.Cells per .NET.
type: docs
weight: 10
url: /it/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
In questo tutorial, ti guideremo attraverso i passaggi per impostare le impostazioni di protezione avanzate per un foglio di calcolo Excel utilizzando la libreria Aspose.Cells per .NET. Seguire le istruzioni riportate di seguito per completare questa attività.

## Passaggio 1: preparazione

Assicurati di aver installato Aspose.Cells per .NET e di aver creato un progetto C# nel tuo ambiente di sviluppo integrato (IDE) preferito.

## Passaggio 2: impostare il percorso della directory del documento

 Dichiara un`dataDir` variabile e inizializzarla con il percorso della directory dei documenti. Per esempio :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIRECTORY"` con il percorso effettivo della tua directory.

## Passaggio 3: creare un flusso di file per aprire il file Excel

 Creare un`FileStream` oggetto contenente il file Excel da aprire:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Assicurati di avere il file Excel`book1.xls` nella directory dei documenti o specificare il nome file e la posizione corretti.

## Passaggio 4: creare un'istanza di un oggetto cartella di lavoro e aprire il file Excel

 Usa il`Workbook`class da Aspose.Cells per creare un'istanza di un oggetto Workbook e aprire il file Excel specificato tramite il flusso di file:

```csharp
Workbook excel = new Workbook(fstream);
```

## Passaggio 5: accedi al primo foglio di lavoro

Passare al primo foglio di lavoro del file Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Passaggio 6: impostare le impostazioni di protezione del foglio di lavoro

Utilizzare le proprietà dell'oggetto del foglio di lavoro per impostare le impostazioni di protezione del foglio di lavoro secondo necessità. Per esempio :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Impostare altre impostazioni di protezione secondo necessità...
```

## Passaggio 7: salvare il file Excel modificato

 Salvare il file Excel modificato utilizzando il file`Save` metodo dell'oggetto Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Assicurarsi di specificare il percorso e il nome file desiderati per il file di output.

## Passaggio 8: chiudi il flusso di file

Una volta salvato, chiudi il flusso di file per rilasciare tutte le risorse associate:

```csharp
fstream.Close();
```
	
### Esempio di codice sorgente per le impostazioni di protezione avanzate per il foglio di lavoro Excel utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Istanziare un oggetto Workbook
// Apertura del file Excel tramite il flusso di file
Workbook excel = new Workbook(fstream);
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = excel.Worksheets[0];
// Limitazione agli utenti di eliminare le colonne del foglio di lavoro
worksheet.Protection.AllowDeletingColumn = false;
// Limitare gli utenti a eliminare la riga del foglio di lavoro
worksheet.Protection.AllowDeletingRow = false;
// Limitazione agli utenti di modificare i contenuti del foglio di lavoro
worksheet.Protection.AllowEditingContent = false;
// Limitazione agli utenti di modificare gli oggetti del foglio di lavoro
worksheet.Protection.AllowEditingObject = false;
// Limitazione agli utenti di modificare gli scenari del foglio di lavoro
worksheet.Protection.AllowEditingScenario = false;
//Limitare gli utenti a filtrare
worksheet.Protection.AllowFiltering = false;
// Consentire agli utenti di formattare le celle del foglio di lavoro
worksheet.Protection.AllowFormattingCell = true;
// Consentire agli utenti di formattare le righe del foglio di lavoro
worksheet.Protection.AllowFormattingRow = true;
// Consentire agli utenti di inserire colonne nel foglio di lavoro
worksheet.Protection.AllowFormattingColumn = true;
// Consentire agli utenti di inserire collegamenti ipertestuali nel foglio di lavoro
worksheet.Protection.AllowInsertingHyperlink = true;
// Consentire agli utenti di inserire righe nel foglio di lavoro
worksheet.Protection.AllowInsertingRow = true;
// Consentire agli utenti di selezionare le celle bloccate del foglio di lavoro
worksheet.Protection.AllowSelectingLockedCell = true;
// Consentire agli utenti di selezionare le celle sbloccate del foglio di lavoro
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Consentire agli utenti di ordinare
worksheet.Protection.AllowSorting = true;
// Consentire agli utenti di utilizzare le tabelle pivot nel foglio di lavoro
worksheet.Protection.AllowUsingPivotTable = true;
// Salvataggio del file Excel modificato
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close();
```

## Conclusione

Congratulazioni! Ora hai imparato come configurare le impostazioni di protezione avanzate per un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Usa questa conoscenza per proteggere i tuoi file Excel e limitare le azioni degli utenti.

### Domande frequenti

#### D: Come posso creare un nuovo progetto C# nel mio IDE?

R: I passaggi per creare un nuovo progetto C# possono variare a seconda dell'IDE in uso. Consulta la documentazione del tuo IDE per istruzioni dettagliate.

#### D: È possibile impostare impostazioni di protezione personalizzate diverse da quelle menzionate nel tutorial?

A: Sì, Aspose.Cells offre una vasta gamma di impostazioni di protezione che è possibile personalizzare in base alle proprie esigenze specifiche. Vedere la documentazione di Aspose.Cells per ulteriori dettagli.

#### D: Qual è il formato file utilizzato per salvare il file Excel modificato nel codice di esempio?

R: Nel codice di esempio, il file Excel modificato viene salvato nel formato Excel 97-2003 (.xls). Puoi scegliere altri formati supportati da Aspose.Cells se necessario.

#### D: Come posso accedere ad altri fogli di lavoro nel file Excel?

 R: Puoi accedere ad altri fogli di lavoro utilizzando l'indice o il nome del foglio, ad esempio:`Worksheet worksheet = excel.Worksheets[1];` O`Worksheet worksheet = excel.Worksheets[" SheetName"];`.