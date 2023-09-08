---
title: Déverrouiller une feuille de calcul Excel protégée par mot de passe
linktitle: Déverrouiller une feuille de calcul Excel protégée par mot de passe
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment déverrouiller une feuille de calcul Excel protégée par mot de passe à l'aide d'Aspose.Cells pour .NET. Tutoriel étape par étape en C#.
type: docs
weight: 10
url: /fr/net/unprotect-excel-sheet/unlock-password-protected-excel-worksheet/
---
La protection par mot de passe d'une feuille de calcul Excel est couramment utilisée pour sécuriser les données sensibles. Dans ce didacticiel, nous vous guiderons étape par étape pour comprendre et implémenter le code source C# fourni pour déverrouiller une feuille de calcul Excel protégée par mot de passe à l'aide de la bibliothèque Aspose.Cells pour .NET.

## Étape 1 : Préparer l’environnement

Avant de commencer, assurez-vous que Aspose.Cells for .NET est installé sur votre ordinateur. Vous pouvez télécharger la bibliothèque depuis le site officiel d'Aspose et l'installer en suivant les instructions fournies.

Une fois l'installation terminée, créez un nouveau projet C# dans votre environnement de développement intégré (IDE) préféré et importez la bibliothèque Aspose.Cells pour .NET.

## Étape 2 : Configuration du chemin du répertoire du document

 Dans le code source fourni, vous devez spécifier le chemin du répertoire où se trouve le fichier Excel que vous souhaitez déverrouiller. Modifier le`dataDir` variable en remplaçant « VOTRE RÉPERTOIRE DE DOCUMENTS » par le chemin absolu du répertoire sur votre machine.

```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Étape 3 : Création d'un objet classeur

Pour commencer, nous devons créer un objet Workbook qui représente notre fichier Excel. Utilisez le constructeur de classe Workbook et spécifiez le chemin complet du fichier Excel à ouvrir.

```csharp
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Étape 4 : Accéder à la feuille de calcul

 Ensuite, nous devons accéder à la première feuille de calcul du fichier Excel. Utilisez le`Worksheets` propriété de l'objet Workbook pour accéder à la collection de feuilles de calcul, puis utilisez le`[0]` index pour accéder à la première feuille.

```csharp
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## Étape 5 : Déverrouiller la feuille de calcul

 Nous allons maintenant déverrouiller la feuille de calcul en utilisant le`Unprotect()` méthode de l’objet Worksheet. Laissez la chaîne du mot de passe vide (`""`) si la feuille de calcul n'est pas protégée par mot de passe.

```csharp
// Déprotéger la feuille de calcul avec un mot de passe
worksheet.Unprotect("");
```

## Étape 6 : Sauvegarde du fichier Excel déverrouillé

Une fois la feuille de calcul déverrouillée, nous pouvons enregistrer le fichier Excel final. Utilisez le`Save()` méthode pour spécifier le chemin complet du fichier de sortie

.

```csharp
// Enregistrer le classeur
workbook.Save(dataDir + "output.out.xls");
```

### Exemple de code source pour déverrouiller une feuille de calcul Excel protégée par mot de passe à l'aide d'Aspose.Cells pour .NET 
```csharp
try
{
    //Le chemin d'accès au répertoire des documents.
    string dataDir = "YOUR DOCUMENT DIRECTORY";
    // Instanciation d'un objet Workbook
    Workbook workbook = new Workbook(dataDir + "book1.xls");
    // Accéder à la première feuille de calcul du fichier Excel
    Worksheet worksheet = workbook.Worksheets[0];
    // Déprotéger la feuille de calcul avec un mot de passe
    worksheet.Unprotect("");
    // Enregistrer le classeur
    workbook.Save(dataDir + "output.out.xls");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## Conclusion

Félicitation ! Vous avez maintenant compris comment utiliser Aspose.Cells pour .NET pour déverrouiller une feuille de calcul Excel protégée par mot de passe à l'aide du code source C#. En suivant les étapes de ce didacticiel, vous pouvez appliquer cette fonctionnalité à vos propres projets et travailler avec des fichiers Excel de manière efficace et sécurisée.

N'hésitez pas à explorer davantage les fonctionnalités offertes par Aspose.Cells pour des opérations plus avancées.

### FAQ

#### Q : Que se passe-t-il si la feuille de calcul est protégée par mot de passe ?

 R : Si la feuille de calcul est protégée par mot de passe, vous devez fournir le mot de passe approprié dans le champ`Unprotect()` méthode pour pouvoir le déverrouiller.

#### Q : Existe-t-il des restrictions ou des précautions lors du déverrouillage d'une feuille de calcul Excel protégée ?

R : Oui, assurez-vous de disposer des autorisations nécessaires pour déverrouiller la feuille de calcul. Assurez-vous également de suivre les politiques de sécurité de votre organisation lorsque vous utilisez cette fonctionnalité.