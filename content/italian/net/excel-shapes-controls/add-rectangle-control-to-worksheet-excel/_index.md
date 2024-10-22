---
title: Aggiungere il controllo rettangolo al foglio di lavoro in Excel
linktitle: Aggiungere il controllo rettangolo al foglio di lavoro in Excel
second_title: API di elaborazione Excel .NET Aspose.Cells
description: Scopri come aggiungere un controllo rettangolo a un foglio di lavoro Excel utilizzando Aspose.Cells per .NET con una guida dettagliata e passo dopo passo.
type: docs
weight: 25
url: /it/net/excel-shapes-controls/add-rectangle-control-to-worksheet-excel/
---
## Introduzione
Quando si tratta di automatizzare le attività di Excel, Aspose.Cells per .NET è uno strumento potente che può aiutarti a raggiungere una serie di obiettivi, uno dei quali è aggiungere forme come rettangoli ai tuoi fogli di lavoro. In questa guida, esploreremo come aggiungere un controllo rettangolo a un foglio di lavoro Excel utilizzando Aspose.Cells per .NET. Alla fine, sarai in grado di creare, personalizzare e salvare un foglio di lavoro con un controllo rettangolo incorporato.
Ma prima di iniziare, parliamo dei prerequisiti.
## Prerequisiti
Per seguire questo tutorial, assicurati di avere i seguenti prerequisiti:
1.  Aspose.Cells per la libreria .NET: se non lo hai già fatto,[Scarica la libreria](https://releases.aspose.com/cells/net/) oppure installarlo utilizzando NuGet in Visual Studio.
2. .NET Framework: è necessario che sul computer sia installato l'ambiente di sviluppo .NET.
3. Conoscenza di base di C#: anche se ti guideremo passo dopo passo, una conoscenza di base di C# e della programmazione orientata agli oggetti sarà utile.
4.  Licenza: l'utilizzo di Aspose.Cells in modalità di valutazione funziona bene per le attività di base, ma per la piena funzionalità, si consiglia di prendere in considerazione l'acquisto di una[licenza temporanea](https://purchase.aspose.com/temporary-license/) acquistandone uno da[Qui](https://purchase.aspose.com/buy).
Adesso, immergiamoci nel codice!
## Importa pacchetti
Per iniziare con Aspose.Cells, assicurati di aver importato i namespace necessari nel tuo progetto. Queste importazioni consentiranno l'accesso a varie classi e metodi di cui hai bisogno per interagire con i file Excel.
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
Queste linee assicurano che il tuo progetto possa interagire con le directory dei file (`System.IO`), cartelle di lavoro di Excel (`Aspose.Cells`), e disegno della forma (`Aspose.Cells.Drawing`).
Ora scomponiamo il processo in semplici passaggi, così potrai seguirli facilmente e replicarli nei tuoi progetti.
## Passaggio 1: impostazione del percorso della directory
La prima cosa che devi fare è definire la directory in cui verrà salvato il tuo file Excel. Questo passaggio assicura che il tuo progetto sappia dove creare e archiviare il file di output.
### Definizione della directory dei dati
```csharp
// Percorso verso la directory dei documenti.
string dataDir = "Your Document Directory";
```
 Qui, specifichi il percorso della directory in cui verrà archiviato il file Excel. Puoi sostituire`"Your Document Directory"` con il percorso effettivo sul tuo computer oppure crea dinamicamente una cartella se non esiste.
### Controllo e creazione della directory
```csharp
//Creare la directory se non è già presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
Questo blocco controlla se la directory esiste. In caso contrario, ne crea una. Immagina di avere il tuo schedario pronto prima di archiviare qualsiasi documento.
## Passaggio 2: creazione di una nuova cartella di lavoro
 In questo passaggio, crei una nuova cartella di lavoro di Excel utilizzando`Aspose.Cells.Workbook` classe. Questo servirà come contenitore per il tuo foglio di lavoro e le tue forme.
```csharp
// Crea una nuova cartella di lavoro.
Workbook excelbook = new Workbook();
```
 Chiamando il`Workbook` costruttore, ora hai una cartella di lavoro Excel vuota pronta per la personalizzazione.
## Passaggio 3: aggiunta di un controllo rettangolo
Ecco dove avviene la magia. Aggiungerai una forma rettangolare al primo foglio di lavoro della tua cartella di lavoro.
```csharp
// Aggiungere un controllo rettangolare.
Aspose.Cells.Drawing.RectangleShape rectangle = excelbook.Worksheets[0].Shapes.AddRectangle(3, 0, 2, 0, 70, 130);
```
Analizziamolo nel dettaglio:
- `excelbook.Worksheets[0]`: Questo consente di accedere al primo foglio di lavoro della cartella di lavoro.
- `.Shapes.AddRectangle(3, 0, 2, 0, 70, 130)`: Aggiunge una forma rettangolare al foglio di lavoro. I parametri qui definiscono la posizione (riga e colonna), così come la larghezza e l'altezza del rettangolo.
## Passaggio 4: personalizzazione del rettangolo
Aggiungere semplicemente un rettangolo non è sufficiente: vorrai personalizzarlo. In questo passaggio, imposteremo il posizionamento, lo spessore della linea e lo stile del tratteggio del rettangolo.
### Impostazione del posizionamento
```csharp
// Imposta la posizione del rettangolo.
rectangle.Placement = PlacementType.FreeFloating;
```
Ciò specifica che il rettangolo è mobile, ovvero non sarà vincolato dalle dimensioni delle celle.
### Impostazione dello spessore della linea
```csharp
// Imposta lo spessore della linea.
rectangle.Line.Weight = 4;
```
Qui, impostiamo lo spessore della linea del rettangolo a 4 punti. Più alto è il numero, più spessa è la linea.
### Impostazione dello stile del trattino
```csharp
// Imposta lo stile del trattino del rettangolo.
rectangle.Line.DashStyle = MsoLineDashStyle.Solid;
```
 Questa linea imposta lo stile tratteggiato del bordo del rettangolo su solido. Puoi sperimentare stili diversi come`Dash` O`Dot` a seconda delle vostre esigenze.
## Passaggio 5: salvataggio della cartella di lavoro
Una volta aggiunto e personalizzato il rettangolo, il passaggio finale consiste nel salvare la cartella di lavoro nella directory specificata.
```csharp
// Salvare il file Excel.
excelbook.Save(dataDir + "book1.out.xls");
```
 Questo salva la cartella di lavoro come`.xls` file nella cartella definita in precedenza. Puoi modificare il formato del file cambiando l'estensione, ad esempio`.xlsx` se preferisci il formato Excel più recente.
## Conclusione
Ed ecco fatto! Aggiungere un controllo rettangolo a un foglio di lavoro Excel usando Aspose.Cells per .NET è un processo semplice una volta che lo si scompone passo dopo passo. Che tu abbia bisogno di aggiungere forme per un impatto visivo, evidenziare sezioni dei tuoi dati o personalizzare i tuoi report, Aspose.Cells ti offre la flessibilità di farlo a livello di programmazione.
Questa guida dovrebbe avervi fornito tutte le conoscenze necessarie per iniziare ad aggiungere forme come rettangoli ai vostri fogli Excel con Aspose.Cells. Ora è il momento di sperimentare e vedere cos'altro potete ottenere con questa potente libreria!
## Domande frequenti
### Posso aggiungere altre forme come cerchi o linee utilizzando Aspose.Cells per .NET?  
Sì, Aspose.Cells consente di aggiungere una varietà di forme, tra cui cerchi, linee, frecce e altro ancora.
### Quali altre proprietà posso impostare per il controllo rettangolo?  
È possibile personalizzare il colore di riempimento, il colore della linea, la trasparenza e persino aggiungere testo all'interno del rettangolo.
### Aspose.Cells è compatibile con .NET Core?  
Sì, Aspose.Cells supporta .NET Core, nonché .NET Framework e altre piattaforme basate su .NET.
### Posso posizionare il rettangolo rispetto a una cella specifica?  
 Sì, puoi posizionare il rettangolo all'interno di righe e colonne specifiche oppure utilizzare`PlacementType` per controllare come è ancorato.
### È disponibile una prova gratuita per Aspose.Cells?  
 Sì, puoi ottenere un[prova gratuita](https://releases.aspose.com/) dal sito web per testare le funzionalità della libreria prima dell'acquisto.