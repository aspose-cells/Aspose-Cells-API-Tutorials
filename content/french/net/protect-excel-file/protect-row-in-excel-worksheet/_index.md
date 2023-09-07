---
title: Protéger la ligne dans la feuille de calcul Excel
linktitle: Protéger la ligne dans la feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez dans ce tutoriel comment protéger les lignes d'un tableur Excel en utilisant Aspose.Cells pour .NET. Tutoriel pas à pas en C#.
type: docs
weight: 60
url: /fr/net/protect-excel-file/protect-row-in-excel-worksheet/
---
Dans ce didacticiel, nous examinerons du code source C # qui utilise la bibliothèque Aspose.Cells pour protéger les lignes d'une feuille de calcul Excel. Nous allons parcourir chaque étape du code et expliquer comment cela fonctionne. Suivez attentivement les instructions pour obtenir les résultats souhaités.

## Étape 1 : Prérequis

Avant de commencer, assurez-vous d'avoir installé la bibliothèque Aspose.Cells pour .NET. Vous pouvez l'obtenir sur le site officiel d'Aspose. Assurez-vous également que vous disposez d'une version récente de Visual Studio ou de tout autre environnement de développement C#.

## Étape 2 : Importer les espaces de noms requis

Pour utiliser la bibliothèque Aspose.Cells, nous devons importer les espaces de noms nécessaires dans notre code. Ajoutez les lignes suivantes en haut de votre fichier source C# :

```csharp
using Aspose.Cells;
```

## Étape 3 : Création d'un classeur Excel

Dans cette étape, nous allons créer un nouveau classeur Excel. Utilisez le code suivant pour créer un classeur Excel :

```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Créez un nouveau classeur.
Workbook wb = new Workbook();
```

 Assurez-vous de remplacer`"YOUR_DOCUMENTS_DIR"` avec le chemin approprié vers votre répertoire de documents.

## Étape 4 : Création d'une feuille de calcul

Maintenant que nous avons créé le classeur Excel, créons une feuille de calcul et obtenons la première feuille. Utilisez le code suivant :

```csharp
// Créez un objet de feuille de calcul et obtenez la première feuille.
Worksheet sheet = wb.Worksheets[0];
```

## Étape 5 : Définir le style

Dans cette étape, nous allons définir le style à appliquer aux lignes du tableur. Utilisez le code suivant :

```csharp
// Définition de l'objet de style.
Styling styling;
```

## Étape 6 : Bouclez pour déverrouiller toutes les colonnes

Nous allons maintenant parcourir toutes les colonnes de la feuille de calcul et les déverrouiller. Utilisez le code suivant :

```csharp
// Parcourez toutes les colonnes de la feuille de calcul et déverrouillez-les.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Étape 7 : Verrouillage de la première ligne

Dans cette étape, nous verrouillerons la première ligne de la feuille de calcul. Utilisez le code suivant :

```csharp
// Obtenez le style de la première ligne.
style = sheet.Cells.Rows[0].Style;
// Verrouillez le style.
style. IsLocked = true;
// Appliquez le style à la première ligne.
sheet.Cells.ApplyRowStyle(0, style);
```

## Étape 8 : Protéger la feuille de calcul

Maintenant que nous avons défini les styles et verrouillé les lignes, protégeons la feuille de calcul. Utilisez le code suivant :

```csharp
// Protégez la feuille de calcul.
sheet.Protect(ProtectionType.All);
```

## Étape 9 : Enregistrer le fichier Excel

Enfin, nous enregistrerons le fichier Excel modifié. Utilisez le code suivant :

```csharp
// Enregistrez le fichier Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Assurez-vous de spécifier le chemin d'accès correct pour enregistrer le fichier Excel modifié.

### Exemple de code source pour Protect Row In Excel Worksheet à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Créez un répertoire s'il n'est pas déjà présent.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Créez un nouveau classeur.
Workbook wb = new Workbook();
// Créez un objet feuille de calcul et obtenez la première feuille.
Worksheet sheet = wb.Worksheets[0];
// Définissez l'objet de style.
Style style;
// Définissez l'objet styleflag.
StyleFlag flag;
// Parcourez toutes les colonnes de la feuille de calcul et déverrouillez-les.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Obtenez le style de la première ligne.
style = sheet.Cells.Rows[0].Style;
// Verrouille le.
style.IsLocked = true;
//Instanciez le drapeau.
flag = new StyleFlag();
// Définissez le paramètre de verrouillage.
flag.Locked = true;
// Appliquez le style à la première ligne.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Protégez la feuille.
sheet.Protect(ProtectionType.All);
// Enregistrez le fichier excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusion

Félicitation ! Vous disposez maintenant d'un code source C# qui vous permet de protéger des lignes dans une feuille de calcul Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Assurez-vous de suivre attentivement les étapes et de personnaliser le code en fonction de vos besoins spécifiques.

### FAQ (Foire Aux Questions)

#### Ce code fonctionne-t-il avec les versions récentes d'Excel ?

Oui, ce code fonctionne avec les versions récentes d'Excel, y compris les fichiers au format Excel 2010 et supérieur.

#### Puis-je protéger uniquement des lignes spécifiques au lieu de toutes les lignes de la feuille de calcul ?

Oui, vous pouvez modifier le code pour spécifier les lignes spécifiques que vous souhaitez protéger. Vous devrez ajuster la boucle et les indices en conséquence.

#### Comment puis-je déverrouiller à nouveau les lignes verrouillées ?

 Vous pouvez utiliser le`IsLocked` méthode de la`Style` objet pour définir la valeur à`false` et déverrouiller les rangées.

#### Est-il possible de protéger plusieurs feuilles de calcul dans le même classeur Excel ?

Oui, vous pouvez répéter les étapes de création d'une feuille de calcul, de définition du style et de protection pour chaque feuille de calcul du classeur.

#### Comment puis-je modifier le mot de passe de protection de la feuille de calcul ?

 Vous pouvez modifier le mot de passe à l'aide du`Protect` méthode et en spécifiant un nouveau mot de passe comme argument.