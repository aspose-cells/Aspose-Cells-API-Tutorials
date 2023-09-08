---
title: Définir la qualité d'impression Excel
linktitle: Définir la qualité d'impression Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à gérer et à personnaliser des fichiers Excel, y compris les options d'impression à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 160
url: /fr/net/excel-page-setup/set-excel-print-quality/
---
Dans ce guide, nous expliquerons comment définir la qualité d'impression d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Nous vous guiderons étape par étape à travers le code source C# fourni pour accomplir cette tâche.

## Étape 1 : Configuration de l'environnement

Avant de commencer, assurez-vous d'avoir configuré votre environnement de développement et installé Aspose.Cells pour .NET. Vous pouvez télécharger la dernière version de la bibliothèque sur le site officiel d'Aspose.

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

## Étape 6 : Définition de la qualité d'impression

Pour définir la qualité d'impression de la feuille de calcul, utilisez le code suivant :

```csharp
worksheet.PageSetup.PrintQuality = 180;
```

Ici, nous avons défini la qualité d'impression sur 180 dpi, mais vous pouvez ajuster cette valeur en fonction de vos besoins.

## Étape 7 : Enregistrement du classeur Excel

 Pour enregistrer le classeur Excel avec la qualité d'impression définie, utilisez le`Save` méthode de l'objet Workbook :

```csharp
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

Cela enregistrera le classeur Excel avec le nom de fichier « SetPrintQuality_out.xls » dans le répertoire spécifié.

### Exemple de code source pour définir la qualité d'impression Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook();
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Définition de la qualité d'impression de la feuille de calcul sur 180 dpi
worksheet.PageSetup.PrintQuality = 180;
// Enregistrez le classeur.
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

## Conclusion

Félicitation ! Vous avez appris à définir la qualité d'impression d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Vous pouvez désormais personnaliser la qualité d'impression de vos fichiers Excel en fonction de vos préférences et besoins spécifiques.

## FAQ


#### 1. Puis-je personnaliser la qualité d’impression de différentes feuilles de calcul dans le même fichier Excel ?

Oui, vous pouvez personnaliser la qualité d'impression de chaque feuille de calcul individuellement en accédant à l'objet Feuille de calcul correspondant et en définissant la qualité d'impression appropriée.

#### 2. Quelles autres options d'impression puis-je personnaliser avec Aspose.Cells pour .NET ?

En plus de la qualité d'impression, vous pouvez personnaliser diverses autres options d'impression telles que les marges, l'orientation de la page, l'échelle d'impression, etc.

#### 3. Aspose.Cells pour .NET prend-il en charge différents formats de fichiers Excel ?

Oui, Aspose.Cells for .NET prend en charge un large éventail de formats de fichiers Excel, notamment XLSX, XLS, CSV, HTML, PDF, etc.