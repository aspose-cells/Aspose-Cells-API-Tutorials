---
title: Excel 용지 크기 관리
linktitle: Excel 용지 크기 관리
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel에서 용지 크기를 관리하는 방법을 알아보세요. C#의 소스 코드가 포함된 단계별 튜토리얼입니다.
type: docs
weight: 70
url: /ko/net/excel-page-setup/manage-excel-paper-size/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 Excel 문서에서 용지 크기를 관리하는 방법을 단계별로 안내합니다. C# 소스 코드를 사용하여 용지 크기를 구성하는 방법을 보여 드리겠습니다.

## 1단계: 환경 설정

컴퓨터에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. 또한 원하는 개발 환경에서 새 프로젝트를 만듭니다.

## 2단계: 필요한 라이브러리 가져오기

코드 파일에서 Aspose.Cells 작업에 필요한 라이브러리를 가져옵니다. 해당 코드는 다음과 같습니다.

```csharp
using Aspose.Cells;
```

## 3단계: 문서 디렉터리 설정

작업하려는 Excel 문서가 있는 디렉터리를 설정합니다. 다음 코드를 사용하여 디렉터리를 설정합니다.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

전체 디렉터리 경로를 지정해야 합니다.

## 4단계: 통합 문서 개체 만들기

Workbook 개체는 작업할 Excel 문서를 나타냅니다. 다음 코드를 사용하여 만들 수 있습니다.

```csharp
Workbook workbook = new Workbook();
```

그러면 새로운 빈 통합 문서 개체가 생성됩니다.

## 5단계: 첫 번째 워크시트에 액세스

Excel 문서의 첫 번째 스프레드시트에 액세스하려면 다음 코드를 사용하십시오.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

이렇게 하면 통합 문서의 첫 번째 워크시트로 작업할 수 있습니다.

## 6단계: 용지 크기 설정

Worksheet 개체의 PageSetup.PaperSize 속성을 사용하여 용지 크기를 설정합니다. 이 예에서는 용지 크기를 A4로 설정하겠습니다. 해당 코드는 다음과 같습니다.

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

그러면 스프레드시트 용지 크기가 A4로 설정됩니다.

## 7단계: 통합 문서 저장

통합 문서에 대한 변경 사항을 저장하려면 Workbook 개체의 Save() 메서드를 사용합니다. 해당 코드는 다음과 같습니다.

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

그러면 지정된 디렉터리에 대한 변경 사항이 포함된 통합 문서가 저장됩니다.

### .NET용 Aspose.Cells를 사용하여 Excel 용지 크기 관리에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
// 용지 크기를 A4로 설정
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// 통합 문서를 저장합니다.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## 결론

이제 Aspose.Cells for .NET을 사용하여 Excel 문서에서 용지 크기를 관리하는 방법을 배웠습니다. 이 튜토리얼에서는 환경 설정부터 변경 사항 저장까지 프로세스의 모든 단계를 안내했습니다. 이제 이 지식을 사용하여 Excel 문서의 용지 크기를 사용자 지정할 수 있습니다.

### FAQ

#### Q1: A4 이외의 사용자 정의 용지 크기를 설정할 수 있습니까?

A1: 예, Aspose.Cells는 미리 정의된 다양한 용지 크기는 물론 원하는 치수를 지정하여 사용자 정의 용지 크기를 설정하는 기능도 지원합니다.

#### Q2: Excel 문서의 현재 용지 크기를 어떻게 알 수 있나요?

 A2: 다음을 사용할 수 있습니다.`PageSetup.PaperSize` 의 재산`Worksheet` 현재 설정된 용지 크기를 가져오는 개체입니다.

#### Q3: 용지 크기에 따라 추가 페이지 여백을 설정할 수 있습니까?

 A3: 그렇습니다, 당신은 사용할 수 있습니다`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` 그리고`PageSetup.BottomMargin` 용지 크기 외에 추가 페이지 여백을 설정하는 속성입니다.

#### 질문 4: 이 방법은 .xls 및 .xlsx와 같은 모든 Excel 파일 형식에 적용됩니까?

답변 4: 예, 이 방법은 .xls 및 .xlsx 파일 형식 모두에 적용됩니다.

#### 질문 5: 동일한 통합 문서의 서로 다른 워크시트에 서로 다른 용지 크기를 적용할 수 있나요?

 A5: 예.`PageSetup.PaperSize` 각 워크시트의 속성입니다.