---
title: 다른 통합 문서에서 Excel 복사 워크시트
linktitle: 다른 통합 문서에서 Excel 복사 워크시트
second_title: .NET API 참조용 Aspose.Cells
description: Aspose.Cells for .NET을 사용하여 한 통합 문서에서 다른 통합 문서로 Excel 워크시트를 쉽게 복사할 수 있습니다.
type: docs
weight: 10
url: /ko/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
이 튜토리얼에서는 .NET용 Aspose.Cells 라이브러리를 사용하여 다른 통합 문서에서 Excel 워크시트를 복사하는 단계를 안내합니다. 이 작업을 완료하려면 아래 지침을 따르세요.

## 1단계: 준비

시작하기 전에 .NET용 Aspose.Cells를 설치하고 원하는 통합 개발 환경(IDE)에서 C# 프로젝트를 생성했는지 확인하세요.

## 2단계: 문서 디렉터리 경로 설정

 선언하다`dataDir` 변수를 지정하고 문서 디렉토리 경로로 초기화하세요. 예를 들어 :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 꼭 교체하세요`"YOUR_DOCUMENTS_DIRECTORY"` 디렉터리의 실제 경로를 사용합니다.

## 3단계: 새 Excel 통합 문서 만들기

 사용`Workbook` Aspose.Cells의 클래스를 사용하여 새 Excel 통합 문서를 만듭니다.

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## 4단계: 통합 문서의 첫 번째 워크시트 가져오기

인덱스 0을 사용하여 통합 문서의 첫 번째 워크시트로 이동합니다.

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## 5단계: 머리글 행(A1:A4)에 데이터 추가

 사용`for` 헤더 행(A1:A4)에 데이터를 추가하는 루프:

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## 6단계: 세부 데이터 추가(A5:A999)

 다른 것을 사용하세요`for` 자세한 데이터를 추가하는 루프(A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## 7단계: 레이아웃 옵션 설정

 다음을 사용하여 워크시트의 페이지 설정 옵션을 설정합니다.`PageSetup` 물체:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## 8단계: 다른 Excel 통합 문서 만들기

다른 Excel 통합 문서를 만듭니다.

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 9단계: 두 번째 통합 문서에서 첫 번째 워크시트 가져오기

두 번째 통합 문서의 첫 번째 워크시트로 이동합니다.

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## 10단계: 워크시트 이름 지정

불에 이름을 붙여라

계산 섬:

```csharp
ws1.Name = "MySheet";
```

## 11단계: 첫 번째 통합 문서의 첫 번째 워크시트에서 두 번째 통합 문서의 첫 번째 워크시트로 데이터 복사

첫 번째 통합 문서의 첫 번째 워크시트에 있는 데이터를 두 번째 통합 문서의 첫 번째 워크시트에 복사합니다.

```csharp
ws1.Copy(ws0);
```

## 12단계: Excel 파일 저장

Excel 파일을 저장합니다.

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

출력 파일에 대해 원하는 경로와 파일 이름을 지정해야 합니다.

### .NET용 Aspose.Cells를 사용하여 다른 통합 문서의 Excel 복사 워크시트에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 새 통합 문서를 만듭니다.
Workbook excelWorkbook0 = new Workbook();
// 책의 첫 번째 워크시트를 가져옵니다.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// 일부 데이터를 헤더 행(A1:A4)에 넣습니다.
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// 세부 데이터 입력(A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// 첫 번째 워크시트를 기반으로 페이지 설정 개체를 정의합니다.
PageSetup pagesetup = ws0.PageSetup;
// 처음 5개 행은 각 페이지에서 반복됩니다.
// 인쇄 미리보기에서 볼 수 있습니다.
pagesetup.PrintTitleRows = "$1:$5";
// 다른 통합 문서를 만듭니다.
Workbook excelWorkbook1 = new Workbook();
// 책의 첫 번째 워크시트를 가져옵니다.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// 워크시트의 이름을 지정합니다.
ws1.Name = "MySheet";
// 첫 번째 통합 문서의 첫 번째 워크시트에서 데이터를 복사합니다.
// 두 번째 통합 문서의 첫 번째 워크시트입니다.
ws1.Copy(ws0);
// 엑셀 파일을 저장합니다.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## 결론

축하합니다! 이제 Aspose.Cells for .NET을 사용하여 다른 통합 문서에서 Excel 워크시트를 복사하는 방법을 배웠습니다. 자신의 프로젝트에서 이 방법을 사용하여 Excel 파일을 효율적으로 조작할 수 있습니다.

### 자주 묻는 질문

#### Q. Aspose.Cells for .NET을 사용하려면 어떤 라이브러리가 필요합니까?

A. .NET용 Aspose.Cells를 사용하려면 프로젝트에 Aspose.Cells 라이브러리를 포함해야 합니다. 통합 개발 환경(IDE)에서 이 라이브러리를 올바르게 참조했는지 확인하세요.

#### Q. Aspose.Cells는 XLSX와 같은 다른 Excel 파일 형식을 지원합니까?

A. 예, Aspose.Cells는 XLSX, XLS, CSV, HTML 등을 포함한 다양한 Excel 파일 형식을 지원합니다. .NET용 Aspose.Cells의 기능을 사용하여 이러한 파일 형식을 조작할 수 있습니다.

#### Q. 워크시트를 복사할 때 레이아웃 옵션을 사용자 지정할 수 있나요?

A.  예, 워크시트를 복사할 때 속성을 사용하여 페이지 설정 옵션을 사용자 정의할 수 있습니다.`PageSetup` 물체. 페이지 머리글, 바닥글, 여백, 방향 등을 지정할 수 있습니다.