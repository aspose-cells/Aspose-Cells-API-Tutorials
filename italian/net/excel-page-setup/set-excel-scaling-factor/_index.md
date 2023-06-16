---
title: Imposta il fattore di scala di Excel
linktitle: Imposta il fattore di scala di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Impara a manipolare facilmente i file Excel e personalizzare il fattore di scala utilizzando Aspose.Cells per .NET.
type: docs
weight: 180
url: /it/net/excel-page-setup/set-excel-scaling-factor/
---
In questa guida, ti illustreremo come impostare il fattore di scala in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Seguire i passaggi seguenti per eseguire questa operazione.

## Passaggio 1: configurazione dell'ambiente

Assicurati di aver impostato il tuo ambiente di sviluppo e installato Aspose.Cells per .NET. È possibile scaricare l'ultima versione della libreria dal sito Web ufficiale di Aspose.

## Passaggio 2: importa gli spazi dei nomi richiesti

Nel tuo progetto C#, importa gli spazi dei nomi necessari per lavorare con Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostazione del percorso della directory dei documenti

 Dichiara un`dataDir` variabile per specificare il percorso della directory in cui si desidera salvare il file Excel generato:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENT_DIRECTORY"` con il percorso corretto sul tuo sistema.

## Passaggio 4: creazione di un oggetto cartella di lavoro

Crea un'istanza di un oggetto Workbook che rappresenta la cartella di lavoro di Excel che desideri creare:

```csharp
Workbook workbook = new Workbook();
```

## Passaggio 5: accesso al primo foglio di lavoro

Passare al primo foglio di lavoro nella cartella di lavoro di Excel utilizzando il codice seguente:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Passaggio 6: impostare il fattore di scala

Impostare il fattore di scala utilizzando il seguente codice:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Qui abbiamo impostato il fattore di scala su 100, il che significa che il foglio di calcolo verrà visualizzato al 100% delle dimensioni normali una volta stampato.

## Passaggio 7: salvare la cartella di lavoro di Excel

 Per salvare la cartella di lavoro di Excel con il fattore di scala definito, utilizzare il file`Save` metodo dell'oggetto Workbook:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Ciò salverà la cartella di lavoro di Excel con il nome file "ScalingFactor_out.xls" nella directory specificata.

### Esempio di codice sorgente per Imposta fattore di scala Excel utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Impostare il fattore di scala su 100
worksheet.PageSetup.Zoom = 100;
// Salva la cartella di lavoro.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Conclusione

Congratulazioni! Hai imparato come impostare il fattore di scala in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Il fattore di scala consente di regolare le dimensioni del foglio di calcolo durante la stampa per una visualizzazione ottimale.

### Domande frequenti

#### 1. Come impostare il fattore di scala nel foglio di calcolo Excel con Aspose.Cells per .NET?

 Usa il`Zoom` proprietà del`PageSetup`oggetto per impostare il fattore di scala. Per esempio,`worksheet.PageSetup.Zoom = 100;` imposterà il fattore di scala al 100%.

#### 2. Posso personalizzare il fattore di scala in base alle mie esigenze?

 Sì, puoi regolare il fattore di scala modificando il valore assegnato a`Zoom` proprietà. Per esempio,`worksheet.PageSetup.Zoom = 75;` imposterà il fattore di scala al 75%.

#### 3. È possibile salvare la cartella di lavoro di Excel con il fattore di scala definito?

 Sì, puoi usare il`Save` metodo del`Workbook` oggetto per salvare la cartella di lavoro di Excel con il fattore di scala definito.