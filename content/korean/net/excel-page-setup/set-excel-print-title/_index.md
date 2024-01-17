---
title: Excel 인쇄 제목 설정
linktitle: Excel 인쇄 제목 설정
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 파일을 쉽게 조작하고 인쇄 옵션을 사용자 정의하는 방법을 알아보세요.
type: docs
weight: 170
url: /ko/net/excel-page-setup/set-excel-print-title/
---
이 가이드에서는 .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 인쇄 제목을 설정하는 방법을 안내합니다. 이 작업을 수행하려면 아래 단계를 따르십시오.

## 1단계: 환경 설정

개발 환경을 설정하고 .NET용 Aspose.Cells를 설치했는지 확인하세요. Aspose 공식 웹사이트에서 최신 버전의 라이브러리를 다운로드할 수 있습니다.

## 2단계: 필수 네임스페이스 가져오기

C# 프로젝트에서 Aspose.Cells 작업에 필요한 네임스페이스를 가져옵니다.

```csharp
using Aspose.Cells;
```

## 3단계: 문서 디렉터리 경로 설정

 선언하다`dataDir` 생성된 Excel 파일을 저장할 디렉터리의 경로를 지정하는 변수:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 꼭 교체하세요`"YOUR_DOCUMENT_DIRECTORY"` 시스템의 올바른 경로를 사용하십시오.

## 4단계: 통합 문서 개체 만들기

만들려는 Excel 통합 문서를 나타내는 Workbook 개체를 인스턴스화합니다.

```csharp
Workbook workbook = new Workbook();
```

## 5단계: 첫 번째 워크시트에 액세스

다음 코드를 사용하여 Excel 통합 문서의 첫 번째 워크시트로 이동합니다.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 6단계: 제목 열 정의

다음 코드를 사용하여 제목 열을 정의합니다.

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

여기서는 A열과 B열을 제목 열로 정의했습니다. 필요에 따라 이 값을 조정할 수 있습니다.

## 7단계: 제목 줄 정의

다음 코드를 사용하여 제목 줄을 정의합니다.

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

행 1과 2를 제목 행으로 정의했습니다. 필요에 따라 이러한 값을 조정할 수 있습니다.

## 8단계: Excel 통합 문서 저장

 정의된 인쇄 제목으로 Excel 통합 문서를 저장하려면`Save` Workbook 개체의 메서드:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

그러면 지정된 디렉터리에 "SetPrintTitle_out.xls"라는 파일 이름으로 Excel 통합 문서가 저장됩니다.

### .NET용 Aspose.Cells를 사용하여 Excel 인쇄 제목 설정에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// 워크시트의 PageSetup 참조 가져오기
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// 열 번호 A & B를 제목 열로 정의
pageSetup.PrintTitleColumns = "$A:$B";
// 행 번호 1 및 2를 제목 행으로 정의
pageSetup.PrintTitleRows = "$1:$2";
// 통합 문서를 저장합니다.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 인쇄 제목을 설정하는 방법을 배웠습니다. 인쇄 제목을 사용하면 인쇄된 각 페이지에 특정 행과 열을 표시할 수 있으므로 데이터를 더 쉽게 읽고 참조할 수 있습니다.

### 자주 묻는 질문

#### 1. Excel에서 특정 열의 인쇄 제목을 설정할 수 있나요?

 예, .NET용 Aspose.Cells를 사용하면 다음을 사용하여 특정 열을 인쇄 제목으로 설정할 수 있습니다.`PrintTitleColumns` 의 재산`PageSetup` 물체.

#### 2. 열 제목과 인쇄 행 제목을 모두 정의할 수 있습니까?

 예, 다음을 사용하여 인쇄 열과 행 제목을 모두 설정할 수 있습니다.`PrintTitleColumns` 그리고`PrintTitleRows` 의 속성`PageSetup` 물체.

#### 3. Aspose.Cells for .NET으로 사용자 정의할 수 있는 다른 레이아웃 설정은 무엇입니까?

.NET용 Aspose.Cells를 사용하면 여백, 페이지 방향, 인쇄 배율 등과 같은 다양한 페이지 레이아웃 설정을 사용자 정의할 수 있습니다.