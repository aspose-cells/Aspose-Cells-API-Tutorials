---
title: Spécification de la version du document d'un fichier Excel par programmation dans .NET
linktitle: Spécification de la version du document d'un fichier Excel par programmation dans .NET
second_title: API de traitement Excel Aspose.Cells .NET
description: Découvrez comment spécifier les propriétés d'un document, telles que la version, l'auteur et le titre dans un fichier Excel par programmation à l'aide d'Aspose.Cells pour .NET avec des instructions étape par étape.
type: docs
weight: 12
url: /fr/net/saving-and-exporting-excel-files-with-options/specifying-document-version-of-excel-file/
---
## Introduction
Aspose.Cells pour .NET est une bibliothèque puissante qui permet aux développeurs de manipuler facilement des fichiers Excel par programmation. Que vous souhaitiez créer des fichiers Excel à partir de zéro ou modifier des fichiers existants, Aspose.Cells propose une API complète pour atteindre vos objectifs. L'une de ces fonctionnalités consiste à spécifier les propriétés du document telles que la version, l'auteur ou le titre. Ce didacticiel vous explique comment spécifier la version du document d'un fichier Excel par programmation à l'aide d'Aspose.Cells pour .NET.
## Prérequis
Avant de plonger dans les détails, assurons-nous que vous disposez de tout ce dont vous avez besoin pour suivre ce tutoriel :
1.  Aspose.Cells pour .NET : vous pouvez télécharger la dernière version[ici](https://releases.aspose.com/cells/net/) . Si vous n'avez pas encore acheté de licence, vous pouvez opter pour une[permis temporaire](https://purchase.aspose.com/temporary-license/) pour explorer les fonctionnalités.
2. Environnement de développement .NET : vous pouvez utiliser Visual Studio ou tout autre IDE compatible .NET.
3. Connaissances de base de C# : la compréhension de la programmation C# facilitera le suivi.
## Paquets d'importation
Avant de pouvoir commencer à coder, vous devez importer les espaces de noms nécessaires à partir de la bibliothèque Aspose.Cells. Cela vous donnera accès aux classes et méthodes requises pour la manipulation des fichiers Excel.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
Ces deux espaces de noms seront essentiels pour interagir avec le classeur et ses propriétés de document intégrées.
Maintenant, décomposons le processus de spécification des propriétés du document dans un fichier Excel, y compris la version, le titre et l'auteur.
## Étape 1 : Initialiser l’objet classeur
 La première étape consiste à créer une nouvelle instance de`Workbook` objet. Cet objet représente l'intégralité du fichier Excel avec lequel vous allez travailler.
```csharp
Workbook wb = new Workbook();
```
 Le`Workbook` La classe fournit une représentation d'un fichier Excel. En l'instanciant, nous créons un classeur Excel vierge que nous pouvons manipuler.
## Étape 2 : Accéder aux propriétés de document intégrées
Aspose.Cells propose des propriétés de document intégrées, qui incluent des champs tels que le titre, l'auteur et la version du document. Vous pouvez accéder à ces propriétés via le`BuiltInDocumentProperties`collection.
```csharp
Aspose.Cells.Properties.BuiltInDocumentPropertyCollection bdpc = wb.BuiltInDocumentProperties;
```
 Le`BuiltInDocumentPropertyCollection` La classe donne accès à une collection de propriétés de document intégrées, telles que le titre, l'auteur et d'autres métadonnées généralement associées au document.
## Étape 3 : définir le titre du document Excel
Ensuite, nous allons définir le titre du document Excel. Ces métadonnées permettent d'identifier et de gérer le fichier ultérieurement.
```csharp
bdpc.Title = "Aspose File Format APIs";
```
La définition du titre est importante pour l'organisation du document. Ces métadonnées sont visibles dans les propriétés du fichier et peuvent être utilisées par des systèmes externes pour cataloguer ou identifier le document plus efficacement.
## Étape 4 : Spécifier l'auteur
L'auteur du document peut également être spécifié pour refléter qui a créé ou modifié le fichier.
```csharp
bdpc.Author = "Aspose APIs Developers";
```
Cette étape permet d’attribuer le document à son créateur, en fournissant des métadonnées supplémentaires pour la gestion des documents ou les scénarios de collaboration.
## Étape 5 : Spécifier la version du document
L'une des propriétés les plus importantes que nous abordons dans ce didacticiel est la version du document. Cette étape vous permet de spécifier la version du document, ce qui est utile lorsque vous travaillez dans des environnements qui nécessitent un contrôle de version.
```csharp
bdpc.DocumentVersion = "Aspose.Cells Version - 18.3";
```
La définition de la version du document permet de savoir clairement quelle version du document ou de la bibliothèque a été utilisée pour créer le fichier. Cela est particulièrement important dans les environnements qui doivent suivre les révisions de fichiers ou la compatibilité avec différentes versions de bibliothèque.
## Étape 6 : Enregistrez le fichier Excel
 Enfin, vous pouvez enregistrer le fichier Excel avec toutes les propriétés que vous venez de définir. Aspose.Cells vous permet d'enregistrer le fichier dans différents formats, mais pour cet exemple, nous nous en tiendrons au format`.xlsx` format.
```csharp
wb.Save("outputSpecifyDocumentVersionOfExcelFile.xlsx", SaveFormat.Xlsx);
```
 Le`Save` La méthode est utilisée pour enregistrer le fichier dans le répertoire spécifié. Ici, nous l'enregistrons sous forme de fichier Excel dans le`.xlsx` format. Si nécessaire, Aspose.Cells prend également en charge des formats tels que`.xls`, `.csv` , et`.pdf`, offrant une flexibilité en fonction des besoins de votre projet.
## Conclusion
Dans ce didacticiel, nous avons expliqué comment spécifier les propriétés d'un document, en particulier la version du document, dans un fichier Excel à l'aide d'Aspose.Cells pour .NET. Aspose.Cells est un outil extrêmement flexible et puissant qui vous permet de manipuler des fichiers Excel par programmation, ce qui en fait un atout précieux pour tout développeur .NET travaillant avec des feuilles de calcul.
## FAQ
### Puis-je modifier d’autres propriétés intégrées à l’aide d’Aspose.Cells ?  
Oui, vous pouvez modifier d’autres propriétés intégrées telles que le sujet, les mots-clés et les commentaires, entre autres.
### Quels formats de fichiers sont pris en charge par Aspose.Cells ?  
 Aspose.Cells prend en charge une grande variété de formats, notamment`.xls`, `.xlsx`, `.csv`, `.pdf`, et plus encore.
### Ai-je besoin d'une licence pour utiliser Aspose.Cells pour .NET ?  
 Vous pouvez explorer Aspose.Cells avec un[essai gratuit](https://releases.aspose.com/) ou postulez pour un[permis temporaire](https://purchase.aspose.com/temporary-license/) pour des tests prolongés.
### Puis-je utiliser Aspose.Cells dans une application Web ?  
Oui, Aspose.Cells peut être utilisé à la fois dans des applications de bureau et sur le Web. Il est très polyvalent et s'intègre parfaitement aux frameworks Web .NET.
### Où puis-je obtenir de l'aide pour Aspose.Cells ?  
 Vous pouvez accéder à la communauté et au soutien via le[Forum d'assistance Aspose.Cells](https://forum.aspose.com/c/cells/9).