---
title: Définir le titre d'impression Excel
linktitle: Définir le titre d'impression Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à manipuler facilement les fichiers Excel et à personnaliser les options d'impression à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 170
url: /fr/net/excel-page-setup/set-excel-print-title/
---
Dans ce guide, nous vous expliquerons comment définir des titres à imprimer dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour accomplir cette tâche.

## Étape 1 : Configuration de l'environnement

Assurez-vous d'avoir configuré votre environnement de développement et installé Aspose.Cells pour .NET. Vous pouvez télécharger la dernière version de la bibliothèque sur le site officiel d'Aspose.

## Étape 2 : Importer les espaces de noms requis

Dans votre projet C#, importez les espaces de noms nécessaires pour travailler avec Aspose.Cells :

```csharp
using Aspose.Cells;
```

## Étape 3 : Définition du chemin d'accès au répertoire des documents

 Déclarer un`dataDir` variable pour spécifier le chemin d'accès au répertoire dans lequel vous souhaitez enregistrer le fichier Excel généré :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENT_DIRECTORY"` avec le chemin correct sur votre système.

## Étape 4 : Création d'un objet classeur

Instanciez un objet Workbook qui représente le classeur Excel que vous souhaitez créer :

```csharp
Workbook workbook = new Workbook();
```

## Étape 5 : Accès à la première feuille de calcul

Accédez à la première feuille de calcul du classeur Excel à l'aide du code suivant :

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Étape 6 : Définition des colonnes de titre

Définissez les colonnes de titre à l'aide du code suivant :

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Ici, nous avons défini les colonnes A et B comme colonnes de titre. Vous pouvez ajuster cette valeur en fonction de vos besoins.

## Étape 7 : Définir les lignes de titre

Définissez les lignes de titre à l'aide du code suivant :

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Nous avons défini les lignes 1 et 2 comme lignes de titre. Vous pouvez ajuster ces valeurs en fonction de vos besoins.

## Étape 8 : Sauvegarde du classeur Excel

 Pour enregistrer le classeur Excel avec les titres d'impression définis, utilisez le`Save` méthode de l'objet Workbook :

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Cela enregistrera le classeur Excel avec le nom de fichier « SetPrintTitle_out.xls » dans le répertoire spécifié.

### Exemple de code source pour définir le titre d'impression Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook();
// Obtention de la référence du PageSetup de la feuille de calcul
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Définir les numéros de colonnes A et B comme colonnes de titre
pageSetup.PrintTitleColumns = "$A:$B";
// Définir les numéros de ligne 1 et 2 comme lignes de titre
pageSetup.PrintTitleRows = "$1:$2";
// Enregistrez le classeur.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Conclusion

Félicitation ! Vous avez appris à définir des titres à imprimer dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Les titres imprimés vous permettent d'afficher des lignes et des colonnes spécifiques sur chaque page imprimée, ce qui facilite la lecture et la référence des données.

### FAQ

#### 1. Puis-je définir des titres à imprimer pour des colonnes spécifiques dans Excel ?

 Oui, avec Aspose.Cells pour .NET, vous pouvez définir des colonnes spécifiques comme titres à imprimer à l'aide du`PrintTitleColumns` propriété du`PageSetup` objet.

#### 2. Est-il possible de définir à la fois les titres des colonnes et des lignes à imprimer ?

 Oui, vous pouvez définir à la fois les titres des colonnes et des lignes à l'aide de l'option`PrintTitleColumns` et`PrintTitleRows` propriétés du`PageSetup` objet.

#### 3. Quels autres paramètres de mise en page puis-je personnaliser avec Aspose.Cells pour .NET ?

Avec Aspose.Cells pour .NET, vous pouvez personnaliser divers paramètres de mise en page, tels que les marges, l'orientation de la page, l'échelle d'impression, etc.