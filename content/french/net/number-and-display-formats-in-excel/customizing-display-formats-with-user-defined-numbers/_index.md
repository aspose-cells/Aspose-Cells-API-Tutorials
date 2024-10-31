---
title: Personnalisation des formats d'affichage avec des nombres définis par l'utilisateur
linktitle: Personnalisation des formats d'affichage avec des nombres définis par l'utilisateur
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment personnaliser les formats d'affichage avec Aspose.Cells pour .NET. Formatez les dates, les pourcentages et les devises à l'aide de ce guide étape par étape.
type: docs
weight: 11
url: /fr/net/number-and-display-formats-in-excel/customizing-display-formats-with-user-defined-numbers/
---
## Introduction
Travailler avec des fichiers Excel nécessite souvent de personnaliser la mise en forme des cellules pour présenter les données de manière plus significative et plus conviviale. Imaginez que vous créez un fichier Excel pour un rapport. Vous ne voulez pas seulement des chiffres bruts. Vous voulez que les dates, les pourcentages et les devises aient un aspect élégant et professionnel, n'est-ce pas ? C'est là que les formats d'affichage personnalisés entrent en jeu. Dans ce didacticiel, nous nous plongeons dans Aspose.Cells pour .NET pour vous montrer comment personnaliser le format d'affichage des nombres à l'aide de paramètres définis par l'utilisateur.
## Prérequis
Avant de commencer, assurez-vous que tout est prêt pour suivre ce tutoriel. Voici ce dont vous aurez besoin :
-  Aspose.Cells pour .NET installé.[Téléchargez-le ici](https://releases.aspose.com/cells/net/).
- Connaissances de base de C# et du framework .NET.
-  Une licence valide pour Aspose.Cells. Si vous n'en avez pas, prenez-en une[essai gratuit](https://releases.aspose.com/) ou demander un[permis temporaire](https://purchase.aspose.com/temporary-license/).
- Un IDE comme Visual Studio.
- .NET Framework 4.0 ou supérieur.
 S'il vous manque quelque chose, ne vous inquiétez pas. Vous pouvez toujours consulter ces liens pour télécharger les fichiers nécessaires ou demander de l'aide au[Forum d'assistance Aspose](https://forum.aspose.com/c/cells/9).
## Importer des espaces de noms
Avant de passer au code, vous devez importer les espaces de noms requis pour accéder à toutes les fonctionnalités Aspose.Cells nécessaires.
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
Ces deux espaces de noms seront vos outils principaux dans ce tutoriel. Passons maintenant à la partie amusante :
## Étape 1 : Configuration du répertoire du projet
Tout d'abord, vous avez besoin d'un endroit où stocker vos fichiers, n'est-ce pas ? Créons un répertoire pour enregistrer le fichier Excel de sortie. Dans cette étape, nous allons également nous assurer que le répertoire existe avant d'enregistrer quoi que ce soit.
```csharp
// Le chemin vers le répertoire des documents.
string dataDir = "Your Document Directory";
// Créez un répertoire s'il n'est pas déjà présent.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
-  Nous définissons un`dataDir` variable pour stocker le chemin où ira le fichier Excel de sortie.
-  Nous vérifions ensuite si le répertoire existe en utilisant`System.IO.Directory.Exists()`.
-  Si le répertoire n'existe pas, il sera créé en utilisant`System.IO.Directory.CreateDirectory()`.
## Étape 2 : créer un nouveau classeur et ajouter une feuille de calcul
Maintenant que nous avons notre répertoire, créons un nouveau classeur Excel et ajoutons-y une feuille de calcul.
```csharp
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook();
// Ajout d'une nouvelle feuille de calcul à l'objet Excel
int i = workbook.Worksheets.Add();
// Obtention de la référence de la feuille de calcul nouvellement ajoutée en passant son index de feuille
Worksheet worksheet = workbook.Worksheets[i];
```
-  Tout d’abord, nous créons un nouveau`Workbook` objet. Considérez ceci comme votre fichier Excel.
-  Nous ajoutons une nouvelle feuille de calcul à ce classeur en utilisant le`Add()`méthode et stocker l'index dans la variable`i`.
-  Nous référençons cette feuille de travail en utilisant le`workbook.Worksheets[i]`.
## Étape 3 : Ajout d'une date à une cellule et personnalisation de son format
 Maintenant, insérons la date actuelle dans une cellule et formatons-la pour qu'elle s'affiche de manière personnalisée. Au lieu du format de date par défaut, nous allons définir un format personnalisé comme`d-mmm-yy`.
```csharp
// Ajout de la date système actuelle à la cellule « A1 »
worksheet.Cells["A1"].PutValue(DateTime.Now);
// Obtenir le style de la cellule A1
Style style = worksheet.Cells["A1"].GetStyle();
// Définition du format d'affichage personnalisé pour afficher la date au format « j-mmm-aa »
style.Custom = "d-mmm-yy";
// Application du style à la cellule A1
worksheet.Cells["A1"].SetStyle(style);
```
-  Nous ajoutons la date actuelle du système à la cellule`A1` en utilisant`PutValue(DateTime.Now)`.
-  Nous récupérons le style actuel de la cellule`A1` en utilisant`GetStyle()`.
-  Nous modifions le style de la cellule en définissant`style.Custom = "d-mmm-yy"`, qui formate la date pour afficher le jour, le mois abrégé et l'année.
-  Enfin, nous appliquons le nouveau style à la cellule avec`SetStyle()`.
## Étape 4 : formater une cellule en pourcentage
 Ensuite, travaillons avec des nombres. Nous allons ajouter une valeur numérique à une autre cellule, par exemple`A2`et le formater sous forme de pourcentage.
```csharp
//Ajout d'une valeur numérique à la cellule « A2 »
worksheet.Cells["A2"].PutValue(20);
// Obtenir le style de la cellule A2
style = worksheet.Cells["A2"].GetStyle();
// Définition du format d'affichage personnalisé pour afficher la valeur sous forme de pourcentage
style.Custom = "0.0%";
// Application du style à la cellule A2
worksheet.Cells["A2"].SetStyle(style);
```
-  Nous ajoutons de la valeur`20` à la cellule`A2`.
-  Nous récupérons le style de la cellule`A2` et définissez le format personnalisé sur`0.0%` pour afficher la valeur en pourcentage (par exemple, 20 %).
-  Enfin, nous appliquons le style à la cellule en utilisant`SetStyle()`.
## Étape 5 : formater une cellule en tant que devise
 Ajoutons une autre valeur, par exemple à la cellule`A3`et le formater pour l'afficher sous forme de devise. Pour rendre les choses plus intéressantes, nous utiliserons un format qui affiche les valeurs positives sous forme de devise en livres et les valeurs négatives en dollars.
```csharp
// Ajout d'une valeur numérique à la cellule « A3 »
worksheet.Cells["A3"].PutValue(2546);
// Obtenir le style de la cellule A3
style = worksheet.Cells["A3"].GetStyle();
// Définition du format d'affichage personnalisé pour afficher la valeur sous forme de devise
style.Custom = "£#,##0;[Red]$-#,##0";
// Application du style à la cellule A3
worksheet.Cells["A3"].SetStyle(style);
```
-  Nous ajoutons de la valeur`2546` à la cellule`A3`.
-  Nous définissons un format personnalisé`£#,##0;[Red]$-#,##0`, qui affiche les valeurs positives avec un signe dièse et les valeurs négatives en rouge avec un signe dollar.
- Nous appliquons le style à la cellule en utilisant`SetStyle()`.
## Étape 6 : Enregistrer le classeur
La dernière étape consiste à enregistrer le classeur sous forme de fichier Excel. Nous utiliserons le format Excel 97-2003 pour ce didacticiel.
```csharp
// Sauvegarde du fichier Excel
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
-  Le`Save()` La méthode enregistre le classeur dans le répertoire spécifié.
-  Nous choisissons`SaveFormat.Excel97To2003` pour assurer la compatibilité avec les anciennes versions d'Excel.
## Conclusion
Et voilà ! Nous venons de créer un fichier Excel, d'ajouter des formats de date, de pourcentage et de devise personnalisés à des cellules spécifiques à l'aide d'Aspose.Cells pour .NET, puis d'enregistrer le fichier. La mise en forme personnalisée rend vos fichiers Excel beaucoup plus lisibles et professionnels. N'oubliez pas d'explorer d'autres options de mise en forme dans Aspose.Cells, comme la mise en forme conditionnelle, pour encore plus de contrôle sur l'apparence de vos données.
## FAQ
### Comment puis-je appliquer des options de formatage plus complexes dans Aspose.Cells ?
Vous pouvez combiner différents styles de formatage, tels que la couleur de police, les bordures et les couleurs d'arrière-plan, avec des formats de nombre personnalisés.
### Puis-je appliquer un format numérique personnalisé à une plage de cellules ?
Oui, Aspose.Cells vous permet d'appliquer un style à une plage de cellules à l'aide de la`Range.SetStyle()` méthode.
### Dans quels autres formats de fichiers puis-je enregistrer le classeur ?
 Aspose.Cells prend en charge de nombreux formats, notamment XLSX, CSV et PDF. Il suffit de modifier le`SaveFormat` dans le`Save()` méthode.
### Puis-je formater les nombres négatifs différemment ?
Absolument ! Vous pouvez utiliser des formats numériques personnalisés pour afficher les nombres négatifs avec des couleurs ou des symboles différents.
### Aspose.Cells pour .NET est-il gratuit ?
 Aspose.Cells propose un essai gratuit, mais pour bénéficier de toutes les fonctionnalités, vous aurez besoin d'une licence valide. Vous pouvez obtenir un[licence temporaire ici](https://purchase.aspose.com/temporary-license/).