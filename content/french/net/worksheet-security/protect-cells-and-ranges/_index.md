---
title: Protégez les cellules et les plages dans une feuille de calcul à l'aide d'Aspose.Cells
linktitle: Protégez les cellules et les plages dans une feuille de calcul à l'aide d'Aspose.Cells
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment protéger les cellules et les plages d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Suivez ce guide étape par étape pour sécuriser vos feuilles de calcul.
type: docs
weight: 11
url: /fr/net/worksheet-security/protect-cells-and-ranges/
---
## Introduction
Travailler avec des feuilles de calcul implique souvent de protéger certaines parties de la feuille contre des modifications indésirables, en particulier dans les environnements collaboratifs. Dans ce didacticiel, nous allons découvrir comment protéger des cellules et des plages spécifiques dans une feuille de calcul à l'aide d'Aspose.Cells pour .NET. Nous vous guiderons tout au long du processus de configuration d'une feuille protégée, en spécifiant les plages modifiables et en enregistrant le fichier. Cette fonctionnalité peut s'avérer extrêmement utile lorsque vous souhaitez restreindre l'accès à des données sensibles tout en autorisant la modification de certaines sections par d'autres.
## Prérequis
Avant de plonger dans le didacticiel, assurez-vous de disposer des prérequis suivants :
1. Aspose.Cells pour .NET : la bibliothèque Aspose.Cells doit être installée dans votre projet. Si ce n'est pas déjà fait, vous pouvez la télécharger à partir du[Site Web d'Aspose](https://releases.aspose.com/cells/net/).
2. Visual Studio : ce guide suppose que vous utilisez Visual Studio ou tout autre IDE similaire prenant en charge le développement C#.
3. Connaissances de base de C# : vous devez être familiarisé avec les bases de la programmation C# et savoir comment configurer un projet dans Visual Studio.
4.  Licence Aspose.Cells : Bien qu'Aspose propose un essai gratuit, une licence valide vous permettra d'utiliser l'ensemble des fonctionnalités de la bibliothèque. Si vous n'en avez pas, vous pouvez en obtenir une[licence temporaire ici](https://purchase.aspose.com/temporary-license/).
Une fois que vous vous êtes assuré que tout ce qui précède est prêt, nous pouvons passer à la partie codage.
## Paquets d'importation
Pour travailler avec Aspose.Cells, vous devez d'abord importer les espaces de noms nécessaires dans votre fichier C#. Voici comment vous pouvez les importer :
```csharp
using System.IO;
using Aspose.Cells;
```
 Le`Aspose.Cells` L'espace de noms vous donne accès aux fonctionnalités de base pour la manipulation de fichiers Excel et`System.IO` est utilisé pour les opérations sur les fichiers comme l'enregistrement du classeur.
Maintenant, décomposons les étapes pour protéger les cellules et les plages dans une feuille de calcul à l'aide d'Aspose.Cells.
## Étape 1 : Configurez votre environnement
Tout d'abord, créez un répertoire dans lequel vous souhaitez enregistrer vos fichiers Excel. Si le répertoire n'existe pas encore, nous en créerons un. Cela permet de garantir que vous disposez d'un emplacement pour stocker votre fichier de sortie.
```csharp
// Définissez le chemin d’accès à votre répertoire de documents
string dataDir = "Your Document Directory";
// Vérifiez si le répertoire existe, sinon créez-le
bool IsExists = Directory.Exists(dataDir);
if (!IsExists)
    Directory.CreateDirectory(dataDir);
```
 Ici, nous utilisons`System.IO.Directory.Exists()` pour vérifier si le dossier existe, et si non, nous le créons en utilisant`Directory.CreateDirectory()`.
## Étape 2 : Créer un nouveau classeur
Maintenant, instancions un nouvel objet Workbook. Il servira de fichier Excel dans lequel nous définirons nos cellules et nos plages.
```csharp
// Instancier un nouvel objet Workbook
Workbook book = new Workbook();
```
 Le`Workbook` class est le point d'entrée pour travailler avec des fichiers Excel dans Aspose.Cells. Il représente le document Excel.
## Étape 3 : Accéder à la feuille de calcul par défaut
Chaque classeur nouvellement créé possède une feuille de calcul par défaut. Nous la récupérerons pour travailler avec son contenu.
```csharp
// Obtenir la première feuille de calcul (par défaut) du classeur
Worksheet sheet = book.Worksheets[0];
```
 Ici,`Worksheets[0]` nous donne la première feuille du classeur (l'indexation commence à 0).
## Étape 4 : définir des plages modifiables
Pour protéger certaines parties de la feuille de calcul tout en permettant aux utilisateurs de modifier des cellules spécifiques, nous devons définir des plages modifiables. Nous allons créer une plage qui peut être modifiée et l'ajouter à la collection AllowEditRanges de la feuille de calcul.
```csharp
// Obtenir la collection AllowEditRanges
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Définissez un ProtectedRange et ajoutez-le à la collection
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
ProtectedRange protectedRange = allowRanges[idx];
```
Dans le code ci-dessus :
- `"r2"` est le nom de la plage modifiable.
-  Les chiffres`1, 1, 3, 3` représentent les indices de ligne et de colonne de début et de fin de la plage (c'est-à-dire de la cellule B2 à D4).
## Étape 5 : définir un mot de passe pour la plage protégée
Maintenant que nous avons défini la plage modifiable, ajoutons un mot de passe pour la protéger. Cela signifie que les utilisateurs auront besoin du mot de passe pour modifier cette plage spécifique.
```csharp
// Spécifiez le mot de passe pour la plage modifiable
protectedRange.Password = "123";
```
 Ici, nous avons défini le mot de passe comme`"123"`, mais vous pouvez choisir n'importe quel mot de passe sécurisé. Cette étape est essentielle pour contrôler l'accès aux zones modifiables.
## Étape 6 : Protégez la feuille entière
À ce stade, nous allons protéger l'intégralité de la feuille de calcul. La protection de la feuille de calcul garantit que les autres parties de la feuille, à l'exception des plages autorisées, ne sont pas modifiables.
```csharp
// Protégez la feuille avec le type de protection spécifié (Tous)
sheet.Protect(ProtectionType.All);
```
Cela garantit que toutes les cellules de la feuille sont verrouillées, à l'exception de celles des plages modifiables.
## Étape 7 : Enregistrer le classeur
Enfin, nous enregistrons le classeur dans un fichier. La feuille protégée sera enregistrée sous le nom que vous aurez spécifié.
```csharp
// Enregistrez le fichier Excel dans le répertoire spécifié
book.Save(dataDir + "protectedrange.out.xls");
```
 Ici, le fichier Excel sera enregistré sous`protectedrange.out.xls` dans le répertoire que nous avons défini précédemment. Si vous souhaitez l'enregistrer sous un nom ou un format différent, vous pouvez modifier le nom et l'extension du fichier.
## Conclusion
En suivant ce didacticiel, vous avez appris à protéger les cellules et les plages d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Cette approche vous offre la possibilité de contrôler les zones de votre feuille de calcul qui peuvent être modifiées et celles qui ne le peuvent pas. Vous pouvez désormais appliquer ces compétences dans vos propres projets, en garantissant la sécurité de vos données sensibles tout en fournissant des zones modifiables aux utilisateurs.
N'oubliez pas qu'Aspose.Cells propose un ensemble robuste d'outils pour travailler avec des fichiers Excel, et ce n'est qu'une des nombreuses choses que vous pouvez faire avec lui. 
## FAQ
### Puis-je protéger uniquement certaines cellules d’une feuille de calcul ?
 Oui, en utilisant le`AllowEditRanges` propriété, vous pouvez spécifier quelles cellules ou plages peuvent être modifiées tandis que le reste de la feuille de calcul reste protégé.
### Puis-je retirer la protection plus tard ?
 Oui, vous pouvez déprotéger une feuille de calcul en utilisant le`Unprotect()` méthode, et si un mot de passe a été défini, vous devrez le fournir.
### Comment protéger une feuille entière avec un mot de passe ?
 Pour protéger toute la feuille, il suffit d'utiliser le`Protect()` méthode avec ou sans mot de passe. Par exemple,`sheet.Protect("password")`.
### Puis-je ajouter plusieurs plages modifiables ?
 Absolument ! Vous pouvez ajouter autant de plages modifiables que vous le souhaitez en appelant`allowRanges.Add()` plusieurs fois.
### Quelles autres fonctionnalités de sécurité Aspose.Cells offre-t-il ?
Aspose.Cells prend en charge diverses fonctionnalités de sécurité telles que le cryptage des classeurs, la définition de mots de passe de fichiers et la protection des cellules et des feuilles.