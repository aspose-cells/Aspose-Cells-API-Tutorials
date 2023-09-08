---
title: Définir les en-têtes et pieds de page Excel
linktitle: Définir les en-têtes et pieds de page Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment définir des en-têtes et des pieds de page dans Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 100
url: /fr/net/excel-page-setup/set-excel-headers-and-footers/
---

Dans ce didacticiel, nous allons vous montrer étape par étape comment définir les en-têtes et pieds de page dans Excel à l'aide d'Aspose.Cells pour .NET. Nous utiliserons le code source C# pour illustrer le processus.

## Étape 1 : Configuration de l'environnement

Assurez-vous que Aspose.Cells pour .NET est installé sur votre ordinateur. Créez également un nouveau projet dans votre environnement de développement préféré.

## Étape 2 : Importer les bibliothèques nécessaires

Dans votre fichier de code, importez les bibliothèques nécessaires pour travailler avec Aspose.Cells. Voici le code correspondant :

```csharp
using Aspose.Cells;
```

## Étape 3 : Définir le répertoire de données

Définissez le répertoire de données dans lequel vous souhaitez enregistrer le fichier Excel modifié. Utilisez le code suivant :

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Assurez-vous de spécifier le chemin complet du répertoire.

## Étape 4 : Création du classeur et de la feuille de calcul

Créez un nouvel objet Workbook et accédez à la première feuille de calcul du classeur à l'aide du code suivant :

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Cela créera un classeur vide avec une feuille de calcul et donnera accès à l'objet PageSetup de cette feuille de calcul.

## Étape 5 : Définition des en-têtes

 Définissez les en-têtes de la feuille de calcul à l'aide du`SetHeader` méthodes de l’objet PageSetup. Voici un exemple de code :

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Cela définira respectivement le nom de la feuille de calcul, la date et l'heure actuelles et le nom du fichier dans les en-têtes.

## Étape 6 : Définir les pieds de page

 Définissez les pieds de page de la feuille de calcul à l'aide de l'outil`SetFooter` méthodes de l’objet PageSetup. Voici un exemple de code :

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Cela définira respectivement une chaîne de texte, le numéro de la page actuelle et le nombre total de pages dans les pieds de page.

## Étape 7 : enregistrement du classeur modifié

Enregistrez le classeur modifié à l'aide du code suivant :

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Cela enregistrera le classeur modifié dans le répertoire de données spécifié.

### Exemple de code source pour définir les en-têtes et pieds de page Excel à l’aide d’Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
Workbook excel = new Workbook();
// Obtention de la référence du PageSetup de la feuille de calcul
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Définition du nom de la feuille de calcul dans la section gauche de l'en-tête
pageSetup.SetHeader(0, "&A");
//Réglage de la date et de l'heure actuelles dans la section centrale de l'en-tête
// et changer la police de l'en-tête
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Définir le nom du fichier actuel dans la section droite de l'en-tête et modifier le
// police de l'en-tête
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Définir une chaîne dans la section gauche du pied de page et modifier la police
// d'une partie de cette chaîne ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Définition du numéro de page actuel dans la section centrale du pied de page
pageSetup.SetFooter(1, "&P");
// Définition du nombre de pages dans la section droite du pied de page
pageSetup.SetFooter(2, "&N");
// Enregistrez le classeur.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Conclusion

Vous avez maintenant appris à définir les en-têtes et les pieds de page dans Excel à l'aide d'Aspose.Cells pour .NET. Ce didacticiel vous a guidé à travers chaque étape du processus, de la configuration de l'environnement à l'enregistrement du classeur modifié. N'hésitez pas à explorer davantage les fonctionnalités d'Aspose.Cells pour effectuer d'autres manipulations dans vos fichiers Excel.

### Foire aux questions (FAQ)

#### 1. Comment puis-je installer Aspose.Cells pour .NET sur mon système ?
Pour installer Aspose.Cells pour .NET, vous devez télécharger le package d'installation depuis le site officiel d'Aspose et suivre les instructions fournies dans la documentation.

#### 2. Cette méthode fonctionne-t-elle avec toutes les versions d’Excel ?
Oui, la méthode de définition des en-têtes et des pieds de page avec Aspose.Cells pour .NET fonctionne avec toutes les versions prises en charge d'Excel.

#### 3. Puis-je personnaliser davantage les en-têtes et les pieds de page ?
Oui, Aspose.Cells offre une large gamme de fonctionnalités pour personnaliser les en-têtes et les pieds de page, notamment le placement du texte, la couleur, la police, les numéros de page, etc.

#### 4. Comment puis-je ajouter des informations dynamiques aux en-têtes et pieds de page ?
Vous pouvez utiliser des variables spéciales et des codes de formatage pour ajouter des informations dynamiques telles que la date, l'heure, le nom de fichier, le numéro de page, etc., aux en-têtes et pieds de page.

#### 5. Puis-je supprimer les en-têtes et les pieds de page après les avoir définis ?
 Oui, vous pouvez supprimer les en-têtes et les pieds de page à l'aide de l'outil`ClearHeaderFooter` méthode du`PageSetup` objet. Cela restaurera les en-têtes et pieds de page par défaut.