---
title: Excel 인쇄 옵션 설정
linktitle: Excel 인쇄 옵션 설정
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 쉽게 Excel 파일을 조작하고 인쇄 옵션을 사용자 정의하는 방법을 알아보세요.
type: docs
weight: 150
url: /ko/net/excel-page-setup/set-excel-print-options/
---
이 가이드에서는 Aspose.Cells for .NET을 사용하여 Excel 통합 문서의 인쇄 옵션을 설정하는 방법을 안내합니다. 이 작업을 수행하기 위해 제공된 C# 소스 코드를 단계별로 안내해 드리겠습니다.

## 1단계: 환경 설정

시작하기 전에 개발 환경을 설정하고 .NET용 Aspose.Cells를 설치했는지 확인하세요. Aspose 공식 웹사이트에서 최신 버전의 라이브러리를 다운로드할 수 있습니다.

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

## 5단계: 워크시트의 PageSetup 참조 가져오기

인쇄 옵션을 설정하려면 먼저 워크시트에서 PageSetup 참조를 가져와야 합니다. 참조를 얻으려면 다음 코드를 사용하십시오.

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## 6단계: 인쇄 격자선 활성화

그리드 선을 인쇄하려면 다음 코드를 사용하십시오.

```csharp
pageSetup. PrintGridlines = true;
```

## 7단계: 행/열 머리글 인쇄 활성화

행 및 열 머리글 인쇄를 활성화하려면 다음 코드를 사용하십시오.

```csharp
pageSetup.PrintHeadings = true;
```

## 8단계: 흑백 인쇄 모드 활성화

흑백 모드로 워크시트 인쇄를 활성화하려면 다음 코드를 사용하십시오.

```csharp
pageSetup.BlackAndWhite = true;
```

## 9단계: 피드백 인쇄 활성화

스프레드시트에 표시된 대로 주석을 인쇄하려면 다음 코드를 사용하십시오.

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## 10단계: 초안 모드 인쇄 활성화

초안 모드에서 스프레드시트 인쇄를 활성화하려면 다음 코드를 사용하세요.

```csharp
pageSetup.PrintDraft = true;
```

## 11단계: 셀 오류 인쇄를 N/A로 활성화

셀 오류를 다음과 같이 인쇄할 수 있도록 하려면

  N/A보다 다음 코드를 사용하십시오.

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## 12단계: Excel 통합 문서 저장

 인쇄 옵션이 설정된 Excel 통합 문서를 저장하려면`Save` Workbook 개체의 메서드:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

그러면 지정된 디렉터리에 "OtherPrintOptions_out.xls"라는 파일 이름으로 Excel 통합 문서가 저장됩니다.

### .NET용 Aspose.Cells를 사용하여 Excel 인쇄 옵션 설정에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// 워크시트의 PageSetup 참조 가져오기
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// 눈금선 인쇄 허용
pageSetup.PrintGridlines = true;
// 행/열 제목 인쇄 허용
pageSetup.PrintHeadings = true;
// 흑백 모드로 워크시트 인쇄 허용
pageSetup.BlackAndWhite = true;
// 워크시트에 표시된 대로 설명을 인쇄하도록 허용
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// 초안 품질로 워크시트 인쇄 허용
pageSetup.PrintDraft = true;
// 셀 오류를 N/A로 인쇄하도록 허용
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// 통합 문서를 저장합니다.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## 결론

이제 Aspose.Cells for .NET을 사용하여 Excel 통합 문서의 인쇄 옵션을 설정하는 방법을 배웠습니다. 이 강력하고 사용자 친화적인 라이브러리를 사용하면 쉽고 효율적인 방법으로 Excel 통합 문서의 인쇄 설정을 사용자 지정할 수 있습니다.

### 자주 묻는 질문


#### 1. 여백이나 페이지 방향과 같은 인쇄 옵션을 추가로 사용자 정의할 수 있습니까?

예, .NET용 Aspose.Cells는 여백, 페이지 방향, 배율 등과 같은 광범위한 사용자 정의 가능한 인쇄 옵션을 제공합니다.

#### 2. .NET용 Aspose.Cells는 다른 Excel 파일 형식을 지원합니까?

예, Aspose.Cells for .NET은 XLSX, XLS, CSV, HTML, PDF 등과 같은 다양한 Excel 파일 형식을 지원합니다.

#### 3. Aspose.Cells for .NET은 모든 버전의 .NET Framework와 호환됩니까?

.NET용 Aspose.Cells는 버전 3.5, 4.0, 4.5, 4.6 등을 포함하여 .NET Framework 2.0 이상과 호환됩니다.