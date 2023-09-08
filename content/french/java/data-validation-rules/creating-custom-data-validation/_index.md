---
title: Création d'une validation de données personnalisée
linktitle: Création d'une validation de données personnalisée
second_title: API de traitement Java Excel Aspose.Cells
description: Découvrez comment créer une validation de données personnalisée à l'aide d'Aspose.Cells pour Java. Guide étape par étape avec le code source.
type: docs
weight: 10
url: /fr/java/data-validation-rules/creating-custom-data-validation/
---

## Introduction

La validation des données permet de maintenir l'intégrité des données en empêchant les utilisateurs de saisir des données incorrectes ou invalides dans des feuilles de calcul Excel. Bien qu'Excel propose des options de validation de données intégrées, il existe des scénarios dans lesquels vous devez définir des règles de validation personnalisées. Aspose.Cells for Java vous permet d'y parvenir efficacement.

## Conditions préalables

Avant de plonger dans le code, assurez-vous d'avoir les prérequis suivants :

-  Aspose.Cells pour Java : téléchargez et installez la bibliothèque à partir de[ici](https://releases.aspose.com/cells/java/).

## Étape 1 : configuration de votre projet Java

Pour commencer, créez un nouveau projet Java dans votre environnement de développement intégré (IDE) préféré. Ajoutez la bibliothèque Aspose.Cells for Java au chemin de classe de votre projet.

## Étape 2 : Création d'un classeur Excel

Commençons par créer un nouveau classeur Excel à l'aide d'Aspose.Cells pour Java.

```java
// Code Java pour créer un nouveau classeur Excel
Workbook workbook = new Workbook();
```

## Étape 3 : Ajout d'une feuille de calcul

Maintenant, ajoutons une feuille de calcul au classeur où nous appliquerons notre validation de données personnalisée.

```java
// Code Java pour ajouter une feuille de calcul
Worksheet worksheet = workbook.getWorksheets().get(0);
```

## Étape 4 : Définition des critères de validation personnalisés

Dans cette étape, nous définirons les critères de validation personnalisés auxquels nos données doivent respecter. Disons que nous souhaitons limiter l'âge saisi dans une cellule entre 18 et 60 ans.

```java
// Code Java pour définir des critères de validation personnalisés
Validation validation = worksheet.getValidations().add();
validation.setType(ValidationType.WHOLE);
validation.setOperator(OperatorType.BETWEEN);
validation.setFormula1("18");
validation.setFormula2("60");
validation.setShowError(true);
validation.setAlertStyle(ValidationAlertType.STOP);
validation.setErrorTitle("Invalid Age");
validation.setErrorMessage("Age must be between 18 and 60.");
```

## Étape 5 : Application de la validation des données à une plage

Maintenant que nous avons défini nos critères de validation personnalisés, appliquons-les à une plage spécifique de cellules.

```java
// Code Java pour appliquer la validation des données à une plage
CellArea area = new CellArea();
area.startRow = 0;
area.startColumn = 0;
area.endRow = 9; // Appliquer la validation aux dix premières lignes
area.endColumn = 0;

validation.addArea(area);
```

## Étape 6 : Sauvegarde du fichier Excel

Enfin, enregistrez le fichier Excel avec les règles personnalisées de validation des données appliquées.

```java
// Code Java pour enregistrer le fichier Excel
workbook.save("CustomDataValidation.xlsx");
```

## Conclusion

Dans ce didacticiel, nous avons expliqué comment créer des règles de validation de données personnalisées à l'aide d'Aspose.Cells pour Java. En suivant ces étapes, vous pouvez vous assurer que vos données Excel respectent des critères spécifiques, améliorant ainsi l'intégrité et la précision des données.

## FAQ

### Comment télécharger Aspose.Cells pour Java ?

 Vous pouvez télécharger Aspose.Cells pour Java à partir du site Web à l'adresse[ici](https://releases.aspose.com/cells/java/).

### Puis-je appliquer une validation de données personnalisée à plusieurs plages dans la même feuille de calcul ?

Oui, vous pouvez appliquer une validation de données personnalisée à plusieurs plages au sein de la même feuille de calcul en répétant l'étape 5 pour chaque plage souhaitée.

### Existe-t-il d'autres types de validation de données pris en charge par Aspose.Cells pour Java ?

Oui, Aspose.Cells pour Java prend en charge différents types de validation de données, notamment les nombres entiers, décimaux, la date, l'heure, la longueur du texte, etc.

### Comment puis-je personnaliser le message d'erreur affiché lorsque la validation des données échoue ?

 Vous pouvez personnaliser le message d'erreur en modifiant le`setErrorMessage` à l'étape 4, où vous définissez les critères de validation.

### Aspose.Cells for Java fonctionne-t-il avec des fichiers Excel dans différents formats ?

Oui, Aspose.Cells for Java prend en charge un large éventail de formats de fichiers Excel, notamment XLS, XLSX, XLSM, etc.