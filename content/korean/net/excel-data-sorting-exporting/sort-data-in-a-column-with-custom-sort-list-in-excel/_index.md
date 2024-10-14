---
title: Excel에서 사용자 지정 정렬 목록을 사용하여 열의 데이터 정렬
linktitle: Excel에서 사용자 지정 정렬 목록을 사용하여 열의 데이터 정렬
second_title: Aspose.Cells .NET Excel 처리 API
description: 이 포괄적인 튜토리얼에서는 Aspose.Cells for .NET의 사용자 지정 정렬 목록을 사용하여 Excel에서 데이터를 정렬하는 방법을 알아봅니다.
type: docs
weight: 10
url: /ko/net/excel-data-sorting-exporting/sort-data-in-a-column-with-custom-sort-list-in-excel/
---
## 소개

이 튜토리얼은 프로젝트를 설정하고, Excel 파일을 로드하고, 사용자 지정 정렬 순서를 사용하여 지정된 범위 내에서 데이터를 정렬하는 과정을 안내합니다. 이 가이드를 따르면 데이터 관리 기술과 Aspose.Cells 라이브러리의 사용성을 향상시킬 수 있는 실무 경험을 얻을 수 있습니다.

## 필수 조건

튜토리얼을 시작하기에 앞서, 원활한 학습 경험을 보장하기 위한 몇 가지 전제 조건을 살펴보겠습니다.

### C#의 기본 지식

튜토리얼은 각 단계를 안내하도록 설계되었지만 C#에 대한 기본적인 이해가 있으면 제시된 개념을 더 쉽게 파악할 수 있습니다.

### .NET 개발 환경

작동하는 .NET 개발 환경이 설정되어 있는지 확인하세요. Visual Studio나 .NET 개발을 지원하는 다른 IDE를 사용할 수 있습니다.

### .NET NuGet 패키지용 Aspose.Cells

프로젝트에 .NET용 Aspose.Cells 라이브러리가 설치되어 있어야 합니다. NuGet Package Manager를 통해 쉽게 추가할 수 있습니다. 

방법은 다음과 같습니다.

1. Visual Studio에서 프로젝트를 엽니다.
2. "도구" > "NuGet 패키지 관리자" > "솔루션용 NuGet 패키지 관리"로 이동합니다.
3.  검색`Aspose.Cells` 최신 버전을 설치하세요.

### 테스트를 위한 기본 Excel 파일

작업할 샘플 Excel 파일이 필요합니다. 무작위 국가 이름과 코드로 간단한 Excel 파일을 만들 수 있습니다.

## 패키지 가져오기

시작하려면 필요한 패키지를 프로젝트에 임포트해 보겠습니다. 다음은 코드를 설정하는 방법에 대한 스니펫입니다.

```csharp
using System;
using System.IO;
using Aspose.Cells;
using System.Drawing;
```

패키지를 수입했으므로 다음 단계로 넘어갈 준비가 되었습니다.

## 1단계: 소스 및 출력 디렉토리 정의 

첫 번째 단계는 입력 파일의 위치와 출력(정렬된 파일)을 저장할 위치를 정의하는 것입니다. 두 개의 경로를 지정해야 합니다. 하나는 원본 Excel 파일에 대한 경로이고 다른 하나는 정렬 후 출력을 저장하는 경로입니다.

```csharp
string sourceDir = "Your Document Directory\\";
string outputDir = "Your Document Directory\\";
```

## 2단계: 소스 Excel 파일 로드

 다음으로 정렬하려는 데이터가 포함된 Excel 파일을 로드합니다. 이는 인스턴스를 생성하여 수행됩니다.`Workbook` 클래스를 사용하고 소스 파일의 경로를 전달합니다.

```csharp
Workbook wb = new Workbook(sourceDir + "sampleSortData_CustomSortList.xlsx");
```

## 3단계: 첫 번째 워크시트에 액세스 

파일이 로드되면 정렬하려는 데이터가 들어 있는 특정 워크시트에 액세스해야 합니다. 이 경우 첫 번째 워크시트를 타겟으로 합니다.

```csharp
Worksheet ws = wb.Worksheets[0];
```

## 4단계: 정렬할 셀 영역 지정

 정렬할 셀 범위를 결정해야 합니다. 이 예에서는 A1에서 A40까지의 셀을 정렬합니다. 다음을 사용합니다.`CellArea.CreateCellArea` 셀 영역을 정의하는 방법입니다.

```csharp
CellArea ca = CellArea.CreateCellArea("A1", "A40");
```

## 5단계: 사용자 정의 정렬 목록 만들기

정렬하기 전에 사용자 지정 정렬에 사용할 기준을 설정해야 합니다. 정렬 목록을 문자열 배열로 정의할 수 있습니다. 사용자 지정 정렬 목록은 정렬 순서를 지시합니다.

```csharp
string[] customSortList = new string[] { "USA,US", "Brazil,BR", "China,CN", "Russia,RU", "Canada,CA" };
```

## 6단계: 정렬 키 추가 및 정렬 수행

이제 정렬할 시간입니다! 이를 위해 DataSorter 클래스를 사용합니다. 사용자 지정 목록을 기반으로 정렬을 위한 키를 만들고 정렬 작업을 실행합니다.

```csharp
wb.DataSorter.AddKey(0, SortOrder.Ascending, customSortList);
wb.DataSorter.Sort(ws.Cells, ca);
```

## 7단계: 출력 Excel 파일 저장

정렬이 완료된 후 마지막 단계는 변경 사항을 새 Excel 파일에 저장하는 것입니다. 출력 파일 이름을 지정하고 통합 문서를 저장합니다.

```csharp
wb.Save(outputDir + "outputSortData_CustomSortList.xlsx");
```

## 8단계: 성공적인 실행 확인

모든 것이 순조롭게 진행되었는지 확인하려면 콘솔에 확인 메시지를 인쇄할 수 있습니다. 이렇게 하면 디버깅에 도움이 되고 작업이 성공했다는 만족감을 얻을 수 있습니다.

```csharp
Console.WriteLine("SortDataInColumnWithCustomSortList executed successfully.\r\n");
```

## 결론

이제 Aspose.Cells for .NET을 사용하여 사용자 지정 정렬 목록을 사용하여 Excel 열의 데이터를 성공적으로 정렬했습니다. 정렬은 데이터에 구조와 명확성을 제공하여 분석 및 해석을 더 쉽게 만듭니다. 이 가이드가 여러분의 기술을 한 단계 끌어올리고 Aspose.Cells가 Excel 관련 작업에 얼마나 강력한지 깨닫는 데 도움이 되기를 바랍니다.

## 자주 묻는 질문

### .NET용 Aspose.Cells란 무엇인가요?
.NET용 Aspose.Cells는 .NET 애플리케이션 내에서 Excel 파일을 조작하고, 이를 통해 파일을 만들고, 편집하고, 변환할 수 있는 포괄적인 라이브러리입니다.

### 사용자 정의 정렬 목록을 사용하여 두 개 이상의 열을 정렬할 수 있나요?
네! 필요하다면 여러 열로 정렬하기 위해 추가 키를 추가할 수 있습니다. 각 키에 대해 동일한 절차를 따르기만 하면 됩니다.

### Aspose.Cells를 사용하려면 C#에 대한 사전 지식이 필요합니까?
도움이 되지만, 이 튜토리얼을 따라가면서 배우세요! C#에 대한 기본적인 이해가 있으면 학습 경험이 향상됩니다.

### Aspose.Cells에 임시 라이센스를 사용할 수 있나요?
물론입니다! 제한 없이 라이브러리의 모든 기능을 테스트하려면 임시 라이선스를 취득할 수 있습니다.

### Aspose.Cells에 대한 예제나 문서를 다운로드할 수 있나요?
 네! Aspose는 광범위한 문서와 샘플 프로젝트를 제공하여 큰 도움이 될 수 있습니다. 다음을 확인하세요.[Aspose.Cells 문서](https://reference.aspose.com/cells/net/).