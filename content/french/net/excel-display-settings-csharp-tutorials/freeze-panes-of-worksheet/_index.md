---
title: Geler les volets de la feuille de calcul
linktitle: Geler les volets de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Manipulez facilement les volets figés d'une feuille de calcul Excel avec Aspose.Cells pour .NET.
type: docs
weight: 70
url: /fr/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
Dans ce didacticiel, nous allons vous montrer comment verrouiller les volets d'une feuille de calcul Excel à l'aide du code source C# avec Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour obtenir le résultat souhaité.

## Étape 1 : Importez les bibliothèques nécessaires

Assurez-vous d'avoir installé la bibliothèque Aspose.Cells pour .NET et importez les bibliothèques nécessaires dans votre projet C#.

```csharp
using Aspose.Cells;
```

## Étape 2 : Définir le chemin du répertoire et ouvrir le fichier Excel

 Définissez le chemin d'accès au répertoire contenant votre fichier Excel, puis ouvrez le fichier en instanciant un`Workbook` objet.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Étape 3 : Accédez à la feuille de calcul et appliquez les paramètres de verrouillage du volet.

 Accédez à la première feuille de calcul du fichier Excel à l'aide du`Worksheet` objet. Utilisez ensuite le`FreezePanes` méthode pour appliquer les paramètres de verrouillage du volet.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Dans l'exemple ci-dessus, les volets sont verrouillés sur la cellule de la ligne 3 et de la colonne 2.

## Étape 4 : Enregistrer les modifications

 Une fois que vous avez apporté les modifications nécessaires, enregistrez le fichier Excel modifié à l'aide du`Save` méthode du`Workbook` objet.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exemple de code source pour geler les volets d'une feuille de calcul à l'aide d'Aspose.Cells pour .NET 

```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichiers contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel via le flux de fichiers
Workbook workbook = new Workbook(fstream);
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Application des paramètres des volets figés
worksheet.FreezePanes(3, 2, 3, 2);
// Sauvegarde du fichier Excel modifié
workbook.Save(dataDir + "output.xls");
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close();
```

## Conclusion

Ce guide étape par étape vous a montré comment verrouiller les volets d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. À l'aide du code source C# fourni, vous pouvez facilement personnaliser les paramètres de verrouillage des volets pour mieux organiser et visualiser vos données dans des fichiers Excel.

### Foire aux questions (FAQ)

#### Qu’est-ce qu’Aspose.Cells pour .NET ?

Aspose.Cells for .NET est une puissante bibliothèque permettant de manipuler des fichiers Excel dans des applications .NET.

#### Comment puis-je installer Aspose.Cells pour .NET ?

 Pour installer Aspose.Cells pour .NET, vous devez télécharger le package correspondant à partir de[Aspose les versions](https://releases/aspose.com/cells/net/) et ajoutez-le à votre projet .NET.

#### Comment verrouiller les volets d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET ?

 Vous pouvez utiliser le`FreezePanes` méthode du`Worksheet` objet pour verrouiller les volets d’une feuille de calcul. Spécifiez les cellules à verrouiller en fournissant des index de ligne et de colonne.

#### Puis-je personnaliser les paramètres de verrouillage du volet avec Aspose.Cells pour .NET ?

 Oui, en utilisant le`FreezePanes` , vous pouvez spécifier les cellules à verrouiller selon vos besoins, en fournissant les index de ligne et de colonne appropriés.
