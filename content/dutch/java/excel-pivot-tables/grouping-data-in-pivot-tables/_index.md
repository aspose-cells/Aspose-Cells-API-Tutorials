---
title: Gegevens groeperen in draaitabellen
linktitle: Gegevens groeperen in draaitabellen
second_title: Aspose.Cells Java Excel-verwerkings-API
description: Leer hoe u draaitabellen maakt in Excel met Aspose.Cells voor Java. Automatiseer het groeperen en analyseren van gegevens met broncodevoorbeelden.
type: docs
weight: 14
url: /nl/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

Draaitabellen zijn een krachtig hulpmiddel voor het analyseren en samenvatten van gegevens in spreadsheets. Hiermee kunt u gegevens groeperen en categoriseren om waardevolle inzichten te verkrijgen. In dit artikel onderzoeken we hoe u gegevens effectief kunt groeperen in draaitabellen met behulp van Aspose.Cells voor Java, samen met broncodevoorbeelden.

## Invoering

Draaitabellen bieden een flexibele manier om gegevens uit grote gegevenssets te ordenen en samen te vatten. Hiermee kunt u aangepaste weergaven van uw gegevens maken door deze in categorieën of hiërarchieën te groeperen. Hierdoor kunt u gemakkelijker trends, patronen en uitschieters in uw gegevens identificeren.

## Stap 1: Maak een draaitabel

Laten we beginnen met het maken van een draaitabel met Aspose.Cells voor Java. Hieronder ziet u een voorbeeld van hoe u een draaitabel kunt maken op basis van een voorbeeld van een Excel-bestand.

```java
// Laad het Excel-bestand
Workbook workbook = new Workbook("sample.xlsx");

// Open het werkblad met de gegevens
Worksheet worksheet = workbook.getWorksheets().get(0);

// Geef het gegevensbereik op
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // Uitgaande van 20 rijen met gegevens
sourceData.startColumn = 0;
sourceData.endColumn = 3; // Uitgaande van 4 kolommen met gegevens

// Maak een draaitabel op basis van het gegevensbereik
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Haal de draaitabel op per index
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Voeg velden toe aan rijen en kolommen
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Voeg waarden toe en pas aggregatie toe
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Sla het gewijzigde Excel-bestand op
workbook.save("output.xlsx");
```

## Stap 2: Groepsgegevens

 In Aspose.Cells voor Java kunt u gegevens binnen de draaitabel groeperen met behulp van de`PivotField` klas. Hier ziet u een voorbeeld van hoe u een veld in de draaitabel groepeert:

```java
// Ga naar het veld 'Product' in de draaitabel
PivotField productField = pivotTable.getPivotFields().get("Product");

//Groepeer het veld "Product" op een specifiek criterium, bijvoorbeeld op beginletter
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Sla het gewijzigde Excel-bestand met gegroepeerde gegevens op
workbook.save("output_grouped.xlsx");
```

## Stap 3: Groepering aanpassen

U kunt de groeperingsinstellingen verder aanpassen, zoals het opgeven van op datum gebaseerde groeperingsintervallen of aangepaste groeperingsregels. Hier is een voorbeeld van het aanpassen van op datum gebaseerde groepering:

```java
// Toegang tot het veld 'Datum' in de draaitabel (ervan uitgaande dat het een datumveld is)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Groepeer datums op maanden
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Sla het gewijzigde Excel-bestand op met aangepaste datumgroepering
workbook.save("output_custom_grouping.xlsx");
```

## Conclusie

Het groeperen van gegevens in draaitabellen is een waardevolle techniek voor het analyseren en samenvatten van gegevens in Excel, en Aspose.Cells voor Java maakt het eenvoudig om dit proces te automatiseren. Met de meegeleverde broncodevoorbeelden kunt u draaitabellen maken, groeperingen aanpassen en op efficiënte wijze inzichten uit uw gegevens verkrijgen.

## Veelgestelde vragen

### 1. Wat is het doel van draaitabellen in Excel?

Draaitabellen in Excel worden gebruikt om grote gegevenssets samen te vatten en te analyseren. Hiermee kunt u aangepaste weergaven van uw gegevens maken, waardoor u gemakkelijker patronen en trends kunt identificeren.

### 2. Hoe kan ik de groepering van gegevens in een draaitabel aanpassen?

 U kunt de groepering van gegevens in een draaitabel aanpassen met behulp van de`PivotField` klasse in Aspose.Cells voor Java. Hiermee kunt u groeperingscriteria opgeven, zoals op datums gebaseerde intervallen of aangepaste regels.

### 3. Kan ik het maken van draaitabellen automatiseren met Aspose.Cells voor Java?

Ja, u kunt het maken van draaitabellen in Excel automatiseren met behulp van Aspose.Cells voor Java, zoals gedemonstreerd in de meegeleverde broncodevoorbeelden.