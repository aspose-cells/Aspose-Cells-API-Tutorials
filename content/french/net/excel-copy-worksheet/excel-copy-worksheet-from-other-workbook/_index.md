---
title: Feuille de calcul de copie Excel à partir d'un autre classeur
linktitle: Feuille de calcul de copie Excel à partir d'un autre classeur
second_title: Référence de l'API Aspose.Cells pour .NET
description: Copiez facilement une feuille de calcul Excel d'un classeur à un autre à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 10
url: /fr/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
Dans ce didacticiel, nous vous guiderons à travers les étapes pour copier une feuille de calcul Excel à partir d'un autre classeur à l'aide de la bibliothèque Aspose.Cells pour .NET. Suivez les instructions ci-dessous pour effectuer cette tâche.

## Étape 1 : Préparation

Avant de commencer, assurez-vous d'avoir installé Aspose.Cells pour .NET et créé un projet C# dans votre environnement de développement intégré (IDE) préféré.

## Étape 2 : Définissez le chemin d'accès au répertoire de documents

 Déclarer un`dataDir` variable et initialisez-la avec le chemin d'accès à votre répertoire de documents. Par exemple :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENTS_DIRECTORY"` avec le chemin d'accès réel à votre répertoire.

## Étape 3 : Créer un nouveau classeur Excel

 Utilisez le`Workbook` classe de Aspose.Cells pour créer un nouveau classeur Excel :

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Étape 4 : Obtenir la première feuille de calcul du classeur

Accédez à la première feuille de calcul du classeur à l'aide de l'index 0 :

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Étape 5 : Ajouter des données aux lignes d'en-tête (A1 : A4)

 Utiliser un`for` boucle pour ajouter des données aux lignes d'en-tête (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Étape 6 : Ajouter des données détaillées (A5 : A999)

 Utilisez un autre`for` boucle pour ajouter des données détaillées (A5:A999) :

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Étape 7 : Définir les options de mise en page

 Définissez les options de mise en page pour la feuille de calcul à l'aide de la`PageSetup` objet:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Étape 8 : Créer un autre classeur Excel

Créez un autre classeur Excel :

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Étape 9 : Obtenir la première feuille de calcul du deuxième classeur

Accédez à la première feuille de calcul du deuxième classeur :

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Étape 10 : Nommez la feuille de calcul

nommer le feu

îlot de calcul :

```csharp
ws1.Name = "MySheet";
```

## Étape 11 : Copier les données de la première feuille de calcul du premier classeur vers la première feuille de calcul du deuxième classeur

Copiez les données de la première feuille de calcul du premier classeur vers la première feuille de calcul du deuxième classeur :

```csharp
ws1.Copy(ws0);
```

## Étape 12 : Enregistrez le fichier Excel

Enregistrez le fichier Excel :

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Assurez-vous de spécifier le chemin et le nom de fichier souhaités pour le fichier de sortie.

### Exemple de code source pour Excel Copier une feuille de calcul à partir d'un autre classeur à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Créez un nouveau classeur.
Workbook excelWorkbook0 = new Workbook();
// Obtenez la première feuille de calcul du livre.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Mettez des données dans les lignes d'en-tête (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Mettez des données détaillées (A5: A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Définissez un objet pagesetup basé sur la première feuille de calcul.
PageSetup pagesetup = ws0.PageSetup;
// Les cinq premières lignes sont répétées dans chaque page...
// Il peut être vu dans l'aperçu avant impression.
pagesetup.PrintTitleRows = "$1:$5";
// Créez un autre classeur.
Workbook excelWorkbook1 = new Workbook();
// Obtenez la première feuille de calcul du livre.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Nommez la feuille de calcul.
ws1.Name = "MySheet";
// Copiez les données de la première feuille de calcul du premier classeur dans le
// première feuille de travail du deuxième cahier.
ws1.Copy(ws0);
// Enregistrez le fichier excel.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Conclusion

Félicitation ! Vous avez maintenant appris à copier une feuille de calcul Excel à partir d'un autre classeur à l'aide d'Aspose.Cells pour .NET. N'hésitez pas à utiliser cette méthode dans vos propres projets pour manipuler efficacement les fichiers Excel.

### FAQ

#### Q. Quelles bibliothèques sont nécessaires pour utiliser Aspose.Cells pour .NET ?

A. Pour utiliser Aspose.Cells pour .NET, vous devez inclure la bibliothèque Aspose.Cells dans votre projet. Assurez-vous d'avoir correctement référencé cette bibliothèque dans votre environnement de développement intégré (IDE).

#### Q. Aspose.Cells prend-il en charge d'autres formats de fichiers Excel, tels que XLSX ?

A. Oui, Aspose.Cells prend en charge divers formats de fichiers Excel, notamment XLSX, XLS, CSV, HTML et bien d'autres. Vous pouvez manipuler ces formats de fichiers à l'aide des fonctionnalités d'Aspose.Cells pour .NET.

#### Q. Puis-je personnaliser les options de mise en page lors de la copie de la feuille de calcul ?

A.  Oui, vous pouvez personnaliser les options de mise en page lors de la copie de la feuille de calcul à l'aide des propriétés du`PageSetup` objet. Vous pouvez spécifier des en-têtes de page, des pieds de page, des marges, des orientations, etc.