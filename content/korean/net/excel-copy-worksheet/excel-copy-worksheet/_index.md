---
title: Excel 복사 워크시트
linktitle: Excel 복사 워크시트
second_title: .NET API 참조용 Aspose.Cells
description: Aspose.Cells for .NET을 사용하여 하나의 Excel 워크시트를 다른 Excel 워크시트에 복사하세요.
type: docs
weight: 20
url: /ko/net/excel-copy-worksheet/excel-copy-worksheet/
---

이 가이드에서는 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 워크시트를 복사하는 방법을 설명합니다. C# 소스 코드를 제공하고 이 작업을 완료하는 데 필요한 단계를 안내해 드립니다. 마지막으로 예상되는 결과를 보여드리겠습니다. 시작하려면 아래 지침을 따르세요.

## 1단계: 준비

시작하기 전에 .NET용 Aspose.Cells를 설치하고 원하는 IDE(통합 개발 환경)에서 C# 프로젝트를 생성했는지 확인하세요. 또한 조작하려는 Excel 파일의 복사본이 있는지 확인하십시오.

## 2단계: 필수 라이브러리 가져오기

 C# 소스 파일에서 다음을 사용하여 Aspose.Cells에서 필요한 라이브러리를 가져옵니다.`using` 지령:

```csharp
using Aspose.Cells;
```

## 3단계: 파일 경로 설정

 선언하다`dataDir` 변수를 선택하고 Excel 파일이 포함된 디렉터리로 초기화하세요. 예를 들어 :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 꼭 교체하세요`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` 디렉터리의 실제 경로를 사용합니다.

## 4단계: 기존 Excel 파일 로드

 사용`Workbook` Aspose.Cells의 클래스를 사용하여 기존 Excel 파일을 엽니다. 사용`InputPath` 파일 경로를 지정하는 변수:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 교체했는지 확인하세요`"book1.xls"` Excel 파일의 실제 이름으로.

## 5단계: 워크시트 복사

 이제 기존 워크시트를 새 워크시트에 복사하겠습니다. 사용`Worksheets` 의 재산`Workbook` 워크시트 컬렉션에 액세스하는 개체:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 그런 다음`AddCopy` 지정된 워크시트를 복사하는 방법입니다. 예를 들어 "Sheet1"을 복사하려면 다음을 수행합니다.

```csharp
sheets.AddCopy("Sheet1");
```

## 6단계: Excel 파일 저장

 사용`Save` 의 방법`Workbook` 새 파일에 대한 변경 사항을 저장하는 개체:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

출력 파일에 대해 원하는 경로와 파일 이름을 지정해야 합니다.

### .NET용 Aspose.Cells를 사용하는 Excel 복사 워크시트의 샘플 소스 코드 

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// 기존 Excel 파일을 엽니다.
Workbook wb = new Workbook(InputPath);
// 다음을 참조하여 Worksheets 개체를 만듭니다.
// 통합 문서의 시트.
WorksheetCollection sheets = wb.Worksheets;
// 기존 시트에서 새 시트로 데이터 복사
// 통합 문서 내의 시트.
sheets.AddCopy("Sheet1");
// 엑셀 파일을 저장합니다.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## 결론

축하합니다! 이제 Aspose.Cells for .NET을 사용하여 Excel 워크시트를 복사하는 방법을 배웠습니다. 이 단계별 가이드에서는 필요한 라이브러리를 가져오고, 기존 Excel 파일을 로드하고, 워크시트를 복사하고, 수정된 파일을 저장하는 방법을 보여주었습니다. 자신의 프로젝트에서 이 방법을 사용하여 Excel 파일을 효율적으로 조작할 수 있습니다.

### 자주 묻는 질문

#### Q. Aspose.Cells는 다른 프로그래밍 언어와 호환됩니까?

A. 예, Aspose.Cells는 C#, Java, Python 등을 포함한 다양한 프로그래밍 언어를 지원합니다.

#### Q. 워크시트를 다른 Excel 통합 문서에 복사할 수 있나요?

A.  예, 다음을 사용할 수 있습니다.`AddCopy` 워크시트를 다른 Excel 통합 문서로 복사하는 방법입니다.

#### Q. Aspose.Cells는 워크시트를 복사할 때 수식과 서식을 유지합니까?

A. 예, Aspose.Cells는 워크시트를 복사할 때 수식, 서식 및 기타 속성을 유지합니다.

#### Q. Aspose.Cells를 상업적으로 사용하려면 라이선스가 필요합니까?

A. 예, Aspose.Cells는 상업용 제품이며 상업용으로 사용하려면 라이센스를 구매해야 합니다. Aspose 공식 웹사이트에서 더 많은 라이선스 정보를 확인할 수 있습니다.