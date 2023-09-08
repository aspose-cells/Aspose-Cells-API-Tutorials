---
title: Crea cartella di lavoro condivisa
linktitle: Crea cartella di lavoro condivisa
second_title: Aspose.Cells per riferimento API .NET
description: Crea una cartella di lavoro condivisa di Excel con Aspose.Cells per .NET per consentire la collaborazione simultanea dei dati.
type: docs
weight: 70
url: /it/net/excel-workbook/create-shared-workbook/
---
In questo tutorial ti guideremo attraverso il codice sorgente C# fornito che ti consentirà di creare una cartella di lavoro condivisa utilizzando Aspose.Cells per .NET. Seguire i passaggi seguenti per eseguire questa operazione.

## Passaggio 1: imposta la directory di output

```csharp
// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

In questo primo passaggio, definiamo la directory di output in cui verrà salvata la cartella di lavoro condivisa.

## Passaggio 2: crea un oggetto cartella di lavoro

```csharp
// Creare un oggetto cartella di lavoro
Workbook wb = new Workbook();
```

Stiamo creando un nuovo oggetto cartella di lavoro che rappresenterà la nostra cartella di lavoro di Excel.

## Passaggio 3: abilitare la condivisione della cartella di lavoro

```csharp
// Condividi la cartella di lavoro
wb.Settings.Shared = true;
```

 Abilitiamo la funzionalità di condivisione della cartella di lavoro impostando il file`Shared` proprietà dell'oggetto Workbook a`true`.

## Passaggio 4: salva la cartella di lavoro condivisa

```csharp
// Salva la cartella di lavoro condivisa
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Salviamo la cartella di lavoro condivisa specificando il percorso e il nome del file di output.

### Codice sorgente di esempio per creare una cartella di lavoro condivisa utilizzando Aspose.Cells per .NET 
```csharp
//Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
//Crea oggetto cartella di lavoro
Workbook wb = new Workbook();
//Condividi la cartella di lavoro
wb.Settings.Shared = true;
//Salva la cartella di lavoro condivisa
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Conclusione

Congratulazioni! Hai imparato come creare una cartella di lavoro condivisa utilizzando Aspose.Cells per .NET. La cartella di lavoro condivisa può essere utilizzata da più utenti contemporaneamente per collaborare sui dati. Sperimenta con i tuoi dati ed esplora ulteriormente le funzionalità di Aspose.Cells per creare cartelle di lavoro Excel potenti e personalizzate.

### Domande frequenti

#### D: Cos'è una cartella di lavoro condivisa?

R: Una cartella di lavoro condivisa è una cartella di lavoro Excel che può essere utilizzata contemporaneamente da più utenti per collaborare sui dati. Ogni utente può apportare modifiche alla cartella di lavoro e gli altri utenti vedranno gli aggiornamenti in tempo reale.

#### D: Come abilitare la condivisione di una cartella di lavoro in Aspose.Cells per .NET?

 R: Per abilitare la condivisione di una cartella di lavoro in Aspose.Cells per .NET, è necessario impostare il file`Shared` proprietà dell'oggetto Workbook a`true`. Ciò consentirà agli utenti di lavorare simultaneamente sulla cartella di lavoro.

#### D: Posso limitare le autorizzazioni utente in una cartella di lavoro condivisa?

R: Sì, puoi limitare le autorizzazioni utente in una cartella di lavoro condivisa utilizzando le funzionalità di sicurezza di Excel. Puoi impostare autorizzazioni specifiche per ciascun utente, come la possibilità di modificare, di sola lettura, ecc.

#### D: Come posso condividere la cartella di lavoro con altri utenti?

R: Una volta creata la cartella di lavoro condivisa, puoi condividerla con altri utenti inviando loro il file Excel. Altri utenti potranno aprire il file e lavorarci sopra contemporaneamente.

#### D: tutte le funzionalità di Excel sono supportate in una cartella di lavoro condivisa?

R: La maggior parte delle funzionalità di Excel sono supportate in una cartella di lavoro condivisa. Tuttavia, alcune funzionalità avanzate, come macro e componenti aggiuntivi, potrebbero presentare limitazioni o restrizioni se utilizzate in una cartella di lavoro condivisa.