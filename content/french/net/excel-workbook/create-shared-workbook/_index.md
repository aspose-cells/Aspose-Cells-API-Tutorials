---
title: Créer un classeur partagé
linktitle: Créer un classeur partagé
second_title: Référence de l'API Aspose.Cells pour .NET
description: Créez un classeur Excel partagé avec Aspose.Cells pour .NET pour permettre une collaboration simultanée sur les données.
type: docs
weight: 70
url: /fr/net/excel-workbook/create-shared-workbook/
---
Dans ce didacticiel, nous vous présenterons le code source C# fourni qui vous permettra de créer un classeur partagé à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour effectuer cette opération.

## Étape 1 : Définir le répertoire de sortie

```csharp
// Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
```

Dans cette première étape, nous définissons le répertoire de sortie dans lequel le classeur partagé sera enregistré.

## Étape 2 : créer un objet classeur

```csharp
// Créer un objet Workbook
Workbook wb = new Workbook();
```

Nous créons un nouvel objet Workbook qui représentera notre classeur Excel.

## Étape 3 : Activer le partage de classeurs

```csharp
// Partager le classeur
wb.Settings.Shared = true;
```

 Nous activons la fonctionnalité de partage du classeur en définissant le`Shared` propriété de l'objet Workbook à`true`.

## Étape 4 : Enregistrez le classeur partagé

```csharp
// Enregistrer le classeur partagé
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Nous enregistrons le classeur partagé en spécifiant le chemin et le nom du fichier de sortie.

### Exemple de code source pour créer un classeur partagé à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
//Créer un objet classeur
Workbook wb = new Workbook();
//Partager le classeur
wb.Settings.Shared = true;
//Enregistrer le classeur partagé
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Conclusion

Félicitation ! Vous avez appris à créer un classeur partagé à l'aide d'Aspose.Cells pour .NET. Le classeur partagé peut être utilisé par plusieurs utilisateurs simultanément pour collaborer sur les données. Expérimentez avec vos propres données et explorez davantage les fonctionnalités d'Aspose.Cells pour créer des classeurs Excel puissants et personnalisés.

### FAQ

#### Q : Qu'est-ce qu'un classeur partagé ?

R : Un classeur partagé est un classeur Excel qui peut être utilisé simultanément par plusieurs utilisateurs pour collaborer sur des données. Chaque utilisateur peut apporter des modifications au classeur et les autres utilisateurs verront les mises à jour en temps réel.

#### Q : Comment activer le partage d'un classeur dans Aspose.Cells pour .NET ?

 R : Pour activer le partage d'un classeur dans Aspose.Cells pour .NET, vous devez définir le`Shared` propriété de l'objet Workbook à`true`. Cela permettra aux utilisateurs de travailler simultanément sur le classeur.

#### Q : Puis-je restreindre les autorisations des utilisateurs dans un classeur partagé ?

: Oui, vous pouvez restreindre les autorisations des utilisateurs dans un classeur partagé à l'aide des fonctionnalités de sécurité d'Excel. Vous pouvez définir des autorisations spécifiques pour chaque utilisateur, telles que la possibilité de modifier, de lire seule, etc.

#### Q : Comment puis-je partager le classeur avec d’autres utilisateurs ?

R : Une fois que vous avez créé le classeur partagé, vous pouvez le partager avec d'autres utilisateurs en leur envoyant le fichier Excel. D'autres utilisateurs pourront ouvrir le fichier et travailler dessus simultanément.

#### Q : Toutes les fonctionnalités d'Excel sont-elles prises en charge dans un classeur partagé ?

R : La plupart des fonctionnalités d'Excel sont prises en charge dans un classeur partagé. Toutefois, certaines fonctionnalités avancées, telles que les macros et les compléments, peuvent présenter des limitations ou des restrictions lorsqu'elles sont utilisées dans un classeur partagé.