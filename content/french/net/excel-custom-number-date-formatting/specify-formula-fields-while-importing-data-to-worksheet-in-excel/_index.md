---
title: Spécifier les champs de formule lors de l'importation de données dans une feuille Excel
linktitle: Spécifier les champs de formule lors de l'importation de données dans une feuille Excel
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment importer des données dans des feuilles Excel avec des champs de formule spécifiés à l'aide d'Aspose.Cells pour .NET dans ce didacticiel détaillé.
type: docs
weight: 11
url: /fr/net/excel-custom-number-date-formatting/specify-formula-fields-while-importing-data-to-worksheet-in-excel/
---
## Introduction

Aspose.Cells for .NET est un outil précieux pour la gestion de fichiers Excel par programmation. Il offre des fonctionnalités robustes pour créer, modifier et manipuler facilement des feuilles de calcul Excel. L'une des fonctionnalités intéressantes qu'il offre est la possibilité de spécifier des champs de formule lors de l'importation de données dans une feuille Excel. Imaginez que vous travaillez sur un rapport financier et que vous devez calculer automatiquement les totaux en fonction des entrées de l'utilisateur. Ce didacticiel vous guidera étape par étape pour y parvenir avec une approche claire et simple.

## Prérequis

Avant de plonger dans le code, assurons-nous que vous disposez de tout ce dont vous avez besoin. 

1. Visual Studio ou tout autre environnement de développement intégré .NET (IDE) : assurez-vous de disposer d'un IDE approprié pour écrire et exécuter votre code C#.
2. Aspose.Cells pour .NET : vous devrez télécharger et référencer la bibliothèque Aspose.Cells dans votre projet. Vous pouvez la télécharger à partir du[Sorties d'Aspose](https://releases.aspose.com/cells/net/).
3. Connaissances de base de C# : une connaissance de C# et des concepts de programmation orientée objet vous aidera à mieux comprendre les exemples.
4. .NET Framework : ce didacticiel suppose que vous utilisez .NET Framework 4.5 ou une version ultérieure.

Une fois les conditions préalables réglées, procédons à l'importation de certaines données dans une feuille Excel avec des champs de formule spécifiés.

## Paquets d'importation

Avant de commencer à écrire votre code, vous devez importer l'espace de noms Aspose.Cells nécessaire. Cette opération s'effectue généralement en haut de votre fichier C# :

```csharp
using Aspose.Cells;
using System;
using System.Collections.Generic;
```

Cela vous permet d'utiliser les classes et méthodes fournies par la bibliothèque Aspose.Cells sans avoir besoin de les préfixer avec l'espace de noms à chaque fois.

Décomposons l’ensemble du processus en étapes gérables :

## Étape 1 : définir le répertoire de sortie

Tout d'abord, vous devez déterminer l'emplacement où vous souhaitez enregistrer votre fichier Excel. Voici comment procéder :

```csharp
static string outputDir = "Your Document Directory"; // spécifiez ici votre répertoire de documents
```

 Remplacer`"Your Document Directory"` avec votre chemin de fichier actuel. C'est ici que le fichier Excel généré sera enregistré.

## Étape 2 : créer une classe définie par l'utilisateur pour les éléments de données

Ensuite, nous allons définir une classe pour structurer les données que nous prévoyons d’importer.

```csharp
class DataItems
{
    public int Number1 { get; set; }
    public int Number2 { get; set; }
    public string Formula1 { get; set; }
    public string Formula2 { get; set; }
}
```

 Ce`DataItems` la classe contiendra les entiers bruts et les formules que nous écrirons dans la feuille Excel. 

## Étape 3 : Initialiser une liste pour contenir des éléments de données

 Nous utiliserons une liste pour contenir plusieurs instances de notre`DataItems` classe.

```csharp
List<DataItems> dis = new List<DataItems>();
```

## Étape 4 : Ajouter des éléments de données à la liste

Ajoutons maintenant quelques entrées à notre liste. Chaque entrée contiendra deux nombres et deux formules.

```csharp
// Définir et ajouter chaque élément de données
DataItems di = new DataItems();
di.Number1 = 2002;
di.Number2 = 3502;
di.Formula1 = "=SUM(A2,B2)";
di.Formula2 = "=HYPERLINK(\"https://www.aspose.com\",\"Site Web Aspose\")";
dis.Add(di);

// Répétez l'opération pour des éléments de données supplémentaires
```

 Assurez-vous de personnaliser chaque`DataItems` instance avec des valeurs et des formules uniques.

## Étape 5 : Créer un classeur et accéder à une feuille de calcul

Ensuite, créez le classeur et accédez à la première feuille de calcul dans laquelle nous importerons éventuellement les données.

```csharp
Workbook wb = new Workbook(); // créer un nouveau classeur
Worksheet ws = wb.Worksheets[0]; // accéder à la première feuille de calcul
```

## Étape 6 : Spécifier les options de la table d’importation

C'est ici que la magie opère. Vous devez spécifier quels champs de vos données correspondent aux formules. 

```csharp
ImportTableOptions opts = new ImportTableOptions();
opts.IsFormulas = new bool[] { false, false, true, true };
```

 Dans cet exemple, les deux derniers champs contiennent des formules, ce qui est indiqué par`true` , tandis que les deux premiers champs sont définis sur`false`.

## Étape 7 : Importer des objets personnalisés

Maintenant que tout est configuré, importons notre liste d’éléments de données dans la feuille de calcul.

```csharp
ws.Cells.ImportCustomObjects(dis, 0, 0, opts);
```

Cette ligne importe efficacement les données à partir de la cellule A1.

## Étape 8 : Calculer les formules

Puisque nous avons importé certaines formules, il est essentiel de les calculer.

```csharp
wb.CalculateFormula();
```

Cette méthode garantit que vos formules sont évaluées en fonction de leurs dépendances.

## Étape 9 : Ajuster automatiquement les colonnes

Pour vous assurer que vos données sont faciles à afficher, vous pouvez ajuster automatiquement les colonnes en fonction du contenu.

```csharp
ws.AutoFitColumns();
```

Cette étape optimise la mise en page du fichier Excel. 

## Étape 10 : Enregistrez votre fichier Excel

Enfin, il est temps d’enregistrer votre fichier Excel nouvellement créé. 

```csharp
wb.Save(outputDir + "outputSpecifyFormulaFieldsWhileImportingDataToWorksheet.xlsx");
```

Assurez-vous que le nom de votre fichier de sortie est pertinent et descriptif !

## Étape 11 : Vérification de l'exécution

Comme moyen simple de confirmer que tout s'est déroulé correctement, vous pouvez imprimer un message.

```csharp
Console.WriteLine("SpecifyFormulaFieldsWhileImportingDataToWorksheet executed successfully.");
```

Cela vous donne un retour immédiat indiquant que le code a fonctionné sans aucun problème.

## Conclusion

Et voilà ! Vous avez importé avec succès des données dans une feuille Excel à l'aide d'Aspose.Cells pour .NET et des champs de formule spécifiés. En suivant ces étapes, vous pouvez appliquer des techniques similaires pour automatiser les tâches de traitement des données adaptées à vos besoins. Que vous traitiez des chiffres pour des rapports ou que vous conserviez simplement des données, maîtriser l'art de la manipulation d'Excel avec Aspose est une compétence qui vaut la peine d'être acquise.

## FAQ

### Qu'est-ce qu'Aspose.Cells ?
Aspose.Cells est une bibliothèque .NET conçue pour créer, manipuler et convertir des fichiers Excel par programmation.

### Comment installer Aspose.Cells pour .NET ?
 Vous pouvez le télécharger à partir du[Sorties d'Aspose](https://releases.aspose.com/cells/net/)et référencez-le dans votre projet.

### Puis-je utiliser Aspose.Cells gratuitement ?
 Oui, Aspose propose un essai gratuit disponible sur[ce lien](https://releases.aspose.com/).

### Où puis-je trouver plus d’exemples ?
 Des exemples et de la documentation supplémentaires peuvent être trouvés sur le site[Page de documentation d'Aspose](https://reference.aspose.com/cells/net/).

### Que faire si je rencontre des problèmes lors de l’utilisation d’Aspose ?
 Vous pouvez demander de l'aide sur le forum d'assistance Aspose[ici](https://forum.aspose.com/c/cells/9).
 