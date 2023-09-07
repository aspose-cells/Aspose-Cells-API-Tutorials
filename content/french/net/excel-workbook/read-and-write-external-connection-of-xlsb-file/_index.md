---
title: Lire et écrire la connexion externe du fichier XLSB
linktitle: Lire et écrire la connexion externe du fichier XLSB
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à lire et à modifier les connexions externes d'un fichier XLSB à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 130
url: /fr/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
La lecture et l'écriture de connexions externes à un fichier XLSB sont essentielles pour manipuler des données provenant de sources externes dans vos classeurs Excel. Avec Aspose.Cells pour .NET, vous pouvez facilement lire et écrire des connexions externes en procédant comme suit :

## Étape 1 : Spécifiez le répertoire source et le répertoire de sortie

Vous devez d'abord spécifier le répertoire source où se trouve le fichier XLSB contenant la connexion externe, ainsi que le répertoire de sortie où vous souhaitez enregistrer le fichier modifié. Voici comment procéder avec Aspose.Cells :

```csharp
// répertoire des sources
string sourceDir = RunExamples.Get_SourceDirectory();

// Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
```

## Étape 2 : Chargez le fichier Excel XLSB source

Ensuite, vous devez charger le fichier Excel XLSB source sur lequel vous souhaitez effectuer des opérations de lecture et d'écriture de connexion externe. Voici un exemple de code :

```csharp
// Charger le fichier Excel XLSB source
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Étape 3 : Lire et modifier la connexion externe

Après avoir chargé le fichier, vous pouvez accéder à la première connexion externe qui est en fait une connexion à la base de données. Vous pouvez lire et modifier diverses propriétés de la connexion externe. Voici comment:

```csharp
// Lire la première connexion externe qui est une connexion à la base de données
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Afficher le nom de la connexion à la base de données, la commande et les informations de connexion
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Modifier le nom de la connexion
dbCon.Name = "NewCustomer";
```

## Étape 4 : Enregistrez le fichier Excel XLSB de sortie

Une fois que vous avez apporté les modifications nécessaires, vous pouvez enregistrer le fichier Excel XLSB modifié dans le répertoire de sortie spécifié. Voici comment procéder :

```csharp
// Enregistrez le fichier Excel XLSB de sortie
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Exemple de code source pour la connexion externe en lecture et en écriture du fichier XLSB à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire des sources
string sourceDir = RunExamples.Get_SourceDirectory();
//Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
//Charger le fichier Excel Xlsb source
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Lire la première connexion externe qui est en fait une connexion DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Imprimer le nom, la commande et les informations de connexion de la connexion DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Modifier le nom de la connexion
dbCon.Name = "NewCust";
//Enregistrez le fichier Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Conclusion

La lecture et l'écriture de connexions externes dans un fichier XLSB vous permettent de manipuler des données provenant de sources externes dans vos classeurs Excel. Avec Aspose.Cells pour .NET, vous pouvez facilement accéder aux connexions externes, lire et modifier les informations de connexion et enregistrer les modifications. Expérimentez avec vos propres fichiers XLSB et exploitez la puissance des connexions externes dans vos applications Excel.

### FAQ

#### Q : Qu'est-ce qu'une connexion externe dans un fichier XLSB ?
    
R : Une connexion externe dans un fichier XLSB fait référence à une connexion établie avec une source de données externe telle qu'une base de données. Il vous permet d'importer des données de cette source externe dans le classeur Excel.

#### Q : Puis-je avoir plusieurs connexions externes dans un fichier XLSB ?
     
R : Oui, vous pouvez avoir plusieurs connexions externes dans un fichier XLSB. Vous pouvez les gérer individuellement en accédant à chaque objet de connexion.

#### Q : Comment puis-je lire les détails d'une connexion externe dans un fichier XLSB avec Aspose.Cells ?
     
R : Vous pouvez utiliser la fonctionnalité fournie par Aspose.Cells pour accéder aux propriétés d'une connexion externe, telles que le nom de la connexion, la commande associée et les informations de connexion.

#### Q : Est-il possible de modifier une connexion externe dans un fichier XLSB avec Aspose.Cells ?
     
R : Oui, vous pouvez modifier les propriétés d'une connexion externe, telles que le nom de la connexion, pour répondre à vos besoins spécifiques. Aspose.Cells fournit des méthodes pour effectuer ces modifications.

#### Q : Comment puis-je enregistrer les modifications apportées à une connexion externe dans un fichier XLSB avec Aspose.Cells ?
     
R : Une fois que vous avez apporté les modifications nécessaires à une connexion externe, vous pouvez simplement enregistrer le fichier Excel XLSB modifié en utilisant la méthode appropriée fournie par Aspose.Cells.