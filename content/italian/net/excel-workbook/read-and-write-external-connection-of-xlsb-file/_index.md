---
title: Leggere e scrivere la connessione esterna del file XLSB
linktitle: Leggere e scrivere la connessione esterna del file XLSB
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come leggere e modificare le connessioni esterne di un file XLSB utilizzando Aspose.Cells per .NET.
type: docs
weight: 130
url: /it/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Leggere e scrivere connessioni esterne a un file XLSB è essenziale per manipolare i dati da fonti esterne nelle cartelle di lavoro di Excel. Con Aspose.Cells per .NET puoi facilmente leggere e scrivere connessioni esterne utilizzando i seguenti passaggi:

## Passaggio 1: specificare la directory di origine e la directory di output

Innanzitutto, è necessario specificare la directory di origine in cui si trova il file XLSB contenente la connessione esterna, nonché la directory di output in cui si desidera salvare il file modificato. Ecco come farlo usando Aspose.Cells:

```csharp
// directory di origine
string sourceDir = RunExamples.Get_SourceDirectory();

// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

## Passaggio 2: caricare il file XLSB di Excel di origine

Successivamente, è necessario caricare il file XLSB di Excel di origine su cui si desidera eseguire le operazioni di lettura e scrittura della connessione esterna. Ecco un codice di esempio:

```csharp
// Carica il file Excel XLSB di origine
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Passaggio 3: leggere e modificare la connessione esterna

Dopo aver caricato il file, è possibile accedere alla prima connessione esterna che in realtà è una connessione al database. È possibile leggere e modificare varie proprietà della connessione esterna. Ecco come:

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

Una volta apportate le modifiche necessarie, è possibile salvare il file XLSB di Excel modificato nella directory di output specificata. Ecco come farlo:

```csharp
// Salva il file Excel XLSB di output
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Esempio di codice sorgente per la lettura e la scrittura della connessione esterna del file XLSB utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
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
//Modifica il nome della connessione
dbCon.Name = "NewCust";
//Salva il file Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Conclusione

La lettura e la scrittura di connessioni esterne in un file XLSB consente di manipolare i dati da fonti esterne nelle cartelle di lavoro di Excel. Con Aspose.Cells per .NET, puoi accedere facilmente a connessioni esterne, leggere e modificare le informazioni di connessione e salvare le modifiche. Sperimenta con i tuoi file XLSB e sfrutta la potenza delle connessioni esterne nelle tue applicazioni Excel.

### Domande frequenti

#### D: Cos'è una connessione esterna in un file XLSB?
    
R: Una connessione esterna in un file XLSB si riferisce a una connessione stabilita con un'origine dati esterna come un database. Ti consente di importare i dati da questa fonte esterna nella cartella di lavoro di Excel.

#### D: Posso avere più connessioni esterne in un file XLSB?
     
R: Sì, puoi avere più connessioni esterne in un file XLSB. Puoi gestirli singolarmente accedendo a ciascun oggetto di connessione.

#### D: Come posso leggere i dettagli di una connessione esterna in un file XLSB con Aspose.Cells?
     
R: È possibile utilizzare la funzionalità fornita da Aspose.Cells per accedere alle proprietà di una connessione esterna, come il nome della connessione, il comando associato e le informazioni sulla connessione.

#### D: È possibile modificare una connessione esterna in un file XLSB con Aspose.Cells?
     
R: Sì, puoi modificare le proprietà di una connessione esterna, come il nome della connessione, per soddisfare le tue esigenze specifiche. Aspose.Cells fornisce metodi per apportare queste modifiche.

#### D: Come posso salvare le modifiche apportate a una connessione esterna a un file XLSB con Aspose.Cells?
     
R: Dopo aver apportato le modifiche necessarie a una connessione esterna, puoi semplicemente salvare il file XLSB di Excel modificato utilizzando il metodo appropriato fornito da Aspose.Cells.