---
title: Estrai il file Mol incorporato
linktitle: Estrai il file Mol incorporato
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come estrarre facilmente file MOL incorporati da una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 90
url: /it/net/excel-workbook/extract-embedded-mol-file/
---
In questo tutorial, ti guideremo passo dopo passo come estrarre un file MOL incorporato da una cartella di lavoro di Excel utilizzando la libreria Aspose.Cells per .NET. Imparerai come sfogliare i fogli della cartella di lavoro, estrarre gli oggetti OLE corrispondenti e salvare i file MOL estratti. Seguire i passaggi seguenti per completare questa attività con successo.

## Passaggio 1: definire le directory di origine e di output
Innanzitutto, dobbiamo definire le directory di origine e di output nel nostro codice. Queste directory indicano dove si trova la cartella di lavoro Excel di origine e dove verranno salvati i file MOL estratti. Ecco il codice corrispondente:

```csharp
// Directory
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Assicurati di specificare i percorsi appropriati secondo necessità.

## Passaggio 2: caricamento della cartella di lavoro di Excel
Il passaggio successivo consiste nel caricare la cartella di lavoro di Excel contenente gli oggetti OLE incorporati e i file MOL. Ecco il codice per caricare la cartella di lavoro:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Assicurati di specificare correttamente il nome del file di origine nel codice.

## Passaggio 3: Attraversa i fogli ed estrai i file MOL
Ora scorreremo ogni foglio della cartella di lavoro ed estrarremo gli oggetti OLE corrispondenti, che contengono i file MOL. Ecco il codice corrispondente:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Questo codice scorre ogni foglio della cartella di lavoro, recupera gli oggetti OLE e salva i file MOL estratti nella directory di output.

### Codice sorgente di esempio per estrarre il file Mol incorporato utilizzando Aspose.Cells per .NET 
```csharp
//directory
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Conclusione
Congratulazioni! Hai imparato come estrarre un file MOL incorporato da una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Ora puoi applicare queste conoscenze per estrarre file MOL dalle tue cartelle di lavoro Excel. Sentiti libero di esplorare ulteriormente la libreria Aspose.Cells e conoscere le sue altre potenti funzionalità.

### Domande frequenti

#### D: Cos'è un file MOL?
 
R: Un file MOL è un formato di file utilizzato per rappresentare strutture chimiche nella chimica computazionale. Contiene informazioni su atomi, legami e altre proprietà molecolari.

#### D: questo metodo funziona con tutti i tipi di file Excel?

R: Sì, questo metodo funziona con tutti i tipi di file Excel supportati da Aspose.Cells.

#### D: Posso estrarre più file MOL contemporaneamente?

R: Sì, puoi estrarre più file MOL contemporaneamente eseguendo l'iterazione degli oggetti OLE su ciascun foglio della cartella di lavoro.