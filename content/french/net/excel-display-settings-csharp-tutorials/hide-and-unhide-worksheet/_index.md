---
title: Masquer et afficher la feuille de calcul
linktitle: Masquer et afficher la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Une bibliothèque puissante pour travailler avec des fichiers Excel, notamment pour créer, modifier et manipuler des données.
type: docs
weight: 90
url: /fr/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
Dans ce didacticiel, nous vous expliquerons étape par étape le code source C# suivant qui est utilisé pour masquer et afficher une feuille de calcul à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous :

## Étape 1 : Préparer l’environnement

Avant de commencer, assurez-vous que Aspose.Cells pour .NET est installé sur votre système. Si vous ne l'avez pas déjà installé, vous pouvez le télécharger depuis le site officiel d'Aspose. Une fois installé, vous pouvez créer un nouveau projet dans votre environnement de développement intégré (IDE) préféré.

## Étape 2 : Importer les espaces de noms requis

Dans votre fichier source C#, ajoutez les espaces de noms nécessaires pour utiliser les fonctionnalités d'Aspose.Cells. Ajoutez les lignes suivantes au début de votre fichier :

```csharp
using Aspose.Cells;
using System.IO;
```

## Étape 3 : Chargez le fichier Excel

Avant de masquer ou d'afficher une feuille de calcul, vous devez charger le fichier Excel dans votre application. Assurez-vous d'avoir le fichier Excel que vous souhaitez utiliser dans le même répertoire que votre projet. Utilisez le code suivant pour charger le fichier Excel :

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Assurez-vous de remplacer « CHEMIN VERS LE RÉPERTOIRE DE VOS DOCUMENTS » par le chemin réel du répertoire contenant votre fichier Excel.

## Étape 4 : Accédez à la feuille de calcul

Une fois le fichier Excel chargé, vous pouvez accéder à la feuille de calcul que vous souhaitez masquer ou afficher. Utilisez le code suivant pour accéder à la première feuille de calcul du fichier :

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Étape 5 : Masquer la feuille de calcul

 Maintenant que vous avez accédé à la feuille de calcul, vous pouvez la masquer à l'aide du`IsVisible` propriété. Utilisez le code suivant pour masquer la première feuille de calcul du fichier :

```csharp
worksheet. IsVisible = false;
```

## Étape 6 : Réafficher la feuille de calcul

Si vous souhaitez réafficher la feuille de calcul précédemment masquée, vous pouvez utiliser le même code en modifiant la valeur du`IsVisible` propriété. Utilisez le code suivant pour réafficher la première feuille de calcul :

```csharp
worksheet. IsVisible = true;
```

## Étape 7 : Enregistrer les modifications

Une fois que vous

  Si vous avez masqué ou affiché la feuille de calcul selon vos besoins, vous devez enregistrer les modifications dans le fichier Excel. Utilisez le code suivant pour enregistrer les modifications :

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Assurez-vous de spécifier le chemin de sortie correct pour enregistrer le fichier Excel modifié.

### Exemple de code source pour masquer et afficher une feuille de calcul à l'aide d'Aspose.Cells pour .NET 

```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichiers contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook avec ouverture du fichier Excel via le flux de fichiers
Workbook workbook = new Workbook(fstream);
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Masquer la première feuille de calcul du fichier Excel
worksheet.IsVisible = false;
// Affiche la première feuille de calcul du fichier Excel
//Feuille de travail.IsVisible = true ;
// Enregistrement du fichier Excel modifié au format par défaut (c'est-à-dire Excel 2003)
workbook.Save(dataDir + "output.out.xls");
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close();
```

## Conclusion

Félicitation ! Vous avez appris à masquer et afficher une feuille de calcul à l'aide d'Aspose.Cells pour .NET. Vous pouvez désormais utiliser cette fonctionnalité pour contrôler la visibilité de vos feuilles de calcul dans vos fichiers Excel.

### Foire aux questions (FAQ)

#### Comment puis-je installer Aspose.Cells pour .NET ?

 Vous pouvez installer Aspose.Cells pour .NET en téléchargeant le package NuGet approprié à partir de[Aspose les versions](https://releases/aspose.com/cells/net/) et en l'ajoutant à votre projet Visual Studio.

#### Quelle est la version minimale requise de .NET Framework pour utiliser Aspose.Cells pour .NET ?

Aspose.Cells pour .NET prend en charge .NET Framework 2.0 et versions ultérieures.

#### Puis-je ouvrir et modifier des fichiers Excel existants avec Aspose.Cells pour .NET ?

Oui, vous pouvez ouvrir et modifier des fichiers Excel existants à l'aide d'Aspose.Cells pour .NET. Vous pouvez accéder aux feuilles de calcul, aux cellules, aux formules et à d'autres éléments du fichier Excel.

#### Aspose.Cells for .NET prend-il en charge la création de rapports et l'exportation vers d'autres formats de fichiers ?

Oui, Aspose.Cells pour .NET prend en charge la génération et l'exportation de rapports vers des formats tels que PDF, HTML, CSV, TXT, etc.

#### La modification du fichier Excel est-elle définitive ?

Oui, la modification du fichier Excel est permanente une fois que vous l'avez enregistré. Assurez-vous d'enregistrer une copie de sauvegarde avant d'apporter des modifications au fichier d'origine.