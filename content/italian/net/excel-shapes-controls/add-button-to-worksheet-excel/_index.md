---
title: Aggiungere un pulsante al foglio di lavoro in Excel
linktitle: Aggiungere un pulsante al foglio di lavoro in Excel
second_title: API di elaborazione Excel .NET Aspose.Cells
description: Scopri come aggiungere un pulsante a un foglio di lavoro Excel usando Aspose.Cells per .NET con questo tutorial passo dopo passo. Migliora i fogli di calcolo Excel con pulsanti interattivi.
type: docs
weight: 12
url: /it/net/excel-shapes-controls/add-button-to-worksheet-excel/
---
## Introduzione
fogli di calcolo Excel sono versatili e comunemente usati per gestire i dati, ma a volte necessitano di interattività aggiuntiva. Uno dei modi migliori per migliorare l'esperienza utente è aggiungere pulsanti a un foglio di lavoro. Questi pulsanti possono attivare macro o indirizzare gli utenti verso link utili. Se sei uno sviluppatore .NET che lavora con file Excel, Aspose.Cells per .NET fornisce un modo semplice per manipolare le cartelle di lavoro Excel a livello di programmazione, inclusa l'aggiunta di pulsanti.
In questo tutorial, ti guideremo attraverso il processo di aggiunta di un pulsante a un foglio di lavoro in Excel usando Aspose.Cells per .NET. Tratteremo ogni dettaglio, dall'impostazione dei prerequisiti alle istruzioni passo-passo. Immergiamoci!
## Prerequisiti
Prima di poter seguire questo tutorial, assicurati di aver installato i seguenti strumenti e pacchetti:
-  Aspose.Cells per la libreria .NET: puoi scaricarla da[Qui](https://releases.aspose.com/cells/net/).
- Ambiente di sviluppo .NET: assicurati di avere installato un ambiente .NET funzionante, come Visual Studio.
- Conoscenza di base di C#: è necessario avere familiarità con le basi della programmazione in C#.
-  Patente: Avrai bisogno di una patente valida. Se non ne hai una, puoi ottenerne una[prova gratuita](https://releases.aspose.com/) o richiedere un[licenza temporanea](https://purchase.aspose.com/temporary-license/).
Passiamo all'importazione dei pacchetti necessari.
## Importa pacchetti
Prima di iniziare a scrivere codice, dovrai importare i pacchetti richiesti nel tuo progetto .NET. Ecco un semplice frammento di codice per aiutarti a importare Aspose.Cells nel tuo progetto:
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
Ora che abbiamo importato i pacchetti necessari, scomponiamo l'esempio in una guida dettagliata passo dopo passo.
## Passaggio 1: impostare la cartella di lavoro e il foglio di lavoro
In questo primo passaggio creeremo una nuova cartella di lavoro Excel e otterremo un riferimento al primo foglio di lavoro.
```csharp
// Definisci il percorso della directory dei tuoi documenti.
string dataDir = "Your Document Directory";
//Creare la directory se non è già presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// Crea una nuova cartella di lavoro.
Workbook workbook = new Workbook();
// Prendi il primo foglio di lavoro della cartella di lavoro.
Worksheet sheet = workbook.Worksheets[0];
```

-  Creazione della cartella di lavoro: iniziamo creando una nuova`Workbook` oggetto, che rappresenta un file Excel.
-  Riferimento al foglio di lavoro: Il`Worksheets[0]` Il comando recupera il primo foglio di lavoro nella cartella di lavoro, che modificheremo.
Questo passaggio getta le basi creando un file Excel vuoto con un singolo foglio di lavoro.
## Passaggio 2: aggiungere un pulsante al foglio di lavoro
Poi aggiungeremo un pulsante al foglio di lavoro. È qui che avviene la magia!
```csharp
// Aggiungere un nuovo pulsante al foglio di lavoro.
Aspose.Cells.Drawing.Button button = sheet.Shapes.AddButton(2, 0, 2, 0, 28, 80);
```

- Metodo AddButton: questo metodo aggiunge un pulsante in una posizione specificata nel foglio di lavoro. I parametri definiscono la posizione del pulsante (riga, colonna, offset x, offset y) e le dimensioni (altezza, larghezza).
- Riga e colonna: il pulsante è posizionato nella riga 2 e nella colonna 0, senza alcun offset aggiuntivo.
- Dimensione: l'altezza del pulsante è impostata su 28 e la larghezza su 80.
Con questo passaggio viene aggiunto un pulsante al foglio di lavoro, ma non è ancora finita: personalizziamolo.
## Passaggio 3: imposta le proprietà del pulsante
Ora è il momento di personalizzare l'aspetto del pulsante impostandone il testo, il carattere e il posizionamento.
```csharp
// Imposta la didascalia del pulsante.
button.Text = "Aspose";
// Imposta il tipo di posizionamento, ovvero il modo in cui il pulsante è collegato alle celle.
button.Placement = PlacementType.FreeFloating;
```

- Testo: Impostiamo la didascalia del pulsante su "Aspose".
-  Posizionamento: definiamo come posizionare il pulsante rispetto alle celle del foglio di lavoro.`FreeFloating` consente al pulsante di muoversi indipendentemente dalle celle.
Questo passaggio personalizza la didascalia e il posizionamento del pulsante.
## Passaggio 4: personalizzare il carattere del pulsante
Diamo un tocco di stile al pulsante personalizzando le proprietà del carattere.
```csharp
// Imposta il nome del font.
button.Font.Name = "Tahoma";
// Imposta la stringa della didascalia in grassetto.
button.Font.IsBold = true;
// Imposta il colore su blu.
button.Font.Color = Color.Blue;
```

- Nome del font: cambiamo il font in "Tahoma", un font pulito e moderno.
- Grassetto: rendiamo il testo del pulsante in grassetto per dargli maggiore enfasi.
- Colore: il colore del carattere è impostato sul blu, facendo risaltare il testo del pulsante.
Questo passaggio migliora l'aspetto del pulsante, rendendolo allo stesso tempo funzionale e visivamente accattivante.
## Passaggio 5: aggiungere un collegamento ipertestuale al pulsante
È possibile rendere il pulsante ancora più utile aggiungendo un collegamento ipertestuale.
```csharp
// Imposta il collegamento ipertestuale per il pulsante.
button.AddHyperlink("https://"http://www.aspose.com/");
```

- AddHyperlink: Utilizziamo questo metodo per aggiungere un collegamento ipertestuale cliccabile al pulsante. Quando cliccato, il pulsante porterà al sito web Aspose.
Questo passaggio aggiunge interattività al pulsante, rendendolo funzionale oltre la mera estetica.
## Passaggio 6: salvare il file Excel
Una volta impostato tutto, non dimenticare di salvare le modifiche!
```csharp
// Salva il file.
workbook.Save(dataDir + "book1.out.xls");
```

-  Metodo di salvataggio: utilizziamo il`Save` metodo per scrivere la cartella di lavoro modificata in un nuovo file. Il file verrà salvato nella directory specificata.
Congratulazioni! Ora hai aggiunto un pulsante completamente personalizzato a un foglio di lavoro Excel.
## Conclusione
Aggiungere pulsanti ai fogli di lavoro Excel può migliorare notevolmente la funzionalità dei tuoi fogli di calcolo, rendendoli più interattivi e intuitivi. Con Aspose.Cells per .NET, puoi ottenere questo risultato con solo poche righe di codice, come abbiamo mostrato in questo tutorial.
Aspose.Cells per .NET è una potente libreria che offre infinite possibilità di manipolazione di Excel. Che tu stia automatizzando attività o aggiungendo nuove funzionalità ai tuoi fogli di calcolo, questa libreria è la soluzione ideale.
 Se non l'hai già fatto,[scarica la libreria Aspose.Cells per .NET](https://releases.aspose.com/cells/net/) e inizia a migliorare i tuoi file Excel.
## Domande frequenti
### Posso usare altre forme oltre ai pulsanti in Aspose.Cells per .NET?
Sì, Aspose.Cells consente di aggiungere varie forme, tra cui caselle di controllo, pulsanti di scelta e altro ancora.
### Posso attivare una macro da un pulsante aggiunto tramite Aspose.Cells?
Sì, puoi collegare il pulsante a una macro, anche se dovrai gestire separatamente il codice della macro in Excel.
### Come posso ridimensionare automaticamente il pulsante con le celle?
 Utilizzare il`PlacementType.Move` proprietà per consentire al pulsante di ridimensionarsi insieme alle celle.
### È possibile aggiungere più pulsanti in un singolo foglio di lavoro?
 Assolutamente! Puoi aggiungere tutti i pulsanti di cui hai bisogno chiamando il`AddButton` metodo più volte.
### Posso personalizzare ulteriormente l'aspetto dei pulsanti?
Sì, puoi modificare molte proprietà, tra cui il colore dello sfondo, lo stile del bordo e altro ancora.