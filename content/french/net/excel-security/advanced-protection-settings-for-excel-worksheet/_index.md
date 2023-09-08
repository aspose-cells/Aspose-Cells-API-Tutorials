---
title: Paramètres de protection avancés pour la feuille de calcul Excel
linktitle: Paramètres de protection avancés pour la feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Protégez vos fichiers Excel en définissant des paramètres de protection avancés avec Aspose.Cells pour .NET.
type: docs
weight: 10
url: /fr/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
Dans ce didacticiel, nous vous guiderons à travers les étapes permettant de définir les paramètres de protection avancés pour une feuille de calcul Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Suivez les instructions ci-dessous pour terminer cette tâche.

## Étape 1 : Préparation

Assurez-vous d'avoir installé Aspose.Cells pour .NET et créé un projet C# dans votre environnement de développement intégré (IDE) préféré.

## Étape 2 : Définir le chemin du répertoire du document

 Déclarer un`dataDir` variable et initialisez-la avec le chemin d’accès à votre répertoire de documents. Par exemple :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENTS_DIRECTORY"` avec le chemin réel de votre répertoire.

## Étape 3 : Créez un flux de fichiers pour ouvrir le fichier Excel

 Créer un`FileStream` objet contenant le fichier Excel à ouvrir :

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Assurez-vous d'avoir le fichier Excel`book1.xls` dans votre répertoire de documents ou spécifiez le nom et l'emplacement corrects du fichier.

## Étape 4 : Instancier un objet Workbook et ouvrir le fichier Excel

 Utilisez le`Workbook`classe d'Aspose.Cells pour instancier un objet Workbook et ouvrir le fichier Excel spécifié via le flux de fichiers :

```csharp
Workbook excel = new Workbook(fstream);
```

## Étape 5 : Accédez à la première feuille de calcul

Accédez à la première feuille de calcul du fichier Excel :

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Étape 6 : Définir les paramètres de protection de la feuille de calcul

Utilisez les propriétés de l'objet Feuille de calcul pour définir les paramètres de protection de la feuille de calcul selon vos besoins. Par exemple :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Définissez d'autres paramètres de protection selon vos besoins...
```

## Étape 7 : Enregistrez le fichier Excel modifié

 Enregistrez le fichier Excel modifié à l'aide du`Save` méthode de l'objet Workbook :

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Assurez-vous de spécifier le chemin et le nom de fichier souhaités pour le fichier de sortie.

## Étape 8 : Fermez le flux de fichiers

Une fois enregistré, fermez le flux de fichiers pour libérer toutes les ressources associées :

```csharp
fstream.Close();
```
	
### Exemple de code source pour les paramètres de protection avancés pour la feuille de calcul Excel utilisant Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichiers contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel via le flux de fichiers
Workbook excel = new Workbook(fstream);
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = excel.Worksheets[0];
// Restreindre les utilisateurs à supprimer des colonnes de la feuille de calcul
worksheet.Protection.AllowDeletingColumn = false;
// Interdire aux utilisateurs de supprimer une ligne de la feuille de calcul
worksheet.Protection.AllowDeletingRow = false;
// Restreindre les utilisateurs à modifier le contenu de la feuille de calcul
worksheet.Protection.AllowEditingContent = false;
// Restreindre les utilisateurs à modifier les objets de la feuille de calcul
worksheet.Protection.AllowEditingObject = false;
// Restreindre les utilisateurs à modifier les scénarios de la feuille de calcul
worksheet.Protection.AllowEditingScenario = false;
//Restreindre les utilisateurs à filtrer
worksheet.Protection.AllowFiltering = false;
// Permettre aux utilisateurs de formater les cellules de la feuille de calcul
worksheet.Protection.AllowFormattingCell = true;
// Permettre aux utilisateurs de formater les lignes de la feuille de calcul
worksheet.Protection.AllowFormattingRow = true;
// Permettre aux utilisateurs d'insérer des colonnes dans la feuille de calcul
worksheet.Protection.AllowFormattingColumn = true;
// Permettre aux utilisateurs d'insérer des hyperliens dans la feuille de calcul
worksheet.Protection.AllowInsertingHyperlink = true;
// Permettre aux utilisateurs d'insérer des lignes dans la feuille de calcul
worksheet.Protection.AllowInsertingRow = true;
// Permettre aux utilisateurs de sélectionner des cellules verrouillées de la feuille de calcul
worksheet.Protection.AllowSelectingLockedCell = true;
// Permettre aux utilisateurs de sélectionner des cellules déverrouillées de la feuille de calcul
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Permettre aux utilisateurs de trier
worksheet.Protection.AllowSorting = true;
// Autoriser les utilisateurs à utiliser des tableaux croisés dynamiques dans la feuille de calcul
worksheet.Protection.AllowUsingPivotTable = true;
// Sauvegarde du fichier Excel modifié
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close();
```

## Conclusion

Félicitation ! Vous avez maintenant appris à définir les paramètres de protection avancés pour une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Utilisez ces connaissances pour sécuriser vos fichiers Excel et restreindre les actions des utilisateurs.

### FAQ

#### Q : Comment puis-je créer un nouveau projet C# dans mon IDE ?

R : Les étapes pour créer un nouveau projet C# peuvent varier en fonction de l'EDI que vous utilisez. Consultez la documentation de votre IDE pour des instructions détaillées.

#### Q : Est-il possible de définir des paramètres de protection personnalisés autres que ceux mentionnés dans le didacticiel ?

R : Oui, Aspose.Cells propose une large gamme de paramètres de protection que vous pouvez personnaliser en fonction de vos besoins spécifiques. Consultez la documentation Aspose.Cells pour plus de détails.

#### Q : Quel est le format de fichier utilisé pour enregistrer le fichier Excel modifié dans l’exemple de code ?

R : Dans l'exemple de code, le fichier Excel modifié est enregistré au format Excel 97-2003 (.xls). Vous pouvez choisir d'autres formats pris en charge par Aspose.Cells si nécessaire.

#### Q : Comment puis-je accéder à d’autres feuilles de calcul dans le fichier Excel ?

 R : Vous pouvez accéder à d'autres feuilles de calcul en utilisant l'index ou le nom de la feuille, par exemple :`Worksheet worksheet = excel.Worksheets[1];` ou`Worksheet worksheet = excel.Worksheets[" SheetName"];`.