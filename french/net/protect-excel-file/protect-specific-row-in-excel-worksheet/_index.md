---
title: Protéger une ligne spécifique dans une feuille de calcul Excel
linktitle: Protéger une ligne spécifique dans une feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Protégez une ligne spécifique dans Excel avec Aspose.Cells pour .NET. Guide étape par étape pour sécuriser vos données confidentielles.
type: docs
weight: 90
url: /fr/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
La protection des données confidentielles dans une feuille de calcul Excel est essentielle pour assurer la sécurité des informations. Aspose.Cells pour .NET offre une solution puissante pour protéger des lignes spécifiques dans une feuille de calcul Excel. Ce guide vous expliquera comment protéger une ligne spécifique dans une feuille de calcul Excel à l'aide du code source C# fourni. Suivez ces étapes simples pour configurer la protection des lignes dans vos fichiers Excel.

## Étape 1 : Importer les bibliothèques requises

Pour commencer, assurez-vous que Aspose.Cells pour .NET est installé sur votre système. Vous devez également ajouter les références appropriées dans votre projet C# pour pouvoir utiliser la fonctionnalité de Aspose.Cells. Voici le code pour importer les bibliothèques requises :

```csharp
// Ajouter les références nécessaires
using Aspose.Cells;
```

## Étape 2 : Création d'un classeur et d'une feuille de calcul Excel

Après avoir importé les bibliothèques requises, vous pouvez créer un nouveau classeur Excel et une nouvelle feuille de calcul. Voici comment procéder :

```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Créez un répertoire s'il n'existe pas déjà.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Créez un nouveau classeur.
Workbook wb = new Workbook();

// Créez un objet de feuille de calcul et obtenez la première feuille.
Worksheet sheet = wb.Worksheets[0];
```

## Étape 3 : Définition du style et de l'indicateur de style

Nous allons maintenant définir le style de cellule et l'indicateur de style pour déverrouiller toutes les colonnes de la feuille de calcul. Voici le code nécessaire :

```csharp
// Définissez l'objet de style.
Styling styling;

// Définissez l'objet styleflag.
StyleFlag flag;

// Parcourez toutes les colonnes de la feuille de calcul et déverrouillez-les.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Étape 4 : Protégez la ligne spécifique

Nous allons maintenant protéger la ligne spécifique dans la feuille de calcul. Nous allons verrouiller la première rangée pour empêcher toute modification. Voici comment:

```csharp
// Obtenez le style de la première ligne.
style = sheet.Cells.Rows[0].Style;

// Verrouille le.
style. IsLocked = true;

// Instanciez le drapeau.
flag = new StyleFlag();

// Définissez le paramètre de verrouillage.
flag. Locked = true;

// Appliquez le style à la première ligne.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Étape 5 : Protéger la feuille de calcul

Enfin, nous protégerons l'intégralité de la feuille de calcul Excel pour empêcher toute modification non autorisée. Voici comment:

```csharp
// Protégez la feuille de calcul.
sheet.Protect(ProtectionType.All);
```

## Étape 6 : Enregistrez le fichier Excel protégé

Une fois que vous avez terminé de protéger la ligne spécifique dans la feuille de calcul Excel, vous pouvez enregistrer le fichier Excel protégé sur votre système. Voici comment:

```csharp
// Enregistrez le fichier Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Après avoir suivi ces étapes, vous aurez protégé avec succès une ligne spécifique dans votre feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET.

### Exemple de code source pour protéger une ligne spécifique dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET 
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
//Définissez l'objet styleflag.
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
// Instanciez le drapeau.
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

La protection des données dans les fichiers Excel est cruciale pour empêcher tout accès non autorisé ou toute modification indésirable. À l'aide de la bibliothèque Aspose.Cells pour .NET, vous pouvez facilement protéger des lignes spécifiques dans une feuille de calcul Excel à l'aide du code source C# fourni. Suivez ce guide étape par étape pour ajouter une couche de sécurité supplémentaire à vos fichiers Excel.

### FAQ

#### La protection de ligne spécifique fonctionne-t-elle dans toutes les versions d'Excel ?
Oui, la protection de ligne spécifique à l'aide d'Aspose.Cells pour .NET fonctionne dans toutes les versions prises en charge d'Excel.

#### Puis-je protéger plusieurs lignes spécifiques dans une feuille de calcul Excel ?
Oui, vous pouvez protéger plusieurs lignes spécifiques en utilisant des méthodes similaires décrites dans ce guide.

#### Comment puis-je déverrouiller une ligne spécifique dans une feuille de calcul Excel ?
 Pour déverrouiller une ligne spécifique, vous devez modifier le code source en conséquence à l'aide de la`IsLocked` méthode de la`Style` objet.