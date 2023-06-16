---
title: Esercitazione Aggiungi nuovo foglio in Excel C#
linktitle: Aggiungi nuovo foglio in Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come aggiungere un nuovo foglio in Excel utilizzando Aspose.Cells per .NET. Tutorial passo passo con codice sorgente in C#.
type: docs
weight: 20
url: /it/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
In questo tutorial, spiegheremo passo dopo passo il codice sorgente C# per aggiungere un nuovo foglio in Excel utilizzando Aspose.Cells per .NET. L'aggiunta di un nuovo foglio di lavoro a una cartella di lavoro di Excel è un'operazione comune durante la creazione di report o la manipolazione dei dati. Aspose.Cells è una potente libreria che semplifica la manipolazione e la generazione di file Excel utilizzando .NET. Seguire i passaggi seguenti per comprendere e implementare questo codice.

## Passaggio 1: impostazione della directory dei documenti

Il primo passaggio consiste nel definire la directory del documento in cui verrà salvato il file Excel. Se la directory non esiste, la creiamo utilizzando il seguente codice:

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Crea la directory se non esiste già.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

Assicurati di sostituire "LA TUA CARTELLA DEI DOCUMENTI" con il percorso appropriato alla tua directory dei documenti.

## Passaggio 2: creazione di un'istanza di un oggetto cartella di lavoro

Il secondo passaggio consiste nell'istanziare un oggetto Workbook, che rappresenta la cartella di lavoro di Excel. Usa il seguente codice:

```csharp
Workbook workbook = new Workbook();
```

Questo oggetto verrà utilizzato per aggiungere un nuovo foglio di lavoro ed eseguire altre operazioni sulla cartella di lavoro di Excel.

## Passaggio 3: aggiunta di un nuovo foglio di lavoro

Il terzo passaggio consiste nell'aggiungere un nuovo foglio di lavoro all'oggetto Workbook. Usa il seguente codice:

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

Questo aggiungerà un nuovo foglio di lavoro all'oggetto Workbook e otterrai un riferimento a questo foglio di lavoro usando il suo indice.

## Passaggio 4: impostazione del nome del nuovo foglio di lavoro

Il quarto passaggio consiste nell'assegnare un nome al nuovo foglio di lavoro. È possibile utilizzare il seguente codice per impostare il nome del foglio di lavoro:

```csharp
worksheet.Name = "My Worksheet";
```

Sostituisci "My Spreadsheet" con il nome desiderato per il nuovo foglio.

## Passaggio 5: salvare il file Excel

Infine, l'ultimo passaggio consiste nel salvare il file Excel. Usa il seguente codice:

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

Ciò salverà la cartella di lavoro di Excel con il nuovo foglio di lavoro nella directory dei documenti specificata.

### Esempio di codice sorgente per l'esercitazione Aggiungi nuovo foglio in Excel C# utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crea directory se non è già presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Aggiunta di un nuovo foglio di lavoro all'oggetto Workbook
int i = workbook.Worksheets.Add();
// Ottenere il riferimento del foglio di lavoro appena aggiunto passando il relativo indice del foglio
Worksheet worksheet = workbook.Worksheets[i];
// Impostazione del nome del foglio di lavoro appena aggiunto
worksheet.Name = "My Worksheet";
// Salvataggio del file Excel
workbook.Save(dataDir + "output.out.xls");
```

## Conclusione

Ora hai imparato come aggiungere un nuovo foglio di lavoro in Excel utilizzando Aspose.Cells per .NET. Puoi usare questo metodo per manipolare e generare file Excel usando C#. Aspose.Cells offre molte potenti funzionalità per semplificare la gestione dei file Excel nelle tue applicazioni.

### Domande frequenti (FAQ)

#### Posso usare Aspose.Cells con linguaggi di programmazione diversi da C#?

Sì, Aspose.Cells supporta più linguaggi di programmazione come Java, Python, Ruby e molti altri.

#### Posso aggiungere la formattazione alle celle nel foglio di lavoro appena creato?

A: Sì, puoi applicare la formattazione alle celle utilizzando i metodi forniti dalla classe Foglio di lavoro di Aspose.Cells. Puoi impostare lo stile della cella, cambiare il colore di sfondo, applicare i bordi, ecc.

#### Come posso accedere ai dati delle celle dal nuovo foglio di lavoro?

È possibile accedere ai dati delle celle utilizzando le proprietà ei metodi forniti dalla classe Worksheet di Aspose.Cells. Ad esempio, è possibile utilizzare la proprietà Cells per accedere a una cella specifica e recuperarne o modificarne il valore.

#### Aspose.Cells supporta le formule in Excel?

Sì, Aspose.Cells supporta le formule di Excel. È possibile impostare formule nelle celle del foglio di lavoro utilizzando il metodo SetFormula della classe Cell.
