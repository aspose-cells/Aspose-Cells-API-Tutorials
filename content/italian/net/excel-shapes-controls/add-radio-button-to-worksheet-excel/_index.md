---
title: Aggiungi pulsante di scelta al foglio di lavoro in Excel
linktitle: Aggiungi pulsante di scelta al foglio di lavoro in Excel
second_title: API di elaborazione Excel .NET Aspose.Cells
description: Scopri come aggiungere pulsanti di scelta a un foglio di lavoro Excel usando Aspose.Cells per .NET con questa semplice guida passo-passo. Perfetta per creare moduli Excel interattivi.
type: docs
weight: 19
url: /it/net/excel-shapes-controls/add-radio-button-to-worksheet-excel/
---
## Introduzione
Ti sei mai chiesto come ravvivare i tuoi fogli Excel con elementi interattivi come i pulsanti di scelta? Che tu stia creando un sondaggio, un modulo o uno strumento di analisi, l'aggiunta di pulsanti di scelta può davvero migliorare l'interazione dell'utente. In questo tutorial, ti guideremo attraverso il processo di aggiunta di pulsanti di scelta ai tuoi fogli Excel utilizzando Aspose.Cells per .NET. Suddivideremo tutto in semplici passaggi da seguire, assicurandoti di essere un professionista entro la fine di questo articolo. Pronto a tuffarti? Cominciamo!
## Prerequisiti
Prima di passare alla parte divertente dell'aggiunta dei pulsanti di scelta, assicuriamoci di aver impostato tutto per iniziare.
1.  Aspose.Cells per .NET: per prima cosa, assicurati di aver scaricato e installato[Aspose.Cells per .NET](https://releases.aspose.com/cells/net/) libreria. Puoi scaricarla tramite NuGet in Visual Studio o dalla pagina di download.
2. IDE (Integrated Development Environment): per scrivere ed eseguire il codice C#, avrai bisogno di un IDE come Visual Studio.
3. .NET Framework: assicurati di avere installato .NET Framework 4.0 o versione successiva sul tuo computer. Aspose.Cells lo richiede per funzionare.
4. Nozioni di base di C#: la familiarità con la sintassi di C# e la programmazione .NET renderà le cose più semplici man mano che seguirete il tutorial.
Una volta che hai sistemato tutto, siamo pronti a partire!
## Importa pacchetti
Prima di scrivere il codice, è essenziale importare i namespace necessari per evitare errori in seguito. Aggiungi quanto segue al tuo codice:
```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Drawing;
```
Queste importazioni sono essenziali per accedere alle funzionalità della cartella di lavoro, aggiungere pulsanti di scelta e gestire le operazioni sui file.
## Passaggio 1: impostazione della cartella di lavoro
Per prima cosa, creiamo una nuova cartella di lavoro di Excel.
 Per iniziare, dovrai creare un'istanza di un nuovo`Workbook` oggetto. Questo rappresenterà il tuo file Excel nel codice.
```csharp
// Crea una nuova cartella di lavoro.
Workbook excelbook = new Workbook();
```
In questo passaggio, stai creando una cartella di lavoro vuota. Immaginala come una tela bianca su cui aggiungerai pulsanti di scelta rapida nei passaggi successivi.
## Passaggio 2: aggiunta e formattazione di un valore di cella
Ora aggiungiamo un titolo al foglio di lavoro. Aggiungeremo del testo alla cella`C2` e formattalo per renderlo in grassetto. Questo passaggio aggiunge contesto ai pulsanti di scelta.
### Inserisci testo nella cella
```csharp
// Inserire un valore nella cella C2.
excelbook.Worksheets[0].Cells["C2"].PutValue("Age Groups");
```
### Rendi il testo in grassetto
```csharp
// Imposta il testo in grassetto nella cella C2.
excelbook.Worksheets[0].Cells["C2"].GetStyle().Font.IsBold = true;
```
 Qui abbiamo aggiunto un titolo semplice, "Gruppi di età", nella cella`C2`, e l'ho reso in grassetto in modo che risalti. Facile, vero?
## Passaggio 3: aggiunta del primo pulsante di scelta
Adesso arriva la parte emozionante: aggiungere il primo pulsante di scelta al foglio di lavoro!
### Aggiungi un pulsante di scelta
```csharp
// Aggiungere un pulsante di scelta al primo foglio.
Aspose.Cells.Drawing.RadioButton radio1 = excelbook.Worksheets[0].Shapes.AddRadioButton(3, 0, 2, 0, 30, 110);
```
Questa riga aggiunge il pulsante di scelta a una posizione specifica sul tuo foglio di lavoro. I numeri rappresentano il suo posizionamento e le sue dimensioni. Immagina di impostare le coordinate X e Y del pulsante.
### Imposta il testo del pulsante di scelta
```csharp
// Imposta la sua stringa di testo.
radio1.Text = "20-29";
```
Qui abbiamo assegnato al pulsante di scelta un'etichetta, "20-29", che rappresenta una fascia d'età.
### Collega il pulsante di scelta a una cella
```csharp
// Imposta la cella A1 come cella collegata per il pulsante di scelta.
radio1.LinkedCell = "A1";
```
 Questo collega il pulsante di scelta alla cella`A1`il che significa che il risultato della selezione del pulsante verrà memorizzato in quella cella.
### Aggiungi effetto 3D
```csharp
// Rendi il pulsante di scelta 3D.
radio1.Shadow = true;
```
Poiché vogliamo che questo pulsante di scelta salti fuori, abbiamo aggiunto un effetto 3D.
### Personalizza la riga del pulsante di scelta
```csharp
// Imposta lo spessore della linea del pulsante di scelta.
radio1.Line.Weight = 4;
// Imposta lo stile del trattino della linea del pulsante di scelta.
radio1.Line.DashStyle = MsoLineDashStyle.Solid;
```
Queste righe di codice regolano lo spessore e lo stile del trattino del bordo del pulsante di scelta per renderlo più accattivante.
## Passaggio 4: aggiunta di pulsanti di scelta aggiuntivi
Aggiungiamo altri due pulsanti di scelta per le fasce d'età rimanenti: "30-39" e "40-49". I passaggi sono gli stessi, solo con piccole variazioni nelle coordinate e nelle etichette.
### Aggiungi il secondo pulsante di scelta
```csharp
// Aggiungere un altro pulsante di scelta al primo foglio.
Aspose.Cells.Drawing.RadioButton radio2 = excelbook.Worksheets[0].Shapes.AddRadioButton(6, 0, 2, 0, 30, 110);
// Imposta la sua stringa di testo.
radio2.Text = "30-39";
// Imposta la cella A1 come cella collegata per il pulsante di scelta.
radio2.LinkedCell = "A1";
// Rendi il pulsante di scelta 3D.
radio2.Shadow = true;
// Imposta il peso del pulsante di scelta.
radio2.Line.Weight = 4;
// Imposta lo stile del trattino del pulsante di scelta.
radio2.Line.DashStyle = MsoLineDashStyle.Solid;
```
### Aggiungi il terzo pulsante di scelta
```csharp
// Aggiungere un altro pulsante di scelta al primo foglio.
Aspose.Cells.Drawing.RadioButton radio3 = excelbook.Worksheets[0].Shapes.AddRadioButton(9, 0, 2, 0, 30, 110);
// Imposta la sua stringa di testo.
radio3.Text = "40-49";
// Imposta la cella A1 come cella collegata per il pulsante di scelta.
radio3.LinkedCell = "A1";
// Rendi il pulsante di scelta 3D.
radio3.Shadow = true;
// Imposta il peso del pulsante di scelta.
radio3.Line.Weight = 4;
// Imposta lo stile del trattino del pulsante di scelta.
radio3.Line.DashStyle = MsoLineDashStyle.Solid;
```
## Passaggio 5: salvataggio del file Excel
Una volta aggiunti e formattati tutti i pulsanti di scelta, è il momento di salvare il file.
```csharp
// Salvare il file Excel.
string dataDir = "Your Document Directory";
excelbook.Save(dataDir + "book1.out.xls");
```
In questo passaggio, la cartella di lavoro viene salvata nella directory specificata. È semplicissimo: il tuo foglio di lavoro interattivo è pronto!
## Conclusione
Ecco fatto! Hai appena aggiunto pulsanti di scelta a un foglio di lavoro Excel usando Aspose.Cells per .NET. Questo tutorial ha trattato tutto, dall'impostazione della cartella di lavoro, all'inserimento e alla formattazione di un valore, all'aggiunta di più pulsanti di scelta e al collegamento a una cella. Ora sei pronto per creare fogli Excel interattivi che non solo hanno un bell'aspetto, ma offrono anche un'esperienza utente migliorata. Divertiti a esplorare altre possibilità con Aspose.Cells!
## Domande frequenti
### Posso aggiungere più pulsanti di scelta a fogli diversi?  
Assolutamente! Puoi ripetere il processo su qualsiasi foglio all'interno della cartella di lavoro specificando l'indice corretto del foglio di lavoro.
### Posso personalizzare ulteriormente l'aspetto dei pulsanti di scelta?  
Sì, Aspose.Cells offre una varietà di opzioni di personalizzazione, tra cui la modifica di colori, dimensioni e altri attributi di formattazione.
### Come posso rilevare quale pulsante di scelta è selezionato?  
La cella collegata (ad esempio, A1) mostrerà l'indice del pulsante di scelta selezionato. Puoi controllare il valore della cella collegata per scoprire quale è selezionata.
### C'è un limite al numero di pulsanti di scelta che posso aggiungere?  
No, non c'è un limite rigido al numero di pulsanti radio che puoi aggiungere. Tuttavia, è bene mantenere l'interfaccia user-friendly.
### Posso usare Aspose.Cells con altri linguaggi di programmazione?  
Sì, Aspose.Cells supporta più linguaggi di programmazione, tra cui Java. Ma questo tutorial si concentra specificamente su .NET.