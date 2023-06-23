---
title: Specifica l'autore durante la protezione dalla scrittura della cartella di lavoro di Excel
linktitle: Specifica l'autore durante la protezione dalla scrittura della cartella di lavoro di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come proteggere e personalizzare le cartelle di lavoro di Excel utilizzando Aspose.Cells per .NET. Tutorial passo passo in C#.
type: docs
weight: 30
url: /it/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

In questo tutorial, ti mostreremo come specificare l'autore durante la protezione da scrittura di una cartella di lavoro di Excel utilizzando la libreria Aspose.Cells per .NET.

## Passaggio 1: preparazione dell'ambiente

Prima di iniziare, assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Scarica la libreria dal sito Web ufficiale di Aspose e segui le istruzioni di installazione fornite.

## Passaggio 2: configurazione delle directory di origine e di output

Nel codice sorgente fornito, è necessario specificare le directory di origine e di output. Modifica il`sourceDir` E`outputDir` variabili sostituendo "YOUR SOURCE DIRECTORY" e "YOUR OUTPUT DIRECTORY" con i rispettivi percorsi assoluti sulla tua macchina.

```csharp
// Rubrica di origine
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Cartella di destinazione
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Passaggio 3: creazione di una cartella di lavoro Excel vuota

Per iniziare, creiamo un oggetto Workbook che rappresenta una cartella di lavoro Excel vuota.

```csharp
// Crea una cartella di lavoro vuota.
Workbook wb = new Workbook();
```

## Passaggio 4: protezione da scrittura con password

 Successivamente, specifichiamo una password per proteggere dalla scrittura la cartella di lavoro di Excel utilizzando il file`WriteProtection.Password` proprietà dell'oggetto Workbook.

```csharp
// Scrivi proteggere la cartella di lavoro con password.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Passaggio 5: specifica dell'autore

 Ora specifichiamo l'autore della cartella di lavoro di Excel utilizzando il file`WriteProtection.Author` proprietà dell'oggetto Workbook.

```csharp
// Specifica l'autore durante la protezione dalla scrittura della cartella di lavoro.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Passaggio 6: cartella di lavoro Excel protetta da backup

 Una volta specificata la protezione da scrittura e l'autore, possiamo salvare la cartella di lavoro di Excel nel formato XLSX utilizzando il file`Save()` metodo.

```csharp
// Salva la cartella di lavoro in formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Esempio di codice sorgente per specificare l'autore durante la protezione dalla scrittura della cartella di lavoro di Excel utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
string sourceDir = "YOUR SOURCE DIRECTORY";

//Cartella di destinazione
string outputDir = "YOUR OUTPUT DIRECTORY";

// Crea una cartella di lavoro vuota.
Workbook wb = new Workbook();

// Scrivi proteggere la cartella di lavoro con password.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Specifica l'autore durante la protezione dalla scrittura della cartella di lavoro.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Salva la cartella di lavoro in formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Conclusione

Congratulazioni! Ora hai imparato come specificare l'autore durante la protezione da scrittura di una cartella di lavoro di Excel con Aspose.Cells per .NET. Puoi applicare questi passaggi ai tuoi progetti per proteggere e personalizzare le cartelle di lavoro di Excel.

Sentiti libero di esplorare ulteriormente le funzionalità di Aspose.Cells per .NET per operazioni più avanzate su file Excel.

## Domande frequenti

#### D: Posso proteggere da scrittura una cartella di lavoro di Excel senza specificare una password?

 R: Sì, puoi utilizzare gli oggetti Workbook`WriteProtect()` metodo senza specificare una password per proteggere da scrittura una cartella di lavoro di Excel. Ciò limiterà le modifiche alla cartella di lavoro senza richiedere una password.

#### D: Come si rimuove la protezione da scrittura da una cartella di lavoro di Excel?

 R: Per rimuovere la protezione da scrittura da una cartella di lavoro di Excel, puoi utilizzare il file`Unprotect()` metodo dell'oggetto Worksheet o del metodo`RemoveWriteProtection()` metodo dell'oggetto Workbook, a seconda del caso d'uso specifico. .

#### D: Ho dimenticato la password per proteggere la mia cartella di lavoro di Excel. Cosa posso fare ?

R: Se hai dimenticato la password per proteggere la cartella di lavoro di Excel, non puoi rimuoverla direttamente. Tuttavia, puoi provare a utilizzare strumenti di terze parti specializzati che forniscono funzionalità di recupero della password per i file Excel protetti.

#### D: È possibile specificare più autori durante la protezione da scrittura di una cartella di lavoro di Excel?

R: No, la libreria Aspose.Cells per .NET consente di specificare un singolo autore durante la protezione da scrittura di una cartella di lavoro di Excel. Se desideri specificare più autori, dovrai prendere in considerazione soluzioni personalizzate manipolando direttamente il file Excel.