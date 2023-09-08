---
title: Ajouter une signature numérique à un fichier Excel déjà signé
linktitle: Ajouter une signature numérique à un fichier Excel déjà signé
second_title: Référence de l'API Aspose.Cells pour .NET
description: Ajoutez facilement des signatures numériques aux fichiers Excel existants avec Aspose.Cells pour .NET.
type: docs
weight: 30
url: /fr/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Dans ce guide étape par étape, nous expliquerons le code source C# fourni qui vous permettra d'ajouter une signature numérique à un fichier Excel déjà signé à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour ajouter une nouvelle signature numérique à un fichier Excel existant.

## Étape 1 : Définir les répertoires source et de sortie

```csharp
// répertoire source
string sourceDir = RunExamples.Get_SourceDirectory();

// Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
```

Dans cette première étape, nous définissons les répertoires source et de sortie qui seront utilisés pour charger le fichier Excel existant et enregistrer le fichier avec la nouvelle signature numérique.

## Étape 2 : Charger le fichier Excel existant

```csharp
// Charger le classeur Excel déjà signé
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Ici, nous chargeons le fichier Excel déjà signé en utilisant le`Workbook` classe d’Aspose.Cells.

## Étape 3 : Créer la collection de signatures numériques

```csharp
// Créer la collection de signatures numériques
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Nous créons une nouvelle collection de signatures numériques en utilisant le`DigitalSignatureCollection` classe.

## Étape 4 : Créer un nouveau certificat

```csharp
// Créer un nouveau certificat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Ici, nous créons un nouveau certificat à partir du fichier et du mot de passe fournis.

## Étape 5 : Ajouter une nouvelle signature numérique à la collection

```csharp
// Créer une nouvelle signature numérique
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Ajouter la signature numérique à la collection
dsCollection.Add(signature);
```

 Nous créons une nouvelle signature numérique en utilisant le`DigitalSignature` classe et ajoutez-le à la collection de signatures numériques.

## Étape 6 : Ajouter la collection de signatures numériques au classeur

```csharp
//Ajouter la collection de signatures numériques au classeur
workbook.AddDigitalSignature(dsCollection);
```

 Nous ajoutons la collection de signatures numériques au classeur Excel existant en utilisant le`AddDigitalSignature()` méthode.

## Étape 7 : Enregistrez et fermez le classeur

```csharp
// Enregistrez le classeur et fermez-le
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Nous enregistrons le classeur avec la nouvelle signature numérique dans le répertoire de sortie spécifié, puis le fermons et libérons les ressources associées.

### Exemple de code source pour ajouter une signature numérique à un fichier Excel déjà signé à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire source
string sourceDir = RunExamples.Get_SourceDirectory();
//Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
//Fichier de certificat et son mot de passe
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Chargez le classeur déjà signé numériquement pour ajouter une nouvelle signature numérique
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Créer la collection de signatures numériques
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Créer un nouveau certificat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Créez une nouvelle signature numérique et ajoutez-la à la collection de signatures numériques
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Ajouter une collection de signatures numériques dans le classeur
workbook.AddDigitalSignature(dsCollection);
//Enregistrez le classeur et supprimez-le.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Conclusion

Félicitation ! Vous avez maintenant appris à ajouter une signature numérique à un fichier Excel déjà signé à l'aide d'Aspose.Cells pour .NET. Les signatures numériques ajoutent une couche de sécurité supplémentaire à vos fichiers Excel, garantissant leur authenticité et leur intégrité.

### FAQ

#### Q : Qu'est-ce qu'Aspose.Cells pour .NET ?

R : Aspose.Cells for .NET est une puissante bibliothèque de classes qui permet aux développeurs .NET de créer, modifier, convertir et manipuler facilement des fichiers Excel.

#### Q : Qu'est-ce qu'une signature numérique dans un fichier Excel ?

R : Une signature numérique dans un fichier Excel est une marque électronique qui garantit l'authenticité, l'intégrité et l'origine du document. Il permet de vérifier que le fichier n'a pas été modifié depuis sa signature et qu'il provient d'une source fiable.

#### Q : Quels sont les avantages de l’ajout d’une signature numérique à un fichier Excel ?

R : L'ajout d'une signature numérique à un fichier Excel offre plusieurs avantages, notamment une protection contre les modifications non autorisées, la garantie de l'intégrité des données, l'authentification de l'auteur du document et la confiance dans les informations qu'il contient.

#### Q : Puis-je ajouter plusieurs signatures numériques à un fichier Excel ?

: Oui, Aspose.Cells vous permet d'ajouter plusieurs signatures numériques à un fichier Excel. Vous pouvez créer une collection de signatures numériques et les ajouter au fichier en une seule opération.

#### Q : Quelles sont les conditions requises pour ajouter une signature numérique à un fichier Excel ?

R : Pour ajouter une signature numérique à un fichier Excel, vous avez besoin d'un certificat numérique valide qui sera utilisé pour signer le document. Assurez-vous d'avoir le certificat et le mot de passe corrects avant d'ajouter la signature numérique.