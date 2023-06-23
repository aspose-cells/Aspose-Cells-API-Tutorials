---
title: Excel Copier des feuilles de calcul entre des classeurs
linktitle: Excel Copier des feuilles de calcul entre des classeurs
second_title: Référence de l'API Aspose.Cells pour .NET
description: Copiez facilement des feuilles de calcul entre des classeurs Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 30
url: /fr/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
Dans ce didacticiel, nous vous guiderons à travers les étapes pour copier des feuilles de calcul entre des classeurs Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Suivez les instructions ci-dessous pour effectuer cette tâche.

## Étape 1 : Préparation

Assurez-vous d'avoir installé Aspose.Cells pour .NET et créé un projet C# dans votre environnement de développement intégré (IDE) préféré.

## Étape 2 : Définissez le chemin d'accès au répertoire de documents

 Déclarer un`dataDir` variable et initialisez-la avec le chemin d'accès à votre répertoire de documents. Par exemple :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENTS_DIRECTORY"` avec le chemin d'accès réel à votre répertoire.

## Étape 3 : Définissez le chemin d'accès au fichier d'entrée

 Déclarer un`InputPath` variable et initialisez-la avec le chemin complet du fichier Excel à partir duquel vous souhaitez copier la feuille de calcul. Par exemple :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Assurez-vous d'avoir le fichier Excel`book1.xls` dans votre répertoire de documents ou spécifiez le nom et l'emplacement corrects du fichier.

## Étape 4 : Créer un premier classeur Excel

 Utilisez le`Workbook` class de Aspose.Cells pour créer un premier classeur Excel et ouvrir le fichier spécifié :

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Étape 5 : Créer un deuxième classeur Excel

Créez un deuxième classeur Excel :

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Étape 6 : Copiez la feuille de calcul du premier classeur vers le deuxième classeur

 Utilisez le`Copy`méthode pour copier la première feuille de calcul du premier classeur vers le deuxième classeur :

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Étape 7 : Enregistrez le fichier Excel

Enregistrez le fichier Excel contenant la feuille de calcul copiée :

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Assurez-vous de spécifier le chemin et le nom de fichier souhaités pour le fichier de sortie.

### Exemple de code source pour Excel Copier des feuilles de calcul entre des classeurs à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Créer un classeur.
// Ouvrez un fichier dans le premier livre.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Créez un autre classeur.
Workbook excelWorkbook1 = new Workbook();
// Copiez la première feuille du premier livre dans le deuxième livre.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Enregistrez le fichier.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Conclusion

Félicitation ! Vous avez maintenant appris à copier des feuilles de calcul entre des classeurs Excel à l'aide d'Aspose.Cells pour .NET. N'hésitez pas à utiliser cette méthode dans vos propres projets pour manipuler efficacement les fichiers Excel.

### FAQ

#### Q. Quelles bibliothèques sont nécessaires pour utiliser Aspose.Cells pour .NET ?

A. Pour utiliser Aspose.Cells pour .NET, vous devez inclure la bibliothèque Aspose.Cells dans votre projet. Assurez-vous d'avoir correctement référencé cette bibliothèque dans votre environnement de développement intégré (IDE).

#### Q. Aspose.Cells prend-il en charge d'autres formats de fichiers Excel, tels que XLSX ?

A. Oui, Aspose.Cells prend en charge divers formats de fichiers Excel, notamment XLSX, XLS, CSV, HTML et bien d'autres. Vous pouvez manipuler ces formats de fichiers à l'aide des fonctionnalités d'Aspose.Cells pour .NET.

#### Q. Puis-je personnaliser les options de mise en page lors de la copie de la feuille de calcul ?

A.  Oui, vous pouvez personnaliser les options de mise en page lors de la copie de la feuille de calcul à l'aide des propriétés du`PageSetup` objet. Vous pouvez spécifier des en-têtes de page, des pieds de page, des marges, des orientations, etc.