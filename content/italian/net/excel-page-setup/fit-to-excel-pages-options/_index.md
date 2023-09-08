---
title: Opzioni Adatta alle pagine Excel
linktitle: Opzioni Adatta alle pagine Excel
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come adattare automaticamente le pagine in un foglio di calcolo Excel con Aspose.Cells per .NET.
type: docs
weight: 30
url: /it/net/excel-page-setup/fit-to-excel-pages-options/
---
In questo articolo, ti guideremo passo dopo passo per spiegare il seguente codice sorgente C#: Adatta alle opzioni delle pagine Excel utilizzando Aspose.Cells per .NET. Utilizzeremo la libreria Aspose.Cells per .NET per eseguire questa operazione. Seguire i passaggi seguenti per configurare l'adattamento alle pagine in Excel.

## Passaggio 1: creazione di una cartella di lavoro
Il primo passo è creare una cartella di lavoro. Creeremo un'istanza di un oggetto cartella di lavoro. Ecco il codice per creare una cartella di lavoro:

```csharp
// Il percorso della directory dei documenti
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Creare un'istanza di un oggetto cartella di lavoro
Workbook workbook = new Workbook();
```

## Passaggio 2: accesso al foglio di lavoro
Ora che abbiamo creato la cartella di lavoro, dobbiamo passare al primo foglio di lavoro. Utilizzeremo l'indice 0 per accedere al primo foglio. Ecco il codice per accedervi:

```csharp
// Accesso al primo foglio di lavoro nella cartella di lavoro
Worksheet worksheet = workbook.Worksheets[0];
```

## Passaggio 3: impostazione dell'adattamento alle pagine
 In questo passaggio, configureremo l'adeguamento alle pagine del foglio di lavoro. Utilizzeremo il`FitToPagesTall` E`FitToPagesWide` proprietà del`PageSetup` oggetto per specificare il numero di pagine desiderato per l'altezza e la larghezza del foglio di lavoro. Ecco il codice per questo:

```csharp
// Configura il numero di pagine per l'altezza del foglio di lavoro
worksheet.PageSetup.FitToPagesTall = 1;

// Configura il numero di pagine per la larghezza del foglio di lavoro
worksheet.PageSetup.FitToPagesWide = 1;
```

## Passaggio 4: salvataggio della cartella di lavoro
 Ora che abbiamo configurato l'adattamento alle pagine, possiamo salvare la cartella di lavoro. Utilizzeremo il`Save` metodo dell'oggetto Workbook per questo. Ecco il codice per salvare la cartella di lavoro:

```csharp
// Salva la cartella di lavoro
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Codice sorgente di esempio per le opzioni Adatta alle pagine Excel utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un'istanza di un oggetto cartella di lavoro
Workbook workbook = new Workbook();
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Impostazione del numero di pagine a cui verrà estesa la lunghezza del foglio di lavoro
worksheet.PageSetup.FitToPagesTall = 1;
//Impostazione del numero di pagine a cui verrà estesa la larghezza del foglio di lavoro
worksheet.PageSetup.FitToPagesWide = 1;
// Salva la cartella di lavoro.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Conclusione
In questo articolo, abbiamo imparato come configurare l'adattamento alle pagine in Excel utilizzando Aspose.Cells per .NET. Abbiamo eseguito i seguenti passaggi: creazione della cartella di lavoro, accesso al foglio di lavoro, configurazione dell'adattamento alle pagine e salvataggio della cartella di lavoro. Ora puoi utilizzare questa conoscenza per adattare i tuoi fogli di calcolo alle pagine desiderate.

### Domande frequenti

#### D: Come posso installare Aspose.Cells per .NET?

R: Per installare Aspose.Cells per .NET, è possibile utilizzare il gestore pacchetti NuGet in Visual Studio. Trova il pacchetto "Aspose.Cells" e installalo nel tuo progetto.

#### D: Posso adattare le pagine sia in altezza che in larghezza?

 R: Sì, puoi regolare sia l'altezza che la larghezza del foglio di lavoro utilizzando`FitToPagesTall` E`FitToPagesWide` proprietà. È possibile specificare il numero di pagine desiderato per ciascuna dimensione.

#### D: Come posso personalizzare le opzioni Adatta alle pagine?

R: Oltre a specificare il numero di pagine, puoi anche personalizzare altre opzioni di adattamento alle pagine come la scala del foglio di lavoro, l'orientamento della carta, i margini e altro ancora. Utilizza le proprietà disponibili in`PageSetup` oggetto di questo.

#### D: Posso utilizzare Aspose.Cells per .NET per elaborare cartelle di lavoro esistenti?

R: Sì, puoi utilizzare Aspose.Cells per .NET per aprire e modificare cartelle di lavoro esistenti. Puoi accedere a fogli di lavoro, celle, formule, stili e altri elementi della cartella di lavoro per eseguire varie operazioni.