---
title: Excel 첫 페이지 번호 설정
linktitle: Excel 첫 페이지 번호 설정
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel에서 첫 번째 페이지 번호를 설정하는 방법을 알아보세요.
type: docs
weight: 90
url: /ko/net/excel-page-setup/set-excel-first-page-number/
---
이 튜토리얼에서는 .NET용 Aspose.Cells를 사용하여 Excel에서 첫 번째 페이지 번호를 설정하는 방법을 안내합니다. 프로세스를 설명하기 위해 C# 소스 코드를 사용하겠습니다.

## 1단계: 환경 설정

컴퓨터에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. 또한 원하는 개발 환경에서 새 프로젝트를 만듭니다.

## 2단계: 필요한 라이브러리 가져오기

코드 파일에서 Aspose.Cells 작업에 필요한 라이브러리를 가져옵니다. 해당 코드는 다음과 같습니다.

```csharp
using Aspose.Cells;
```

## 3단계: 데이터 디렉터리 설정

수정된 엑셀 파일을 저장할 데이터 디렉터리를 설정합니다. 다음 코드를 사용하세요.

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

전체 디렉터리 경로를 지정해야 합니다.

## 4단계: 통합 문서 및 워크시트 만들기

새 Workbook 개체를 만들고 다음 코드를 사용하여 통합 문서의 첫 번째 워크시트로 이동합니다.

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

이렇게 하면 워크시트가 포함된 빈 통합 문서가 생성됩니다.

## 5단계: 첫 번째 페이지 번호 설정

다음 코드를 사용하여 워크시트 페이지의 첫 번째 페이지 번호를 설정합니다.

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

그러면 첫 번째 페이지 번호가 2로 설정됩니다.

## 6단계: 수정된 통합 문서 저장

다음 코드를 사용하여 수정된 통합 문서를 저장합니다.

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

그러면 수정된 통합 문서가 지정된 데이터 디렉터리에 저장됩니다.

### .NET용 Aspose.Cells를 사용하여 Excel 첫 페이지 번호 설정에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
// 워크시트 페이지의 첫 번째 페이지 번호 설정
worksheet.PageSetup.FirstPageNumber = 2;
// 통합 문서를 저장합니다.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## 결론

이제 .NET용 Aspose.Cells를 사용하여 Excel에서 첫 번째 페이지 번호를 설정하는 방법을 배웠습니다. 이 튜토리얼에서는 환경 설정부터 첫 번째 페이지 번호 설정까지 프로세스의 모든 단계를 안내했습니다. 이제 이 지식을 사용하여 Excel 파일의 페이지 번호 매기기를 사용자 지정할 수 있습니다.

### FAQ

#### Q1: 워크시트마다 첫 번째 페이지 번호를 다르게 설정할 수 있나요?

 A1: 예.`FirstPageNumber`해당 워크시트의 속성`PageSetup` 물체.

#### Q2: 기존 스프레드시트의 첫 번째 페이지 번호를 어떻게 확인할 수 있나요?

 A2: 기존 워크시트의 첫 번째 페이지 번호는`FirstPageNumber` 의 재산`PageSetup` 해당 워크시트에 해당하는 개체입니다.

#### Q3: 페이지 번호 매기기는 기본적으로 항상 1부터 시작합니까?

A3: 예, Excel에서는 페이지 번호 매기기가 기본적으로 1부터 시작됩니다. 그러나 이 자습서에 표시된 코드를 사용하여 다른 첫 번째 페이지 번호를 설정할 수 있습니다.

#### Q4: 편집된 Excel 파일의 첫 번째 페이지 번호에 대한 변경 사항은 영구적입니까?

A4: 예, 첫 번째 페이지 번호에 대한 변경 사항은 수정된 Excel 파일에 영구적으로 저장됩니다.

#### 질문 5: 이 방법은 .xls 및 .xlsx와 같은 모든 Excel 파일 형식에 작동합니까?

A5: 예, 이 방법은 .xls 및 .xlsx를 포함하여 Aspose.Cells에서 지원하는 모든 Excel 파일 형식에 작동합니다.