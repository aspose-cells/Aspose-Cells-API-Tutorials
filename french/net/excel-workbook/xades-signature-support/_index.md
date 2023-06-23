---
title: Prise en charge des signatures Xades
linktitle: Prise en charge des signatures Xades
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment ajouter une signature Xades à un fichier Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 190
url: /fr/net/excel-workbook/xades-signature-support/
---
Dans cet article, nous vous expliquerons étape par étape le code source C # ci-dessous, qui concerne la prise en charge de la signature Xades à l'aide de la bibliothèque Aspose.Cells pour .NET. Vous découvrirez comment utiliser cette bibliothèque pour ajouter une signature numérique Xades à un fichier Excel. Nous vous fournirons également un aperçu du processus de signature et de son exécution. Suivez les étapes ci-dessous pour obtenir des résultats concluants.

## Étape 1 : Définir les répertoires source et de sortie
Pour commencer, nous devons définir les répertoires source et de sortie dans notre code. Ces répertoires indiquent où se trouvent les fichiers source et où le fichier de sortie sera enregistré. Voici le code correspondant :

```csharp
// Répertoire des sources
string sourceDir = RunExamples.Get_SourceDirectory();
// Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
```

Assurez-vous d'adapter les chemins d'accès aux répertoires selon vos besoins.

## Étape 2 : chargement du classeur Excel
L'étape suivante consiste à charger le classeur Excel sur lequel nous voulons ajouter la signature numérique Xades. Voici le code pour charger le classeur :

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Assurez-vous de spécifier correctement le nom du fichier source dans le code.

## Étape 3 : Configuration de la signature numérique
Nous allons maintenant configurer la signature numérique Xades en fournissant les informations nécessaires. Il faut préciser le fichier PFX contenant le certificat numérique, ainsi que le mot de passe associé. Voici le code correspondant :

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Assurez-vous de remplacer "pfxPassword" par votre mot de passe actuel et "pfxFile" par le chemin d'accès au fichier PFX.

## Étape 4 : Ajout de la signature numérique
Maintenant que nous avons configuré la signature numérique, nous pouvons l'ajouter au classeur Excel. Voici le code correspondant :

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Cette étape ajoute la signature numérique Xades au classeur Excel.

## Étape 5 : Enregistrer le classeur avec la signature
Enfin, nous enregistrons le classeur Excel avec la signature numérique ajoutée. Voici le code correspondant :

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Assurez-vous d'adapter le nom du fichier de sortie en fonction de vos besoins.

### Exemple de code source pour la prise en charge de la signature Xades à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire des sources
string sourceDir = RunExamples.Get_SourceDirectory();
//Répertoire de sortie
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

## Conclusion
Félicitation ! Vous avez appris à utiliser la bibliothèque Aspose.Cells pour .NET pour ajouter une signature numérique Xades à un fichier Excel. En suivant les étapes fournies dans cet article, vous pourrez implémenter cette fonctionnalité dans vos propres projets. N'hésitez pas à expérimenter davantage avec la bibliothèque et à découvrir d'autres fonctionnalités puissantes qu'elle offre.

### FAQ

#### Q : Qu'est-ce que Xades ?

R : Xades est une norme de signature électronique avancée utilisée pour garantir l'intégrité et l'authenticité des documents numériques.

#### Q : Puis-je utiliser d'autres types de signatures numériques avec Aspose.Cells ?

R : Oui, Aspose.Cells prend également en charge d'autres types de signatures numériques, telles que les signatures XMLDSig et les signatures PKCS#7.

#### Q : Puis-je appliquer une signature à d'autres types de fichiers que les fichiers Excel ?
 
R : Oui, Aspose.Cells permet également d'appliquer des signatures numériques à d'autres types de fichiers pris en charge tels que les fichiers Word, PDF et PowerPoint.