---
title: Grupowanie danych w tabelach przestawnych
linktitle: Grupowanie danych w tabelach przestawnych
second_title: Aspose.Cells API przetwarzania Java Excel
description: Dowiedz się, jak tworzyć tabele przestawne w programie Excel przy użyciu Aspose.Cells dla Java. Zautomatyzuj grupowanie i analizę danych za pomocą przykładów kodu źródłowego.
type: docs
weight: 14
url: /pl/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

Tabele przestawne to potężne narzędzie do analizowania i podsumowywania danych w arkuszach kalkulacyjnych. Umożliwiają grupowanie i kategoryzację danych w celu uzyskania cennych informacji. W tym artykule przyjrzymy się, jak efektywnie grupować dane w tabelach przestawnych przy użyciu Aspose.Cells dla Java, wraz z przykładami kodu źródłowego.

## Wstęp

Tabele przestawne umożliwiają elastyczny sposób organizowania i podsumowywania danych z dużych zbiorów danych. Umożliwiają tworzenie niestandardowych widoków danych poprzez grupowanie ich w kategorie lub hierarchie. Może to pomóc w łatwiejszej identyfikacji trendów, wzorców i wartości odstających w danych.

## Krok 1: Utwórz tabelę przestawną

Zacznijmy od utworzenia tabeli przestawnej przy użyciu Aspose.Cells dla Java. Poniżej znajduje się przykład tworzenia tabeli przestawnej z przykładowego pliku Excel.

```java
// Załaduj plik Excel
Workbook workbook = new Workbook("sample.xlsx");

// Uzyskaj dostęp do arkusza zawierającego dane
Worksheet worksheet = workbook.getWorksheets().get(0);

// Określ zakres danych
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // Zakładając 20 wierszy danych
sourceData.startColumn = 0;
sourceData.endColumn = 3; // Zakładając 4 kolumny danych

// Utwórz tabelę przestawną na podstawie zakresu danych
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Pobierz tabelę przestawną według indeksu
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Dodaj pola do wierszy i kolumn
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Dodaj wartości i zastosuj agregację
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Zapisz zmodyfikowany plik Excel
workbook.save("output.xlsx");
```

## Krok 2: Dane grupowe

 W Aspose.Cells for Java możesz grupować dane w tabeli przestawnej za pomocą`PivotField` klasa. Oto przykład grupowania pola w tabeli przestawnej:

```java
// Uzyskaj dostęp do pola „Produkt” w tabeli przestawnej
PivotField productField = pivotTable.getPivotFields().get("Product");

//Pogrupuj pole „Produkt” według określonego kryterium, np. według litery początkowej
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Zapisz zmodyfikowany plik Excel z pogrupowanymi danymi
workbook.save("output_grouped.xlsx");
```

## Krok 3: Dostosuj grupowanie

Możesz dodatkowo dostosować ustawienia grupowania, na przykład określając interwały grupowania na podstawie daty lub niestandardowe reguły grupowania. Oto przykład dostosowywania grupowania na podstawie daty:

```java
// Uzyskaj dostęp do pola „Data” w tabeli przestawnej (zakładając, że jest to pole daty)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Grupuj daty według miesięcy
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Zapisz zmodyfikowany plik Excel z niestandardowym grupowaniem dat
workbook.save("output_custom_grouping.xlsx");
```

## Wniosek

Grupowanie danych w tabelach przestawnych jest cenną techniką analizy i podsumowania danych w Excelu, a Aspose.Cells dla Java ułatwia automatyzację tego procesu. Dzięki dostarczonym przykładom kodu źródłowego możesz tworzyć tabele przestawne, dostosowywać grupowanie i efektywnie uzyskiwać wgląd w dane.

## Często zadawane pytania

### 1. Do czego służą tabele przestawne w Excelu?

Tabele przestawne w programie Excel służą do podsumowywania i analizowania dużych zbiorów danych. Umożliwiają tworzenie niestandardowych widoków danych, ułatwiając identyfikację wzorców i trendów.

### 2. Jak mogę dostosować grupowanie danych w tabeli przestawnej?

 Możesz dostosować grupowanie danych w tabeli przestawnej, korzystając z opcji`PivotField` klasa w Aspose.Cells dla Java. Umożliwia to określenie kryteriów grupowania, takich jak interwały oparte na datach lub reguły niestandardowe.

### 3. Czy mogę zautomatyzować tworzenie tabel przestawnych za pomocą Aspose.Cells dla Java?

Tak, możesz zautomatyzować tworzenie tabel przestawnych w programie Excel za pomocą Aspose.Cells for Java, jak pokazano w dostarczonych przykładach kodu źródłowego.