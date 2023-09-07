---
title: Protéger la feuille de calcul Excel
linktitle: Protéger la feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez dans ce tutoriel comment protéger une feuille de calcul Excel en utilisant Aspose.Cells pour .NET. Guide pas à pas en C#.
type: docs
weight: 50
url: /fr/net/protect-excel-file/protect-excel-worksheet/
---
Dans ce didacticiel, nous examinerons du code source C # qui utilise la bibliothèque Aspose.Cells pour protéger une feuille de calcul Excel. Nous allons parcourir chaque étape du code et expliquer comment cela fonctionne. Assurez-vous de suivre attentivement les instructions pour obtenir les résultats souhaités.

## Étape 1 : Prérequis

Avant de commencer, assurez-vous d'avoir installé la bibliothèque Aspose.Cells pour .NET. Vous pouvez l'obtenir sur le site officiel d'Aspose. Assurez-vous également que vous disposez d'une version récente de Visual Studio ou de tout autre environnement de développement C#.

## Étape 2 : Importer les espaces de noms requis

Pour utiliser la bibliothèque Aspose.Cells, nous devons importer les espaces de noms nécessaires dans notre code. Ajoutez les lignes suivantes en haut de votre fichier source C# :

```csharp
using Aspose.Cells;
using System.IO;
```

## Étape 3 : Chargez le fichier Excel

Dans cette étape, nous allons charger le fichier Excel que nous voulons protéger. Assurez-vous de spécifier le chemin d'accès correct au répertoire contenant le fichier Excel. Utilisez le code suivant pour télécharger le fichier :

```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Créez un flux de fichiers contenant le fichier Excel à ouvrir.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Instanciez un objet Workbook.
//Ouvrez le fichier Excel via le flux de fichiers.
Workbook excel = new Workbook(fstream);
```

 Assurez-vous de remplacer`"YOUR_DOCUMENTS_DIR"` avec le chemin approprié vers votre répertoire de documents.

## Étape 4 : Accéder à la feuille de calcul

Maintenant que nous avons chargé le fichier Excel, nous pouvons accéder à la première feuille de calcul. Utilisez le code suivant pour accéder à la première feuille de calcul :

```csharp
// Accès à la première feuille de calcul du fichier Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Étape 5 : Protégez la feuille de calcul

Dans cette étape, nous allons protéger la feuille de calcul à l'aide d'un mot de passe. Utilisez le code suivant pour protéger la feuille de calcul :

```csharp
// Protégez la feuille de calcul avec un mot de passe.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Remplacer`"YOUR_PASSWORD"` avec le mot de passe que vous souhaitez utiliser pour protéger la feuille de calcul.

## Étape 6 : Enregistrer le fichier Excel modifié Maintenant que nous avons protégé

é la feuille de calcul, nous enregistrerons le fichier Excel modifié dans le format par défaut. Utilisez le code suivant pour enregistrer le fichier Excel :

```csharp
// Enregistrez le fichier Excel modifié dans le format par défaut.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Assurez-vous de spécifier le chemin d'accès correct pour enregistrer le fichier Excel modifié.

## Étape 7 : Fermer le flux de fichiers

Pour libérer toutes les ressources, nous devons fermer le flux de fichiers utilisé pour charger le fichier Excel. Utilisez le code suivant pour fermer le flux de fichiers :

```csharp
// Fermez le flux de fichiers pour libérer toutes les ressources.
fstream.Close();
```

Assurez-vous d'inclure cette étape à la fin de votre code.


### Exemple de code source pour protéger la feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichier contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel via le flux de fichiers
Workbook excel = new Workbook(fstream);
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = excel.Worksheets[0];
// Protéger la feuille de calcul avec un mot de passe
worksheet.Protect(ProtectionType.All, "aspose", null);
// Enregistrement du fichier Excel modifié au format par défaut
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close();
```

## Conclusion

Félicitation ! Vous disposez maintenant d'un code source C# qui vous permet de protéger une feuille de calcul Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Assurez-vous de suivre attentivement les étapes et de personnaliser le code en fonction de vos besoins spécifiques.

### FAQ (Foire Aux Questions)

#### Est-il possible de protéger plusieurs feuilles de calcul dans un seul fichier Excel ?

R : Oui, vous pouvez protéger plusieurs feuilles de calcul dans un seul fichier Excel en répétant les étapes 4 à 6 pour chaque feuille de calcul.

#### Comment puis-je spécifier des autorisations spécifiques pour les utilisateurs autorisés ?

 R : Vous pouvez utiliser les options supplémentaires fournies par le`Protect`méthode pour spécifier des autorisations spécifiques pour les utilisateurs autorisés. Voir la documentation Aspose.Cells pour plus d'informations.

#### Puis-je protéger le fichier Excel lui-même avec un mot de passe ?

R : Oui, vous pouvez protéger par mot de passe le fichier Excel lui-même en utilisant d'autres méthodes fournies par la bibliothèque Aspose.Cells. Veuillez vous référer à la documentation pour des exemples spécifiques.

#### La bibliothèque Aspose.Cells prend-elle en charge d'autres formats de fichiers Excel ?

R : Oui, la bibliothèque Aspose.Cells prend en charge une large gamme de formats de fichiers Excel, notamment XLSX, XLSM, XLSB, CSV, etc.