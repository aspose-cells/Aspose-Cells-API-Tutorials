---
title: Ottieni la larghezza della carta e l'altezza del foglio di lavoro
linktitle: Ottieni la larghezza della carta e l'altezza del foglio di lavoro
second_title: Riferimento all'API Aspose.Cells per .NET
description: Crea una guida passo passo per spiegare il seguente codice sorgente C# per ottenere la larghezza e l'altezza della carta di un foglio di calcolo utilizzando Aspose.Cells per .NET.
type: docs
weight: 80
url: /it/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
In questo tutorial, ti guideremo passo dopo passo per spiegare il seguente codice sorgente C# per ottenere la larghezza e l'altezza della carta di un foglio di lavoro utilizzando Aspose.Cells per .NET. Segui i passaggi seguenti:

## Passaggio 1: creare la cartella di lavoro
 Inizia creando una nuova cartella di lavoro utilizzando il file`Workbook` classe:

```csharp
Workbook wb = new Workbook();
```

## Passaggio 2: accedi al primo foglio di lavoro
 Successivamente, vai al primo foglio di lavoro nella cartella di lavoro utilizzando il file`Worksheet` classe:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Passaggio 3: imposta il formato della carta su A2 e mostra la larghezza e l'altezza della carta in pollici
 Usa il`PaperSize` proprietà del`PageSetup` oggetto per impostare il formato carta su A2, quindi utilizzare il file`PaperWidth` E`PaperHeight` properties per ottenere rispettivamente la larghezza e l'altezza della carta. Visualizza questi valori utilizzando il`Console.WriteLine` metodo:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Passaggio 4: ripetere i passaggi per altri formati di carta
Ripetere i passaggi precedenti, modificando il formato della carta in A3, A4 e Letter, quindi visualizzando i valori di larghezza e altezza della carta per ciascun formato:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Codice sorgente di esempio per ottenere la larghezza della carta e l'altezza del foglio di lavoro utilizzando Aspose.Cells per .NET 

```csharp
//Crea cartella di lavoro
Workbook wb = new Workbook();
//Accedi al primo foglio di lavoro
Worksheet ws = wb.Worksheets[0];
//Impostare il formato carta su A2 e stampare la larghezza e l'altezza della carta in pollici
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Impostare il formato carta su A3 e stampare la larghezza e l'altezza della carta in pollici
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Impostare il formato della carta su A4 e stampare la larghezza e l'altezza della carta in pollici
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Impostare il formato carta su Lettera e stampare la larghezza e l'altezza della carta in pollici
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Conclusione

Hai imparato a utilizzare Aspose.Cells per .NET per ottenere la larghezza e l'altezza della carta di un foglio di calcolo. Questa funzione può essere utile per la configurazione e il layout preciso dei tuoi documenti Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una potente libreria per la manipolazione e l'elaborazione di file Excel nelle applicazioni .NET. Offre molte funzionalità per la creazione, la modifica, la conversione e l'analisi dei file Excel.

#### Come posso ottenere il formato carta di un foglio di calcolo con Aspose.Cells per .NET?

 Puoi usare il`PageSetup` classe del`Worksheet` oggetto per accedere al formato carta. Usa il`PaperSize` proprietà per impostare il formato della carta e il`PaperWidth` E`PaperHeight` properties per ottenere rispettivamente la larghezza e l'altezza della carta.

#### Quali formati di carta supporta Aspose.Cells per .NET?

Aspose.Cells per .NET supporta un'ampia gamma di formati carta comunemente usati, come A2, A3, A4 e Letter, così come molti altri formati personalizzati.

#### Posso personalizzare il formato carta di un foglio di calcolo con Aspose.Cells per .NET?

 Sì, puoi impostare un formato carta personalizzato specificando le dimensioni esatte di larghezza e altezza utilizzando il`PaperWidth` E`PaperHeight` proprietà del`PageSetup` classe.