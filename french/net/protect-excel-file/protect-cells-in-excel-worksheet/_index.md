---
title: Protéger les cellules dans la feuille de calcul Excel
linktitle: Protéger les cellules dans la feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à protéger des cellules spécifiques dans Excel avec Aspose.Cells pour .NET. Tutoriel pas à pas en C#.
type: docs
weight: 30
url: /fr/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel est un outil largement utilisé pour créer et gérer des feuilles de calcul. L'une des principales fonctionnalités d'Excel est la possibilité de protéger certaines cellules pour préserver l'intégrité des données. Dans ce didacticiel, nous vous guiderons pas à pas pour protéger des cellules spécifiques dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Aspose.Cells pour .NET est une puissante bibliothèque de programmation qui facilite la manipulation des fichiers Excel avec une grande flexibilité et des fonctionnalités avancées. Suivez les étapes fournies pour savoir comment protéger vos cellules importantes et assurer la sécurité de vos données.

## Étape 1 : Configurer l'environnement

Assurez-vous que Aspose.Cells pour .NET est installé dans votre environnement de développement. Téléchargez la bibliothèque sur le site officiel d'Aspose et consultez la documentation pour les instructions d'installation.

## Étape 2 : Initialisation du classeur et de la feuille de calcul

Pour commencer, nous devons créer un nouveau classeur et obtenir la référence à la feuille de calcul où nous voulons protéger les cellules. Utilisez le code suivant :

```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Créez le répertoire s'il n'existe pas déjà.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Créer un nouveau classeur
Workbook workbook = new Workbook();

// Obtenir la première feuille de calcul
Worksheet sheet = workbook.Worksheets[0];
```

 Dans cet extrait de code, nous définissons d'abord le chemin d'accès au répertoire où le fichier Excel sera enregistré. Ensuite, nous créons une nouvelle instance de`Workbook` classe et obtenir la référence à la première feuille de calcul en utilisant le`Worksheets`propriété.

## Étape 3 : Définir le style de cellule

Maintenant, nous devons définir le style des cellules que nous voulons protéger. Utilisez le code suivant :

```csharp
// Définir l'objet de style
Styling styling;

// Parcourez toutes les colonnes de la feuille de calcul et déverrouillez-les
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 Dans ce code, nous utilisons une boucle pour parcourir toutes les colonnes de la feuille de calcul et déverrouiller leurs cellules en définissant le style`IsLocked` propriété à`false` . On utilise alors le`ApplyStyle` méthode pour appliquer le style aux colonnes avec la`StyleFlag` drapeau pour verrouiller les cellules.

## Étape 4 : Protégez des cellules spécifiques

Nous allons maintenant protéger les cellules spécifiques que nous voulons verrouiller. Utilisez le code suivant :

```csharp
// Verrouillez les trois cellules : A1, B1, C1
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

 Dans ce code, nous obtenons le style de chaque cellule spécifique en utilisant le`GetStyle` méthode, puis nous définissons la`IsLocked` propriété du style à`true`pour verrouiller la cellule. Enfin, nous appliquons le style mis à jour à chaque cellule à l'aide de la`SetStyle` méthode.

## Étape 5 : Protéger la feuille de calcul

Maintenant que nous avons défini les cellules à protéger, nous pouvons protéger la feuille de calcul elle-même. Utilisez le code suivant :

```csharp
// Protéger la feuille de calcul
leaf.Protect(ProtectionType.All);
```

 Ce code utilise le`Protect` méthode pour protéger la feuille de calcul avec le type de protection spécifié, dans ce cas`ProtectionType.All` qui protège tous les éléments de la feuille de calcul.

## Étape 6 : Enregistrez le fichier Excel

Enfin, nous enregistrons le fichier Excel avec les modifications apportées. Utilisez le code suivant :

```csharp
// Enregistrez le fichier Excel
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 Dans ce code, nous utilisons le`Save` méthode pour enregistrer le classeur dans le répertoire spécifié avec la`Excel97To2003` format.

### Exemple de code source pour Protéger les cellules dans la feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET 
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
//Enfin, Protégez la feuille maintenant.
sheet.Protect(ProtectionType.All);
// Enregistrez le fichier excel.
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Conclusion

Félicitation ! Vous avez appris à protéger des cellules spécifiques dans une feuille de calcul Excel à l'aide de Aspose.Cells pour .NET. Vous pouvez maintenant appliquer cette technique dans vos propres projets et améliorer la sécurité de vos fichiers Excel.


### FAQ

#### Q : Pourquoi devrais-je utiliser Aspose.Cells pour .NET pour protéger les cellules d'une feuille de calcul Excel ?
R : Aspose.Cells pour .NET est une bibliothèque puissante qui facilite le travail avec les fichiers Excel. Il offre des fonctionnalités avancées pour protéger les cellules, déverrouiller les plages, etc.

#### Q : Est-il possible de protéger des plages de cellules au lieu de cellules individuelles ?
 R : Oui, vous pouvez définir des plages de cellules spécifiques à protéger à l'aide de`ApplyStyle` méthode avec une méthode appropriée`StyleFlag`.

#### Q : Comment puis-je ouvrir le fichier Excel protégé après l'avoir enregistré ?
R : Lorsque vous ouvrez le fichier Excel protégé, vous devrez fournir le mot de passe spécifié lors de la protection de la feuille de calcul.

#### Q : Existe-t-il d'autres types de protection que je peux appliquer à une feuille de calcul Excel ?
: Oui, Aspose.Cells pour .NET prend en charge plusieurs types de protection, tels que la protection de la structure, la protection des fenêtres, etc. Vous pouvez choisir le type de protection approprié en fonction de vos besoins.