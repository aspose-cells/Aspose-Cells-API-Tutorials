---
title: Autoriser l'apostrophe principale
linktitle: Autoriser l'apostrophe principale
second_title: Référence de l'API Aspose.Cells pour .NET
description: Autoriser les apostrophes de début dans les classeurs Excel avec Aspose.Cells pour .NET.
type: docs
weight: 60
url: /fr/net/excel-workbook/allow-leading-apostrophe/
---
Dans ce didacticiel étape par étape, nous expliquerons le code source C# fourni qui vous permettra d'autoriser l'utilisation d'une apostrophe de début dans un classeur Excel à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour effectuer cette opération.

## Étape 1 : Définir les répertoires source et de sortie

```csharp
// répertoire source
string sourceDir = RunExamples.Get_SourceDirectory();
// Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
```

Dans cette première étape, nous définissons les répertoires source et de sortie des fichiers Excel.

## Étape 2 : instancier un objet WorkbookDesigner

```csharp
// Instancier un objet WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Nous créons une instance du`WorkbookDesigner` classe d’Aspose.Cells.

## Étape 3 : Charger le classeur Excel

```csharp
// Charger le classeur Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Nous chargeons le classeur Excel à partir du fichier spécifié et désactivons la conversion automatique des apostrophes initiales en style de texte.

## Étape 4 : Définir la source de données

```csharp
// Définir la source de données pour le classeur du concepteur
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Nous définissons une liste d'objets de données et utilisons le`SetDataSource` méthode pour définir la source de données pour le classeur du concepteur.

## Étape 5 : Traiter les marqueurs intelligents

```csharp
// Traiter les marqueurs intelligents
designer. Process();
```

 Nous utilisons le`Process` méthode pour traiter les marqueurs intelligents dans le classeur du concepteur.

## Étape 6 : Enregistrez le classeur Excel modifié

```csharp
// Enregistrez le classeur Excel modifié
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Nous enregistrons le classeur Excel modifié avec les modifications apportées.

### Exemple de code source pour Autoriser l’apostrophe principale à l’aide d’Aspose.Cells pour .NET 
```csharp
//Répertoire source
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Instanciation d'un objet WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Ouvrir une feuille de calcul de concepteur contenant des marqueurs intelligents
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Définir la source de données pour la feuille de calcul du concepteur
designer.SetDataSource("sampleData", list);
// Traiter les marqueurs intelligents
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Conclusion

Félicitation ! Vous avez appris à autoriser l’utilisation d’une apostrophe de début dans un classeur Excel à l’aide d’Aspose.Cells pour .NET. Expérimentez avec vos propres données pour personnaliser davantage vos classeurs Excel.

### FAQ

#### Q : Qu'est-ce que l'autorisation d'apostrophe principale dans un classeur Excel ?

R : Autoriser l'apostrophe initiale dans un classeur Excel permet aux données commençant par une apostrophe de s'afficher correctement sans les convertir en style de texte. Ceci est utile lorsque vous souhaitez conserver l’apostrophe dans les données.

#### Q : Pourquoi dois-je désactiver la conversion automatique des apostrophes initiales ?

R : En désactivant la conversion automatique des guillemets principaux, vous pouvez conserver leur utilisation telle quelle dans vos données. Cela évite toute modification involontaire des données lors de l'ouverture ou de la manipulation du classeur Excel.

#### Q : Comment définir la source de données dans le classeur du concepteur ?

 R : Pour définir la source de données dans le classeur du concepteur, vous pouvez utiliser l'outil`SetDataSource` méthode spécifiant le nom de la source de données et une liste d’objets de données correspondants.

#### Q : Autoriser l'apostrophe de début affecte-t-il les autres données du classeur Excel ?

R : Non, autoriser l'apostrophe initiale n'affecte que les données commençant par une apostrophe. Les autres données du classeur Excel restent inchangées.

#### Q : Puis-je utiliser cette fonctionnalité avec d’autres formats de fichiers Excel ?

R : Oui, vous pouvez utiliser cette fonctionnalité avec d'autres formats de fichiers Excel pris en charge par Aspose.Cells, tels que .xls, .xlsm, etc.