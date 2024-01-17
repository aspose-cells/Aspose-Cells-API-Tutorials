---
title: 피벗 테이블에서 데이터 그룹화
linktitle: 피벗 테이블에서 데이터 그룹화
second_title: Aspose.Cells Java Excel 처리 API
description: Aspose.Cells for Java를 사용하여 Excel에서 피벗 테이블을 만드는 방법을 알아보세요. 소스 코드 예제를 사용하여 데이터 그룹화 및 분석을 자동화합니다.
type: docs
weight: 14
url: /ko/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

피벗 테이블은 스프레드시트의 데이터를 분석하고 요약하는 강력한 도구입니다. 이를 통해 데이터를 그룹화하고 분류하여 귀중한 통찰력을 얻을 수 있습니다. 이 기사에서는 소스 코드 예제와 함께 Aspose.Cells for Java를 사용하여 피벗 테이블의 데이터를 효과적으로 그룹화하는 방법을 살펴보겠습니다.

## 소개

피벗 테이블은 대규모 데이터 세트의 데이터를 구성하고 요약하는 유연한 방법을 제공합니다. 이를 통해 데이터를 카테고리나 계층으로 그룹화하여 데이터에 대한 사용자 정의 보기를 만들 수 있습니다. 이를 통해 데이터의 추세, 패턴 및 이상값을 보다 쉽게 식별할 수 있습니다.

## 1단계: 피벗 테이블 만들기

Aspose.Cells for Java를 사용하여 피벗 테이블을 만드는 것부터 시작해 보겠습니다. 다음은 샘플 Excel 파일에서 피벗 테이블을 만드는 방법의 예입니다.

```java
// 엑셀 파일 불러오기
Workbook workbook = new Workbook("sample.xlsx");

// 데이터가 포함된 워크시트에 액세스
Worksheet worksheet = workbook.getWorksheets().get(0);

// 데이터 범위 지정
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // 20행의 데이터를 가정
sourceData.startColumn = 0;
sourceData.endColumn = 3; // 4개의 데이터 열을 가정

// 데이터 범위를 기반으로 피벗 테이블 만들기
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// 인덱스로 피벗 테이블 가져오기
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// 행과 열에 필드 추가
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// 값 추가 및 집계 적용
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// 수정된 Excel 파일을 저장합니다.
workbook.save("output.xlsx");
```

## 2단계: 그룹 데이터

 Aspose.Cells for Java에서는 다음을 사용하여 피벗 테이블 내의 데이터를 그룹화할 수 있습니다.`PivotField` 수업. 다음은 피벗 테이블에서 필드를 그룹화하는 방법에 대한 예입니다.

```java
// 피벗 테이블의 '제품' 필드에 액세스합니다.
PivotField productField = pivotTable.getPivotFields().get("Product");

//특정 기준(예: 시작 문자)으로 "제품" 필드를 그룹화합니다.
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// 수정된 엑셀 파일을 그룹화된 데이터로 저장
workbook.save("output_grouped.xlsx");
```

## 3단계: 그룹화 사용자 정의

날짜 기반 그룹화 간격 또는 사용자 정의 그룹화 규칙을 지정하는 등 그룹화 설정을 추가로 사용자 정의할 수 있습니다. 다음은 날짜 기반 그룹화를 사용자 정의하는 예입니다.

```java
// 피벗 테이블의 "날짜" 필드에 액세스합니다(날짜 필드라고 가정).
PivotField dateField = pivotTable.getPivotFields().get("Date");

// 날짜를 월별로 그룹화
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// 사용자 정의 날짜 그룹화를 사용하여 수정된 Excel 파일을 저장합니다.
workbook.save("output_custom_grouping.xlsx");
```

## 결론

피벗 테이블에서 데이터를 그룹화하는 것은 Excel에서 데이터를 분석하고 요약하는 데 유용한 기술이며 Aspose.Cells for Java를 사용하면 이 프로세스를 쉽게 자동화할 수 있습니다. 제공된 소스 코드 예제를 사용하면 피벗 테이블을 생성하고, 그룹화를 사용자 정의하고, 데이터에서 효율적으로 통찰력을 얻을 수 있습니다.

## 자주 묻는 질문

### 1. Excel에서 피벗 테이블의 목적은 무엇입니까?

Excel의 피벗 테이블은 대규모 데이터 세트를 요약하고 분석하는 데 사용됩니다. 이를 통해 데이터에 대한 사용자 정의 보기를 생성하여 패턴과 추세를 더 쉽게 식별할 수 있습니다.

### 2. 피벗 테이블의 데이터 그룹화를 어떻게 맞춤설정할 수 있나요?

 다음을 사용하여 피벗 테이블의 데이터 그룹화를 맞춤설정할 수 있습니다.`PivotField` Java용 Aspose.Cells의 클래스입니다. 이를 통해 날짜 기반 간격 또는 사용자 정의 규칙과 같은 그룹화 기준을 지정할 수 있습니다.

### 3. Aspose.Cells for Java를 사용하여 피벗 테이블 생성을 자동화할 수 있나요?

예, 제공된 소스 코드 예제에 설명된 대로 Aspose.Cells for Java를 사용하여 Excel에서 피벗 테이블 생성을 자동화할 수 있습니다.