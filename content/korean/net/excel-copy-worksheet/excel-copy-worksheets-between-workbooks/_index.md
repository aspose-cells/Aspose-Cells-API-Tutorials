---
title: 통합 문서 간 Excel 복사 워크시트
linktitle: 통합 문서 간 Excel 복사 워크시트
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 통합 문서 간에 워크시트를 쉽게 복사할 수 있습니다.
type: docs
weight: 30
url: /ko/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
이 튜토리얼에서는 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 통합 문서 간에 워크시트를 복사하는 단계를 안내합니다. 이 작업을 완료하려면 아래 지침을 따르세요.

## 1단계: 준비

.NET용 Aspose.Cells를 설치하고 원하는 통합 개발 환경(IDE)에서 C# 프로젝트를 생성했는지 확인하세요.

## 2단계: 문서 디렉터리 경로 설정

 선언하다`dataDir` 변수를 지정하고 문서 디렉토리 경로로 초기화하세요. 예를 들어 :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 꼭 교체하세요`"YOUR_DOCUMENTS_DIRECTORY"` 디렉터리의 실제 경로를 사용합니다.

## 3단계: 입력 파일 경로 정의

 선언하다`InputPath` 변수를 복사하고 스프레드시트를 복사하려는 Excel 파일의 전체 경로로 초기화합니다. 예를 들어 :

```csharp
string InputPath = dataDir + "book1.xls";
```

 엑셀 파일이 있는지 확인하세요`book1.xls` 문서 디렉토리에 있거나 올바른 파일 이름과 위치를 지정하십시오.

## 4단계: 첫 번째 Excel 통합 문서 만들기

 사용`Workbook` Aspose.Cells 클래스를 사용하여 첫 번째 Excel 통합 문서를 만들고 지정된 파일을 엽니다.

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## 5단계: 두 번째 Excel 통합 문서 만들기

두 번째 Excel 통합 문서를 만듭니다.

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 6단계: 첫 번째 통합 문서의 워크시트를 두 번째 통합 문서에 복사합니다.

 사용`Copy`첫 번째 통합 문서의 첫 번째 워크시트를 두 번째 통합 문서로 복사하는 방법:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## 7단계: Excel 파일 저장

복사한 스프레드시트가 포함된 Excel 파일을 저장합니다.

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

출력 파일에 대해 원하는 경로와 파일 이름을 지정해야 합니다.

### .NET용 Aspose.Cells를 사용하여 통합 문서 간 Excel 복사 워크시트에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// 통합 문서를 만듭니다.
// 첫 번째 책에 파일을 엽니다.
Workbook excelWorkbook0 = new Workbook(InputPath);
// 다른 통합 문서를 만듭니다.
Workbook excelWorkbook1 = new Workbook();
// 첫 번째 책의 첫 번째 시트를 두 번째 책에 복사합니다.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// 파일을 저장합니다.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## 결론

축하합니다! 이제 Aspose.Cells for .NET을 사용하여 Excel 통합 문서 간에 워크시트를 복사하는 방법을 배웠습니다. 자신의 프로젝트에서 이 방법을 사용하여 Excel 파일을 효율적으로 조작할 수 있습니다.

### 자주 묻는 질문

#### Q. Aspose.Cells for .NET을 사용하려면 어떤 라이브러리가 필요합니까?

A. .NET용 Aspose.Cells를 사용하려면 프로젝트에 Aspose.Cells 라이브러리를 포함해야 합니다. 통합 개발 환경(IDE)에서 이 라이브러리를 올바르게 참조했는지 확인하세요.

#### Q. Aspose.Cells는 XLSX와 같은 다른 Excel 파일 형식을 지원합니까?

A. 예, Aspose.Cells는 XLSX, XLS, CSV, HTML 등을 포함한 다양한 Excel 파일 형식을 지원합니다. .NET용 Aspose.Cells의 기능을 사용하여 이러한 파일 형식을 조작할 수 있습니다.

#### Q. 스프레드시트를 복사할 때 레이아웃 옵션을 사용자 정의할 수 있나요?

A.  예, 스프레드시트를 복사할 때 속성을 사용하여 페이지 설정 옵션을 사용자 정의할 수 있습니다.`PageSetup` 물체. 페이지 머리글, 바닥글, 여백, 방향 등을 지정할 수 있습니다.