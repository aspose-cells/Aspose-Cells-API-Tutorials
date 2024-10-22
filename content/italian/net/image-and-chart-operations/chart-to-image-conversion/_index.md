---
title: Conversione da grafico a immagine in .NET
linktitle: Conversione da grafico a immagine in .NET
second_title: API di elaborazione Excel .NET Aspose.Cells
description: Scopri come convertire i grafici in immagini in .NET usando Aspose.Cells con questa guida passo-passo. Converti facilmente i grafici Excel in immagini di alta qualità.
type: docs
weight: 10
url: /it/net/image-and-chart-operations/chart-to-image-conversion/
---
## Introduzione
Convertire un grafico da Excel in un'immagine può essere un requisito cruciale quando si creano sistemi di reporting o si condividono rappresentazioni di dati visivi. Fortunatamente, con Aspose.Cells per .NET, questo processo è facile come bere un bicchier d'acqua! Che tu stia generando report o semplicemente convertendo grafici Excel in immagini per una migliore visualizzazione, questa guida ti guiderà passo dopo passo nel processo.
## Prerequisiti
Prima di iniziare, assicuriamoci che tutto sia a posto per seguire questo tutorial.
### Aspose.Cells per la libreria .NET
Per prima cosa, dovrai scaricare e fare riferimento alla libreria Aspose.Cells for .NET nel tuo progetto. Puoi prendere l'ultima versione qui:
- [Scarica Aspose.Cells per .NET](https://releases.aspose.com/cells/net/)
### Ambiente .NET
Assicurati di avere il framework .NET installato sul tuo sistema. Puoi usare Visual Studio o qualsiasi altro ambiente di sviluppo .NET per eseguire questo esempio.
### Impostazione della licenza (facoltativo)
 Sebbene tu possa utilizzare Aspose.Cells con una prova gratuita, per una funzionalità completa senza limitazioni, prendi in considerazione la possibilità di richiedere una[licenza temporanea](https://purchase.aspose.com/temporary-license/) oppure acquistane uno da[Qui](https://purchase.aspose.com/buy).

## Importa pacchetti
Per iniziare, importiamo i namespace necessari per lavorare con la libreria Aspose.Cells. Questo ci consentirà di manipolare file Excel e generare immagini.
```csharp
using System.IO;
using System.Drawing;
using Aspose.Cells;
```
Assicuratevi di avere pronti questi pacchetti prima di iniziare la parte di codifica.

Ora scomponiamo il processo di conversione di un grafico in un'immagine in semplici passaggi.
## Passaggio 1: imposta la directory del progetto
Hai bisogno di un posto dove salvare le immagini generate, giusto? Per prima cosa creiamo una directory in cui verranno salvate le immagini di output.

Iniziamo definendo il percorso per la nostra directory di documenti e assicurandoci che la cartella esista. In caso contrario, ne creeremo una.
```csharp
// Definisci la directory in cui salvare le immagini
string dataDir = "Your Document Directory";
// Controlla se la directory esiste
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
Con questo passaggio sei pronto per generare e salvare le immagini dei tuoi grafici in questa directory.
## Passaggio 2: creare una nuova cartella di lavoro
Qui, istanziamo un oggetto Workbook. Questo rappresenterà il nostro file Excel in cui verrà incorporato il grafico.

Una cartella di lavoro è come un file Excel che contiene fogli. Creando una nuova cartella di lavoro, stiamo ripartendo da zero con un file Excel vuoto.
```csharp
// Crea un nuovo oggetto Cartella di lavoro
Workbook workbook = new Workbook();
```
## Passaggio 3: aggiungere un nuovo foglio di lavoro
Ogni file Excel ha fogli di lavoro (o schede). Aggiungiamone uno alla nostra cartella di lavoro.

Aggiungere un nuovo foglio di lavoro è essenziale poiché inseriremo i nostri dati e grafici in questo foglio. Una volta aggiunto il foglio, recuperiamo il suo riferimento.
```csharp
// Aggiungere un nuovo foglio di lavoro alla cartella di lavoro
int sheetIndex = workbook.Worksheets.Add();
// Recupera il foglio di lavoro appena aggiunto
Worksheet worksheet = workbook.Worksheets[sheetIndex];
```
## Passaggio 4: popolare il foglio di lavoro con i dati
Per creare un grafico significativo, abbiamo bisogno di alcuni dati, giusto? Riempiamo alcune celle con valori campione.

Aggiungeremo dati a celle specifiche del foglio di lavoro. Questi dati saranno utilizzati per generare il nostro grafico in seguito.
```csharp
// Aggiungere dati campione alle celle
worksheet.Cells["A1"].PutValue(50);
worksheet.Cells["A2"].PutValue(100);
worksheet.Cells["A3"].PutValue(150);
worksheet.Cells["B1"].PutValue(4);
worksheet.Cells["B2"].PutValue(20);
worksheet.Cells["B3"].PutValue(50);
```
## Passaggio 5: aggiungere un grafico al foglio di lavoro
Ora creiamo un grafico a colonne che visualizzi i dati appena aggiunti.

Specifichiamo il tipo di grafico (istogramma) e ne definiamo le dimensioni e la posizione all'interno del foglio di lavoro.
```csharp
// Aggiungere un grafico a colonne al foglio di lavoro
int chartIndex = worksheet.Charts.Add(Aspose.Cells.Charts.ChartType.Column, 5, 0, 15, 5);
```
## Passaggio 6: definire l'origine dati del grafico
Ed è qui che avviene la magia: collegando il grafico ai dati nel foglio di lavoro!

Colleghiamo il grafico ai dati nelle colonne da A1 a B3. Questo indica al grafico da dove estrarre i dati.
```csharp
// Collega il grafico ai dati nell'intervallo A1 a B3
Aspose.Cells.Charts.Chart chart = worksheet.Charts[chartIndex];
chart.NSeries.Add("A1:B3", true);
```
## Passaggio 7: Convertire il grafico in un'immagine
Il momento della verità: convertiremo questo grafico in un file immagine!

 Qui utilizziamo il`ToImage`metodo per convertire il grafico in un formato immagine a tua scelta. In questo caso, lo stiamo convertendo in un formato EMF (Enhanced Metafile).
```csharp
// Convertire il grafico in un'immagine e salvarlo nella directory
chart.ToImage(dataDir + "Chart.emf", ImageFormat.Emf);
```
Ed ecco fatto! Il tuo grafico è stato salvato come immagine. È il momento di darti una pacca sulla spalla.
## Passaggio 8: visualizza il messaggio di successo
Per concludere, mostriamo un messaggio di conferma della generazione dell'immagine.
```csharp
// Visualizza un messaggio per indicare il successo
System.Console.WriteLine("Image generated successfully.");
```
## Conclusione
Boom! Ecco quanto è facile convertire un grafico da Excel a un'immagine usando Aspose.Cells per .NET. Questo processo non solo semplifica la presentazione dei dati, ma migliora anche la flessibilità di report o dashboard in cui le immagini sono preferite ai grafici incorporati.
Seguendo i passaggi descritti in questa guida, ora puoi convertire qualsiasi grafico Excel in un'immagine, integrando così senza problemi i dati visivi in varie applicazioni.
## Domande frequenti
### Posso convertire diversi tipi di grafici utilizzando questo metodo?
Sì, puoi convertire qualsiasi tipo di grafico supportato da Aspose.Cells, inclusi grafici a torta, grafici a barre, grafici a linee e altro ancora!
### È possibile cambiare il formato dell'immagine?
 Assolutamente! Mentre abbiamo utilizzato EMF in questo esempio, puoi cambiare il formato dell'immagine in PNG, JPEG, BMP e altri semplicemente modificando il`ImageFormat` parametro.
### Aspose.Cells supporta immagini ad alta risoluzione?
Sì, Aspose.Cells consente di controllare la risoluzione delle immagini e le impostazioni di qualità quando si esportano grafici in immagini.
### Posso convertire più grafici in immagini in una sola volta?
Sì, è possibile scorrere più grafici all'interno di una cartella di lavoro e convertirli tutti in immagini in poche righe di codice.
### Esiste un limite al numero di grafici che posso convertire?
Aspose.Cells non impone alcun limite intrinseco, ma l'elaborazione di grandi quantità di dati potrebbe dipendere dalla memoria e dalle prestazioni del sistema.