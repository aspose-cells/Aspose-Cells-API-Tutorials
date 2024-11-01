---
title: Contrôler les ressources externes dans Excel en PDF dans Aspose.Cells
linktitle: Contrôler les ressources externes dans Excel en PDF dans Aspose.Cells
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment contrôler les ressources externes dans la conversion Excel en PDF à l'aide d'Aspose.Cells pour .NET avec notre guide facile à suivre.
type: docs
weight: 12
url: /fr/net/rendering-and-export/control-loading-of-external-resources/
---
## Introduction
À l'ère du numérique, la conversion de feuilles de calcul Excel en documents PDF est une tâche courante. Qu'il s'agisse de préparer des rapports, des données financières ou des supports de présentation, vous souhaitez vous assurer que vos PDF ressemblent exactement à ce que vous souhaitez. Aspose.Cells pour .NET est une bibliothèque robuste qui vous permet de contrôler ce processus de conversion dans les moindres détails, en particulier lors de la gestion de ressources externes telles que les images qui accompagnent vos fichiers Excel. Dans ce guide, nous expliquons comment contrôler les ressources externes pendant le processus de conversion d'Excel en PDF à l'aide d'Aspose.Cells. Alors, prenez votre boisson préférée et commençons !
## Prérequis
Avant de passer aux choses sérieuses, assurons-nous que vous disposez de tout ce dont vous avez besoin pour démarrer. Voici une liste de contrôle rapide :
1. Visual Studio ou tout autre IDE compatible .NET : vous aurez besoin d’un environnement pour écrire et tester votre code.
2.  Aspose.Cells pour .NET : si vous ne l'avez pas encore installé, rendez-vous sur le[Téléchargements Aspose](https://releases.aspose.com/cells/net/) page et récupérez la dernière version.
3. Connaissances de base de C# : une connaissance du langage de programmation C# sera utile. Si vous avez des doutes sur certains concepts, n'hésitez pas à les consulter.
4. Exemple de fichier Excel : préparez un fichier Excel avec toutes les ressources externes que vous souhaitez convertir. Vous pouvez utiliser le fichier d'exemple fourni « samplePdfSaveOptions_StreamProvider.xlsx ».
5. Un fichier image pour les tests : il sera utilisé comme ressource externe pendant la conversion. Le fichier image « newPdfSaveOptions_StreamProvider.png » est un bon espace réservé.
## Paquets d'importation
Pour commencer, vous devrez importer les espaces de noms nécessaires à partir de la bibliothèque Aspose.Cells. Cela est essentiel pour accéder à ses fonctionnalités. Assurez-vous d'ajouter les directives using suivantes en haut de votre fichier :
```csharp
using System.IO;
using System.Drawing;
using System.Drawing.Imaging;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using Aspose.Cells.Rendering;
using System;
```
Ces packages fourniront toutes les classes et méthodes essentielles dont vous aurez besoin pour effectuer vos tâches.
## Étape 1 : créez votre classe de fournisseur de flux
 La première étape consiste à créer une classe de fournisseur de flux qui implémente le`IStreamProvider` interface. Cette classe vous permettra de contrôler la manière dont les ressources externes sont chargées.
```csharp
class MyStreamProvider : IStreamProvider
{
    public void CloseStream(StreamProviderOptions options)
    {
        Debug.WriteLine("-----Close Stream-----");
    }
    public void InitStream(StreamProviderOptions options)
    {
        string sourceDir = "Your Document Directory";
        Debug.WriteLine("-----Init Stream-----");
        // Lire la nouvelle image dans un flux de mémoire et l'affecter à la propriété Stream
        byte[] bts = File.ReadAllBytes(sourceDir + "newPdfSaveOptions_StreamProvider.png");
        MemoryStream ms = new MemoryStream(bts);
        options.Stream = ms;
    }
}
```
Dans cette classe :
- CloseStream : cette méthode sera appelée lorsque le flux sera fermé. Pour l'instant, nous écrivons simplement un message de débogage pour le suivi.
-  InitStream : c'est ici que la magie commence. Ici, vous lirez votre image externe sous forme de tableau d'octets, la convertirez en flux mémoire et l'affecterez à`options.Stream` propriété.
## Étape 2 : Configurer les répertoires source et de sortie
Maintenant que votre fournisseur de flux est prêt, il est temps de déterminer où se trouve votre fichier Excel et où vous souhaitez enregistrer votre PDF.
```csharp
// Répertoire des sources
string sourceDir = "Your Document Directory";
// Répertoire de sortie
string outputDir = "Your Document Directory";
```
 Remplacez simplement`"Your Document Directory"` avec le chemin réel sur votre ordinateur où se trouvent vos fichiers. Garder vos fichiers organisés est essentiel !
## Étape 3 : Chargez votre fichier Excel
Ensuite, vous chargerez le fichier Excel à partir duquel vous souhaitez créer le PDF.
```csharp
// Charger le fichier source Excel contenant des images externes
Workbook wb = new Workbook(sourceDir + "samplePdfSaveOptions_StreamProvider.xlsx");
```
 Nous utilisons le`Workbook` classe de Aspose.Cells, qui représente votre fichier Excel. Le fichier peut inclure diverses ressources externes comme des images que vous souhaitez contrôler pendant la conversion.
## Étape 4 : définir les options d’enregistrement du PDF
Avant d'enregistrer le classeur au format PDF, vous devez spécifier comment vous souhaitez l'enregistrer. Vous pouvez ajuster ces options selon vos besoins.
```csharp
// Spécifier les options d'enregistrement PDF - Fournisseur de flux
PdfSaveOptions opts = new PdfSaveOptions();
opts.OnePagePerSheet = true; // Enregistrer chaque feuille sur une nouvelle page
```
 Ici, nous créons une nouvelle instance de`PdfSaveOptions` , qui vous permet de personnaliser la façon dont votre PDF sera formaté.`OnePagePerSheet`Cette option est pratique pour garantir que chaque feuille Excel obtienne sa propre page dans le PDF final.
## Étape 5 : Attribuez votre fournisseur de streaming
Une fois vos options PDF définies, vous devez indiquer à Aspose d'utiliser votre fournisseur de flux personnalisé pour les ressources externes.
```csharp
wb.Settings.StreamProvider = new MyStreamProvider();
```
 Cette ligne relie votre`Workbook` exemple avec le`MyStreamProvider` classe que vous avez créée précédemment. Cela signifie que chaque fois que des ressources externes sont rencontrées lors de la conversion, votre fournisseur les gérera comme spécifié.
## Étape 6 : Enregistrer le classeur au format PDF
Une fois tout configuré, il est enfin temps d'enregistrer votre classeur Excel au format PDF.
```csharp
// Enregistrer le classeur au format PDF
wb.Save(outputDir + "outputPdfSaveOptions_StreamProvider.pdf", opts);
```
 En appelant le`Save` en cliquant sur la méthode sur l'objet classeur et en transmettant votre répertoire de sortie avec les options PDF, vous convertissez le fichier Excel en un PDF magnifiquement formaté.
## Étape 7 : Confirmer l’exécution réussie
Pour conclure, c'est toujours agréable de confirmer que votre démarche a réussi !
```csharp
Console.WriteLine("ControlLoadingOfExternalResourcesInExcelToPDF executed successfully.\r\n");
```
L'affichage d'un message de réussite sur la console vous permet de rester informé de l'état de votre opération. C'est une bonne habitude d'inclure ces petites confirmations dans votre code.
## Conclusion
Et voilà ! En suivant ces étapes simples, vous pouvez contrôler de manière experte la manière dont les ressources externes sont gérées lors des conversions Excel en PDF à l'aide d'Aspose.Cells. Cela signifie que vos documents peuvent désormais inclure des images et d'autres éléments externes avec précision, garantissant ainsi un produit final soigné à chaque fois.
## FAQ
### Qu'est-ce qu'Aspose.Cells ?  
Aspose.Cells est une bibliothèque puissante pour les développeurs .NET qui vous permet de créer, manipuler, convertir et restituer des fichiers Excel dans divers formats.
### Comment télécharger Aspose.Cells ?  
 Vous pouvez télécharger la dernière version d'Aspose.Cells à partir du[Lien de téléchargement](https://releases.aspose.com/cells/net/).
### Puis-je essayer Aspose.Cells gratuitement ?  
 Oui ! Vous pouvez obtenir un essai gratuit en visitant le[Page d'essai gratuite](https://releases.aspose.com/).
### Où puis-je trouver du support pour Aspose.Cells ?  
 Pour toute question relative au support, vous pouvez visiter le[Forum d'assistance Aspose](https://forum.aspose.com/c/cells/9).
### Comment puis-je obtenir une licence temporaire pour Aspose.Cells ?  
 Vous pouvez demander une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).