---
title: Leggere e scrivere la connessione esterna del file XLSB
linktitle: Leggere e scrivere la connessione esterna del file XLSB
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come leggere e modificare le connessioni esterne di un file XLSB utilizzando Aspose.Cells per .NET.
type: docs
weight: 130
url: /it/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Leggere e scrivere connessioni esterne a un file XLSB è essenziale per manipolare i dati da fonti esterne nelle cartelle di lavoro di Excel. Con Aspose.Cells per .NET puoi facilmente leggere e scrivere connessioni esterne utilizzando i seguenti passaggi:

## Passaggio 1: specificare la directory di origine e la directory di output

Innanzitutto, devi specificare la directory di origine in cui si trova il file XLSB contenente la connessione esterna, nonché la directory di output in cui desideri salvare il file modificato. Ecco come farlo utilizzando Aspose.Cells:

```csharp
// directory di origine
string sourceDir = RunExamples.Get_SourceDirectory();

// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

## Passaggio 2: caricare il file XLSB Excel di origine

Successivamente è necessario caricare il file Excel XLSB di origine sul quale si desidera eseguire le operazioni di lettura e scrittura della connessione esterna. Ecco un codice di esempio:

```csharp
// Carica il file XLSB di Excel di origine
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Passaggio 3: leggere e modificare la connessione esterna

Dopo aver caricato il file, puoi accedere alla prima connessione esterna che in realtà è una connessione al database. È possibile leggere e modificare varie proprietà della connessione esterna. Ecco come:

```csharp
// Leggere la prima connessione esterna che è una connessione al database
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Visualizza il nome della connessione al database, il comando e le informazioni sulla connessione
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Modificare il nome della connessione
dbCon.Name = "NewCustomer";
```

## Passaggio 4: salvare il file XLSB Excel di output

Dopo aver apportato le modifiche necessarie, è possibile salvare il file XLSB Excel modificato nella directory di output specificata. Ecco come farlo:

```csharp
// Salvare il file XLSB Excel di output
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Codice sorgente di esempio per la connessione esterna di lettura e scrittura del file XLSB utilizzando Aspose.Cells per .NET 
```csharp
//Directory di origine
string sourceDir = RunExamples.Get_SourceDirectory();
//Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
//Carica il file Excel Xlsb di origine
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Leggi la prima connessione esterna che in realtà è una connessione DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Stampa il nome, il comando e le informazioni di connessione della connessione DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Modificare il nome della connessione
dbCon.Name = "NewCust";
//Salvare il file Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Conclusione

Leggere e scrivere connessioni esterne a un file XLSB consente di manipolare dati da fonti esterne nelle cartelle di lavoro di Excel. Con Aspose.Cells per .NET, puoi accedere facilmente alle connessioni esterne, leggere e modificare le informazioni di connessione e salvare le modifiche. Sperimenta i tuoi file XLSB e sfrutta la potenza delle connessioni esterne nelle tue applicazioni Excel.

### Domande frequenti

#### D: Cos'è una connessione esterna in un file XLSB?
    
R: Una connessione esterna in un file XLSB si riferisce a una connessione stabilita con un'origine dati esterna come un database. Ti consente di importare dati da questa fonte esterna nella cartella di lavoro di Excel.

#### D: Posso avere più connessioni esterne in un file XLSB?
     
R: Sì, puoi avere più connessioni esterne in un file XLSB. Puoi gestirli singolarmente accedendo a ciascun oggetto di connessione.

#### D: Come posso leggere i dettagli di una connessione esterna in un file XLSB con Aspose.Cells?
     
R: È possibile utilizzare la funzionalità fornita da Aspose.Cells per accedere alle proprietà di una connessione esterna, come il nome della connessione, il comando associato e le informazioni sulla connessione.

#### D: È possibile modificare una connessione esterna in un file XLSB con Aspose.Cells?
     
R: Sì, puoi modificare le proprietà di una connessione esterna, come il nome della connessione, per soddisfare le tue esigenze specifiche. Aspose.Cells fornisce metodi per apportare queste modifiche.

#### D: Come posso salvare le modifiche apportate a una connessione esterna a un file XLSB con Aspose.Cells?
     
R: Dopo aver apportato le modifiche necessarie a una connessione esterna, puoi semplicemente salvare il file XLSB Excel modificato utilizzando il metodo appropriato fornito da Aspose.Cells.