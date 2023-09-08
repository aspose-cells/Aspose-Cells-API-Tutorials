---
title: Copia le impostazioni di impostazione della pagina da un altro foglio di lavoro
linktitle: Copia le impostazioni di impostazione della pagina da un altro foglio di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come copiare le impostazioni di configurazione della pagina da un foglio di calcolo a un altro utilizzando Aspose.Cells per .NET. Una guida passo passo per ottimizzare l'uso di questa libreria.
type: docs
weight: 10
url: /it/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
In questo articolo, ti guideremo passo dopo passo per spiegare il seguente codice sorgente C#: Copia le impostazioni di configurazione della pagina da un altro foglio di calcolo utilizzando Aspose.Cells per .NET. Utilizzeremo la libreria Aspose.Cells per .NET per eseguire questa operazione. Se desideri copiare le impostazioni di impostazione della pagina da un foglio di lavoro a un altro, procedi nel seguente modo.

## Passaggio 1: creazione della cartella di lavoro
Il primo passo è creare una cartella di lavoro. Nel nostro caso utilizzeremo la classe Workbook fornita dalla libreria Aspose.Cells. Ecco il codice per creare una cartella di lavoro:

```csharp
Workbook wb = new Workbook();
```

## Passaggio 2: aggiunta di fogli di lavoro di prova
Dopo aver creato la cartella di lavoro, dobbiamo aggiungere fogli di lavoro di prova. In questo esempio, aggiungeremo due fogli di lavoro. Ecco il codice per aggiungere due fogli di lavoro:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Passaggio 3: accesso ai fogli di lavoro
Ora che abbiamo aggiunto i fogli di lavoro, dobbiamo accedervi per poter modificare le loro impostazioni. Accederemo ai fogli di lavoro "TestSheet1" e "TestSheet2" utilizzando i loro nomi. Ecco il codice per accedervi:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Passaggio 4: impostazione del formato carta
 In questo passaggio, imposteremo la dimensione della carta del foglio di lavoro "TestSheet1". Utilizzeremo il`PageSetup.PaperSize` proprietà per impostare la dimensione della carta. Ad esempio, imposteremo il formato carta su "PaperA3ExtraTransverse". Ecco il codice per questo:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Passaggio 5: copia delle impostazioni di impostazione della pagina
Ora copieremo le impostazioni di configurazione della pagina dal foglio di lavoro "TestSheet1" a "TestSheet2". Utilizzeremo il`PageSetup.Copy` metodo per eseguire questa operazione. Ecco il codice per questo:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Passaggio 6: stampa dei formati carta
 Dopo aver copiato le impostazioni di impostazione della pagina, stamperemo i formati carta dei due fogli di lavoro. Noi useremo`Console.WriteLine` per visualizzare i formati carta. Ecco il codice per questo:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Codice sorgente di esempio per copiare le impostazioni di impostazione della pagina da un altro foglio di lavoro utilizzando Aspose.Cells per .NET 
```csharp
//Crea cartella di lavoro
Workbook wb = new Workbook();
//Aggiungi due fogli di lavoro di prova
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Accedi a entrambi i fogli di lavoro come TestSheet1 e TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Imposta il formato carta di TestSheet1 su PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Stampa il formato carta di entrambi i fogli di lavoro
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Copiare il PageSetup da TestSheet1 a TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Stampa il formato carta di entrambi i fogli di lavoro
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Conclusione
In questo articolo, abbiamo imparato come copiare le impostazioni di configurazione della pagina da un foglio di lavoro a un altro utilizzando Aspose.Cells per .NET. Abbiamo eseguito i seguenti passaggi: creazione della cartella di lavoro, aggiunta di fogli di lavoro di prova, accesso ai fogli di lavoro, impostazione del formato carta, copia delle impostazioni di impostazione della pagina e stampa dei formati carta. Ora puoi utilizzare questa conoscenza per copiare le impostazioni di configurazione della pagina nei tuoi progetti.

### Domande frequenti

#### D: Posso copiare le impostazioni di configurazione della pagina tra diverse istanze della cartella di lavoro?

 R: Sì, puoi copiare le impostazioni di impostazione della pagina tra diverse istanze della cartella di lavoro utilizzando il file`PageSetup.Copy` metodo della libreria Aspose.Cells.

#### D: Posso copiare altre impostazioni di impostazione della pagina, come l'orientamento o i margini?

 R: Sì, puoi copiare altre impostazioni di impostazione della pagina utilizzando il file`PageSetup.Copy` metodo con le opzioni appropriate. Ad esempio, puoi copiare l'orientamento utilizzando`CopyOptions.Orientation` e margini utilizzando`CopyOptions.Margins`.

#### D: Come faccio a sapere quali opzioni sono disponibili per il formato carta?

R: Puoi controllare il riferimento API della libreria Aspose.Cells per le opzioni disponibili per il formato carta. C'è un enum chiamato`PaperSizeType` che elenca i diversi formati carta supportati.

#### D: Come posso scaricare la libreria Aspose.Cells per .NET?

 R: Puoi scaricare la libreria Aspose.Cells per .NET da[Rilasci Aspose](https://releases.aspose.com/cells/net). Sono disponibili versioni di prova gratuite, nonché licenze a pagamento per uso commerciale.

#### D: La libreria Aspose.Cells supporta altri linguaggi di programmazione?

R: Sì, la libreria Aspose.Cells supporta più linguaggi di programmazione tra cui C#, Java, Python e molti altri.