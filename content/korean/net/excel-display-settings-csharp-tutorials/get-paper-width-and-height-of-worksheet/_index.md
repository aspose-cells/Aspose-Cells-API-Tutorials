---
title: 워크시트의 용지 너비와 높이 가져오기
linktitle: 워크시트의 용지 너비와 높이 가져오기
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 스프레드시트의 용지 너비와 높이를 가져오는 다음 C# 소스 코드를 설명하는 단계별 가이드를 만듭니다.
type: docs
weight: 80
url: /ko/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 워크시트의 용지 너비와 높이를 가져오는 다음 C# 소스 코드를 단계별로 설명합니다. 아래 단계를 따르십시오.

## 1단계: 통합 문서 만들기
 다음을 사용하여 새 통합 문서를 만드는 것부터 시작하세요.`Workbook` 수업:

```csharp
Workbook wb = new Workbook();
```

## 2단계: 첫 번째 워크시트에 액세스
 다음으로, 통합 문서의 첫 번째 워크시트로 이동합니다.`Worksheet` 수업:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## 3단계: 용지 크기를 A2로 설정하고 용지 너비와 높이를 인치 단위로 표시합니다.
 사용`PaperSize` 의 재산`PageSetup` 개체를 사용하여 용지 크기를 A2로 설정한 다음`PaperWidth` 그리고`PaperHeight` 속성을 사용하여 용지 너비와 높이를 각각 가져옵니다. 다음을 사용하여 이러한 값을 표시합니다.`Console.WriteLine` 방법:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## 4단계: 다른 용지 크기에 대해 단계 반복
이전 단계를 반복하여 용지 크기를 A3, A4 및 Letter로 변경한 다음 각 크기에 대한 용지 너비 및 높이 값을 표시합니다.

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### .NET용 Aspose.Cells를 사용하여 워크시트의 용지 너비 및 높이 가져오기에 대한 샘플 소스 코드 

```csharp
//통합 문서 만들기
Workbook wb = new Workbook();
//첫 번째 워크시트에 액세스
Worksheet ws = wb.Worksheets[0];
//용지 크기를 A2로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//용지 크기를 A3으로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//용지 크기를 A4로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//용지 크기를 Letter로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## 결론

.NET용 Aspose.Cells를 사용하여 스프레드시트의 용지 너비와 높이를 얻는 방법을 배웠습니다. 이 기능은 Excel 문서의 구성 및 정확한 레이아웃에 유용할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### .NET용 Aspose.Cells란 무엇입니까?

Aspose.Cells for .NET은 .NET 애플리케이션에서 Excel 파일을 조작하고 처리하기 위한 강력한 라이브러리입니다. Excel 파일 생성, 수정, 변환 및 분석을 위한 다양한 기능을 제공합니다.

#### .NET용 Aspose.Cells를 사용하여 스프레드시트의 용지 크기를 어떻게 알 수 있나요?

 당신은 사용할 수 있습니다`PageSetup` 클래스의`Worksheet` 개체를 사용하여 용지 크기에 액세스합니다. 사용`PaperSize` 속성을 사용하여 용지 크기와`PaperWidth` 그리고`PaperHeight` 속성을 사용하여 용지 너비와 높이를 각각 가져옵니다.

#### .NET용 Aspose.Cells는 어떤 용지 크기를 지원합니까?

Aspose.Cells for .NET은 A2, A3, A4, Letter 등 일반적으로 사용되는 다양한 용지 크기와 기타 다양한 사용자 정의 크기를 지원합니다.

#### .NET용 Aspose.Cells를 사용하여 스프레드시트의 용지 크기를 사용자 정의할 수 있나요?

 예.`PaperWidth` 그리고`PaperHeight` 의 속성`PageSetup` 수업.