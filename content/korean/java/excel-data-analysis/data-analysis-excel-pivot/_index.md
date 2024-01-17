---
title: 데이터 분석 Excel 피벗
linktitle: 데이터 분석 Excel 피벗
second_title: Aspose.Cells Java Excel 처리 API
description: Aspose.Cells for Java를 사용하여 Excel에서 데이터 분석을 알아보세요. 효과적인 피벗 테이블 사용을 위한 단계별 가이드입니다.
type: docs
weight: 13
url: /ko/java/excel-data-analysis/data-analysis-excel-pivot/
---

## Java용 Aspose.Cells 소개

데이터 분석의 핵심을 살펴보기 전에 Java용 Aspose.Cells에 대해 알아봅시다. 이 Java 라이브러리는 Excel 파일 처리 기능으로 유명한 Aspose.Cells 제품군의 일부입니다. Aspose.Cells for Java를 사용하면 Excel 통합 문서, 워크시트, 차트 및 피벗 테이블을 프로그래밍 방식으로 생성, 수정 및 조작할 수 있습니다.

## 전제 조건

이 가이드를 따르려면 다음이 필요합니다.

- Java 개발 환경: 시스템에 Java가 설치되어 있는지 확인하십시오.
-  Aspose.Cells for Java: 프로젝트에 Aspose.Cells for Java 라이브러리를 다운로드하고 포함하세요. 다운로드 링크를 찾을 수 있습니다[여기](https://releases.aspose.com/cells/java/).
- 샘플 데이터: 분석하려는 Excel 데이터를 준비합니다.

## 새 Excel 통합 문서 만들기

Aspose.Cells for Java를 사용하여 새로운 Excel 통합 문서를 만드는 것부터 시작해 보겠습니다. 이는 데이터 분석의 기초가 될 것입니다.

```java
// 새로운 Excel 통합 문서를 생성하는 Java 코드
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.getWorksheets().get(0);
```

## Excel로 데이터 가져오기

이제 빈 통합 문서가 있으므로 데이터를 가져올 수 있습니다. 데이터베이스, CSV 파일과 같은 다양한 소스에서 데이터를 읽을 수 있으며 수동으로 입력한 데이터도 읽을 수 있습니다.

```java
// Excel로 데이터를 가져오는 Java 코드
Cells cells = worksheet.getCells();
cells.importData(yourDataArray, 0, 0, importOptions);
```

## 피벗 테이블 만들기

피벗 테이블은 Excel에서 데이터를 요약하고 분석하는 강력한 방법입니다. 데이터 분석을 용이하게 하기 위해 통합 문서에 피벗 테이블을 만들어 보겠습니다.

```java
// 피벗 테이블을 생성하는 Java 코드
PivotTableCollection pivotTables = worksheet.getPivotTables();
int index = pivotTables.add("A1", "E10", "PivotTable");
PivotTable pivotTable = pivotTables.get(index);
```

## 피벗 테이블 필드 정의

데이터 분석을 효과적으로 수행하려면 피벗 테이블에 포함할 필드를 지정해야 합니다. 이러한 필드는 가져온 데이터의 열일 수 있습니다.

```java
// 피벗 테이블 필드를 정의하는 Java 코드
PivotFieldCollection pivotFields = pivotTable.getRowFields();
pivotFields.add(cells, 0); // 첫 번째 열을 행 필드로 추가
```

## 데이터 집계

피벗 테이블이 설정되면 요구 사항에 따라 데이터를 집계하고 요약할 수 있습니다. 합계, 평균, 개수 등과 같은 집계 함수를 지정할 수 있습니다.

```java
// 피벗 테이블의 데이터를 집계하는 Java 코드
pivotTable.addFieldToArea(0, PivotFieldType.DATA); // 첫 번째 열을 데이터 필드로 추가
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunctionType.SUM); // SUM 함수 사용
```

## 피벗 테이블 레이아웃 사용자 정의

피벗 테이블을 더욱 유익하게 만들기 위해 필터 추가, 정렬, 필드 위치 변경 등 레이아웃을 사용자 정의할 수 있습니다.

```java
// 피벗 테이블 레이아웃을 사용자 정의하는 Java 코드
pivotTable.addFieldToArea(1, PivotFieldType.PAGE); // 두 번째 열을 페이지 필드로 추가(필터)
pivotTable.getField(1).setDisplayAutomaticSubtotals(false); // 자동 소계 비활성화
```

## 데이터 분석

이제 피벗 테이블을 만들고 사용자 정의했으므로 데이터를 분석할 차례입니다. 피벗 테이블을 사용하여 통찰력을 생성하고 추세를 감지하며 정보에 근거한 결정을 내릴 수 있습니다.

## 결론

이 가이드에서는 Aspose.Cells for Java를 사용하여 Excel에서 데이터 분석을 수행하는 방법을 살펴보았습니다. 우리는 새 통합 문서를 만들고, 데이터를 가져오고, 피벗 테이블을 만드는 것부터 시작했습니다. 그런 다음 피벗 테이블 필드와 집계된 데이터를 정의하고 레이아웃을 사용자 정의했습니다. 이러한 도구를 사용하면 Java를 사용하여 Excel에서 데이터 분석의 잠재력을 최대한 활용할 수 있습니다.

## FAQ

### Java용 Aspose.Cells를 어떻게 설치하나요?

 웹사이트에서 Aspose.Cells for Java를 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cells/java/). 제공된 설치 지침에 따라 Java 프로젝트에 설정하세요.

### 피벗 테이블에서 고급 계산을 수행할 수 있나요?

예, 피벗 테이블에서 합계, 평균, 개수 등 다양한 계산을 수행할 수 있습니다. Aspose.Cells for Java는 피벗 테이블 계산 사용자 정의를 위한 광범위한 지원을 제공합니다.

### Aspose.Cells for Java는 대규모 데이터 세트에 적합합니까?

예, Aspose.Cells for Java는 대규모 데이터 세트를 효율적으로 처리하도록 설계되었습니다. 상당한 양의 데이터로 성능을 최적화하기 위해 데이터 페이징 및 스트리밍과 같은 기능을 제공합니다.

### Aspose.Cells for Java를 사용하여 데이터 분석 작업을 자동화할 수 있나요?

전적으로! Aspose.Cells for Java를 사용하면 Excel 파일을 조작하는 Java 코드를 작성하여 데이터 분석 작업을 자동화할 수 있습니다. 원활한 자동화를 위해 이러한 작업을 예약하거나 애플리케이션에 통합할 수 있습니다.

### Aspose.Cells for Java에 대한 라이선스 요구 사항이 있나요?

예, Aspose.Cells for Java는 상용 라이브러리이므로 프로젝트에서 사용하려면 유효한 라이선스가 필요합니다. 라이선스 세부정보 및 가격 정보를 보려면 Aspose 웹사이트를 방문하세요.