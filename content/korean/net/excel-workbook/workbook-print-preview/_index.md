---
title: 통합 문서 인쇄 미리보기
linktitle: 통합 문서 인쇄 미리보기
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 통합 문서의 인쇄 미리 보기를 생성하는 방법을 알아보세요.
type: docs
weight: 170
url: /ko/net/excel-workbook/workbook-print-preview/
---
통합 문서의 인쇄 미리 보기는 Aspose.Cells for .NET을 사용하여 Excel 파일로 작업할 때 필수적인 기능입니다. 다음 단계에 따라 인쇄 미리보기를 쉽게 생성할 수 있습니다.

## 1단계: 소스 디렉터리 지정

먼저 미리 보려는 Excel 파일이 있는 소스 디렉터리를 지정해야 합니다. 수행 방법은 다음과 같습니다.

```csharp
// 소스 디렉토리
string sourceDir = RunExamples.Get_SourceDirectory();
```

## 2단계: 통합 문서 로드

그런 다음 지정된 Excel 파일에서 통합 문서 통합 문서를 로드해야 합니다. 수행 방법은 다음과 같습니다.

```csharp
// 통합 문서 통합 문서 로드
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## 3단계: 이미지 및 인쇄 옵션 구성

인쇄 미리보기를 생성하기 전에 필요에 따라 이미지와 인쇄 옵션을 구성할 수 있습니다. 이 예에서는 기본 옵션을 사용하고 있습니다. 수행 방법은 다음과 같습니다.

```csharp
// 이미지 및 인쇄 옵션
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## 4단계: 통합 문서의 인쇄 미리 보기 생성

이제 WorkbookPrintingPreview 클래스를 사용하여 통합 문서 통합 문서의 인쇄 미리 보기를 생성할 수 있습니다. 수행 방법은 다음과 같습니다.

```csharp
// 통합 문서의 인쇄 미리 보기
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## 5단계: 워크시트의 인쇄 미리 보기 생성

특정 워크시트의 인쇄 미리 보기를 생성하려면 SheetPrintingPreview 클래스를 사용할 수 있습니다. 예는 다음과 같습니다.

```csharp
// 워크시트의 인쇄 미리보기
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### .NET용 Aspose.Cells를 사용하는 통합 문서 인쇄 미리 보기의 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## 결론

통합 문서의 인쇄 미리 보기를 생성하는 것은 Aspose.Cells for .NET에서 제공하는 강력한 기능입니다. 위에 제공된 단계를 수행하면 Excel 통합 문서를 쉽게 미리 보고 인쇄할 페이지 수에 대한 정보를 얻을 수 있습니다.

### 자주 묻는 질문

#### Q: 내 통합 문서를 로드하기 위해 다른 소스 디렉터리를 어떻게 지정합니까?
    
 A: 다음을 사용할 수 있습니다.`Set_SourceDirectory` 다른 소스 디렉터리를 지정하는 방법입니다. 예를 들어:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Q: 인쇄 미리보기를 생성할 때 이미지와 인쇄 옵션을 사용자 정의할 수 있습니까?
    
 A: 예, 속성을 변경하여 이미지와 인쇄 옵션을 사용자 정의할 수 있습니다.`ImageOrPrintOptions` 물체. 예를 들어 이미지 해상도, 출력 파일 형식 등을 설정할 수 있습니다.

#### Q: 통합 문서의 여러 워크시트에 대한 인쇄 미리 보기를 생성할 수 있습니까?
    
A: 예, 통합 문서의 다양한 워크시트를 반복하고 다음을 사용하여 각 시트에 대한 인쇄 미리 보기를 생성할 수 있습니다.`SheetPrintingPreview` 수업.

#### Q: 인쇄 미리보기를 이미지나 PDF 파일로 저장하려면 어떻게 해야 하나요?
    
 A: 당신은 사용할 수 있습니다`ToImage` 또는`ToPdf` 의 방법`WorkbookPrintingPreview` 또는`SheetPrintingPreview` 인쇄 미리보기를 이미지나 PDF 파일로 저장하는 개체입니다.

#### Q: 생성된 인쇄 미리보기로 무엇을 할 수 있나요?
    
A: 인쇄 미리보기를 생성하면 화면에서 볼 수 있고, 이미지나 PDF 파일로 저장하거나, 이메일로 전송하거나 인쇄하는 등 다른 작업에 사용할 수 있습니다.
	