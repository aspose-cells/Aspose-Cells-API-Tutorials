---
title: 워크시트의 용지 크기가 자동인지 확인
linktitle: 워크시트의 용지 크기가 자동인지 확인
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 스프레드시트의 용지 크기가 자동인지 확인하는 방법을 알아보세요.
type: docs
weight: 20
url: /ko/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
이 문서에서는 다음 C# 소스 코드를 단계별로 설명합니다. .NET용 Aspose.Cells를 사용하여 워크시트의 용지 크기가 자동인지 확인합니다. 이 작업을 수행하기 위해 .NET용 Aspose.Cells 라이브러리를 사용하겠습니다. 워크시트의 용지 크기가 자동인지 확인하려면 아래 단계를 따르세요.

## 1단계: 통합 문서 로드
첫 번째 단계는 통합 문서를 로드하는 것입니다. 두 개의 통합 문서가 있습니다. 하나는 자동 용지 크기가 비활성화되어 있고 다른 하나는 자동 용지 크기가 활성화되어 있습니다. 통합 문서를 로드하는 코드는 다음과 같습니다.

```csharp
// 소스 디렉토리
string sourceDir = "YOUR_SOURCE_DIR";
// 출력 디렉토리
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// 자동 용지 크기가 비활성화된 첫 번째 통합 문서 로드
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// 자동 용지 크기가 활성화된 두 번째 통합 문서 로드
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## 2단계: 스프레드시트에 액세스하기
이제 통합 문서를 로드했으므로 자동 용지 크기를 확인할 수 있도록 워크시트에 액세스해야 합니다. 두 통합 문서의 첫 번째 워크시트로 이동하겠습니다. 액세스하는 코드는 다음과 같습니다.

```csharp
//첫 번째 통합 문서의 첫 번째 워크시트로 이동
Worksheet ws11 = wb1.Worksheets[0];

// 두 번째 통합 문서의 첫 번째 워크시트로 이동
Worksheet ws12 = wb2.Worksheets[0];
```

## 3단계: 자동 용지 크기 확인
 이 단계에서는 워크시트 용지 크기가 자동인지 확인합니다. 우리는`PageSetup.IsAutomaticPaperSize` 이 정보를 얻기 위한 속성입니다. 그러면 결과가 표시됩니다. 이에 대한 코드는 다음과 같습니다.

```csharp
// 첫 번째 통합 문서에서 첫 번째 워크시트의 IsAutomaticPaperSize 속성을 표시합니다.
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// 두 번째 통합 문서에서 첫 번째 워크시트의 IsAutomaticPaperSize 속성을 표시합니다.
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### .NET용 Aspose.Cells를 사용하여 워크시트의 용지 크기가 자동인지 확인하기 위한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//출력 디렉토리
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//자동 용지 크기가 false인 첫 번째 통합 문서 로드
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//자동 용지 크기가 true인 두 번째 통합 문서를 로드합니다.
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//두 통합 문서의 첫 번째 워크시트에 액세스
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//두 워크시트의 PageSetup.IsAutomaticPaperSize 속성을 인쇄합니다.
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## 결론
이 기사에서는 .NET용 Aspose.Cells를 사용하여 워크시트의 용지 크기가 자동인지 확인하는 방법을 배웠습니다. 우리는 다음 단계를 따랐습니다. 통합 문서를 로드하고,

스프레드시트에 액세스하고 자동 용지 크기 확인이 가능합니다. 이제 이 지식을 사용하여 스프레드시트의 용지 크기가 자동인지 확인할 수 있습니다.

### 자주 묻는 질문

#### Q: .NET용 Aspose.Cells를 사용하여 통합 문서를 어떻게 로드할 수 있나요?

A: Aspose.Cells 라이브러리의 Workbook 클래스를 사용하여 통합 문서를 로드할 수 있습니다. Workbook.Load 메서드를 사용하여 파일에서 통합 문서를 로드합니다.

#### Q: 다른 스프레드시트의 자동 용지 크기를 확인할 수 있나요?

A: 예, 해당 Worksheet 개체의 PageSetup.IsAutomaticPaperSize 속성에 액세스하여 모든 워크시트의 자동 용지 크기를 확인할 수 있습니다.

#### 질문: 스프레드시트의 자동 용지 크기를 어떻게 변경합니까?

A: 워크시트의 자동 용지 크기를 변경하려면 PageSetup.IsAutomaticPaperSize 속성을 사용하고 원하는 값(true 또는 false)으로 설정할 수 있습니다.

#### Q: Aspose.Cells for .NET은 어떤 다른 기능을 제공합니까?

A: Aspose.Cells for .NET은 통합 문서 생성, 수정, 변환은 물론 데이터, 수식, 서식 조작 등 스프레드시트 작업을 위한 다양한 기능을 제공합니다.