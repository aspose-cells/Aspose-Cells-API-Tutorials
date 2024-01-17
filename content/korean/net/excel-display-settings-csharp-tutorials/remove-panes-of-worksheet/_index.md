---
title: 워크시트 창 제거
linktitle: 워크시트 창 제거
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 워크시트에서 창을 제거하는 단계별 가이드입니다.
type: docs
weight: 120
url: /ko/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 Excel 워크시트에서 창을 제거하는 방법을 설명합니다. 원하는 결과를 얻으려면 다음 단계를 따르십시오.

## 1단계: 환경 설정

.NET용 Aspose.Cells를 설치하고 개발 환경을 설정했는지 확인하세요. 또한 창을 제거하려는 Excel 파일의 복사본이 있는지 확인하세요.

## 2단계: 필요한 종속성 가져오기

Aspose.Cells의 클래스를 사용하는 데 필요한 지시문을 추가합니다.

```csharp
using Aspose.Cells;
```

## 3단계: 코드 초기화

Excel 문서가 포함된 디렉터리의 경로를 초기화하는 것부터 시작하세요.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 4단계: Excel 파일 열기

 새 인스턴스화`Workbook` 개체를 사용하여 Excel 파일을 엽니다.`Open` 방법:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## 5단계: 활성 셀 정의

 다음을 사용하여 워크시트의 활성 셀을 설정합니다.`ActiveCell` 재산:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## 6단계: 창 삭제

 다음을 사용하여 워크시트 창에서 창을 제거합니다.`RemoveSplit` 방법:

```csharp
book.Worksheets[0].RemoveSplit();
```

## 7단계: 변경 사항 저장

Excel 파일의 변경 사항을 저장합니다.

```csharp
book.Save(dataDir + "output.xls");
```

### .NET용 Aspose.Cells를 사용하여 워크시트 창 제거에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 새 통합 문서를 인스턴스화하고 템플릿 파일을 엽니다.
Workbook book = new Workbook(dataDir + "Book1.xls");
// 활성 셀 설정
book.Worksheets[0].ActiveCell = "A20";
// 워크시트 창 분할
book.Worksheets[0].RemoveSplit();
// 엑셀 파일을 저장하세요
book.Save(dataDir + "output.xls");
```

## 결론

이 자습서에서는 .NET용 Aspose.Cells를 사용하여 Excel 워크시트에서 창을 제거하는 방법을 배웠습니다. 설명된 단계를 따르면 Excel 파일의 모양과 동작을 쉽게 사용자 지정할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### .NET용 Aspose.Cells란 무엇입니까?

Aspose.Cells for .NET은 .NET 애플리케이션에서 Excel 파일을 조작하는 데 널리 사용되는 소프트웨어 라이브러리입니다.

#### Aspose.Cells에서 워크시트의 활성 셀을 어떻게 설정합니까?

 다음을 사용하여 활성 셀을 설정할 수 있습니다.`ActiveCell`Worksheet 개체의 속성입니다.

#### 워크시트 창에서 가로 또는 세로 창만 제거할 수 있나요?

 예, Aspose.Cells를 사용하면 다음과 같은 적절한 방법을 사용하여 수평 또는 수직 창만 제거할 수 있습니다.`RemoveHorizontalSplit` 또는`RemoveVerticalSplit`.

#### Aspose.Cells는 .xls 형식의 Excel 파일에서만 작동합니까?

아니요, Aspose.Cells는 .xls 및 .xlsx를 포함한 다양한 Excel 파일 형식을 지원합니다.
	