---
title: Excel 페이지에 맞추기 옵션
linktitle: Excel 페이지에 맞추기 옵션
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트의 페이지를 자동 맞춤하는 방법을 알아보세요.
type: docs
weight: 30
url: /ko/net/excel-page-setup/fit-to-excel-pages-options/
---
이 문서에서는 다음 C# 소스 코드를 단계별로 설명합니다. .NET용 Aspose.Cells를 사용하여 Excel 페이지 옵션에 맞추기. 이 작업을 수행하기 위해 .NET용 Aspose.Cells 라이브러리를 사용하겠습니다. Excel에서 페이지에 맞춤을 구성하려면 아래 단계를 따르세요.

## 1단계: 통합 문서 만들기
첫 번째 단계는 통합 문서를 만드는 것입니다. Workbook 개체를 인스턴스화하겠습니다. 통합 문서를 만드는 코드는 다음과 같습니다.

```csharp
// 문서 디렉토리의 경로
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
```

## 2단계: 워크시트에 액세스
이제 통합 문서를 만들었으므로 첫 번째 워크시트로 이동해야 합니다. 첫 번째 시트에 액세스하기 위해 인덱스 0을 사용합니다. 액세스하는 코드는 다음과 같습니다.

```csharp
// 통합 문서의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
```

## 3단계: 페이지에 맞춤 설정
 이 단계에서는 워크시트 페이지에 대한 조정을 구성합니다. 우리는`FitToPagesTall` 그리고`FitToPagesWide` 의 속성`PageSetup` 워크시트의 높이와 너비에 대해 원하는 페이지 수를 지정하는 개체입니다. 이에 대한 코드는 다음과 같습니다.

```csharp
// 워크시트 높이에 맞게 페이지 수를 구성합니다.
worksheet.PageSetup.FitToPagesTall = 1;

// 워크시트 너비에 맞게 페이지 수를 구성합니다.
worksheet.PageSetup.FitToPagesWide = 1;
```

## 4단계: 통합 문서 저장
 이제 페이지에 맞춤을 구성했으므로 통합 문서를 저장할 수 있습니다. 우리는`Save` 이에 대한 Workbook 개체의 메서드입니다. 통합 문서를 저장하는 코드는 다음과 같습니다.

```csharp
// 통합 문서 저장
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### .NET용 Aspose.Cells를 사용하여 Excel 페이지에 맞춤 옵션에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
// 워크시트의 길이를 확장할 페이지 수 설정
worksheet.PageSetup.FitToPagesTall = 1;
//워크시트 너비를 확장할 페이지 수 설정
worksheet.PageSetup.FitToPagesWide = 1;
// 통합 문서를 저장합니다.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## 결론
이 기사에서는 .NET용 Aspose.Cells를 사용하여 Excel에서 페이지에 맞게 구성하는 방법을 배웠습니다. 통합 문서 만들기, 워크시트에 액세스하기, 페이지에 맞게 구성하기, 통합 문서 저장하기 등의 단계를 진행했습니다. 이제 이 지식을 사용하여 스프레드시트를 원하는 페이지에 맞게 조정할 수 있습니다.

### 자주 묻는 질문

#### Q: .NET용 Aspose.Cells를 어떻게 설치하나요?

A: .NET용 Aspose.Cells를 설치하려면 Visual Studio에서 NuGet 패키지 관리자를 사용할 수 있습니다. "Aspose.Cells" 패키지를 찾아 프로젝트에 설치하세요.

#### 질문: 페이지의 높이와 너비를 모두 맞출 수 있나요?

 A: 예, 다음을 사용하여 워크시트의 높이와 너비를 모두 조정할 수 있습니다.`FitToPagesTall` 그리고`FitToPagesWide` 속성. 각 차원에 대해 원하는 페이지 수를 지정할 수 있습니다.

#### Q: 페이지에 맞춤 옵션을 어떻게 사용자 정의할 수 있나요?

A: 페이지 수를 지정하는 것 외에도 워크시트 배율, 용지 방향, 여백 등과 같은 기타 페이지에 맞춤 옵션을 사용자 정의할 수도 있습니다. 다음에서 사용 가능한 속성을 사용하세요.`PageSetup` 이에 반대합니다.

#### Q: .NET용 Aspose.Cells를 사용하여 기존 통합 문서를 처리할 수 있습니까?

A: 예, .NET용 Aspose.Cells를 사용하여 기존 통합 문서를 열고 편집할 수 있습니다. 워크시트, 셀, 수식, 스타일 및 기타 통합 문서 항목에 액세스하여 다양한 작업을 수행할 수 있습니다.