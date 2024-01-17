---
title: Excel 배율 인수 설정
linktitle: Excel 배율 인수 설정
second_title: .NET API 참조용 Aspose.Cells
description: Excel 파일을 쉽게 조작하고 Aspose.Cells for .NET을 사용하여 배율을 사용자 정의하는 방법을 알아보세요.
type: docs
weight: 180
url: /ko/net/excel-page-setup/set-excel-scaling-factor/
---
이 가이드에서는 .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 배율 인수를 설정하는 방법을 안내합니다. 이 작업을 수행하려면 아래 단계를 따르십시오.

## 1단계: 환경 설정

개발 환경을 설정하고 .NET용 Aspose.Cells를 설치했는지 확인하세요. Aspose 공식 웹사이트에서 최신 버전의 라이브러리를 다운로드할 수 있습니다.

## 2단계: 필수 네임스페이스 가져오기

C# 프로젝트에서 Aspose.Cells 작업에 필요한 네임스페이스를 가져옵니다.

```csharp
using Aspose.Cells;
```

## 3단계: 문서 디렉터리 경로 설정

 선언하다`dataDir` 생성된 Excel 파일을 저장할 디렉터리의 경로를 지정하는 변수:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 꼭 교체하세요`"YOUR_DOCUMENT_DIRECTORY"` 시스템의 올바른 경로를 사용하십시오.

## 4단계: 통합 문서 개체 만들기

만들려는 Excel 통합 문서를 나타내는 Workbook 개체를 인스턴스화합니다.

```csharp
Workbook workbook = new Workbook();
```

## 5단계: 첫 번째 워크시트에 액세스

다음 코드를 사용하여 Excel 통합 문서의 첫 번째 워크시트로 이동합니다.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 6단계: 배율 인수 설정

다음 코드를 사용하여 배율 인수를 설정합니다.

```csharp
worksheet.PageSetup.Zoom = 100;
```

여기서는 배율 인수를 100으로 설정했습니다. 이는 스프레드시트가 인쇄될 때 일반 크기의 100%로 표시된다는 의미입니다.

## 7단계: Excel 통합 문서 저장

 정의된 배율 인수로 Excel 통합 문서를 저장하려면`Save` Workbook 개체의 메서드:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

그러면 지정된 디렉터리에 "ScalingFactor_out.xls"라는 파일 이름으로 Excel 통합 문서가 저장됩니다.

### .NET용 Aspose.Cells를 사용하여 Excel 배율 인수 설정에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
// 배율 인수를 100으로 설정
worksheet.PageSetup.Zoom = 100;
// 통합 문서를 저장합니다.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 배율 인수를 설정하는 방법을 배웠습니다. 배율 인수를 사용하면 최적의 표시를 위해 인쇄할 때 스프레드시트의 크기를 조정할 수 있습니다.

### 자주 묻는 질문

#### 1. .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 배율 인수를 설정하는 방법은 무엇입니까?

 사용`Zoom` 의 재산`PageSetup`배율 인수를 설정하는 개체입니다. 예를 들어,`worksheet.PageSetup.Zoom = 100;` 배율 인수를 100%로 설정합니다.

#### 2. 필요에 따라 배율을 맞춤 설정할 수 있나요?

 예, 할당된 값을 변경하여 배율 인수를 조정할 수 있습니다.`Zoom` 재산. 예를 들어,`worksheet.PageSetup.Zoom = 75;` 배율 인수를 75%로 설정합니다.

#### 3. 정의된 배율 인수로 Excel 통합 문서를 저장할 수 있습니까?

 예, 다음을 사용할 수 있습니다.`Save` 의 방법`Workbook` 정의된 배율 인수를 사용하여 Excel 통합 문서를 저장하는 개체입니다.