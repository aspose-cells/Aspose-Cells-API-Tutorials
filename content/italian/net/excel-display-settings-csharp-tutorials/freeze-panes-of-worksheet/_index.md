---
title: Blocca i riquadri del foglio di lavoro
linktitle: Blocca i riquadri del foglio di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Manipola facilmente i riquadri di blocco del foglio di lavoro Excel con Aspose.Cells per .NET.
type: docs
weight: 70
url: /it/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
In questo tutorial, ti mostreremo come bloccare i riquadri in un foglio di lavoro Excel utilizzando il codice sorgente C# con Aspose.Cells per .NET. Seguire i passaggi seguenti per ottenere il risultato desiderato.

## Passaggio 1: importa le librerie necessarie

Assicurati di aver installato la libreria Aspose.Cells per .NET e importa le librerie necessarie nel tuo progetto C#.

```csharp
using Aspose.Cells;
```

## Passaggio 2: imposta il percorso della directory e apri il file Excel

 Imposta il percorso della directory contenente il tuo file Excel, quindi apri il file istanziando a`Workbook` oggetto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Passaggio 3: vai al foglio di calcolo e applica le impostazioni di blocco del riquadro

 Passare al primo foglio di lavoro nel file Excel utilizzando il file`Worksheet` oggetto. Quindi utilizzare il`FreezePanes` metodo per applicare le impostazioni di blocco del riquadro.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Nell'esempio precedente, i riquadri sono bloccati sulla cella nella riga 3 e nella colonna 2.

## Passaggio 4: salva le modifiche

 Una volta apportate le modifiche necessarie, salvare il file Excel modificato utilizzando il file`Save` metodo del`Workbook` oggetto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Codice sorgente di esempio per Freeze Panes Of Worksheet utilizzando Aspose.Cells per .NET 

```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Creazione di un'istanza di un oggetto cartella di lavoro
// Apertura del file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Applicazione delle impostazioni di blocco dei riquadri
worksheet.FreezePanes(3, 2, 3, 2);
// Salvataggio del file Excel modificato
workbook.Save(dataDir + "output.xls");
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close();
```

## Conclusione

Questa guida passo passo ti ha mostrato come bloccare i riquadri in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Utilizzando il codice sorgente C# fornito, puoi personalizzare facilmente le impostazioni di blocco del riquadro per organizzare e visualizzare meglio i tuoi dati nei file Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una potente libreria per manipolare file Excel in applicazioni .NET.

#### Come posso installare Aspose.Cells per .NET?

 Per installare Aspose.Cells per .NET, è necessario scaricare il relativo pacchetto da[Rilasci Aspose](https://releases/aspose.com/cells/net/) e aggiungilo al tuo progetto .NET.

#### Come bloccare i riquadri in un foglio di lavoro Excel utilizzando Aspose.Cells per .NET?

 Puoi usare il`FreezePanes` metodo del`Worksheet` oggetto per bloccare i riquadri di un foglio di lavoro. Specificare le celle da bloccare fornendo indici di riga e colonna.

#### Posso personalizzare le impostazioni di blocco del riquadro con Aspose.Cells per .NET?

 Sì, utilizzando il`FreezePanes` metodo, è possibile specificare quali celle bloccare secondo necessità, fornendo gli indici di riga e colonna appropriati.
