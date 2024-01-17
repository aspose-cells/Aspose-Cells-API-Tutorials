---
title: 렌더링을 위한 워크시트의 사용자 정의 용지 크기 구현
linktitle: 렌더링을 위한 워크시트의 사용자 정의 용지 크기 구현
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 사용자 정의 워크시트 크기를 구현하기 위한 단계별 가이드입니다. 크기를 설정하고 메시지를 추가한 후 PDF로 저장하세요.
type: docs
weight: 50
url: /ko/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
워크시트에 대한 사용자 정의 크기를 구현하는 것은 특정 크기의 PDF 문서를 생성하려는 경우 매우 유용할 수 있습니다. 이 튜토리얼에서는 .NET용 Aspose.Cells를 사용하여 워크시트의 사용자 정의 크기를 설정한 다음 문서를 PDF로 저장하는 방법을 알아봅니다.

## 1단계: 출력 폴더 만들기

시작하기 전에 생성된 PDF 파일을 저장할 출력 폴더를 만들어야 합니다. 출력 폴더에 대해 원하는 경로를 사용할 수 있습니다.

```csharp
// 출력 디렉터리
string outputDir = "YOUR_OUTPUT_FOLDER";
```

출력 폴더에 대한 올바른 경로를 지정했는지 확인하십시오.

## 2단계: 통합 문서 개체 만들기

시작하려면 Aspose.Cells를 사용하여 통합 문서 개체를 만들어야 합니다. 이 개체는 스프레드시트를 나타냅니다.

```csharp
// 통합 문서 개체 만들기
Workbook wb = new Workbook();
```

## 3단계: 첫 번째 워크시트에 액세스

Workbook 개체를 생성한 후 해당 개체 내의 첫 번째 워크시트에 액세스할 수 있습니다.

```csharp
// 첫 번째 워크시트에 액세스
Worksheet ws = wb.Worksheets[0];
```

## 4단계: 사용자 정의 워크시트 크기 설정

 이제 다음을 사용하여 사용자 정의 워크시트 크기를 설정할 수 있습니다.`CustomPaperSize(width, height)` PageSetup 클래스의 메서드입니다.

```csharp
// 사용자 정의 워크시트 크기 설정(인치)
ws.PageSetup.CustomPaperSize(6, 4);
```

이 예에서는 워크시트 크기를 너비 6인치, 높이 4인치로 설정했습니다.

## 5단계: B4 셀에 액세스

그런 다음 워크시트의 특정 셀에 액세스할 수 있습니다. 이 경우 셀 B4에 액세스합니다.

```csharp
// 셀 B4에 대한 액세스
Cell b4 = ws.Cells["B4"];
```

## 6단계: B4 셀에 메시지 추가

 이제 다음을 사용하여 셀 B4에 메시지를 추가할 수 있습니다.`PutValue(value)` 방법.

```csharp
// B4 셀에 메시지를 추가하세요.
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

이 예에서는 셀 B4에 "PDF 페이지 크기: 6.00" x 4.00"이라는 메시지를 추가했습니다.

## 7단계: 워크시트를 PDF 형식으로 저장

 마지막으로 다음을 사용하여 워크시트를 PDF 형식으로 저장할 수 있습니다.`Save(filePath)` Workbook 개체의 메서드입니다.

```csharp
// 워크시트를 PDF 형식으로 저장
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

이전에 생성된 출력 폴더를 사용하여 생성된 PDF 파일에 대한 원하는 경로를 지정합니다.

### .NET용 Aspose.Cells를 사용하여 렌더링하기 위한 워크시트의 사용자 정의 용지 크기를 구현하기 위한 샘플 소스 코드 
```csharp
//출력 디렉토리
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//통합 문서 개체 만들기
Workbook wb = new Workbook();
//첫 번째 워크시트에 액세스
Worksheet ws = wb.Worksheets[0];
//인치 단위로 사용자 정의 용지 크기 설정
ws.PageSetup.CustomPaperSize(6, 4);
//셀 B4에 액세스
Cell b4 = ws.Cells["B4"];
//B4 셀에 메시지를 추가하세요.
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//통합 문서를 PDF 형식으로 저장
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## 결론

이 튜토리얼에서는 .NET용 Aspose.Cells를 사용하여 워크시트의 사용자 정의 크기를 구현하는 방법을 배웠습니다. 다음 단계를 사용하여 워크시트의 특정 치수를 설정한 다음 문서를 PDF 형식으로 저장할 수 있습니다. 이 가이드가 사용자 정의 스프레드시트 크기를 구현하는 프로세스를 이해하는 데 도움이 되었기를 바랍니다.

### 자주 묻는 질문(FAQ)

#### 질문 1: 스프레드시트 레이아웃을 추가로 사용자 정의할 수 있습니까?

예, Aspose.Cells는 워크시트 레이아웃을 사용자 정의할 수 있는 다양한 옵션을 제공합니다. 사용자 정의 크기, 페이지 방향, 여백, 머리글 및 바닥글 등을 설정할 수 있습니다.

#### 질문 2: Aspose.Cells는 어떤 다른 출력 형식을 지원합니까?

Aspose.Cells는 PDF, XLSX, XLS, CSV, HTML, TXT 등을 포함한 다양한 출력 형식을 지원합니다. 필요에 따라 원하는 출력 형식을 선택할 수 있습니다.