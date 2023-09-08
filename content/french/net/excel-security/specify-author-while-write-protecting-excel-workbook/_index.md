---
title: Spécifier l'auteur lors de la protection en écriture du classeur Excel
linktitle: Spécifier l'auteur lors de la protection en écriture du classeur Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment protéger et personnaliser vos classeurs Excel à l'aide d'Aspose.Cells pour .NET. Tutoriel étape par étape en C#.
type: docs
weight: 30
url: /fr/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

Dans ce didacticiel, nous allons vous montrer comment spécifier l'auteur lors de la protection en écriture d'un classeur Excel à l'aide de la bibliothèque Aspose.Cells pour .NET.

## Étape 1 : Préparer l’environnement

Avant de commencer, assurez-vous que Aspose.Cells for .NET est installé sur votre ordinateur. Téléchargez la bibliothèque depuis le site officiel d'Aspose et suivez les instructions d'installation fournies.

## Étape 2 : Configuration des répertoires source et de sortie

Dans le code source fourni, vous devez spécifier les répertoires source et de sortie. Modifier le`sourceDir` et`outputDir` variables en remplaçant « VOTRE RÉPERTOIRE SOURCE » et « VOTRE RÉPERTOIRE DE SORTIE » par les chemins absolus respectifs sur votre machine.

```csharp
// Répertoire source
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Répertoire de sortie
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Étape 3 : Création d'un classeur Excel vide

Pour commencer, nous créons un objet Workbook qui représente un classeur Excel vide.

```csharp
// Créez un classeur vide.
Workbook wb = new Workbook();
```

## Étape 4 : Protection en écriture avec mot de passe

 Ensuite, nous spécifions un mot de passe pour protéger en écriture le classeur Excel à l'aide du`WriteProtection.Password` propriété de l’objet Workbook.

```csharp
// Écrire un classeur protégé avec un mot de passe.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Étape 5 : Spécification de l'auteur

 Nous spécifions maintenant l'auteur du classeur Excel à l'aide du`WriteProtection.Author` propriété de l’objet Workbook.

```csharp
// Spécifiez l’auteur lors de la protection en écriture du classeur.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Étape 6 : Sauvegarder le classeur Excel protégé

 Une fois la protection en écriture et l'auteur précisés, nous pouvons enregistrer le classeur Excel au format XLSX à l'aide du`Save()` méthode.

```csharp
// Enregistrez le classeur au format XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Exemple de code source pour Spécifier l’auteur lors de la protection en écriture du classeur Excel à l’aide d’Aspose.Cells pour .NET 
```csharp
//Répertoire source
string sourceDir = "YOUR SOURCE DIRECTORY";

//Répertoire de sortie
string outputDir = "YOUR OUTPUT DIRECTORY";

// Créez un classeur vide.
Workbook wb = new Workbook();

// Écrire un classeur protégé avec un mot de passe.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Spécifiez l’auteur lors de la protection en écriture du classeur.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Enregistrez le classeur au format XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Conclusion

Félicitation ! Vous avez maintenant appris à spécifier l'auteur lors de la protection en écriture d'un classeur Excel avec Aspose.Cells pour .NET. Vous pouvez appliquer ces étapes à vos propres projets pour protéger et personnaliser vos classeurs Excel.

N'hésitez pas à explorer davantage les fonctionnalités d'Aspose.Cells pour .NET pour des opérations plus avancées sur les fichiers Excel.

## FAQ

#### Q : Puis-je protéger en écriture un classeur Excel sans spécifier de mot de passe ?

 R : Oui, vous pouvez utiliser l'objet Workbook`WriteProtect()` sans spécifier de mot de passe pour protéger en écriture un classeur Excel. Cela limitera les modifications apportées au classeur sans nécessiter de mot de passe.

#### Q : Comment supprimer la protection en écriture d’un classeur Excel ?

 R : Pour supprimer la protection en écriture d'un classeur Excel, vous pouvez utiliser l'outil`Unprotect()` méthode de l'objet Worksheet ou du`RemoveWriteProtection()` méthode de l’objet Workbook, en fonction de votre cas d’utilisation spécifique. .

#### Q : J'ai oublié le mot de passe pour protéger mon classeur Excel. Que puis-je faire ?

R : Si vous avez oublié le mot de passe pour protéger votre classeur Excel, vous ne pouvez pas le supprimer directement. Cependant, vous pouvez essayer d'utiliser des outils tiers spécialisés offrant des fonctionnalités de récupération de mot de passe pour les fichiers Excel protégés.

#### Q : Est-il possible de spécifier plusieurs auteurs lors de la protection en écriture d'un classeur Excel ?

R : Non, la bibliothèque Aspose.Cells for .NET permet de spécifier un seul auteur lors de la protection en écriture d'un classeur Excel. Si vous souhaitez spécifier plusieurs auteurs, vous devrez envisager des solutions personnalisées en manipulant directement le fichier Excel.