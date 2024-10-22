---
title: Ajouter une zone de texte à une feuille de calcul dans Excel
linktitle: Ajouter une zone de texte à une feuille de calcul dans Excel
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment ajouter des zones de texte personnalisables à Excel à l’aide d’Aspose.Cells pour .NET dans ce didacticiel étape par étape.
type: docs
weight: 14
url: /fr/net/excel-shapes-controls/add-textbox-to-worksheet-excel/
---
## Introduction
Vous souhaitez enrichir vos feuilles de calcul Excel avec des éléments visuels uniques qui peuvent intéresser votre public ? L'ajout de zones de texte est un excellent moyen d'y parvenir ! Avec Aspose.Cells pour .NET, vous pouvez facilement intégrer des zones de texte dans vos feuilles de calcul Excel, rendant ainsi vos documents plus informatifs et visuellement attrayants. Ce guide étape par étape vous guidera tout au long du processus simple d'ajout de zones de texte à l'aide d'Aspose.Cells, en vous montrant comment les personnaliser avec du texte, des couleurs, des hyperliens et bien plus encore !
## Prérequis
Avant de plonger dans les merveilles du codage, voici les prérequis essentiels pour garantir une expérience de navigation fluide :
1. Environnement de développement .NET : vous aurez besoin d'un framework .NET fonctionnel ainsi que d'un IDE comme Visual Studio. Assurez-vous qu'il est mis à jour vers la dernière version !
2.  Aspose.Cells pour .NET : assurez-vous que la bibliothèque Aspose.Cells est téléchargée. Vous pouvez récupérer la dernière version à partir de[ici](https://releases.aspose.com/cells/net/).
3. Connaissances de base en programmation : une familiarité avec C# et quelques concepts généraux de gestion des fichiers Excel rendront ce tutoriel plus facile !
## Paquets d'importation
Assurez-vous d'importer les packages nécessaires au début de votre fichier C#. Voici comment procéder :
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
## Installer Aspose.Cells
Si vous ne l’avez pas déjà fait, vous pouvez ajouter Aspose.Cells via le gestionnaire de packages NuGet dans Visual Studio :
1. Ouvrez Visual Studio.
2.  Aller à`Tools` ->`NuGet Package Manager` ->`Manage NuGet Packages for Solution`.
3. Recherchez « Aspose.Cells » et installez-le pour votre projet.
Maintenant que nous avons posé les bases, passons à la partie amusante !
## Étape 1 : Configuration de votre répertoire de documents
Tout d'abord, configurons le répertoire dans lequel seront stockés tous vos documents Excel. Il est essentiel de s'assurer que ce répertoire existe avant de commencer à créer notre classeur.
```csharp
// Le chemin vers le répertoire des documents.
string dataDir = "Your Document Directory"; 
//Créez un répertoire s'il n'est pas déjà présent.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists) 
    System.IO.Directory.CreateDirectory(dataDir);
```
Cet extrait de code créera un répertoire nommé`Your Document Directory` (veuillez le remplacer par votre chemin actuel) s'il n'existe pas déjà. Facile comme tout, n'est-ce pas ?
## Étape 2 : Instanciation d'un nouveau classeur
Ensuite, nous devons créer un nouveau classeur dans lequel nous ajouterons nos zones de texte. Cela peut être facilement réalisé avec quelques lignes de code :
```csharp
// Instancier un nouveau classeur.
Workbook workbook = new Workbook();
```
Cette ligne de code crée un nouveau classeur Excel. Simple et direct !
## Étape 3 : Accéder à la première feuille de calcul
Maintenant que notre classeur est prêt, prenons la première feuille de calcul dans laquelle nous ajouterons notre zone de texte :
```csharp
// Procurez-vous la première feuille de travail du livre.
Worksheet worksheet = workbook.Worksheets[0];
```
 Comme ça, vous avez maintenant accès à la première feuille de calcul nommée`worksheet`Il est temps de le faire briller !
## Étape 4 : Ajout d'une zone de texte
Très bien, il est temps d'ajouter notre première zone de texte ! Voici comment procéder :
```csharp
// Ajoutez une nouvelle zone de texte à la collection.
int textboxIndex = worksheet.TextBoxes.Add(2, 1, 160, 200);
```
Dans cette ligne, nous spécifions la ligne et la colonne où la zone de texte sera placée, ainsi que sa largeur et sa hauteur (160 et 200, respectivement). N'hésitez pas à ajuster ces chiffres en fonction de votre mise en page !
## Étape 5 : Obtenir l'objet TextBox
Après avoir ajouté la zone de texte, nous devons obtenir une référence à celle-ci afin de pouvoir personnaliser son contenu :
```csharp
// Obtenez l'objet zone de texte.
Aspose.Cells.Drawing.TextBox textbox0 = worksheet.TextBoxes[textboxIndex];
```
 Maintenant,`textbox0` est votre ticket d'or pour modifier cette zone de texte !
## Étape 6 : Remplissage de la zone de texte avec du contenu
Ensuite, fournissons du texte pour la zone de texte :
```csharp
// Remplissez le texte.
textbox0.Text = "ASPOSE______The .NET & JAVA Component Publisher!";
```
Insérer du texte dans votre zone de texte est aussi simple que cela ! 
## Étape 7 : Personnaliser l'apparence de la zone de texte
Et si on le rafraichissait un peu ? Vous pouvez ajuster les couleurs de police, les styles et bien plus encore !
```csharp
// Définissez la couleur de la police.
textbox0.Font.Color = Color.Blue;
// Réglez la police en gras.
textbox0.Font.IsBold = true;
// Définir la taille de la police.
textbox0.Font.Size = 14;
// Définir l'attribut de police sur italique.
textbox0.Font.IsItalic = true;
```
N'hésitez pas à jouer avec différentes couleurs et styles pour voir ce qui ressort le mieux visuellement !
## Étape 8 : Ajout d’un lien hypertexte
Vous souhaitez transformer votre zone de texte en lien cliquable ? C'est exactement ce que nous faisons :
```csharp
// Ajoutez un lien hypertexte à la zone de texte.
textbox0.AddHyperlink("http://www.aspose.com/");
```
Désormais, quiconque clique sur votre zone de texte sera transporté vers le site Web d'Aspose. C'est comme de la magie !
## Étape 9 : Définition du type de placement de la zone de texte
Vous avez le choix entre plusieurs options pour définir le comportement de la zone de texte par rapport à votre feuille de calcul. Voici un exemple de configuration pour qu'elle soit flottante :
```csharp
// Définissez le placement.
textbox0.Placement = PlacementType.FreeFloating;
```
Alternativement, si vous souhaitez qu'il soit redimensionné et déplacé avec les cellules, vous pouvez le définir comme ceci :
```csharp
// Définissez le type de placement car la zone de texte se déplacera et se redimensionnera avec les cellules.
textbox1.Placement = PlacementType.MoveAndSize;
```
## Étape 10 : Personnalisation des formats de ligne et de remplissage
Voici comment vous pouvez modifier l'apparence de la bordure et du remplissage de la zone de texte :
```csharp
// Obtenir le format de remplissage de la zone de texte.
Aspose.Cells.Drawing.FillFormat fillformat = textbox0.Fill;            
// Obtenir le type de format de ligne de la zone de texte.
Aspose.Cells.Drawing.LineFormat lineformat = textbox0.Line;           
// Définissez l'épaisseur de la ligne.
lineformat.Weight = 6;
// Définissez le style du tiret sur carrépoint.
lineformat.DashStyle = MsoLineDashStyle.SquareDot;
```
Grâce à cela, vous pouvez personnaliser davantage votre zone de texte en ajoutant des éléments visuels adaptés à votre style.
## Étape 11 : Ajout d'une autre zone de texte
Personne n'a dit que nous ne pouvions ajouter qu'une seule zone de texte ! Insérons-en une autre avec un texte différent :
```csharp
// Ajoutez une autre zone de texte.
textboxIndex = worksheet.TextBoxes.Add(15, 4, 85, 120);
// Obtenez la deuxième zone de texte.
Aspose.Cells.Drawing.TextBox textbox1 = worksheet.TextBoxes[textboxIndex];
// Saisissez-y du texte.
textbox1.Text = "This is another simple text box";
```
Vous égayez désormais vraiment votre feuille Excel avec plusieurs zones de texte !
## Étape 12 : Enregistrer votre classeur
Enfin, il est temps de sauvegarder notre chef-d'œuvre ! Voici la dernière ligne de code de la journée :
```csharp
// Enregistrez le fichier Excel.
workbook.Save(dataDir + "book1.out.xls");
```
Avec seulement cette ligne de code, vous avez créé et modifié un fichier Excel avec des zones de texte personnalisables !
## Conclusion
Félicitations ! Vous avez navigué avec succès dans le monde des zones de texte dans Excel à l'aide d'Aspose.Cells pour .NET. Vous avez non seulement appris à ajouter une zone de texte, mais également à la personnaliser pour rendre vos feuilles de calcul plus attrayantes. Du changement de couleurs et de styles à l'ajout d'hyperliens, les possibilités sont pratiquement infinies ! 
Etes-vous prêt à commencer à transformer vos documents Excel ? Laissez libre cours à votre créativité et expérimentez différentes mises en page !
## FAQ
### Qu'est-ce qu'Aspose.Cells pour .NET ?
Aspose.Cells pour .NET est une bibliothèque puissante qui permet aux développeurs de créer, manipuler et convertir des fichiers Excel sans effort.
### Puis-je essayer Aspose.Cells avant d'acheter ?
 Oui ! Vous pouvez télécharger et utiliser une version d'essai gratuite[ici](https://releases.aspose.com/).
### Où puis-je trouver la documentation d'Aspose.Cells ?
 Vous pouvez accéder à une documentation complète sur[Documentation sur Aspose.Cells](https://reference.aspose.com/cells/net/).
### Existe-t-il une assistance disponible si je rencontre des problèmes ?
 Absolument ! Si vous avez besoin d'aide, rendez-vous sur le[Forum Aspose](https://forum.aspose.com/c/cells/9) pour obtenir de l'aide.
### Puis-je utiliser Aspose.Cells sans licence ?
 Bien que vous puissiez utiliser une version d'essai gratuite, pour accéder à toutes les fonctionnalités, vous devrez acheter une licence. Consultez les tarifs[ici](https://purchase.aspose.com/buy).