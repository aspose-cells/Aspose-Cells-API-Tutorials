---
title: Enregistrement de tableaux croisés dynamiques avec tri et masquage personnalisés dans .NET
linktitle: Enregistrement de tableaux croisés dynamiques avec tri et masquage personnalisés dans .NET
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment enregistrer des tableaux croisés dynamiques avec un tri personnalisé et masquer des lignes à l'aide d'Aspose.Cells pour .NET. Guide étape par étape avec des exemples pratiques inclus.
type: docs
weight: 26
url: /fr/net/creating-and-configuring-pivot-tables/saving-with-custom-sort-and-hide/
---
## Introduction
Dans le monde de l'analyse de données, les tableaux croisés dynamiques sont l'un des outils les plus puissants pour résumer, analyser et présenter des données dans un format digeste. Si vous travaillez avec .NET et que vous recherchez un moyen simple de manipuler des tableaux croisés dynamiques, en particulier pour les enregistrer avec un tri personnalisé et masquer des lignes spécifiques, vous êtes au bon endroit ! Aujourd'hui, nous allons décortiquer la technique d'enregistrement des tableaux croisés dynamiques à l'aide d'Aspose.Cells pour .NET. Ce guide vous guidera à travers tout, des prérequis aux exemples pratiques, en vous assurant d'être équipé pour vous attaquer à des tâches similaires par vous-même. Alors, allons-y !
## Prérequis
Avant de plonger dans les détails du codage, assurez-vous de disposer des prérequis suivants :
1. Visual Studio : idéalement, vous souhaitez disposer d'un IDE solide pour gérer vos projets .NET. Visual Studio est un excellent choix.
2.  Aspose.Cells pour .NET : vous aurez besoin d'accéder à la bibliothèque d'Aspose pour gérer les fichiers Excel par programmation. Vous pouvez[Téléchargez Aspose.Cells pour .NET ici](https://releases.aspose.com/cells/net/).
3. Connaissances de base de C# : la familiarité avec les concepts de programmation de base et la syntaxe en C# rendra le processus plus fluide.
4.  Exemple de fichier Excel : nous utiliserons un exemple de fichier nommé`PivotTableHideAndSortSample.xlsx`Assurez-vous d'avoir ce fichier dans votre répertoire de documents désigné.
Une fois votre environnement de développement configuré et votre fichier d’exemple prêt, vous êtes prêt !
## Paquets d'importation
Maintenant que nous avons vérifié les prérequis, importons les packages nécessaires. Dans votre fichier C#, utilisez la directive suivante pour inclure Aspose.Cells :
```csharp
using System;
using Aspose.Cells.Pivot;
```
Cette directive vous permet d'accéder aux classes et méthodes fournies par la bibliothèque Aspose.Cells. Assurez-vous d'avoir ajouté Aspose.Cells.dll aux références de votre projet.
## Étape 1 : Configurer le classeur
Tout d'abord, nous devons charger notre classeur. L'extrait de code suivant permet d'y parvenir :
```csharp
// Répertoires pour les fichiers source et de sortie
string sourceDir = "Your Document Directory";
string outputDir = "Your Document Directory";
// Charger le classeur
Workbook workbook = new Workbook(sourceDir + "PivotTableHideAndSortSample.xlsx");
```
 Dans cette étape, vous définissez les répertoires dans lesquels vos fichiers source et de sortie sont stockés.`Workbook`Le constructeur chargera votre fichier Excel existant, le rendant prêt à être manipulé.
## Étape 2 : Accéder à la feuille de calcul et au tableau croisé dynamique
Maintenant, accédons à la feuille de calcul spécifique dans le classeur et sélectionnons le tableau croisé dynamique avec lequel nous voulons travailler.
```csharp
// Accéder à la première feuille de calcul
Worksheet worksheet = workbook.Worksheets[0];
// Accéder au premier tableau croisé dynamique de la feuille de calcul
var pivotTable = worksheet.PivotTables[0];
```
 Dans cet extrait,`Worksheets[0]` sélectionne la première feuille de votre document Excel et`PivotTables[0]` récupère le premier tableau croisé dynamique. Cela vous permet de cibler exactement le tableau croisé dynamique que vous souhaitez modifier.
## Étape 3 : Trier les lignes du tableau croisé dynamique
Ensuite, nous allons mettre en œuvre un tri personnalisé pour organiser nos données. Plus précisément, nous allons trier les scores par ordre décroissant.
```csharp
// Trier le champ de la première ligne par ordre décroissant
PivotField field = pivotTable.RowFields[0];
field.IsAutoSort = true;
field.IsAscendSort = false;  // faux pour décroissant
field.AutoSortField = 0;     // Tri basé sur la première colonne
```
 Ici, nous utilisons le`PivotField` pour définir les paramètres de tri. Cela indique au tableau croisé dynamique de trier le champ de ligne spécifié en fonction de la première colonne, et de le faire dans l'ordre décroissant. 
## Étape 4 : Actualiser et calculer les données
Après avoir appliqué le tri, il est essentiel d'actualiser les données du tableau croisé dynamique pour garantir qu'elles reflètent nos modifications.
```csharp
// Actualiser et calculer les données du tableau croisé dynamique
pivotTable.RefreshData();
pivotTable.CalculateData();
```
Cette étape synchronise le tableau croisé dynamique avec vos données actuelles, en appliquant toutes les modifications de tri ou de filtrage que vous avez apportées jusqu'à présent. Considérez cela comme un clic sur « Actualiser » pour voir la nouvelle organisation de vos données !
## Étape 5 : Masquer des lignes spécifiques
Masquons maintenant les lignes qui contiennent des scores inférieurs à un certain seuil, par exemple inférieurs à 60. C'est ici que nous pouvons filtrer encore plus les données.
```csharp
// Spécifiez la ligne de départ pour la vérification des scores
int currentRow = 3;
int rowsUsed = pivotTable.DataBodyRange.EndRow;
// Masquer les lignes avec un score inférieur à 60
while (currentRow < rowsUsed)
{
    Cell cell = worksheet.Cells[currentRow, 1]; // En supposant que le score soit dans la première colonne
    double score = Convert.ToDouble(cell.Value);
    if (score < 60)
    {
        worksheet.Cells.HideRow(currentRow);  // Masquer la ligne si le score est inférieur à 60
    }
    currentRow++;
}
```
Dans cette boucle, nous vérifions chaque ligne dans la plage de données du tableau croisé dynamique. Si un score est inférieur à 60, nous masquons cette ligne. C'est comme nettoyer votre espace de travail : supprimer le fouillis qui ne vous aide pas à voir la situation dans son ensemble !
## Étape 6 : Actualisation finale et enregistrement du classeur
Avant de terminer, effectuons une dernière actualisation du tableau croisé dynamique pour nous assurer que le masquage des lignes prend effet, puis enregistrons le classeur dans un nouveau fichier.
```csharp
// Actualiser et calculer les données une dernière fois
pivotTable.RefreshData();
pivotTable.CalculateData();
// Enregistrer le classeur modifié
workbook.Save(outputDir + "PivotTableHideAndSort_out.xlsx");
```
Cette actualisation finale garantit que tout est à jour et en enregistrant le classeur, vous créez un nouveau fichier qui reflète toutes les modifications que nous avons apportées.
## Étape 7 : Confirmer le succès
Enfin, nous imprimerons un message de réussite pour confirmer que notre opération s'est déroulée sans accroc.
```csharp
Console.WriteLine("PivotTableSortAndHide executed successfully.");
```
Cette ligne a pour double objectif de confirmer le succès et de fournir des commentaires dans votre console, rendant le processus un peu plus interactif et convivial.
## Conclusion
Et voilà ! Vous avez appris avec succès à enregistrer des tableaux croisés dynamiques avec des fonctionnalités de tri et de masquage personnalisées à l'aide d'Aspose.Cells pour .NET. Du chargement de votre classeur au tri des données et au masquage des détails inutiles, ces étapes fournissent une approche structurée pour gérer vos tableaux croisés dynamiques par programmation. Que vous analysiez des données de vente, suiviez les performances de votre équipe ou organisiez simplement des informations, la maîtrise de ces compétences avec Aspose.Cells peut vous faire gagner un temps précieux et améliorer votre flux de travail d'analyse des données.
## FAQ
### Qu'est-ce qu'Aspose.Cells pour .NET ?
Aspose.Cells for .NET est une bibliothèque .NET qui permet aux développeurs de créer, de manipuler et de convertir des feuilles de calcul Excel sans avoir recours à Microsoft Excel. Elle est parfaite pour automatiser les tâches dans les documents Excel.
### Puis-je utiliser Aspose.Cells sans Microsoft Office installé ?
Absolument ! Aspose.Cells est une bibliothèque autonome, vous n'avez donc pas besoin que Microsoft Office soit installé sur votre système pour travailler avec des fichiers Excel.
### Comment puis-je obtenir une licence temporaire pour Aspose.Cells ?
 Vous pouvez demander une licence temporaire via le[page de licence temporaire](https://purchase.aspose.com/temporary-license/).
### Où puis-je trouver de l'aide pour les problèmes liés à Aspose.Cells ?
 Pour toute question ou problème, vous pouvez visiter le[Forum Aspose](https://forum.aspose.com/c/cells/9), où vous trouverez le soutien de la communauté et de l'équipe Aspose.
### Existe-t-il un essai gratuit disponible pour Aspose.Cells ?
 Oui ! Vous pouvez télécharger une version d'essai gratuite d'Aspose.Cells pour tester ses fonctionnalités avant de procéder à un achat. Visitez le[page d'essai gratuite](https://releases.aspose.com/) pour commencer.