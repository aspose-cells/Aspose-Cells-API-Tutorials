---
title: Ottieni le dimensioni della pagina
linktitle: Ottieni le dimensioni della pagina
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come recuperare le dimensioni della pagina in Excel utilizzando Aspose.Cells per .NET. Guida passo passo con codice sorgente in C#.
type: docs
weight: 40
url: /it/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells per .NET è una potente libreria che consente agli sviluppatori di lavorare con file di Microsoft Excel a livello di codice. Offre un'ampia gamma di funzionalità per la manipolazione di documenti Excel, inclusa la possibilità di ottenere le dimensioni della pagina. In questo tutorial, ti guideremo attraverso i passaggi per recuperare le dimensioni della pagina utilizzando Aspose.Cells per .NET.

## Passaggio 1: crea un'istanza della classe Workbook

Per iniziare, dobbiamo creare un'istanza della classe Workbook, che rappresenta la cartella di lavoro di Excel. Ciò può essere ottenuto utilizzando il seguente codice:

```csharp
Workbook book = new Workbook();
```

## Passaggio 2: accesso al foglio di calcolo

Successivamente, dobbiamo accedere al foglio di lavoro nella cartella di lavoro in cui vogliamo impostare le dimensioni della pagina. In questo esempio, supponiamo di voler lavorare con il primo foglio di lavoro. Possiamo accedervi utilizzando il seguente codice:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Passaggio 3: impostare il formato carta su A2 e stampare larghezza e altezza in pollici

Ora imposteremo il formato carta su A2 e stamperemo la larghezza e l'altezza della pagina in pollici. Ciò può essere ottenuto utilizzando il seguente codice:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Passaggio 4: imposta il formato carta su A3 e stampa larghezza e altezza in pollici

Successivamente, imposteremo il formato carta su A3 e stamperemo la larghezza e l'altezza della pagina in pollici. Ecco il codice corrispondente:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Passaggio 5: impostare il formato carta su A4 e stampare larghezza e altezza in pollici

Ora imposteremo il formato carta su A4 e stamperemo la larghezza e l'altezza della pagina in pollici. Ecco il codice:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Passaggio 6: impostare il formato carta su Lettera e stampare la larghezza e l'altezza in pollici

Infine, imposteremo il formato carta su Lettera e stamperemo la larghezza e l'altezza della pagina in pollici. Ecco il codice:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Codice sorgente di esempio per Get Page Dimensions utilizzando Aspose.Cells per .NET 
```csharp
// Crea un'istanza della classe Workbook
Workbook book = new Workbook();
// Accedi al primo foglio di lavoro
Worksheet sheet = book.Worksheets[0];
// Impostare il formato carta su A2 e stampare la larghezza e l'altezza della carta in pollici
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Impostare il formato carta su A3 e stampare la larghezza e l'altezza della carta in pollici
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Imposta il formato carta su A4 e stampa la larghezza e l'altezza della carta in pollici
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Impostare il formato carta su Lettera e stampare la larghezza e l'altezza della carta in pollici
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Conclusione

Congratulazioni! Hai imparato come recuperare le dimensioni della pagina utilizzando Aspose.Cells per .NET. Questa funzionalità può essere utile quando è necessario eseguire operazioni specifiche in base alle dimensioni della pagina nei file Excel.

Non dimenticare di esplorare ulteriormente la documentazione di Aspose.Cells per scoprire tutte le potenti funzionalità che offre.

### Domande frequenti

#### 1. Quali altri formati carta supporta Aspose.Cells per .NET?

Aspose.Cells per .NET supporta una varietà di formati carta tra cui A1, A5, B4, B5, Executive, Legal, Letter e molti altri. È possibile controllare la documentazione per l'elenco completo dei formati carta supportati.

#### 2. Posso impostare dimensioni di pagina personalizzate con Aspose.Cells per .NET?

Sì, puoi impostare dimensioni di pagina personalizzate specificando la larghezza e l'altezza desiderate. Aspose.Cells offre la massima flessibilità per personalizzare le dimensioni della pagina in base alle proprie esigenze.

#### 3. Posso ottenere le dimensioni della pagina in unità diverse dai pollici?

Sì, Aspose.Cells per .NET ti consente di ottenere le dimensioni della pagina in diverse unità, inclusi pollici, centimetri, millimetri e punti.

#### 4. Aspose.Cells per .NET supporta altre funzionalità di modifica delle impostazioni della pagina?

Sì, Aspose.Cells offre una gamma completa di funzionalità per la modifica delle impostazioni della pagina, inclusa l'impostazione dei margini, dell'orientamento, delle intestazioni e dei piè di pagina, ecc.