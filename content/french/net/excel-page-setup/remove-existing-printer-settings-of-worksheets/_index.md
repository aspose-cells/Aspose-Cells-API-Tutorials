---
title: Supprimer les paramètres d'imprimante existants des feuilles de calcul
linktitle: Supprimer les paramètres d'imprimante existants des feuilles de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment supprimer les paramètres d'imprimante existants des feuilles de calcul Excel avec Aspose.Cells pour .NET.
type: docs
weight: 80
url: /fr/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
Dans ce didacticiel, nous vous expliquerons étape par étape comment supprimer les paramètres d'imprimante existants des feuilles de calcul dans Excel à l'aide d'Aspose.Cells pour .NET. Nous utiliserons le code source C# pour illustrer le processus.

## Étape 1 : Configuration de l'environnement

Assurez-vous que Aspose.Cells pour .NET est installé sur votre ordinateur. Créez également un nouveau projet dans votre environnement de développement préféré.

## Étape 2 : Importer les bibliothèques nécessaires

Dans votre fichier de code, importez les bibliothèques nécessaires pour travailler avec Aspose.Cells. Voici le code correspondant :

```csharp
using Aspose.Cells;
```

## Étape 3 : Définir les répertoires source et de sortie

Définissez respectivement les répertoires source et de sortie où se trouve le fichier Excel d'origine et où vous souhaitez enregistrer le fichier modifié. Utilisez le code suivant :

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Assurez-vous de spécifier les chemins de répertoire complets.

## Étape 4 : Chargement du fichier Excel source

Chargez le fichier Excel source à l'aide du code suivant :

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Cela chargera le fichier Excel spécifié dans l'objet Workbook.

## Étape 5 : Parcourir les feuilles de calcul

Parcourez toutes les feuilles de calcul du classeur à l’aide d’une boucle. Utilisez le code suivant :

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Le reste du code sera ajouté à l'étape suivante.
}
```

## Étape 6 : Supprimer les paramètres d'imprimante existants

Vérifiez si les paramètres d'imprimante existent pour chaque feuille de calcul et supprimez-les si nécessaire. Utilisez le code suivant :

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Étape 7 : enregistrement du classeur modifié

Enregistrez le classeur modifié à l'aide du code suivant :

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Cela enregistrera le classeur modifié dans le répertoire de sortie spécifié.

### Exemple de code source pour supprimer les paramètres d'imprimante existants des feuilles de calcul à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire source
string sourceDir = RunExamples.Get_SourceDirectory();
//Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
//Charger le fichier Excel source
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Obtenez le nombre de feuilles du classeur
int sheetCount = wb.Worksheets.Count;
//Itérer toutes les feuilles
for (int i = 0; i < sheetCount; i++)
{
    //Accéder à la ième feuille de calcul
    Worksheet ws = wb.Worksheets[i];
    //Accéder à la configuration de la page de la feuille de calcul
    PageSetup ps = ws.PageSetup;
    //Vérifiez si les paramètres d'imprimante pour cette feuille de calcul existent
    if (ps.PrinterSettings != null)
    {
        //Imprimez le message suivant
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Imprimer le nom de la feuille et son format de papier
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Supprimez les paramètres de l'imprimante en les définissant sur null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//si
}//pour
//Enregistrez le classeur
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Conclusion

Vous avez maintenant appris à supprimer les paramètres d'imprimante existants des feuilles de calcul dans Excel à l'aide d'Aspose.Cells pour .NET. Ce didacticiel vous a guidé à travers chaque étape du processus, de la configuration de l'environnement à la navigation dans les feuilles de calcul et à la suppression des paramètres de l'imprimante. Vous pouvez désormais utiliser ces connaissances pour gérer les paramètres de l'imprimante dans vos fichiers Excel.

### FAQ

#### Q1 : Comment puis-je savoir si une feuille de calcul comporte des paramètres d'imprimante existants ?

 A1 : Vous pouvez vérifier si les paramètres d'imprimante existent pour une feuille de calcul en accédant au`PrinterSettings` propriété du`PageSetup` objet. Si la valeur n'est pas nulle, cela signifie qu'il existe des paramètres d'imprimante existants.

#### Q2 : Puis-je supprimer les paramètres de l'imprimante pour une feuille de calcul spécifique uniquement ?

 A2 : Oui, vous pouvez utiliser la même approche pour supprimer les paramètres d'imprimante d'une feuille de calcul spécifique en accédant aux paramètres de cette feuille de calcul.`PageSetup` objet.

#### Q3 : Cette méthode supprime-t-elle également d'autres paramètres de mise en page ?

A3 : Non, cette méthode supprime uniquement les paramètres de l'imprimante. Les autres paramètres de mise en page, tels que les marges, l'orientation du papier, etc., restent inchangés.

#### Q4 : Cette méthode fonctionne-t-elle pour tous les formats de fichiers Excel, tels que .xls et .xlsx ?

A4 : Oui, cette méthode fonctionne pour tous les formats de fichiers Excel pris en charge par Aspose.Cells, y compris .xls et .xlsx.

#### Q5 : Les modifications apportées aux paramètres de l'imprimante sont-elles permanentes dans le fichier Excel modifié ?

A5 : Oui, les modifications apportées aux paramètres de l'imprimante sont enregistrées de manière permanente dans le fichier Excel modifié.