---
title: Proteggi con password o non proteggi la cartella di lavoro condivisa
linktitle: Proteggi con password o non proteggi la cartella di lavoro condivisa
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come proteggere con password o rimuovere la protezione di una cartella di lavoro condivisa utilizzando Aspose.Cells per .NET.
type: docs
weight: 120
url: /it/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
La protezione di una cartella di lavoro condivisa con una password è importante per garantire la riservatezza dei dati. Con Aspose.Cells per .NET, puoi facilmente proteggere o rimuovere la protezione di una cartella di lavoro condivisa utilizzando le password. Seguire i passaggi seguenti per ottenere i risultati desiderati:

## Passaggio 1: specificare la directory di output

Innanzitutto, è necessario specificare la directory di output in cui verrà salvato il file Excel protetto. Ecco come farlo usando Aspose.Cells:

```csharp
// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

## Passaggio 2: creare un file Excel vuoto

Quindi puoi creare un file Excel vuoto su cui desideri applicare la protezione o la rimozione della protezione. Ecco un codice di esempio:

```csharp
// Crea una cartella di lavoro Excel vuota
Workbook wb = new Workbook();
```

## Passaggio 3: proteggere o rimuovere la protezione della cartella di lavoro condivisa

Dopo aver creato la cartella di lavoro, è possibile proteggere o rimuovere la protezione della cartella di lavoro condivisa specificando la password appropriata. Ecco come:

```csharp
// Proteggi la cartella di lavoro condivisa con una password
wb.ProtectSharedWorkbook("1234");

// Rimuovere il commento da questa riga per rimuovere la protezione della cartella di lavoro condivisa
// wb.UnprotectSharedWorkbook("1234");
```

## Passaggio 4: salvare il file Excel di output

Una volta applicata la protezione o la rimozione della protezione, è possibile salvare il file Excel protetto nella directory di output specificata. Ecco come farlo:

```csharp
// Salva il file Excel di output
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Esempio di codice sorgente per proteggere con password o rimuovere la protezione della cartella di lavoro condivisa utilizzando Aspose.Cells per .NET 
```csharp
//Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
//Crea un file Excel vuoto
Workbook wb = new Workbook();
//Proteggi la cartella di lavoro condivisa con password
wb.ProtectSharedWorkbook("1234");
//Rimuovere il commento da questa riga per rimuovere la protezione della cartella di lavoro condivisa
//wb.UnprotectSharedWorkbook("1234");
//Salva il file Excel di output
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusione

Proteggere o rimuovere la protezione di una cartella di lavoro condivisa con una password è essenziale per garantire la sicurezza dei dati. Con Aspose.Cells per .NET puoi facilmente aggiungere questa funzionalità ai tuoi file Excel. Seguendo i passaggi di questa guida, puoi proteggere o sproteggere in modo efficace le tue cartelle di lavoro condivise utilizzando le password. Sperimenta con i tuoi file Excel e assicurati di mantenere la sicurezza dei tuoi dati sensibili.

### Domande frequenti

#### D: Quali tipi di protezione posso applicare a una cartella di lavoro condivisa con Aspose.Cells?
    
R: Con Aspose.Cells, puoi proteggere una cartella di lavoro condivisa specificando una password per impedire l'accesso non autorizzato, la modifica o la cancellazione dei dati.

#### D: Posso proteggere una cartella di lavoro condivisa senza specificare una password?
    
R: Sì, puoi proteggere una cartella di lavoro condivisa senza specificare una password. Tuttavia, si consiglia di utilizzare una password complessa per una maggiore sicurezza.

#### D: Come posso rimuovere la protezione da una cartella di lavoro condivisa con Aspose.Cells?
    
R: Per rimuovere la protezione da una cartella di lavoro condivisa, è necessario specificare la stessa password utilizzata durante la protezione della cartella di lavoro. Ciò consente di rimuovere la protezione e di accedere liberamente ai dati.

#### D: La protezione di una cartella di lavoro condivisa influisce sulle funzionalità e sulle formule nella cartella di lavoro?
    
R: Quando proteggi una cartella di lavoro condivisa, gli utenti possono comunque accedere alle funzioni e alle formule presenti nella cartella di lavoro. La protezione influisce solo sulle modifiche strutturali alla cartella di lavoro.