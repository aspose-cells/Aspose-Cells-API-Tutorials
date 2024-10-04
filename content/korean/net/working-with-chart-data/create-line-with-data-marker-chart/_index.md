---
title: 데이터 마커 차트로 라인 만들기
linktitle: 데이터 마커 차트로 라인 만들기
second_title: Aspose.Cells .NET Excel 처리 API
description: Aspose.Cells for .NET을 사용하여 Excel에서 데이터 마커가 있는 선 차트를 만드는 방법을 알아보세요. 이 단계별 가이드를 따라 차트를 쉽게 생성하고 사용자 지정하세요.
type: docs
weight: 10
url: /ko/net/working-with-chart-data/create-line-with-data-marker-chart/
---
## 소개

Excel에서 프로그래밍 방식으로 멋진 차트를 만드는 방법에 대해 생각해 본 적이 있나요? 안전띠를 매세요. 오늘은 Aspose.Cells for .NET을 사용하여 데이터 마커가 있는 선 차트를 만드는 방법을 알아보겠습니다. 이 튜토리얼은 각 단계를 안내하여 Aspose.Cells를 처음 사용하는 경우에도 차트 생성에 대한 확실한 이해를 돕습니다.

## 필수 조건

시작하기에 앞서, 원활하게 따라갈 수 있도록 모든 것이 준비되어 있는지 확인하세요.

1.  Aspose.Cells for .NET Library – 설치해야 합니다. 가져올 수 있습니다.[여기](https://releases.aspose.com/cells/net/).
2. .NET Framework – 개발 환경이 최신 버전의 .NET으로 설정되어 있는지 확인하세요.
3. IDE(통합 개발 환경) – Visual Studio를 권장합니다.
4. 유효한 Aspose.Cells 라이센스 - 라이센스가 없는 경우 다음을 요청할 수 있습니다.[임시 면허](https://purchase.aspose.com/temporary-license/) 또는 그들의 것을 확인하세요[무료 체험](https://releases.aspose.com/).

출발할 준비가 되셨나요? 자세히 살펴보겠습니다!

## 필요한 패키지 가져오기

시작하려면 다음 네임스페이스를 프로젝트로 가져와야 합니다. 이는 차트를 만드는 데 필요한 클래스와 메서드를 제공합니다.

```csharp
using System;
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Charts;
using System.Drawing;
```

이걸 다 익히면 코딩을 시작할 수 있어요!

## 1단계: 워크북 및 워크시트 설정

먼저, 새 통합 문서를 만들고 첫 번째 워크시트에 액세스해야 합니다.

```csharp
//출력 디렉토리
static string outputDir = "Your Document Directory";
		
// 통합 문서 인스턴스화
Workbook workbook = new Workbook();

// 첫 번째 워크시트에 접근하세요
Worksheet worksheet = workbook.Worksheets[0];
```

통합 문서를 Excel 파일로 생각하고 워크시트를 그 안의 특정 시트로 생각해보세요. 이 경우, 우리는 첫 번째 시트로 작업하고 있습니다.

## 2단계: 워크시트에 데이터 채우기

이제 워크시트가 있으니 데이터를 채워 봅시다. 두 개의 값 시리즈에 대한 무작위 데이터 포인트를 만들고 있습니다.

```csharp
// 열 제목 설정
worksheet.Cells[0, 0].Value = "X";
worksheet.Cells[0, 1].Value = "Y";

// 차트 생성을 위한 랜덤 데이터
Random R = new Random();

// 랜덤 데이터를 생성하여 셀에 저장합니다.
for (int i = 1; i < 21; i++)
{
    worksheet.Cells[i, 0].Value = i;
    worksheet.Cells[i, 1].Value = 0.8;
}

for (int i = 21; i < 41; i++)
{
    worksheet.Cells[i, 0].Value = i - 20;
    worksheet.Cells[i, 1].Value = 0.9;
}
```

여기에서는 난수를 사용하여 데이터를 시뮬레이션하지만 실제 응용 프로그램에서는 데이터 세트의 실제 값으로 채울 수 있습니다.

## 3단계: 워크시트에 차트 추가

다음으로, 워크시트에 차트를 추가하고 유형을 선택합니다. 이 경우에는 데이터 표식이 있는 선 차트입니다.

```csharp
// 워크시트에 차트 추가
int idx = worksheet.Charts.Add(ChartType.LineWithDataMarkers, 1, 3, 20, 20);

// 새로 생성된 차트에 액세스하세요
Chart chart = worksheet.Charts[idx];
```

이 스니펫은 워크시트에 데이터 마커가 있는 선형 차트를 추가하여 특정 범위(1,3~20,20)에 배치합니다. 꽤 간단하죠?

## 4단계: 차트 모양 사용자 지정

차트가 생성되면 원하는 대로 스타일을 지정할 수 있습니다. 배경, 제목, 차트 스타일을 변경해 보겠습니다.

```csharp
// 차트 스타일 설정
chart.Style = 3;

// 자동 크기 조정 값을 true로 설정하세요
chart.AutoScaling = true;

// 전경색을 흰색으로 설정
chart.PlotArea.Area.ForegroundColor = Color.White;

// 차트 제목 속성 설정
chart.Title.Text = "Sample Chart";

// 차트 유형 설정
chart.Type = ChartType.LineWithDataMarkers;
```

여기서는 흰색 배경을 설정하고, 자동 크기 조정을 하고, 의미 있는 제목을 지정하여 차트가 깔끔하게 보이도록 합니다.

## 5단계: 시리즈 정의 및 데이터 포인트 플롯

이제 차트가 보기 좋아졌으므로 표시할 데이터 시리즈를 정의해야 합니다.

```csharp
// 카테고리 축 제목의 속성 설정
chart.CategoryAxis.Title.Text = "Units";

// 차트에 대해 두 개의 시리즈를 정의합니다.
int s2_idx = chart.NSeries.Add("A2: A21", true);
int s3_idx = chart.NSeries.Add("A22: A41", true);
```

이러한 시리즈는 우리가 이전에 채웠던 데이터 포인트의 범위에 해당합니다.

## 6단계: 색상 추가 및 시리즈 마커 사용자 지정

데이터 마커에 사용자 정의 색상을 추가하여 이 차트를 더욱 매력적으로 만들어 보겠습니다.

```csharp
// 첫 번째 시리즈를 사용자 정의하세요
chart.NSeries[s2_idx].Marker.Area.ForegroundColor = Color.Yellow;
chart.NSeries[s2_idx].Marker.Border.IsVisible = false;

// 두 번째 시리즈를 사용자 정의하세요
chart.NSeries[s3_idx].Marker.Area.ForegroundColor = Color.Green;
chart.NSeries[s3_idx].Marker.Border.IsVisible = false;
```

색상을 사용자 정의하면 차트의 기능성뿐만 아니라 시각적으로도 매력적으로 만들 수 있습니다!

## 7단계: 각 시리즈에 대한 X 및 Y 값 설정

마지막으로 각 시리즈에 X와 Y 값을 할당해 보겠습니다.

```csharp
// 첫 번째 시리즈의 X 및 Y 값 설정
chart.NSeries[s2_idx].XValues = "A2: A21";
chart.NSeries[s2_idx].Values = "B2: B21";

// 두 번째 시리즈의 X 및 Y 값 설정
chart.NSeries[s3_idx].XValues = "A22: A41";
chart.NSeries[s3_idx].Values = "B22: B41";
```

이 값은 2단계에서 채운 데이터를 기반으로 합니다.

## 8단계: 통합 문서 저장

이제 모든 것이 설정되었으니 통합 문서를 저장하여 차트가 실제로 어떻게 실행되는지 살펴보겠습니다.

```csharp
// 통합 문서 저장
workbook.Save(outputDir + @"LineWithDataMarkerChart.xlsx", Aspose.Cells.SaveFormat.Xlsx);
```

그리고 그게 전부입니다! 방금 Aspose.Cells for .NET을 사용하여 데이터 마커가 있는 선형 차트를 만들었습니다.

## 결론

Excel에서 차트를 프로그래밍 방식으로 만드는 것은 어려울 수 있지만 Aspose.Cells for .NET을 사용하면 단계별 레시피를 따르는 것만큼 쉽습니다. 통합 문서 설정에서 차트 모양 사용자 지정까지 이 강력한 라이브러리는 모든 것을 처리합니다. 보고서, 대시보드 또는 데이터 시각화를 작성하든 Aspose.Cells를 사용하면 손쉽게 할 수 있습니다.

## 자주 묻는 질문

### 차트를 더욱 세부적으로 사용자 지정할 수 있나요?  
물론입니다! Aspose.Cells는 글꼴부터 격자선까지 다양한 사용자 정의 옵션을 제공합니다.

### Aspose.Cells를 사용하려면 라이선스가 필요한가요?  
 네, 모든 기능을 사용하려면 라이센스가 필요합니다.[임시 면허](https://purchase.aspose.com/temporary-license/) 또는 ~로 시작하세요[무료 체험](https://releases.aspose.com/).

### 더 많은 데이터 시리즈를 어떻게 추가할 수 있나요?  
 다음을 사용하여 추가 시리즈를 추가하세요.`NSeries.Add` 새 데이터에 대한 셀 범위를 지정하는 방법입니다.

### 차트를 이미지로 내보낼 수 있나요?  
 예, 다음을 사용하여 차트를 이미지로 직접 내보낼 수 있습니다.`Chart.ToImage` 방법.

### Aspose.Cells는 3D 차트를 지원합니까?  
네, Aspose.Cells는 3D 차트를 포함한 다양한 차트 유형을 지원합니다.