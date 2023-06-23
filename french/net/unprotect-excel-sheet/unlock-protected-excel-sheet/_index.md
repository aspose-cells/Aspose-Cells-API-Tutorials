---
title: Déverrouiller la feuille Excel protégée
linktitle: Déverrouiller la feuille Excel protégée
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment déverrouiller une feuille de calcul Excel protégée à l'aide d'Aspose.Cells pour .NET. Tutoriel pas à pas en C#.
type: docs
weight: 20
url: /fr/net/unprotect-excel-sheet/unlock-protected-excel-sheet/
---
La protection d'une feuille de calcul Excel est souvent utilisée pour restreindre l'accès et la modification des données. Dans ce didacticiel, nous vous guiderons étape par étape pour comprendre et implémenter le code source C # fourni pour déverrouiller une feuille de calcul Excel protégée à l'aide de la bibliothèque Aspose.Cells pour .NET.

## Etape 1 : Préparation de l'environnement

Avant de commencer, assurez-vous que Aspose.Cells pour .NET est installé sur votre machine. Vous pouvez télécharger la bibliothèque depuis le site officiel d'Aspose et l'installer en suivant les instructions fournies.

Une fois l'installation terminée, créez un nouveau projet C# dans votre environnement de développement intégré (IDE) préféré et importez la bibliothèque Aspose.Cells pour .NET.

## Étape 2 : Configuration du chemin d'accès au répertoire de documents

 Dans le code source fourni, vous devez spécifier le chemin du répertoire où se trouve le fichier Excel que vous souhaitez déverrouiller. Modifier le`dataDir` variable en remplaçant "VOTRE RÉPERTOIRE DE DOCUMENTS" par le chemin absolu du répertoire sur votre machine.

```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Étape 3 : Création d'un objet de classeur

Pour commencer, nous devons créer un objet Workbook qui représente notre fichier Excel. Utilisez le constructeur de classe Workbook et spécifiez le chemin complet du fichier Excel à ouvrir.

```csharp
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Étape 4 : Accéder à la feuille de calcul

 Ensuite, nous devons accéder à la première feuille de calcul du fichier Excel. Utilisez le`Worksheets` propriété de l'objet Workbook pour accéder à la collection de feuilles de calcul, puis utilisez la`[0]` index pour accéder à la première feuille.

```csharp
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## Étape 5 : Déverrouiller la feuille de calcul

 Nous allons maintenant déverrouiller la feuille de calcul à l'aide de la`Unprotect()` méthode de l'objet Worksheet. Laissez la chaîne de mot de passe vide (`""`) si la feuille de calcul n'est pas protégée par un mot de passe.

```csharp
// Déprotéger la feuille de calcul avec un mot de passe
worksheet.Unprotect("");
```

## Étape 6 : Enregistrer le fichier Excel déverrouillé

Une fois la feuille de calcul déverrouillée, nous pouvons enregistrer le fichier Excel final. Utilisez le`Save()` méthode pour spécifier le chemin complet du fichier de sortie.

```csharp
// Enregistrer le classeur


workbook.Save(dataDir + "output.out.xls");
```

### Exemple de code source pour déverrouiller une feuille Excel protégée à l'aide d'Aspose.Cells pour .NET 
```csharp
try
{
    // Chemin d'accès au répertoire des documents.
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
catch(Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## Conclusion

Félicitation ! Vous avez maintenant compris comment utiliser Aspose.Cells pour .NET pour déverrouiller une feuille de calcul Excel protégée à l'aide du code source C#. En suivant les étapes de ce didacticiel, vous pouvez appliquer cette fonctionnalité à vos propres projets et travailler avec des fichiers Excel de manière efficace et sécurisée.

N'hésitez pas à explorer davantage les fonctionnalités offertes par Aspose.Cells pour des opérations plus avancées.

### FAQ

#### Q : Quelles précautions dois-je prendre lors du déverrouillage d'une feuille de calcul Excel protégée ?

R : Lorsque vous déverrouillez une feuille de calcul Excel protégée, assurez-vous que vous disposez des autorisations nécessaires pour accéder au fichier. Vérifiez également que vous utilisez la bonne méthode de déverrouillage et fournissez le mot de passe correct, le cas échéant.

#### Q : Comment savoir si la feuille de calcul est protégée par un mot de passe ?

 R : Vous pouvez vérifier si la feuille de calcul est protégée par un mot de passe en utilisant les propriétés ou les méthodes de la bibliothèque Aspose.Cells pour .NET. Par exemple, vous pouvez utiliser le`IsProtected()` de l'objet Worksheet pour vérifier l'état de protection de la feuille.

#### Q : Je reçois une exception lorsque j'essaie de déverrouiller la feuille de calcul. Que dois-je faire ?

R : Si vous rencontrez une exception lors du déverrouillage de la feuille de calcul, assurez-vous d'avoir correctement spécifié le chemin d'accès au fichier Excel et vérifiez que vous disposez des autorisations nécessaires pour accéder au fichier. Si le problème persiste, n'hésitez pas à contacter le support Aspose.Cells pour obtenir de l'aide.