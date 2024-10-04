---
title: Appliquer le format 3D au graphique
linktitle: Appliquer le format 3D au graphique
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment créer de superbes graphiques 3D dans Excel à l'aide d'Aspose.Cells pour .NET. Suivez notre guide simple étape par étape.
type: docs
weight: 10
url: /fr/net/advanced-chart-operations/apply-3d-format-to-chart/
---
## Introduction

À une époque où la visualisation des données est primordiale, la façon dont nous présentons nos données va au-delà des graphiques et diagrammes de base. Avec des outils comme Aspose.Cells pour .NET, vous pouvez améliorer vos présentations de données avec de superbes graphiques 3D qui non seulement attirent l'attention, mais transmettent également des informations de manière efficace. Ce guide vous guidera à travers les étapes à suivre pour appliquer un format 3D à un graphique à l'aide d'Aspose.Cells, transformant vos données brutes en un affichage attrayant.

## Prérequis

Avant de plonger dans le vif du sujet de l'application d'un format 3D à un graphique, assurons-nous que vous disposez de tout ce dont vous avez besoin.

### Configuration logicielle requise

- Visual Studio : assurez-vous que Visual Studio est installé pour fonctionner avec les applications .NET.
-  Aspose.Cells pour .NET : si vous ne l'avez pas encore fait, téléchargez et installez Aspose.Cells depuis[ici](https://releases.aspose.com/cells/net/).

### Configuration de l'environnement de codage

1. Créez un nouveau projet .NET : ouvrez Visual Studio, sélectionnez « Créer un nouveau projet » et choisissez une application console.
2. Ajouter Aspose.Cells Référence : via le gestionnaire de packages NuGet, ajoutez Aspose.Cells en le recherchant ou via la console du gestionnaire de packages :

```bash
Install-Package Aspose.Cells
```

3. Configurer le répertoire de sortie : désignez un répertoire de sortie dans lequel vos fichiers générés seront enregistrés. Cela peut être aussi simple que de créer un dossier sur votre bureau.

Maintenant que vous êtes prêt, il est temps de passer au code et de créer des graphiques 3D éblouissants !

## Paquets d'importation

Pour commencer, vous devez importer les espaces de noms nécessaires. Cela vous aidera à accéder aux classes et méthodes fournies par Aspose.Cells. Voici comment procéder :

```csharp
using System;
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
using Aspose.Cells.Charts;
```

Cette section décomposera le processus en étapes gérables, vous offrant une compréhension claire de chaque étape.

## Étape 1 : Initialisez votre classeur

 Tout d’abord, vous devez créer une instance de`Workbook` classe. Cet objet servira de base à votre document Excel.

```csharp
//Répertoire de sortie
string outputDir = "Your Document Directory";
Workbook book = new Workbook();
```
 Pensez à cela`Workbook` comme une toile vierge, prête à être remplie de données colorées et de visualisations percutantes.

## Étape 2 : renommer la première feuille de calcul

Ensuite, renommons la première feuille de calcul. Cela permet de clarifier les données avec lesquelles nous travaillons.

```csharp
book.Worksheets[0].Name = "DataSheet";
```

Les noms doivent être intuitifs. Dans ce cas, nous l'appelons « DataSheet » afin de savoir où se trouvent nos données.

## Étape 3 : Créer des données pour le graphique

Nous allons maintenant ajouter quelques données à notre « feuille de données ». Complétons-la avec les valeurs que notre graphique utilisera.

```csharp
Worksheet dataSheet = book.Worksheets["DataSheet"];
dataSheet.Cells["B1"].PutValue(1);
dataSheet.Cells["B2"].PutValue(2);
dataSheet.Cells["B3"].PutValue(3);
dataSheet.Cells["A1"].PutValue("A");
dataSheet.Cells["A2"].PutValue("B");
dataSheet.Cells["A3"].PutValue("C");
```

Tout comme une recette dépend des ingrédients, l'efficacité de votre graphique dépend de la qualité et de l'organisation de vos données d'entrée.

## Étape 4 : Configurer une nouvelle feuille de calcul graphique

Il est temps de créer une nouvelle feuille de calcul pour le graphique lui-même. Cela permet d'organiser la visualisation de vos données.

```csharp
Worksheet sheet = book.Worksheets.Add("MyChart");
```

Considérez cette feuille de travail comme votre étape, celle où se déroulent les performances de vos données.

## Étape 5 : Ajouter un graphique

Ici, nous allons ajouter un graphique à colonnes à la feuille de calcul nouvellement créée.  

```csharp
ChartCollection charts = sheet.Charts;
int chartSheetIdx = charts.Add(ChartType.Column, 5, 0, 25, 15);
```

Nous définissons un espace pour notre graphique et précisons son type. Considérez cela comme la sélection du type de cadre pour votre œuvre d'art.

## Étape 6 : Personnaliser l’apparence du graphique

Maintenant, personnalisons l'apparence de notre graphique en définissant des couleurs d'arrière-plan. 

```csharp
Aspose.Cells.Charts.Chart chart = book.Worksheets["MyChart"].Charts[0];
chart.PlotArea.Area.BackgroundColor = Color.White;
chart.ChartArea.Area.BackgroundColor = Color.White;
chart.PlotArea.Area.ForegroundColor = Color.White;
chart.ChartArea.Area.ForegroundColor = Color.White;
chart.ShowLegend = false;
```

Un arrière-plan blanc propre fait souvent ressortir les couleurs de vos données, améliorant ainsi leur visibilité.

## Étape 7 : Ajouter une série de données au graphique

Il est temps d'alimenter notre graphique avec les données. Nous allons ajouter une série de données de notre « feuille de données » pour garantir que notre graphique reflète les données dont nous avons besoin.

```csharp
chart.NSeries.Add("DataSheet!B1:B3", true);
chart.NSeries.CategoryData = "DataSheet!A1:A3";
```

C'est un peu comme si un chef préparait un plat avec des ingrédients spécifiques. Chaque donnée compte !

## Étape 8 : Accéder et formater la série de données

Maintenant que nos données sont liées, récupérons la série de données et commençons à appliquer des effets 3D.

```csharp
Aspose.Cells.Charts.Series ser = chart.NSeries[0];
ShapePropertyCollection spPr = ser.ShapeProperties;
Format3D fmt3d = spPr.Format3D;
```

Nous nous préparons à ajouter une touche d'originalité à notre plat : considérez-le comme un assaisonnement qui rehausse la saveur générale.

## Étape 9 : appliquer des effets de biseau 3D

Ensuite, nous allons ajouter un effet de biseau pour donner une certaine dimension à notre graphique.

```csharp
Bevel bevel = fmt3d.TopBevel;
bevel.Type = BevelPresetType.Circle;
bevel.Height = 2;
bevel.Width = 5;
```

Tout comme un sculpteur façonne la pierre, nous créons une profondeur qui donne vie à notre thème !

## Étape 10 : Personnaliser le matériau de surface et l'éclairage

Faisons briller notre carte ! Nous allons ajuster le matériau de surface et les paramètres d'éclairage.

```csharp
fmt3d.SurfaceMaterialType = PresetMaterialType.WarmMatte;
fmt3d.SurfaceLightingType = LightRigType.ThreePoint;
fmt3d.LightingAngle = 20;
```

Un éclairage et des matériaux appropriés peuvent transformer un objet plat en un visuel captivant. Pensez à un plateau de tournage éclairé de manière experte pour mettre en valeur chaque scène.

## Étape 11 : Touches finales sur l'apparence de la série

Il convient maintenant de finaliser l’apparence de notre série de données en ajustant sa couleur.

```csharp
ser.Area.BackgroundColor = Color.Maroon;
ser.Area.ForegroundColor = Color.Maroon;
ser.Border.Color = Color.Maroon;
```

La bonne couleur peut évoquer certains sentiments et réactions : le marron ajoute une touche d’élégance et de sophistication.

## Étape 12 : Enregistrez votre classeur

Enfin, il est temps de sauvegarder votre chef-d'œuvre ! N'oubliez pas de préciser la destination où vous souhaitez le stocker.

```csharp
book.Save(outputDir + "outputApplying3DFormat.xlsx");
Console.WriteLine("Applying3DFormat executed successfully.");
```

Sauvegarder votre travail, c'est comme mettre votre art dans une galerie ; c'est un moment à chérir et à partager.

## Conclusion

Félicitations ! Vous avez réussi à créer un graphique 3D visuellement attrayant à l'aide d'Aspose.Cells pour .NET. En suivant ces étapes, vous disposez désormais d'un outil puissant pour améliorer vos présentations de données, en les rendant non seulement informatives, mais également visuellement captivantes. Lorsque vous peaufinez vos graphiques, n'oubliez pas que chaque visualisation est une histoire : rendez-la attrayante, claire et percutante !

## FAQ

### Qu'est-ce qu'Aspose.Cells pour .NET ?
Aspose.Cells pour .NET est une bibliothèque puissante qui permet aux développeurs de manipuler des documents Excel par programmation, notamment en créant des graphiques et des diagrammes.

### Puis-je personnaliser les types de graphiques dans Aspose.Cells ?
Oui ! Aspose.Cells prend en charge différents types de graphiques tels que les graphiques à colonnes, les graphiques en lignes, les graphiques à secteurs et bien d'autres, qui peuvent être facilement personnalisés.

### Existe-t-il un essai gratuit disponible pour Aspose.Cells ?
 Absolument ! Vous pouvez télécharger une version d'essai gratuite à partir de[ici](https://releases.aspose.com/).

### Puis-je appliquer d’autres effets aux graphiques en plus des formats 3D ?
Oui, vous pouvez appliquer divers effets tels que des ombres, des dégradés et différents styles pour améliorer vos graphiques au-delà de la 3D.

### Où puis-je trouver du support pour Aspose.Cells ?
 Pour obtenir de l'aide, vous pouvez visiter le[Forum Aspose](https://forum.aspose.com/c/cells/9) pour l'assistance et l'aide à la communauté.