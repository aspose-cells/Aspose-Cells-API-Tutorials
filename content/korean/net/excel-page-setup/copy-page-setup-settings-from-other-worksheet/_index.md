---
title: 다른 워크시트에서 페이지 설정 복사
linktitle: 다른 워크시트에서 페이지 설정 복사
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 한 스프레드시트에서 다른 스프레드시트로 페이지 구성 설정을 복사하는 방법을 알아보세요. 이 라이브러리의 사용을 최적화하기 위한 단계별 가이드입니다.
type: docs
weight: 10
url: /ko/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
이 문서에서는 다음 C# 소스 코드를 단계별로 설명합니다. .NET용 Aspose.Cells를 사용하여 다른 스프레드시트에서 페이지 구성 설정을 복사합니다. 이 작업을 수행하기 위해 .NET용 Aspose.Cells 라이브러리를 사용하겠습니다. 한 워크시트에서 다른 워크시트로 페이지 설정 설정을 복사하려면 아래 단계를 따르세요.

## 1단계: 통합 문서 만들기
첫 번째 단계는 통합 문서를 만드는 것입니다. 우리의 경우 Aspose.Cells 라이브러리에서 제공하는 Workbook 클래스를 사용하겠습니다. 통합 문서를 만드는 코드는 다음과 같습니다.

```csharp
Workbook wb = new Workbook();
```

## 2단계: 테스트 워크시트 추가
통합 문서를 만든 후에는 테스트 워크시트를 추가해야 합니다. 이 예에서는 두 개의 워크시트를 추가합니다. 두 개의 워크시트를 추가하는 코드는 다음과 같습니다.

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## 3단계: 워크시트에 액세스하기
이제 워크시트를 추가했으므로 워크시트에 액세스하여 설정을 변경해야 합니다. 이름을 사용하여 "TestSheet1" 및 "TestSheet2" 워크시트에 액세스하겠습니다. 액세스하는 코드는 다음과 같습니다.

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## 4단계: 용지 크기 설정
 이 단계에서는 "TestSheet1" 워크시트의 용지 크기를 설정합니다. 우리는`PageSetup.PaperSize` 속성은 용지 크기를 설정합니다. 예를 들어 용지 크기를 "PaperA3ExtraTransverse"로 설정하겠습니다. 이에 대한 코드는 다음과 같습니다.

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## 5단계: 페이지 설정 복사
이제 "TestSheet1" 워크시트의 페이지 구성 설정을 "TestSheet2"로 복사하겠습니다. 우리는`PageSetup.Copy` 이 작업을 수행하는 방법입니다. 이에 대한 코드는 다음과 같습니다.

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## 6단계: 용지 크기 인쇄
 페이지 설정 설정을 복사한 후 두 워크시트의 용지 크기를 인쇄합니다. 우리는 사용할 것이다`Console.WriteLine` 용지 크기를 표시합니다. 이에 대한 코드는 다음과 같습니다.

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### .NET용 Aspose.Cells를 사용하여 다른 워크시트에서 페이지 설정 복사에 대한 샘플 소스 코드 
```csharp
//통합 문서 만들기
Workbook wb = new Workbook();
//두 개의 테스트 워크시트 추가
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//TestSheet1 및 TestSheet2로 두 워크시트 모두에 액세스
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//TestSheet1의 용지 크기를 PaperA3ExtraTransverse로 설정
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//두 워크시트의 용지 크기를 인쇄합니다.
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//TestSheet1에서 TestSheet2로 PageSetup을 복사합니다.
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//두 워크시트의 용지 크기를 인쇄합니다.
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## 결론
이 기사에서는 .NET용 Aspose.Cells를 사용하여 한 워크시트에서 다른 워크시트로 페이지 구성 설정을 복사하는 방법을 배웠습니다. 통합 문서 만들기, 테스트 워크시트 추가, 워크시트 액세스, 용지 크기 설정, 페이지 설정 복사, 용지 크기 인쇄 등의 단계를 거쳤습니다. 이제 이 지식을 사용하여 페이지 구성 설정을 자신의 프로젝트에 복사할 수 있습니다.

### 자주 묻는 질문

#### Q: 서로 다른 통합 문서 인스턴스 간에 페이지 구성 설정을 복사할 수 있나요?

 A: 예, 다음을 사용하여 서로 다른 통합 문서 인스턴스 간에 페이지 설정 설정을 복사할 수 있습니다.`PageSetup.Copy` Aspose.Cells 라이브러리의 메서드입니다.

#### Q: 방향이나 여백과 같은 다른 페이지 설정 설정을 복사할 수 있습니까?

 A: 예, 다음을 사용하여 다른 페이지 설정 설정을 복사할 수 있습니다.`PageSetup.Copy` 적절한 옵션을 사용하는 방법입니다. 예를 들어 다음을 사용하여 방향을 복사할 수 있습니다.`CopyOptions.Orientation` 및 여백을 사용하여`CopyOptions.Margins`.

#### 질문: 용지 크기에 어떤 옵션을 사용할 수 있는지 어떻게 알 수 있나요?

A: Aspose.Cells 라이브러리 API 참조에서 용지 크기에 사용 가능한 옵션을 확인할 수 있습니다. 라는 열거형이 있습니다.`PaperSizeType` 지원되는 다양한 용지 크기가 나열되어 있습니다.

#### Q: .NET용 Aspose.Cells 라이브러리를 어떻게 다운로드할 수 있나요?

 A: 다음에서 .NET용 Aspose.Cells 라이브러리를 다운로드할 수 있습니다.[Aspose 릴리스](https://releases.aspose.com/cells/net). 무료 평가판도 있고, 상업용 유료 라이센스도 있습니다.

#### Q: Aspose.Cells 라이브러리는 다른 프로그래밍 언어를 지원합니까?

A: 예, Aspose.Cells 라이브러리는 C#, Java, Python 등을 포함한 여러 프로그래밍 언어를 지원합니다.