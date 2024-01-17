---
title: 동적 피벗 테이블
linktitle: 동적 피벗 테이블
second_title: Aspose.Cells Java Excel 처리 API
description: Aspose.Cells for Java를 사용하여 동적 피벗 테이블을 손쉽게 생성하세요. 데이터를 쉽게 분석하고 요약하세요. 데이터 분석 역량을 강화하세요.
type: docs
weight: 13
url: /ko/java/excel-pivot-tables/dynamic-pivot-tables/
---

피벗 테이블은 데이터 분석의 강력한 도구로, 스프레드시트에서 데이터를 요약하고 조작할 수 있습니다. 이 튜토리얼에서는 Aspose.Cells for Java API를 사용하여 동적 피벗 테이블을 생성하는 방법을 살펴보겠습니다.

## 피벗 테이블 소개

피벗 테이블은 스프레드시트의 데이터를 요약하고 분석할 수 있는 대화형 테이블입니다. 이는 데이터를 구성하고 분석하는 동적 방법을 제공하여 더 쉽게 통찰력을 얻고 정보에 입각한 결정을 내릴 수 있도록 해줍니다.

## 1단계: Aspose.Cells 라이브러리 가져오기

 동적 피벗 테이블을 생성하기 전에 Aspose.Cells 라이브러리를 Java 프로젝트로 가져와야 합니다. Aspose 릴리스에서 라이브러리를 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cells/java/).

라이브러리를 다운로드한 후 프로젝트의 빌드 경로에 추가하세요.

## 2단계: 통합 문서 로드

피벗 테이블을 사용하려면 먼저 분석하려는 데이터가 포함된 통합 문서를 로드해야 합니다. 다음 코드를 사용하여 이 작업을 수행할 수 있습니다.

```java
// 엑셀 파일 불러오기
Workbook workbook = new Workbook("your_excel_file.xlsx");
```

 바꾸다`"your_excel_file.xlsx"` Excel 파일의 경로와 함께.

## 3단계: 피벗 테이블 만들기

이제 통합 문서를 로드했으므로 피벗 테이블을 만들어 보겠습니다. 피벗 테이블의 원본 데이터 범위와 이를 워크시트에 배치할 위치를 지정해야 합니다. 예는 다음과 같습니다.

```java
// 첫 번째 워크시트 가져오기
Worksheet worksheet = workbook.getWorksheets().get(0);

// 피벗 테이블의 데이터 범위 지정
String sourceData = "A1:D10"; // 데이터 범위로 바꾸기

// 피벗 테이블의 위치를 지정하세요.
int firstRow = 1;
int firstColumn = 5;

// 피벗 테이블 만들기
PivotTable pivotTable = worksheet.getPivotTables().add(sourceData, worksheet.getCells().get(firstRow, firstColumn), "PivotTable1");
```

## 4단계: 피벗 테이블 구성

이제 피벗 테이블을 만들었으므로 필요에 따라 데이터를 요약하고 분석하도록 구성할 수 있습니다. 행 필드, 열 필드, 데이터 필드를 설정하고 다양한 계산을 적용할 수 있습니다. 예는 다음과 같습니다.

```java
// 피벗 테이블에 필드 추가
pivotTable.addFieldToArea(PivotFieldType.ROW, 0); // 행 필드
pivotTable.addFieldToArea(PivotFieldType.COLUMN, 1); // 열 필드
pivotTable.addFieldToArea(PivotFieldType.DATA, 2); // 데이터 필드

// 데이터 필드에 대한 계산 설정
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);
```

## 5단계: 피벗 테이블 새로 고침

피벗 테이블은 동적일 수 있습니다. 즉, 소스 데이터가 변경되면 자동으로 업데이트됩니다. 피벗 테이블을 새로 고치려면 다음 코드를 사용할 수 있습니다.

```java
// 피벗 테이블 새로 고침
pivotTable.refreshData();
pivotTable.calculateData();
```

## 결론

이 튜토리얼에서는 Aspose.Cells for Java API를 사용하여 동적 피벗 테이블을 생성하는 방법을 배웠습니다. 피벗 테이블은 데이터 분석을 위한 유용한 도구이며 Aspose.Cells를 사용하면 Java 애플리케이션에서 테이블 생성 및 조작을 자동화할 수 있습니다.

궁금한 점이 있거나 추가 지원이 필요한 경우 언제든지 문의해 주세요. 즐거운 코딩하세요!

## 자주 묻는 질문

### Q1: 피벗 테이블 데이터 필드에 사용자 정의 계산을 적용할 수 있습니까?

예, 자체 논리를 구현하여 데이터 필드에 사용자 정의 계산을 적용할 수 있습니다.

### Q2: 피벗 테이블의 서식을 어떻게 변경할 수 있나요?

스타일 속성에 액세스하고 원하는 서식을 적용하여 피벗 테이블의 서식을 변경할 수 있습니다.

### Q3: 동일한 워크시트에 여러 피벗 테이블을 만들 수 있습니까?

예, 서로 다른 대상 위치를 지정하여 동일한 워크시트에 여러 피벗 테이블을 만들 수 있습니다.

### Q4: 피벗 테이블의 데이터를 필터링할 수 있나요?

예, 피벗 테이블에 필터를 적용하여 특정 데이터 하위 집합을 표시할 수 있습니다.

### 질문 5: Aspose.Cells는 Excel의 고급 피벗 테이블 기능을 지원합니까?

예, Aspose.Cells는 Excel의 고급 피벗 테이블 기능을 광범위하게 지원하므로 복잡한 피벗 테이블을 만들 수 있습니다.