---
title: Protéger ou déprotéger le classeur partagé par mot de passe
linktitle: Protéger ou déprotéger le classeur partagé par mot de passe
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment protéger ou déprotéger par mot de passe un classeur partagé à l’aide d’Aspose.Cells pour .NET.
type: docs
weight: 120
url: /fr/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Protéger un classeur partagé avec un mot de passe est important pour garantir la confidentialité des données. Avec Aspose.Cells pour .NET, vous pouvez facilement protéger ou déprotéger un classeur partagé à l'aide de mots de passe. Suivez les étapes ci-dessous pour obtenir les résultats souhaités :

## Étape 1 : Spécifiez le répertoire de sortie

Tout d'abord, vous devez spécifier le répertoire de sortie dans lequel le fichier Excel protégé sera enregistré. Voici comment procéder à l'aide d'Aspose.Cells :

```csharp
// Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
```

## Étape 2 : Créez un fichier Excel vide

Vous pouvez ensuite créer un fichier Excel vide sur lequel vous souhaitez appliquer une protection ou une déprotection. Voici un exemple de code :

```csharp
// Créer un classeur Excel vide
Workbook wb = new Workbook();
```

## Étape 3 : Protéger ou déprotéger le classeur partagé

Après avoir créé le classeur, vous pouvez protéger ou déprotéger le classeur partagé en spécifiant le mot de passe approprié. Voici comment:

```csharp
// Protéger le classeur partagé avec un mot de passe
wb.ProtectSharedWorkbook("1234");

// Décommentez cette ligne pour déprotéger le classeur partagé
// wb.UnprotectSharedWorkbook("1234");
```

## Étape 4 : Enregistrez le fichier Excel de sortie

Une fois que vous avez appliqué ou non la protection, vous pouvez enregistrer le fichier Excel protégé dans le répertoire de sortie spécifié. Voici comment procéder :

```csharp
// Enregistrez le fichier Excel de sortie
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Exemple de code source pour la protection par mot de passe ou la déprotection du classeur partagé à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
//Créer un fichier Excel vide
Workbook wb = new Workbook();
//Protéger le classeur partagé avec un mot de passe
wb.ProtectSharedWorkbook("1234");
//Décommentez cette ligne pour déprotéger le classeur partagé
//wb.UnprotectSharedWorkbook("1234");
//Enregistrez le fichier Excel de sortie
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusion

Protéger ou déprotéger un classeur partagé avec un mot de passe est essentiel pour garantir la sécurité des données. Avec Aspose.Cells pour .NET, vous pouvez facilement ajouter cette fonctionnalité à vos fichiers Excel. En suivant les étapes de ce guide, vous pouvez protéger ou déprotéger efficacement vos classeurs partagés à l'aide de mots de passe. Expérimentez avec vos propres fichiers Excel et assurez-vous de maintenir la sécurité de vos données sensibles.

### FAQ

#### Q : Quels types de protection puis-je appliquer à un classeur partagé avec Aspose.Cells ?
    
R : Avec Aspose.Cells, vous pouvez protéger un classeur partagé en spécifiant un mot de passe pour empêcher tout accès non autorisé, modification ou suppression de données.

#### Q : Puis-je protéger un classeur partagé sans spécifier de mot de passe ?
    
R : Oui, vous pouvez protéger un classeur partagé sans spécifier de mot de passe. Il est toutefois recommandé d’utiliser un mot de passe fort pour une meilleure sécurité.

#### Q : Comment puis-je déprotéger un classeur partagé avec Aspose.Cells ?
    
R : Pour déprotéger un classeur partagé, vous devez spécifier le même mot de passe que celui utilisé lors de la protection du classeur. Cela permet de supprimer la protection et d’accéder librement aux données.

#### Q : La protection d'un classeur partagé affecte-t-elle les fonctionnalités et les formules du classeur ?
    
R : Lorsque vous protégez un classeur partagé, les utilisateurs peuvent toujours accéder aux fonctionnalités et aux formules présentes dans le classeur. La protection affecte uniquement les modifications structurelles apportées au classeur.