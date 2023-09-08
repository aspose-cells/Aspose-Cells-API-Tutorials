---
title: Protéger des cellules spécifiques dans une feuille de calcul Excel
linktitle: Protéger des cellules spécifiques dans une feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment protéger des cellules spécifiques dans Excel avec Aspose.Cells pour .NET. Tutoriel étape par étape en C#.
type: docs
weight: 70
url: /fr/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
Dans ce didacticiel, nous examinerons le code source C# qui utilise la bibliothèque Aspose.Cells pour protéger des cellules spécifiques dans une feuille de calcul Excel. Nous passerons en revue chaque étape du code et expliquerons son fonctionnement. Suivez attentivement les instructions pour obtenir les résultats souhaités.

## Étape 1 : prérequis

Avant de commencer, assurez-vous d'avoir installé la bibliothèque Aspose.Cells pour .NET. Vous pouvez l'obtenir sur le site officiel d'Aspose. Assurez-vous également de disposer d'une version récente de Visual Studio ou de tout autre environnement de développement C#.

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

## Étape 4 : Création d'une feuille de calcul

Maintenant que nous avons créé le classeur Excel, créons une feuille de calcul et récupérons la première feuille. Utilisez le code suivant :

```csharp
// Créez un objet de feuille de calcul et obtenez la première feuille.
Worksheet sheet = wb.Worksheets[0];
```

## Étape 5 : Définir le style

Dans cette étape, nous définirons le style à appliquer à des cellules spécifiques. Utilisez le code suivant :

```csharp
// Définition de l'objet de style.
Styling styling;
```

## Étape 6 : Boucle pour déverrouiller toutes les colonnes

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

## Étape 7 : Verrouillage de cellules spécifiques

Dans cette étape, nous verrouillerons des cellules spécifiques. Utilisez le code suivant :

```csharp
//Verrouillage des trois cellules... c'est-à-dire A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Étape 8 : Protéger la feuille de calcul

Enfin, nous protégerons la feuille de calcul pour empêcher la modification de cellules spécifiques. Utilisez le code suivant :

```csharp
// Protégez la feuille de calcul.
sheet.Protect(ProtectionType.All);
```

## Étape 9 : Sauvegarde du fichier Excel

Nous allons maintenant sauvegarder le fichier Excel modifié. Utilisez le code suivant :

```csharp
// Enregistrez le fichier Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Assurez-vous de spécifier le chemin correct pour enregistrer le fichier Excel modifié.

### Exemple de code source pour protéger des cellules spécifiques dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Créez un répertoire s'il n'est pas déjà présent.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Créez un nouveau classeur.
Workbook wb = new Workbook();
// Créez un objet de feuille de calcul et obtenez la première feuille.
Worksheet sheet = wb.Worksheets[0];
// Définissez l'objet de style.
Style style;
// Définir l'objet styleflag
StyleFlag styleflag;
// Parcourez toutes les colonnes de la feuille de calcul et déverrouillez-les.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Verrouillez les trois cellules... c'est-à-dire A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Enfin, protégez la feuille maintenant.
sheet.Protect(ProtectionType.All);
// Enregistrez le fichier Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Conclusion

Félicitation ! Vous disposez désormais d'un code source C# qui vous permet de protéger des cellules spécifiques dans une feuille de calcul Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. N'hésitez pas à personnaliser le code en fonction de vos besoins spécifiques.

### FAQ (Foire aux questions)

#### Ce code fonctionne-t-il avec les versions récentes d'Excel ?

Oui, ce code fonctionne avec les versions récentes d'Excel, y compris les fichiers au format Excel 2010 et supérieur.

#### Puis-je protéger d’autres cellules que A1, B1 et C1 ?

Oui, vous pouvez modifier le code pour verrouiller d'autres cellules spécifiques en ajustant les références de cellules dans les lignes de code correspondantes.

#### Comment puis-je déverrouiller à nouveau les cellules verrouillées ?

 Vous pouvez utiliser`SetStyle` méthode avec`IsLocked` mis à`false` pour déverrouiller les cellules.

#### Puis-je ajouter plus de feuilles de calcul au classeur ?

 Oui, vous pouvez ajouter d'autres feuilles de calcul au classeur à l'aide de l'outil`Worksheets.Add()`méthode et répétez les étapes de protection cellulaire pour chaque feuille de travail.

#### Comment puis-je changer le format de sauvegarde du fichier Excel ?

 Vous pouvez modifier le format de sauvegarde à l'aide du`SaveFormat` méthode avec le format souhaité, par exemple`SaveFormat.Xlsx` pour Excel 2007 et versions ultérieures.