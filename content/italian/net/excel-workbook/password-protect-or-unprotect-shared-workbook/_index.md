---
title: Proteggi o rimuovi la protezione con password della cartella di lavoro condivisa
linktitle: Proteggi o rimuovi la protezione con password della cartella di lavoro condivisa
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come proteggere con password o rimuovere la protezione di una cartella di lavoro condivisa utilizzando Aspose.Cells per .NET.
type: docs
weight: 120
url: /it/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Proteggere una cartella di lavoro condivisa con una password è importante per garantire la privacy dei dati. Con Aspose.Cells per .NET, puoi facilmente proteggere o rimuovere la protezione di una cartella di lavoro condivisa utilizzando le password. Seguire i passaggi seguenti per ottenere i risultati desiderati:

## Passaggio 1: specificare la directory di output

Innanzitutto, è necessario specificare la directory di output in cui verrà salvato il file Excel protetto. Ecco come farlo utilizzando Aspose.Cells:

```csharp
// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

## Passaggio 2: crea un file Excel vuoto

Quindi puoi creare un file Excel vuoto su cui desideri applicare la protezione o l'annullamento della protezione. Ecco un codice di esempio:

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

## Passaggio 4: salva il file Excel di output

Dopo aver applicato la protezione o l'annullamento della protezione, è possibile salvare il file Excel protetto nella directory di output specificata. Ecco come farlo:

```csharp
// Salvare il file Excel di output
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Codice sorgente di esempio per proteggere con password o rimuovere la protezione della cartella di lavoro condivisa utilizzando Aspose.Cells per .NET 
```csharp
//Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
//Crea un file Excel vuoto
Workbook wb = new Workbook();
//Proteggi la cartella di lavoro condivisa con password
wb.ProtectSharedWorkbook("1234");
//Decommentare questa riga per rimuovere la protezione della cartella di lavoro condivisa
//wb.UnprotectSharedWorkbook("1234");
//Salvare il file Excel di output
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusione

Proteggere o rimuovere la protezione di una cartella di lavoro condivisa con una password è essenziale per garantire la sicurezza dei dati. Con Aspose.Cells per .NET puoi facilmente aggiungere questa funzionalità ai tuoi file Excel. Seguendo i passaggi di questa guida, puoi proteggere o rimuovere in modo efficace la protezione delle cartelle di lavoro condivise utilizzando le password. Sperimenta con i tuoi file Excel e assicurati di mantenere la sicurezza dei tuoi dati sensibili.

### Domande frequenti

#### D: Quali tipi di protezione posso applicare a una cartella di lavoro condivisa con Aspose.Cells?
    
R: Con Aspose.Cells, puoi proteggere una cartella di lavoro condivisa specificando una password per impedire l'accesso non autorizzato, la modifica o la cancellazione dei dati.

#### D: posso proteggere una cartella di lavoro condivisa senza specificare una password?
    
R: Sì, puoi proteggere una cartella di lavoro condivisa senza specificare una password. Tuttavia, si consiglia di utilizzare una password complessa per una maggiore sicurezza.

#### D: Come posso rimuovere la protezione di una cartella di lavoro condivisa con Aspose.Cells?
    
R: Per rimuovere la protezione da una cartella di lavoro condivisa, è necessario specificare la stessa password utilizzata durante la protezione della cartella di lavoro. Ciò consente di rimuovere la protezione e di accedere liberamente ai dati.

#### D: La protezione di una cartella di lavoro condivisa influisce sulle funzionalità e sulle formule della cartella di lavoro?
    
R: Quando proteggi una cartella di lavoro condivisa, gli utenti possono comunque accedere alle funzionalità e alle formule presenti nella cartella di lavoro. La protezione influisce solo sulle modifiche strutturali della cartella di lavoro.