---
title: Insérer une image dans l'en-tête
linktitle: Insérer une image dans l'en-tête
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à insérer une image dans l'en-tête ou le pied de page d'un document Excel à l'aide d'Aspose.Cells pour .NET. Guide étape par étape avec code source en C#.
type: docs
weight: 60
url: /fr/net/excel-page-setup/insert-image-in-header-footer/
---
La possibilité d'insérer une image dans l'en-tête ou le pied de page d'un document Excel peut être très utile pour personnaliser vos rapports ou ajouter des logos d'entreprise. Dans cet article, nous vous guiderons pas à pas pour insérer une image dans l'en-tête ou le pied de page d'un document Excel en utilisant Aspose.Cells pour .NET. Vous apprendrez comment y parvenir en utilisant le code source C#.

## Étape 1 : Configurer l'environnement

Avant de commencer, assurez-vous que Aspose.Cells pour .NET est installé sur votre machine. Créez également un nouveau projet dans votre environnement de développement préféré.

## Étape 2 : Importer les bibliothèques nécessaires

Dans votre fichier de code, importez les bibliothèques nécessaires pour travailler avec Aspose.Cells. Voici le code correspondant :

```csharp
using Aspose.Cells;
```

## Étape 3 : Définir le répertoire de documents

Définissez le répertoire dans lequel se trouve le document Excel avec lequel vous souhaitez travailler. Utilisez le code suivant pour définir le répertoire :

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Assurez-vous de spécifier le chemin d'accès complet au répertoire.

## Étape 4 : Création d'un objet de classeur

L'objet Workbook représente le document Excel avec lequel vous allez travailler. Vous pouvez le créer en utilisant le code suivant :

```csharp
Workbook workbook = new Workbook();
```

Cela crée un nouvel objet Workbook vide.

## Étape 5 : Stocker l'URL de l'image

Définissez l'URL ou le chemin de l'image que vous souhaitez insérer dans l'en-tête ou le pied de page. Utilisez le code suivant pour stocker l'URL de l'image :

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Assurez-vous que le chemin spécifié est correct et que l'image existe à cet emplacement.

## Étape 6 : Ouverture du fichier image

Pour ouvrir le fichier image, nous allons utiliser un objet FileStream et lire les données binaires de l'image. Voici le code correspondant :

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Assurez-vous que le chemin de l'image est correct et que vous disposez des autorisations appropriées pour y accéder.

## Étape 7 : Configuration de la configuration de la page

L'objet PageSetup est utilisé pour définir les paramètres de page du document Excel, y compris l'en-tête et le pied de page. Utilisez le code suivant pour obtenir l'objet PageSetup de la première feuille de calcul :

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Cela vous permettra d'accéder aux paramètres de page pour la première feuille de calcul du classeur.

## Étape 8 : Ajouter l'image à l'en-tête

Utilisez la méthode SetHeaderPicture() de l'objet PageSetup pour définir l'image dans la section centrale de l'en-tête de page. Voici le code correspondant :

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Cela ajoutera l'image spécifiée à l'en-tête de la page.

## Étape 9 : Ajouter un script à l'en-tête

Pour ajouter un script à l'en-tête de page, utilisez la méthode SetHeader() de l'objet PageSetup. Voici le code correspondant :

```csharp
pageSetup.SetHeader(1, "&G");
```

Cela ajoutera le script spécifié à l'en-tête de la page. Dans cet exemple, le script "&G" affiche le numéro de page.

## Étape 10 : Ajouter le nom de la feuille à l'en-tête

Pour afficher le nom de la feuille dans l'en-tête de page, utilisez à nouveau la méthode SetHeader() de l'objet PageSetup. Voici le code correspondant :

```csharp
pageSetup.SetHeader(2, "&A");
```

Cela ajoutera le nom de la feuille à l'en-tête de la page. Le script "&A" est utilisé pour représenter le nom de la feuille.

## Étape 11 : Enregistrer le classeur

Pour enregistrer les modifications apportées au classeur, utilisez la méthode Save() de l'objet Workbook. Voici le code correspondant :

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Cela enregistrera le classeur avec les modifications dans le répertoire spécifié.

## Étape 12 : Fermeture du FileStream

Après avoir lu les données binaires de l'image, assurez-vous de fermer le FileStream pour libérer les ressources. Utilisez le code suivant pour fermer le FileStream :

```csharp
inFile.Close();
```

Assurez-vous de toujours fermer FileStreams lorsque vous avez fini de les utiliser.

### Exemple de code source pour Insérer une image dans l'en-tête de pied de page à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Création d'un objet Workbook
Workbook workbook = new Workbook();
// Création d'une variable de chaîne pour stocker l'url du logo/image
string logo_url = dataDir + "aspose-logo.jpg";
// Déclarer un objet FileStream
FileStream inFile;
// Déclarer un tableau d'octets
byte[] binaryData;
// Création de l'instance de l'objet FileStream pour ouvrir le logo/l'image dans le flux
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Instanciation du tableau d'octets de la taille de l'objet FileStream
binaryData = new Byte[inFile.Length];
// Lit un bloc d'octets à partir du flux et écrit des données dans un tampon donné de tableau d'octets.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Création d'un objet PageSetup pour obtenir les paramètres de page de la première feuille de calcul du classeur
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Réglage du logo/image dans la section centrale de l'en-tête de page
pageSetup.SetHeaderPicture(1, binaryData);
// Définition du script pour le logo/l'image
pageSetup.SetHeader(1, "&G");
// Définir le nom de la feuille dans la section droite de l'en-tête de page avec le script
pageSetup.SetHeader(2, "&A");
// Enregistrement du classeur
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Fermeture de l'objet FileStream
inFile.Close();       
```
## Conclusion

Félicitation ! Vous savez maintenant comment insérer une image dans l'en-tête ou le pied de page d'un document Excel à l'aide d'Aspose.Cells pour .NET. Ce didacticiel vous a guidé à chaque étape du processus, de la configuration de l'environnement à l'enregistrement du classeur modifié. N'hésitez pas à expérimenter davantage les fonctionnalités d'Aspose.Cells pour créer des documents Excel personnalisés et professionnels.

### FAQ

#### Q1 : Est-il possible d'insérer plusieurs images dans l'en-tête ou le pied de page d'un document Excel ?

R1 : Oui, vous pouvez insérer plusieurs images dans l'en-tête ou le pied de page d'un document Excel en répétant les étapes 8 et 9 pour chaque image supplémentaire.

#### Q2 : Quels formats d'image sont pris en charge pour l'insertion dans l'en-tête ou le pied de page ?
A2 : Aspose.Cells prend en charge une variété de formats d'image courants tels que JPEG, PNG, GIF, BMP, etc.

#### Q3 : Puis-je personnaliser davantage l'apparence de l'en-tête ou du pied de page ?

R3 : Oui, vous pouvez utiliser des scripts et des codes spéciaux pour formater et personnaliser davantage l'apparence de l'en-tête ou du pied de page. Reportez-vous à la documentation Aspose.Cells pour plus d'informations sur les options de personnalisation.

#### Q4 : Aspose.Cells fonctionne-t-il avec différentes versions d'Excel ?

R4 : Oui, Aspose.Cells est compatible avec différentes versions d'Excel, notamment Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 et Excel 2019.

#### Q5 : Est-il possible d'insérer des images dans d'autres parties du document Excel, telles que des cellules ou des graphiques ?

A5 : Oui, Aspose.Cells fournit des fonctionnalités étendues pour insérer des images dans différentes parties du document Excel, y compris des cellules, des graphiques et des objets de dessin.