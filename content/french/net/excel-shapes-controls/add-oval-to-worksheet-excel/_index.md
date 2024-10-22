---
title: Ajouter un ovale à une feuille de calcul dans Excel
linktitle: Ajouter un ovale à une feuille de calcul dans Excel
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment ajouter un ovale à une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Guide étape par étape avec explications de code détaillées.
type: docs
weight: 17
url: /fr/net/excel-shapes-controls/add-oval-to-worksheet-excel/
---
## Introduction
Créer des fichiers Excel époustouflants et interactifs peut impliquer bien plus que de simples chiffres et formules. Des formes telles que des ovales peuvent ajouter un attrait visuel ou fournir des éléments fonctionnels dans vos feuilles de calcul. Dans ce didacticiel, nous découvrirons comment utiliser Aspose.Cells pour .NET pour ajouter des ovales à une feuille de calcul Excel par programmation. Que vous cherchiez à ajouter du style ou des fonctionnalités, nous vous proposons un guide étape par étape qui explique tout.
## Prérequis
Avant de plonger dans le code, vous devez mettre en place quelques éléments :
1.  Bibliothèque Aspose.Cells pour .NET : vous pouvez la télécharger à partir de[ici](https://releases.aspose.com/cells/net/) ou installez-le à l’aide de NuGet dans Visual Studio.
2. Environnement de développement : AC# IDE comme Visual Studio.
3. Compréhension de base de C# : vous devez être familiarisé avec les concepts de codage de base en C#.
 N'oubliez pas non plus de configurer votre projet en installant la bibliothèque Aspose.Cells pour .NET. Si vous n'avez pas encore de licence, vous pouvez en demander une[permis temporaire](https://purchase.aspose.com/temporary-license/) ou utilisez le[essai gratuit](https://releases.aspose.com/) version.
## Paquets d'importation
Avant d'écrire du code, assurez-vous d'avoir inclus les espaces de noms requis. Voici l'extrait de code C# pour vous assurer que vous utilisez les bonnes bibliothèques :
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
## Étape 1 : Configurez votre répertoire
La première étape pour ajouter un ovale à une feuille Excel consiste à spécifier où votre fichier Excel sera enregistré. Définissons le chemin du répertoire et assurons-nous que le répertoire existe avant d'enregistrer notre travail.

Nous allons créer un chemin de répertoire et vérifier s'il existe. Si le dossier n'existe pas, il sera créé.
```csharp
// Le chemin vers le répertoire des documents.
string dataDir = "Your Document Directory";
//Créez un répertoire s'il n'est pas déjà présent.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
Cette étape est cruciale car elle garantit que votre fichier est enregistré dans un emplacement approprié et que vous ne rencontrerez pas de problèmes de chemin de fichier plus tard.
## Étape 2 : Initialiser un nouveau classeur
Ensuite, nous devons créer un nouveau classeur dans lequel nous ajouterons nos formes ovales. Le classeur représente un fichier Excel et nous pouvons y ajouter du contenu ou des formes.

 Dans cette étape, nous instancions un nouveau`Workbook` objet qui servira de conteneur à notre fichier Excel.
```csharp
// Instancier un nouveau classeur.
Workbook excelbook = new Workbook();
```
## Étape 3 : Ajoutez la première forme ovale
Vient maintenant la partie amusante : ajouter une forme ovale à la feuille de calcul. Cet ovale peut représenter un élément visuel comme un bouton ou un élément en surbrillance. Nous commencerons par ajouter la première forme ovale à la première feuille de calcul de notre classeur.

 Ici, nous utilisons le`Shapes.AddOval()` méthode pour créer un ovale sur la feuille de calcul sur une ligne et une colonne spécifiques.
```csharp
// Ajoutez une forme ovale.
Aspose.Cells.Drawing.Oval oval1 = excelbook.Worksheets[0].Shapes.AddOval(2, 0, 2, 0, 130, 160);
```
 Les paramètres à l'intérieur`AddOval()` sont les suivantes :
- Les deux premiers chiffres représentent la ligne et la colonne du coin supérieur gauche de l’ovale.
- Les deux chiffres suivants représentent la hauteur et la largeur de l'ovale.
## Étape 4 : Définir l'emplacement et le style de l'ovale
 Une fois l'ovale créé, nous pouvons définir sa position, son épaisseur de ligne et son style de tiret.`Placement` La propriété détermine le comportement de l'ovale lorsque vous redimensionnez ou déplacez des cellules dans la feuille de calcul.

Nous rendons l'ovale flottant librement et ajustons son apparence.
```csharp
// Définissez l'emplacement de l'ovale.
oval1.Placement = PlacementType.FreeFloating;
// Définissez l'épaisseur de la ligne.
oval1.Line.Weight = 1;
// Définissez le style de tiret de l'ovale.
oval1.Line.DashStyle = MsoLineDashStyle.Solid;
```
Cela permet à l'ovale de se déplacer librement dans la feuille de calcul, et son épaisseur de ligne et son style sont définis pour une cohérence visuelle.
## Étape 5 : Ajoutez une autre forme ovale (cercle)
Pourquoi s'arrêter à une seule ? Dans cette étape, nous allons ajouter une autre forme ovale, en créant cette fois un cercle parfait en faisant en sorte que la hauteur et la largeur soient identiques.

Nous créons un autre ovale, le plaçons à un endroit différent et nous assurons qu'il a une forme circulaire en définissant une hauteur et une largeur égales.
```csharp
// Ajoutez une autre forme ovale (cercle).
Aspose.Cells.Drawing.Oval oval2 = excelbook.Worksheets[0].Shapes.AddOval(9, 0, 2, 15, 130, 130);
```
## Étape 6 : Styliser le deuxième ovale
Tout comme précédemment, nous ajusterons le placement, le poids et le style du tiret de ce deuxième ovale (ou cercle).

Nous appliquons des propriétés similaires au deuxième ovale pour correspondre au style du premier.
```csharp
// Définissez l'emplacement de l'ovale.
oval2.Placement = PlacementType.FreeFloating;
// Définissez l'épaisseur de la ligne.
oval2.Line.Weight = 1;
// Définissez le style de tiret de l'ovale.
oval2.Line.DashStyle = MsoLineDashStyle.Solid;
```
## Étape 7 : Enregistrer le classeur
Enfin, nous devons enregistrer le classeur avec les ovales que nous venons d'ajouter. L'enregistrement du fichier garantit que toutes nos modifications sont enregistrées.

Nous enregistrons le classeur dans le chemin de répertoire que nous avons défini précédemment.
```csharp
// Enregistrez le fichier Excel.
excelbook.Save(dataDir + "book1.out.xls");
```
Et voilà ! Vous avez ajouté avec succès des ovales à votre feuille de calcul Excel et enregistré le fichier.
## Conclusion
L'ajout de formes telles que des ovales à une feuille Excel à l'aide d'Aspose.Cells pour .NET est non seulement simple, mais constitue également une manière amusante d'améliorer vos feuilles de calcul avec des éléments visuels supplémentaires. Que ce soit à des fins de conception ou pour ajouter des éléments cliquables, les formes peuvent jouer un rôle important dans l'apparence et le fonctionnement de vos fichiers Excel. Ainsi, la prochaine fois que vous travaillerez sur un projet qui nécessite des feuilles Excel interactives ou visuellement attrayantes, vous saurez exactement comment ajouter ces ovales parfaits !
## FAQ
### Puis-je ajouter d’autres formes comme des rectangles ou des lignes à l’aide d’Aspose.Cells pour .NET ?
 Oui, vous pouvez ajouter diverses formes comme des rectangles, des lignes et des flèches à l'aide de la`Shapes` collection dans Aspose.Cells.
### Est-il possible de redimensionner les ovales après les avoir ajoutés ?
Absolument ! Vous pouvez modifier les propriétés de hauteur et de largeur des ovales après les avoir ajoutés.
### Dans quels formats de fichiers puis-je enregistrer le classeur en plus de XLS ?
Aspose.Cells prend en charge plusieurs formats tels que XLSX, CSV et PDF, entre autres.
### Puis-je modifier la couleur du contour de l'ovale ?
 Oui, vous pouvez modifier la couleur de la ligne de l'ovale à l'aide du`Line.Color` propriété.
### Est-il nécessaire d'avoir une licence pour Aspose.Cells ?
 Bien que vous puissiez essayer Aspose.Cells avec un essai gratuit, vous aurez besoin d'un[licence](https://purchase.aspose.com/buy) pour une utilisation à long terme ou pour accéder à des fonctionnalités avancées.