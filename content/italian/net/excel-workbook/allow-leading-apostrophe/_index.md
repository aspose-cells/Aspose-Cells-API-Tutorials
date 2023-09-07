---
title: Consenti l'apostrofo iniziale
linktitle: Consenti l'apostrofo iniziale
second_title: Riferimento all'API Aspose.Cells per .NET
description: Consenti l'apostrofo iniziale nelle cartelle di lavoro di Excel con Aspose.Cells per .NET.
type: docs
weight: 60
url: /it/net/excel-workbook/allow-leading-apostrophe/
---
In questo tutorial passo-passo, spiegheremo il codice sorgente C# fornito che ti consentirà di consentire l'uso di un apostrofo iniziale in una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Seguire i passaggi seguenti per eseguire questa operazione.

## Passaggio 1: imposta le directory di origine e di output

```csharp
// directory di origine
string sourceDir = RunExamples.Get_SourceDirectory();
// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

In questo primo passaggio, definiamo le directory di origine e di output per i file Excel.

## Passaggio 2: creare un'istanza di un oggetto WorkbookDesigner

```csharp
// Crea un'istanza di un oggetto WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Creiamo un'istanza di`WorkbookDesigner` classe da Aspose.Cells.

## Passaggio 3: caricare la cartella di lavoro di Excel

```csharp
//Carica la cartella di lavoro di Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Carichiamo la cartella di lavoro di Excel dal file specificato e disabilitiamo la conversione automatica degli apostrofi iniziali in stile di testo.

## Passaggio 4: impostare l'origine dati

```csharp
// Definire l'origine dati per la cartella di lavoro del progettista
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

 Definiamo un elenco di oggetti dati e usiamo il file`SetDataSource` metodo per impostare l'origine dati per la cartella di lavoro della finestra di progettazione.

## Passaggio 5: elaborare i marcatori intelligenti

```csharp
// Elabora marcatori intelligenti
designer. Process();
```

 Noi usiamo il`Process` metodo per elaborare i marcatori intelligenti nella cartella di lavoro del progettista.

## Passaggio 6: salvare la cartella di lavoro di Excel modificata

```csharp
// Salva la cartella di lavoro di Excel modificata
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Salviamo la cartella di lavoro di Excel modificata con le modifiche apportate.

### Esempio di codice sorgente per Consenti apostrofo iniziale utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Creazione di un'istanza di un oggetto WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Apri un foglio di lavoro per designer contenente marcatori intelligenti
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
// Imposta l'origine dati per il foglio di calcolo del designer
designer.SetDataSource("sampleData", list);
// Elabora i marcatori intelligenti
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Conclusione

Congratulazioni! Hai imparato come consentire l'uso di un apostrofo iniziale in una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Sperimenta con i tuoi dati per personalizzare ulteriormente le cartelle di lavoro di Excel.

### Domande frequenti

#### D: Qual è l'autorizzazione dell'apostrofo iniziale in una cartella di lavoro di Excel?

R: Consentire l'apostrofo iniziale in una cartella di lavoro di Excel consente di visualizzare correttamente i dati che iniziano con un apostrofo senza convertirli in uno stile di testo. Questo è utile quando vuoi mantenere l'apostrofo come parte dei dati.

#### D: Perché devo disattivare la conversione automatica degli apostrofi iniziali?

R: Disabilitando la conversione automatica delle virgolette principali, puoi preservarne l'uso così com'è nei tuoi dati. Ciò evita qualsiasi modifica involontaria dei dati durante l'apertura o la manipolazione della cartella di lavoro di Excel.

#### D: Come impostare l'origine dati nella cartella di lavoro del designer?

 R: Per impostare l'origine dati nella cartella di lavoro del progettista, puoi utilizzare il file`SetDataSource` metodo che specifica il nome dell'origine dati e un elenco di oggetti dati corrispondenti.

#### D: Consentire l'apostrofo iniziale influisce su altri dati nella cartella di lavoro di Excel?

R: No, consentire l'apostrofo iniziale influisce solo sui dati che iniziano con un apostrofo. Gli altri dati nella cartella di lavoro di Excel rimangono invariati.

#### D: Posso utilizzare questa funzione con altri formati di file Excel?

A: Sì, puoi utilizzare questa funzione con altri formati di file Excel supportati da Aspose.Cells, come .xls, .xlsm, ecc.