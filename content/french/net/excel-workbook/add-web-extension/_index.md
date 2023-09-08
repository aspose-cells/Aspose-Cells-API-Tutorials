---
title: Ajouter une extension Web
linktitle: Ajouter une extension Web
second_title: Référence de l'API Aspose.Cells pour .NET
description: Ajoutez facilement une extension Web à vos classeurs Excel avec Aspose.Cells pour .NET.
type: docs
weight: 40
url: /fr/net/excel-workbook/add-web-extension/
---
Dans ce didacticiel étape par étape, nous expliquerons le code source C# fourni qui vous permettra d'ajouter une extension Web à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour ajouter une extension Web à votre classeur Excel.

## Étape 1 : Définir le répertoire de sortie

```csharp
// Répertoire de sortie
string outDir = RunExamples.Get_OutputDirectory();
```

Dans cette première étape, nous définissons le répertoire de sortie dans lequel le classeur Excel modifié sera enregistré.

## Étape 2 : Créer un nouveau classeur

```csharp
// Créer un nouveau classeur
Workbook workbook = new Workbook();
```

Ici, nous créons un nouveau classeur Excel en utilisant le`Workbook` classe d’Aspose.Cells.

## Étape 3 : Accédez à la collection d'extensions Web

```csharp
// Accédez à la collection d'extensions Web
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Nous accédons à la collection d'extensions Web du classeur Excel à l'aide du`WebExtensions` propriété du`Worksheets` objet.

## Étape 4 : Ajouter une nouvelle extension Web

```csharp
// Ajouter une nouvelle extension Web
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Nous ajoutons une nouvelle extension Web à la collection d'extensions. Nous définissons l'ID de référence, le nom du magasin et le type de magasin de l'extension.

## Étape 5 : accéder à la collection de volets de tâches de l'extension Web

```csharp
// Accéder à la collection de volets de tâches de l'extension Web
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Nous accédons à la collection de volets de tâches Excel Workbook Web Extension à l'aide du`WebExtensionTaskPanes` propriété du`Worksheets` objet.

## Étape 6 : Ajouter un nouveau volet de tâches

```csharp
// Ajouter un nouveau volet de tâches
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Nous ajoutons un nouveau volet de tâches à la collection de volets de tâches. Nous définissons la visibilité du volet, son état d'ancrage et l'extension Web associée.

## Étape 7 : Enregistrez et fermez le classeur

```csharp
// Enregistrez et fermez le classeur
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Nous enregistrons le classeur modifié dans le répertoire de sortie spécifié, puis le fermons.

### Exemple de code source pour ajouter une extension Web à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire source
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Conclusion

Félicitation ! Vous avez maintenant appris à ajouter une extension Web à l'aide d'Aspose.Cells pour .NET. Expérimentez avec le code et explorez les fonctionnalités supplémentaires d'Aspose.Cells pour tirer le meilleur parti de la manipulation des extensions Web dans vos classeurs Excel.

## FAQ

#### Q : Qu'est-ce qu'une extension Web dans un classeur Excel ?

R : Une extension Web dans un classeur Excel est un composant qui vous permet d'ajouter des fonctionnalités supplémentaires à Excel en intégrant des applications Web. Il peut offrir des fonctionnalités interactives, des tableaux de bord personnalisés, des intégrations externes, etc.

#### Q : Comment ajouter une extension Web au classeur Excel avec Aspose.Cells ?

 R : Pour ajouter une extension Web à un classeur Excel avec Aspose.Cells, vous pouvez suivre les étapes fournies dans notre guide étape par étape. Utilisez le`WebExtensionCollection` et`WebExtensionTaskPaneCollection` classes pour ajouter et configurer l’extension Web et le volet des tâches associé.

#### Q : Quelles informations sont requises pour ajouter une extension Web ?

R : Lors de l'ajout d'une extension Web, vous devez fournir l'ID SKU de l'extension, le nom du magasin et le type de magasin. Ces informations permettent d’identifier et de charger correctement l’extension.

#### Q : Puis-je ajouter plusieurs extensions Web à un seul classeur Excel ?

 R : Oui, vous pouvez ajouter plusieurs extensions Web à un seul classeur Excel. Utilisez le`Add` méthode de la collection d'extensions Web pour ajouter chaque extension, puis les associer aux volets de tâches correspondants.