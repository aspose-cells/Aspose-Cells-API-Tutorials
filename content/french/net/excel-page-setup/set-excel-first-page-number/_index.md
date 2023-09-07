---
title: Définir le numéro de la première page Excel
linktitle: Définir le numéro de la première page Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à définir le premier numéro de page dans Excel à l'aide de Aspose.Cells pour .NET.
type: docs
weight: 90
url: /fr/net/excel-page-setup/set-excel-first-page-number/
---
Dans ce didacticiel, nous vous expliquerons comment définir le premier numéro de page dans Excel à l'aide d'Aspose.Cells pour .NET. Nous utiliserons le code source C# pour illustrer le processus.

## Étape 1 : Configurer l'environnement

Assurez-vous que Aspose.Cells pour .NET est installé sur votre machine. Créez également un nouveau projet dans votre environnement de développement préféré.

## Étape 2 : Importer les bibliothèques nécessaires

Dans votre fichier de code, importez les bibliothèques nécessaires pour travailler avec Aspose.Cells. Voici le code correspondant :

```csharp
using Aspose.Cells;
```

## Étape 3 : Définir le répertoire de données

Définissez le répertoire de données dans lequel vous souhaitez enregistrer le fichier Excel modifié. Utilisez le code suivant :

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Assurez-vous de spécifier le chemin d'accès complet au répertoire.

## Étape 4 : Création du classeur et de la feuille de calcul

Créez un nouvel objet Workbook et accédez à la première feuille de calcul du classeur à l'aide du code suivant :

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Cela créera un classeur vide avec une feuille de calcul.

## Étape 5 : Définition du numéro de la première page

Définissez le numéro de la première page des pages de la feuille de calcul à l'aide du code suivant :

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Cela définira le premier numéro de page sur 2.

## Étape 6 : enregistrement du classeur modifié

Enregistrez le classeur modifié à l'aide du code suivant :

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Cela enregistrera le classeur modifié dans le répertoire de données spécifié.

### Exemple de code source pour définir le numéro de la première page Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook();
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Définition du premier numéro de page des pages de la feuille de calcul
worksheet.PageSetup.FirstPageNumber = 2;
// Enregistrez le classeur.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Conclusion

Vous avez maintenant appris à définir le premier numéro de page dans Excel à l'aide d'Aspose.Cells pour .NET. Ce didacticiel vous a guidé à chaque étape du processus, de la configuration de l'environnement à la définition du premier numéro de page. Vous pouvez maintenant utiliser ces connaissances pour personnaliser la numérotation des pages dans vos fichiers Excel.

### FAQ

#### Q1 : Puis-je définir un numéro de première page différent pour chaque feuille de calcul ?

 R1 : Oui, vous pouvez définir un numéro de première page différent pour chaque feuille de calcul en accédant au`FirstPageNumber`propriété de la feuille de calcul respective`PageSetup` objet.

#### Q2 : Comment puis-je vérifier le numéro de la première page d'une feuille de calcul existante ?

 A2 : Vous pouvez vérifier le numéro de la première page d'une feuille de calcul existante en accédant au`FirstPageNumber` propriété de la`PageSetup` objet correspondant à cette feuille de calcul.

#### Q3 : La numérotation des pages commence-t-elle toujours à partir de 1 par défaut ?

A3 : Oui, la numérotation des pages commence à partir de 1 par défaut dans Excel. Cependant, vous pouvez utiliser le code présenté dans ce didacticiel pour définir un numéro de première page différent.

#### Q4 : Les modifications apportées au premier numéro de page sont-elles permanentes dans le fichier Excel modifié ?

R4 : Oui, les modifications apportées au premier numéro de page sont enregistrées de manière permanente dans le fichier Excel modifié.

#### Q5 : Cette méthode fonctionne-t-elle pour tous les formats de fichier Excel, tels que .xls et .xlsx ?

A5 : Oui, cette méthode fonctionne pour tous les formats de fichiers Excel pris en charge par Aspose.Cells, y compris .xls et .xlsx.