---
title: Rendi le pagine sequenziali in Aspose.Cells
linktitle: Rendi le pagine sequenziali in Aspose.Cells
second_title: API di elaborazione Excel .NET Aspose.Cells
description: Impara a eseguire il rendering di pagine sequenziali in Excel con Aspose.Cells per .NET. Questo tutorial passo dopo passo fornisce una guida dettagliata per convertire le pagine selezionate in immagini.
type: docs
weight: 18
url: /it/net/rendering-and-export/render-limited-number-of-sequential-pages/
---
## Introduzione
Il rendering di pagine specifiche da una cartella di lavoro Excel può essere incredibilmente utile, specialmente quando hai bisogno solo di determinati elementi visivi di dati senza l'intero file. Aspose.Cells per .NET è una potente libreria che offre un controllo preciso sui documenti Excel nelle applicazioni .NET, rendendo possibile il rendering di pagine selezionate, la modifica dei formati e altro ancora. Questo tutorial ti guida attraverso la conversione di pagine specifiche di fogli di lavoro Excel in formati immagine, ideali per creare snapshot di dati personalizzati.
## Prerequisiti
Prima di iniziare a scrivere il codice, assicurati di aver impostato i seguenti elementi:
-  Aspose.Cells per la libreria .NET: puoi[scaricalo qui](https://releases.aspose.com/cells/net/).
- Ambiente di sviluppo: qualsiasi ambiente supportato da .NET come Visual Studio.
- File Excel: un file Excel di esempio con più pagine, salvato nella directory locale.
 Inoltre, assicurati di ottenere una prova gratuita o di acquistare una licenza se non ne hai una. Dai un'occhiata a[licenza temporanea](https://purchase.aspose.com/temporary-license/) per scoprire tutte le funzionalità prima di effettuare un acquisto.
## Importa pacchetti
Per iniziare, dovremo importare Aspose.Cells e tutti gli spazi dei nomi necessari nel tuo ambiente .NET.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells.Rendering;
```
Questi pacchetti forniscono tutte le classi e i metodi necessari per manipolare e rendere i file Excel. Ora, analizziamo in dettaglio ogni parte del processo di rendering.
## Passaggio 1: impostare le directory di origine e di output
Per prima cosa definiamo le directory per i file di input e output, assicurandoci che il nostro programma sappia dove recuperare e archiviare i file.
```csharp
// Elenco di origine
string sourceDir = "Your Document Directory";
// Directory di uscita
string outputDir = "Your Document Directory";
```
Specificando le directory di origine e di output, ottimizzi l'accesso ai file sia per le operazioni di lettura che di scrittura. Assicurati che queste directory esistano per evitare errori di runtime.
## Passaggio 2: caricare il file Excel di esempio
 Successivamente, carichiamo il nostro file Excel utilizzando Aspose.Cells'`Workbook` classe. Questo file conterrà i dati e le pagine che vogliamo rendere.
```csharp
// Carica il file Excel di esempio
Workbook wb = new Workbook(sourceDir + "sampleImageOrPrintOptions_PageIndexPageCount.xlsx");
```
 IL`Workbook`La classe è come il gestore principale di Excel in Aspose.Cells, che fornisce accesso diretto a fogli, stili e altro ancora.
## Passaggio 3: accedere al foglio di lavoro di destinazione
Ora, selezioniamo il foglio di lavoro specifico con cui vogliamo lavorare. Per questo tutorial, useremo il primo foglio, ma puoi modificarlo in qualsiasi foglio di cui hai bisogno.
```csharp
// Accedi al primo foglio di lavoro
Worksheet ws = wb.Worksheets[0];
```
Ogni cartella di lavoro può avere più fogli di lavoro, e selezionare quello giusto è fondamentale. Questa riga garantisce l'accesso al foglio di lavoro specificato in cui avrà luogo il rendering.
## Passaggio 4: imposta le opzioni di immagine o stampa
Per controllare come vengono renderizzate le nostre pagine, definiremo alcune opzioni di stampa. Qui, specifichiamo quali pagine renderizzare, il formato dell'immagine e altre impostazioni.
```csharp
// Specificare le opzioni di immagine o stampa
ImageOrPrintOptions opts = new ImageOrPrintOptions();
opts.PageIndex = 3; // Inizia a pagina 4
opts.PageCount = 4; // Rendere quattro pagine
opts.ImageType = Drawing.ImageType.Png;
```
 Con`ImageOrPrintOptions` , puoi impostare`PageIndex` (la pagina iniziale),`PageCount` (numero di pagine da rendere) e`ImageType` (il formato per l'output). Questa configurazione ti dà un controllo preciso sul processo di rendering.
## Passaggio 5: creare un oggetto di rendering del foglio
Ora creiamo un`SheetRender` oggetto, che prenderà le nostre opzioni del foglio di lavoro e dell'immagine e renderà ogni pagina specificata come un'immagine.
```csharp
// Crea oggetto di rendering del foglio
SheetRender sr = new SheetRender(ws, opts);
```
 IL`SheetRender` class è essenziale per il rendering di fogli di lavoro in immagini, PDF o altri formati. Utilizza il foglio di lavoro e le opzioni che hai configurato per generare output.
## Passaggio 6: renderizzare e salvare ogni pagina come immagine
Infine, eseguiamo un ciclo su ogni pagina specificata e salviamola come immagine. Questo ciclo gestisce il rendering di ogni pagina e il suo salvataggio con un nome univoco.
```csharp
// Stampa tutte le pagine come immagini
for (int i = opts.PageIndex; i < sr.PageCount; i++)
{
    sr.ToImage(i, outputDir + "outputImage-" + (i + 1) + ".png");
}
```
Ecco una ripartizione di ciò che sta accadendo:
-  IL`for` il ciclo attraversa ogni pagina nell'intervallo specificato.
- `ToImage` viene utilizzato per rappresentare ogni pagina come un'immagine, con un formato di nome file personalizzato per distinguere ogni pagina.
## Passaggio 7: conferma il completamento
Aggiungere un semplice messaggio di conferma una volta completato il rendering. Questo passaggio è facoltativo ma può essere utile per verificare l'esecuzione corretta.
```csharp
Console.WriteLine("RenderLimitedNoOfSequentialPages executed successfully.\r\n");
```
Questa riga finale conferma che tutto ha funzionato come previsto. Vedrai questo messaggio nella tua console dopo che tutte le pagine saranno state renderizzate e salvate.
## Conclusione
Ed ecco fatto! Il rendering di pagine specifiche in una cartella di lavoro Excel con Aspose.Cells per .NET è un modo semplice ma potente per personalizzare l'output dei dati. Che tu abbia bisogno di uno snapshot di metriche chiave o di immagini di dati specifiche, questo tutorial ti copre. Seguendo questi passaggi, ora puoi eseguire il rendering di qualsiasi pagina o intervallo di pagine dai tuoi file Excel in splendidi formati immagine.
 Sentiti libero di esplorare altre opzioni all'interno`ImageOrPrintOptions` E`SheetRender` per un controllo ancora maggiore. Buona programmazione!
## Domande frequenti
### Posso eseguire il rendering di più fogli di lavoro contemporaneamente?  
 Sì, puoi scorrere il`Worksheets` raccolta e applicazione del processo di rendering individualmente a ciascun foglio.
### Oltre al PNG, in quali altri formati posso visualizzare le pagine?  
 Aspose.Cells supporta diversi formati, tra cui JPEG, BMP, TIFF e GIF. Basta cambiare`ImageType` In`ImageOrPrintOptions`.
### Come posso gestire file Excel di grandi dimensioni con molte pagine?  
Per i file di grandi dimensioni, si consiglia di suddividere il rendering in sezioni più piccole per gestire in modo efficace l'utilizzo della memoria.
### È possibile personalizzare la risoluzione dell'immagine?  
 SÌ,`ImageOrPrintOptions` consente di impostare DPI per una risoluzione personalizzata utilizzando`HorizontalResolution` E`VerticalResolution`.
### Cosa succede se devo visualizzare solo una parte di una pagina?  
Puoi usare il`PrintArea` proprietà in`PageSetup` per definire aree specifiche su un foglio di lavoro da riprodurre.