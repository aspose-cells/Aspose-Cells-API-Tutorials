---
title: 페이지 크기 가져오기
linktitle: 페이지 크기 가져오기
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel에서 페이지 크기를 검색하는 방법을 알아보세요. C#의 소스 코드를 단계별로 안내합니다.
type: docs
weight: 40
url: /ko/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET은 개발자가 Microsoft Excel 파일을 프로그래밍 방식으로 작업할 수 있는 강력한 라이브러리입니다. 페이지 크기를 가져오는 기능을 포함하여 Excel 문서를 조작하기 위한 다양한 기능을 제공합니다. 이 튜토리얼에서는 .NET용 Aspose.Cells를 사용하여 페이지 크기를 검색하는 단계를 안내합니다.

## 1단계: Workbook 클래스의 인스턴스 만들기

시작하려면 Excel 통합 문서를 나타내는 Workbook 클래스의 인스턴스를 만들어야 합니다. 이는 다음 코드를 사용하여 달성할 수 있습니다.

```csharp
Workbook book = new Workbook();
```

## 2단계: 스프레드시트에 액세스하기

다음으로 페이지 크기를 설정하려는 통합 문서의 워크시트로 이동해야 합니다. 이 예에서는 첫 번째 워크시트로 작업한다고 가정합니다. 다음 코드를 사용하여 액세스할 수 있습니다.

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 3단계: 용지 크기를 A2로 설정하고 인쇄 너비와 높이를 인치 단위로 설정합니다.

이제 용지 크기를 A2로 설정하고 페이지 너비와 높이를 인치 단위로 인쇄하겠습니다. 이는 다음 코드를 사용하여 달성할 수 있습니다.

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 4단계: 용지 크기를 A3으로 설정하고 인쇄 너비와 높이(인치)를 설정합니다.

다음으로 용지 크기를 A3으로 설정하고 페이지 너비와 높이를 인치 단위로 인쇄하겠습니다. 해당 코드는 다음과 같습니다.

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 5단계: 용지 크기를 A4로 설정하고 인쇄 너비와 높이(인치)를 설정합니다.

이제 용지 크기를 A4로 설정하고 페이지 너비와 높이를 인치 단위로 인쇄하겠습니다. 코드는 다음과 같습니다.

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 6단계: 용지 크기를 Letter로 설정하고 너비와 높이를 인치 단위로 인쇄합니다.

마지막으로 용지 크기를 Letter로 설정하고 페이지 너비와 높이를 인치 단위로 인쇄합니다. 코드는 다음과 같습니다.

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### .NET용 Aspose.Cells를 사용하여 페이지 차원 가져오기의 샘플 소스 코드 
```csharp
// Workbook 클래스의 인스턴스 만들기
Workbook book = new Workbook();
// 첫 번째 워크시트에 액세스
Worksheet sheet = book.Worksheets[0];
// 용지 크기를 A2로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// 용지 크기를 A3으로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// 용지 크기를 A4로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// 용지 크기를 Letter로 설정하고 용지 너비와 높이를 인치 단위로 인쇄합니다.
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 페이지 크기를 검색하는 방법을 배웠습니다. 이 기능은 Excel 파일의 페이지 크기를 기반으로 특정 작업을 수행해야 할 때 유용할 수 있습니다.

Aspose.Cells가 제공하는 모든 강력한 기능을 알아보려면 Aspose.Cells의 문서를 더 자세히 살펴보세요.

### FAQ

#### 1. Aspose.Cells for .NET은 어떤 다른 용지 크기를 지원합니까?

.NET용 Aspose.Cells는 A1, A5, B4, B5, Executive, Legal, Letter 등을 포함한 다양한 용지 크기를 지원합니다. 지원되는 용지 크기의 전체 목록은 설명서를 확인하세요.

#### 2. .NET용 Aspose.Cells를 사용하여 사용자 정의 페이지 크기를 설정할 수 있습니까?

예, 원하는 너비와 높이를 지정하여 사용자 정의 페이지 크기를 설정할 수 있습니다. Aspose.Cells는 귀하의 필요에 맞게 페이지 크기를 사용자 정의할 수 있는 완전한 유연성을 제공합니다.

#### 3. 인치가 아닌 다른 단위로 페이지 치수를 얻을 수 있나요?

예, .NET용 Aspose.Cells를 사용하면 인치, 센티미터, 밀리미터, 포인트 등 다양한 단위로 페이지 치수를 얻을 수 있습니다.

#### 4. .NET용 Aspose.Cells는 다른 페이지 설정 편집 기능을 지원합니까?

예, Aspose.Cells는 여백, 방향, 머리글 및 바닥글 설정 등을 포함하여 페이지 설정 편집을 위한 모든 기능을 제공합니다.