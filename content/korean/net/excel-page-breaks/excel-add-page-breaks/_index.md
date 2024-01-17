---
title: Excel 페이지 나누기 추가
linktitle: Excel 페이지 나누기 추가
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel에서 페이지 나누기를 추가하는 방법을 알아보세요. 잘 구성된 보고서를 생성하기 위한 단계별 튜토리얼입니다.
type: docs
weight: 10
url: /ko/net/excel-page-breaks/excel-add-page-breaks/
---
Excel 파일에 페이지 나누기를 추가하는 것은 대규모 보고서나 문서를 작성할 때 필수적인 기능입니다. 이 튜토리얼에서는 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 파일에 페이지 나누기를 추가하는 방법을 살펴보겠습니다. 제공된 C# 소스 코드를 이해하고 구현할 수 있도록 단계별로 안내해 드립니다.

## 1단계: 환경 준비

 시작하기 전에 컴퓨터에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. 라이브러리는 다음에서 다운로드할 수 있습니다.[Aspose 릴리스](https://releases.aspose.com/cells/net)제공된 지침에 따라 설치하세요.

설치가 완료되면 원하는 통합 개발 환경(IDE)에서 새 C# 프로젝트를 만들고 .NET용 Aspose.Cells 라이브러리를 가져옵니다.

## 2단계: 문서 디렉터리 경로 구성

 제공된 소스 코드에서 생성된 Excel 파일을 저장할 디렉터리 경로를 지정해야 합니다. 수정하다`dataDir` "YOUR DOCUMENT DIRECTORY"를 컴퓨터에 있는 디렉터리의 절대 경로로 바꿔 변수를 지정합니다.

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## 3단계: 통합 문서 개체 만들기

시작하려면 Excel 파일을 나타내는 통합 문서 개체를 만들어야 합니다. 이는 Aspose.Cells에서 제공하는 Workbook 클래스를 사용하여 달성할 수 있습니다.

```csharp
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
```

## 4단계: 가로 페이지 나누기 추가

이제 Excel 워크시트에 가로 페이지 나누기를 추가해 보겠습니다. 샘플 코드에서는 첫 번째 워크시트의 "Y30" 셀에 가로 페이지 나누기를 추가합니다.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
```

## 5단계: 세로 페이지 나누기 추가

마찬가지로, 다음을 사용하여 세로 페이지 나누기를 추가할 수 있습니다.`VerticalPageBreaks.Add()` 방법. 이 예에서는 첫 번째 워크시트의 "Y30" 셀에 세로 페이지 나누기를 추가합니다.

```csharp
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
```

## 6단계: Excel 파일 저장

 이제 페이지 나누기를 추가했으므로 최종 Excel 파일을 저장해야 합니다. 사용`Save()` 출력 파일의 전체 경로를 지정하는 방법입니다.

```csharp
// 엑셀 파일을 저장합니다.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```
### .NET용 Aspose.Cells를 사용하여 Excel 추가 페이지 나누기용 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// Y30 셀에 페이지 나누기 추가
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
// 엑셀 파일을 저장합니다.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```

## 결론

이 튜토리얼에서는 중단을 추가하는 방법을 배웠습니다.

  .NET용 Aspose.Cells를 사용하여 Excel 파일의 페이지. 제공된 단계를 따르면 동적으로 생성된 Excel 파일에 가로 및 세로 페이지 나누기를 쉽게 삽입할 수 있습니다. Aspose.Cells 라이브러리를 더 많이 실험하여 그것이 제공하는 다른 강력한 기능을 찾아보세요.

### 자주 묻는 질문

#### Q: Aspose.Cells for .NET은 무료 라이브러리입니까?

A: Aspose.Cells for .NET은 상용 라이브러리이지만 기능을 평가하는 데 사용할 수 있는 무료 평가판을 제공합니다.

#### Q: Excel 파일에 여러 페이지 나누기를 추가할 수 있나요?

A: 예, 스프레드시트의 여러 부분에 필요한 만큼 페이지 나누기를 추가할 수 있습니다.

#### Q: 이전에 추가한 페이지 나누기를 제거할 수 있나요?

A: 예, Aspose.Cells를 사용하면 Worksheet 개체의 적절한 방법을 사용하여 기존 페이지 나누기를 제거할 수 있습니다.

#### Q: 이 방법은 XLSX 또는 XLSM과 같은 다른 Excel 파일 형식에서도 작동합니까?

A: 예, 이 튜토리얼에서 설명하는 방법은 Aspose.Cells가 지원하는 다양한 Excel 파일 형식에서 작동합니다.

#### Q: Excel에서 페이지 나누기 모양을 사용자 지정할 수 있나요?

A: 예, Aspose.Cells는 스타일, 색상, 크기 등 페이지 나누기를 사용자 정의할 수 있는 다양한 기능을 제공합니다.
