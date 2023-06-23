---
title: Supporto firma Xades
linktitle: Supporto firma Xades
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come aggiungere una firma Xades a un file Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 190
url: /it/net/excel-workbook/xades-signature-support/
---
In questo articolo, ti guideremo passo dopo passo per spiegare il codice sorgente C # di seguito, che riguarda il supporto della firma Xades utilizzando la libreria Aspose.Cells per .NET. Scoprirai come utilizzare questa libreria per aggiungere una firma digitale Xades a un file Excel. Ti forniremo anche una panoramica del processo di firma e della sua esecuzione. Segui i passaggi seguenti per ottenere risultati conclusivi.

## Passaggio 1: definire le directory di origine e di output
Per iniziare, dobbiamo definire le directory di origine e di output nel nostro codice. Queste directory indicano dove si trovano i file di origine e dove verrà salvato il file di output. Ecco il codice corrispondente:

```csharp
// Rubrica di origine
string sourceDir = RunExamples.Get_SourceDirectory();
// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

Assicurarsi di adattare i percorsi delle directory secondo necessità.

## Passaggio 2: caricamento della cartella di lavoro di Excel
Il prossimo passo è caricare la cartella di lavoro di Excel su cui vogliamo aggiungere la firma digitale Xades. Ecco il codice per caricare la cartella di lavoro:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Assicurati di specificare correttamente il nome del file di origine nel codice.

## Passaggio 3: configurazione della firma digitale
Ora configureremo la firma digitale Xades fornendo le informazioni necessarie. Dobbiamo specificare il file PFX contenente il certificato digitale, nonché la password associata. Ecco il codice corrispondente:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Assicurati di sostituire "pfxPassword" con la tua password effettiva e "pfxFile" con il percorso del file PFX.

## Passaggio 4: aggiunta della firma digitale
Ora che abbiamo configurato la firma digitale, possiamo aggiungerla alla cartella di lavoro di Excel. Ecco il codice corrispondente:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Questo passaggio aggiunge la firma digitale Xades alla cartella di lavoro di Excel.

## Passaggio 5: salvare la cartella di lavoro con la firma
Infine, salviamo la cartella di lavoro di Excel con la firma digitale aggiunta. Ecco il codice corrispondente:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Assicurati di adattare il nome del file di output in base alle tue esigenze.

### Esempio di codice sorgente per Xades Signature Support utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
string sourceDir = RunExamples.Get_SourceDirectory();
//Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Conclusione
Congratulazioni! Hai imparato come utilizzare la libreria Aspose.Cells per .NET per aggiungere una firma digitale Xades a un file Excel. Seguendo i passaggi forniti in questo articolo, sarai in grado di implementare questa funzionalità nei tuoi progetti. Sentiti libero di sperimentare di più con la libreria e scoprire altre potenti funzionalità che offre.

### Domande frequenti

#### D: Cos'è Xades?

R: Xades è uno standard avanzato di firma elettronica utilizzato per garantire l'integrità e l'autenticità dei documenti digitali.

#### D: Posso utilizzare altri tipi di firme digitali con Aspose.Cells?

R: Sì, Aspose.Cells supporta anche altri tipi di firme digitali, come le firme XMLDSig e le firme PKCS#7.

#### D: Posso applicare una firma a tipi di file diversi dai file Excel?
 
R: Sì, Aspose.Cells consente anche di applicare firme digitali ad altri tipi di file supportati come file Word, PDF e PowerPoint.