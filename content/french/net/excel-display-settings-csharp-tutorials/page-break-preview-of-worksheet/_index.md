---
title: Aperçu du saut de page de la feuille de calcul
linktitle: Aperçu du saut de page de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Guide étape par étape pour afficher l'aperçu du saut de page de la feuille de calcul à l'aide de Aspose.Cells pour .NET.
type: docs
weight: 110
url: /fr/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
Dans ce didacticiel, nous allons expliquer comment afficher l'aperçu du saut de page d'une feuille de calcul à l'aide de Aspose.Cells pour .NET. Suivez ces étapes pour obtenir le résultat souhaité :

## Étape 1 : Configurer l'environnement

Assurez-vous d'avoir installé Aspose.Cells pour .NET et configuré votre environnement de développement. Assurez-vous également que vous disposez d'une copie du fichier Excel sur lequel vous souhaitez afficher l'aperçu du saut de page.

## Étape 2 : Importez les dépendances nécessaires

Ajoutez les directives nécessaires pour utiliser les classes d'Aspose.Cells :

```csharp
using Aspose.Cells;
using System.IO;
```

## Étape 3 : Initialisation du code

Commencez par initialiser le chemin du répertoire contenant vos documents Excel :

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Étape 4 : Ouvrir le fichier Excel

 Créer un`FileStream` objet contenant le fichier Excel à ouvrir :

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Instancier un`Workbook` objet et ouvrez le fichier Excel à l'aide du flux de fichiers :

```csharp
Workbook workbook = new Workbook(fstream);
```

## Étape 5 : Accéder à la feuille de calcul

Accédez à la première feuille de calcul du fichier Excel :

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Étape 6 : Affichage de l'aperçu du saut de page

Activez l'aperçu saut de page pour la feuille de calcul :

```csharp
worksheet. IsPageBreakPreview = true;
```

## Étape 7 : Enregistrer les modifications

Enregistrez les modifications apportées au fichier Excel :

```csharp
workbook.Save(dataDir + "output.xls");
```

## Étape 8 : Fermeture du flux de fichiers

Fermez le flux de fichiers pour libérer toutes les ressources :

```csharp
fstream.Close();
```

### Exemple de code source pour l'aperçu du saut de page de la feuille de calcul à l'aide de Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichier contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel via le flux de fichiers
Workbook workbook = new Workbook(fstream);
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Affichage de la feuille de calcul dans l'aperçu des sauts de page
worksheet.IsPageBreakPreview = true;
// Enregistrement du fichier Excel modifié
workbook.Save(dataDir + "output.xls");
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close();
```

## Conclusion

Dans ce didacticiel, vous avez appris à afficher l'aperçu du saut de page d'une feuille de calcul à l'aide de Aspose.Cells pour .NET. En suivant les étapes décrites, vous pouvez facilement contrôler l'apparence et la disposition de vos fichiers Excel.

### Foire aux questions (FAQ)

#### Qu'est-ce qu'Aspose.Cells pour .NET ?

Aspose.Cells pour .NET est une bibliothèque logicielle populaire pour manipuler des fichiers Excel dans des applications .NET.

#### Puis-je afficher l'aperçu saut de page pour une feuille de calcul spécifique au lieu de la feuille de calcul entière ?

Oui, en utilisant Aspose.Cells, vous pouvez activer l'aperçu des sauts de page pour une feuille de calcul spécifique en accédant à l'objet Worksheet correspondant.

#### Aspose.Cells prend-il en charge d'autres fonctionnalités d'édition de fichiers Excel ?

Oui, Aspose.Cells offre un large éventail de fonctionnalités pour l'édition et la manipulation de fichiers Excel, telles que l'ajout de données, le formatage, la création de graphiques, etc.

#### Aspose.Cells fonctionne-t-il uniquement avec des fichiers Excel au format .xls ?

Non, Aspose.Cells prend en charge divers formats de fichiers Excel, notamment .xls et .xlsx.
	