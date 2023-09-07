---
title: Définir le facteur d'échelle Excel
linktitle: Définir le facteur d'échelle Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à manipuler facilement des fichiers Excel et à personnaliser le facteur d'échelle à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 180
url: /fr/net/excel-page-setup/set-excel-scaling-factor/
---
Dans ce guide, nous vous expliquerons comment définir le facteur d'échelle dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour accomplir cette tâche.

## Étape 1 : Configurer l'environnement

Assurez-vous d'avoir configuré votre environnement de développement et installé Aspose.Cells pour .NET. Vous pouvez télécharger la dernière version de la bibliothèque sur le site officiel d'Aspose.

## Étape 2 : Importer les espaces de noms requis

Dans votre projet C#, importez les espaces de noms nécessaires pour travailler avec Aspose.Cells :

```csharp
using Aspose.Cells;
```

## Étape 3 : Définition du chemin d'accès au répertoire des documents

 Déclarer un`dataDir` variable pour spécifier le chemin d'accès au répertoire où vous souhaitez enregistrer le fichier Excel généré :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENT_DIRECTORY"` avec le bon chemin sur votre système.

## Étape 4 : Création d'un objet de classeur

Instanciez un objet Workbook qui représente le classeur Excel que vous souhaitez créer :

```csharp
Workbook workbook = new Workbook();
```

## Étape 5 : Accéder à la première feuille de travail

Accédez à la première feuille de calcul du classeur Excel à l'aide du code suivant :

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Étape 6 : Définir le facteur d'échelle

Définissez le facteur d'échelle à l'aide du code suivant :

```csharp
worksheet.PageSetup.Zoom = 100;
```

Ici, nous avons défini le facteur d'échelle sur 100, ce qui signifie que la feuille de calcul sera affichée à 100 % de sa taille normale lors de l'impression.

## Étape 7 : Enregistrer le classeur Excel

 Pour enregistrer le classeur Excel avec le facteur d'échelle défini, utilisez le`Save` méthode de l'objet Workbook :

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Cela enregistrera le classeur Excel avec le nom de fichier "ScalingFactor_out.xls" dans le répertoire spécifié.

### Exemple de code source pour définir le facteur d'échelle Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook();
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Réglage du facteur d'échelle sur 100
worksheet.PageSetup.Zoom = 100;
// Enregistrez le classeur.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Conclusion

Félicitation ! Vous avez appris à définir le facteur d'échelle dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Le facteur d'échelle vous permet d'ajuster la taille de la feuille de calcul lors de l'impression pour un affichage optimal.

### FAQ

#### 1. Comment définir le facteur d'échelle dans une feuille de calcul Excel avec Aspose.Cells pour .NET ?

 Utilisez le`Zoom` propriété de la`PageSetup`objet pour définir le facteur d'échelle. Par exemple,`worksheet.PageSetup.Zoom = 100;` définira le facteur d'échelle sur 100 %.

#### 2. Puis-je personnaliser le facteur d'échelle en fonction de mes besoins ?

 Oui, vous pouvez ajuster le facteur d'échelle en modifiant la valeur attribuée au`Zoom` propriété. Par exemple,`worksheet.PageSetup.Zoom = 75;` définira le facteur d'échelle sur 75 %.

#### 3. Est-il possible d'enregistrer le classeur Excel avec le facteur d'échelle défini ?

 Oui, vous pouvez utiliser le`Save` méthode de la`Workbook` objet pour enregistrer le classeur Excel avec le facteur d'échelle défini.