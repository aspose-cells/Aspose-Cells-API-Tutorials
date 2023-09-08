---
title: Ottieni la larghezza della carta e l'altezza del foglio di lavoro
linktitle: Ottieni la larghezza della carta e l'altezza del foglio di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Creare una guida passo passo per spiegare il seguente codice sorgente C# per ottenere la larghezza e l'altezza della carta di un foglio di calcolo utilizzando Aspose.Cells per .NET.
type: docs
weight: 80
url: /it/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
In questo tutorial, ti guideremo passo dopo passo per spiegare il seguente codice sorgente C# per ottenere la larghezza e l'altezza della carta di un foglio di lavoro utilizzando Aspose.Cells per .NET. Seguire i passaggi seguenti:

## Passaggio 1: creare la cartella di lavoro
 Inizia creando una nuova cartella di lavoro utilizzando il file`Workbook` classe:

```csharp
Workbook wb = new Workbook();
```

## Passaggio 2: accedi al primo foglio di lavoro
 Successivamente, vai al primo foglio di lavoro nella cartella di lavoro utilizzando`Worksheet` classe:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Passaggio 3: imposta il formato carta su A2 e mostra la larghezza e l'altezza della carta in pollici
 Usa il`PaperSize` proprietà del`PageSetup` oggetto per impostare il formato carta su A2, quindi utilizzare il file`PaperWidth` E`PaperHeight` proprietà per ottenere rispettivamente la larghezza e l'altezza della carta. Visualizza questi valori utilizzando il`Console.WriteLine` metodo:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Passaggio 4: ripetere i passaggi per altri formati carta
Ripeti i passaggi precedenti, modificando il formato carta in A3, A4 e Lettera, quindi visualizzando i valori di larghezza e altezza della carta per ciascun formato:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Codice sorgente di esempio per Ottieni larghezza carta e altezza del foglio di lavoro utilizzando Aspose.Cells per .NET 

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
//Imposta il formato carta su A4 e stampa la larghezza e l'altezza della carta in pollici
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Impostare il formato carta su Lettera e stampare la larghezza e l'altezza della carta in pollici
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Conclusione

Hai imparato come utilizzare Aspose.Cells per .NET per ottenere la larghezza della carta e l'altezza di un foglio di calcolo. Questa funzionalità può essere utile per la configurazione e il layout preciso dei tuoi documenti Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una potente libreria per manipolare ed elaborare file Excel in applicazioni .NET. Offre molte funzionalità per creare, modificare, convertire e analizzare file Excel.

#### Come posso ottenere la dimensione della carta di un foglio di calcolo con Aspose.Cells per .NET?

 Puoi usare il`PageSetup` classe del`Worksheet` oggetto per accedere al formato carta. Usa il`PaperSize` proprietà per impostare la dimensione della carta e il file`PaperWidth` E`PaperHeight` proprietà per ottenere rispettivamente la larghezza e l'altezza della carta.

#### Quali formati carta supporta Aspose.Cells per .NET?

Aspose.Cells per .NET supporta un'ampia gamma di formati carta comunemente utilizzati, come A2, A3, A4 e Lettera, nonché molti altri formati personalizzati.

#### Posso personalizzare la dimensione della carta di un foglio di calcolo con Aspose.Cells per .NET?

 Sì, puoi impostare un formato carta personalizzato specificando le dimensioni esatte di larghezza e altezza utilizzando il file`PaperWidth` E`PaperHeight` proprietà del`PageSetup` classe.