---
title: Excel에서 워크시트에 버튼 추가
linktitle: Excel에서 워크시트에 버튼 추가
second_title: Aspose.Cells .NET Excel 처리 API
description: 이 단계별 튜토리얼을 통해 Aspose.Cells for .NET을 사용하여 Excel 워크시트에 버튼을 추가하는 방법을 알아보세요. 대화형 버튼으로 Excel 스프레드시트를 강화하세요.
type: docs
weight: 12
url: /ko/net/excel-shapes-controls/add-button-to-worksheet-excel/
---
## 소개
Excel 스프레드시트는 다재다능하고 일반적으로 데이터 관리에 사용되지만 때로는 추가적인 상호 작용이 필요합니다. 사용자 경험을 향상시키는 가장 좋은 방법 중 하나는 워크시트에 버튼을 추가하는 것입니다. 이러한 버튼은 매크로를 트리거하거나 사용자를 유용한 링크로 안내할 수 있습니다. Excel 파일을 사용하는 .NET 개발자인 경우 Aspose.Cells for .NET은 버튼을 추가하는 것을 포함하여 Excel 통합 문서를 프로그래밍 방식으로 조작하는 쉬운 방법을 제공합니다.
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 Excel에서 워크시트에 버튼을 추가하는 과정을 안내해 드리겠습니다. 필수 조건 설정부터 단계별 지침까지 모든 세부 사항을 다루겠습니다. 시작해 볼까요!
## 필수 조건
이 튜토리얼을 따라하기 전에 다음 도구와 패키지가 설치되어 있는지 확인하세요.
-  .NET 라이브러리용 Aspose.Cells: 여기에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cells/net/).
- .NET 개발 환경: Visual Studio 등의 작동하는 .NET 환경이 설치되어 있는지 확인하세요.
- C#에 대한 기본적인 이해: C# 프로그래밍의 기본을 알고 있어야 합니다.
-  면허: 유효한 면허가 필요합니다. 면허가 없으면 다음을 받을 수 있습니다.[무료 체험](https://releases.aspose.com/) 또는 신청하세요[임시 면허](https://purchase.aspose.com/temporary-license/).
이제 필요한 패키지를 가져오는 단계로 넘어가겠습니다.
## 패키지 가져오기
코딩을 시작하기 전에 필요한 패키지를 .NET 프로젝트로 가져와야 합니다. Aspose.Cells를 프로젝트로 가져오는 데 도움이 되는 간단한 코드 조각은 다음과 같습니다.
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
이제 필요한 패키지를 가져왔으니, 예제를 자세한 단계별 가이드로 나누어 보겠습니다.
## 1단계: 워크북 및 워크시트 설정
첫 번째 단계에서는 새 Excel 통합 문서를 만들고 첫 번째 워크시트에 대한 참조를 가져옵니다.
```csharp
// 문서 디렉토리의 경로를 정의합니다.
string dataDir = "Your Document Directory";
//디렉토리가 없으면 디렉토리를 생성합니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// 새로운 통합 문서를 만듭니다.
Workbook workbook = new Workbook();
// 워크북의 첫 번째 워크시트를 받으세요.
Worksheet sheet = workbook.Worksheets[0];
```

-  워크북 생성: 새 워크북을 만드는 것으로 시작합니다.`Workbook` Excel 파일을 나타내는 개체입니다.
-  워크시트 참조:`Worksheets[0]` 명령은 우리가 수정할 통합 문서의 첫 번째 워크시트를 검색합니다.
이 단계에서는 단일 워크시트가 있는 빈 Excel 파일을 만들어 기초를 마련합니다.
## 2단계: 워크시트에 버튼 추가
다음으로, 워크시트에 버튼을 추가해 보겠습니다. 여기서 마법이 일어납니다!
```csharp
// 워크시트에 새로운 버튼을 추가합니다.
Aspose.Cells.Drawing.Button button = sheet.Shapes.AddButton(2, 0, 2, 0, 28, 80);
```

- AddButton 메서드: 이 메서드는 워크시트의 지정된 위치에 버튼을 추가합니다. 매개변수는 버튼의 위치(행, 열, x-오프셋, y-오프셋)와 크기(높이, 너비)를 정의합니다.
- 행과 열: 버튼은 추가 오프셋 없이 행 2, 열 0에 배치됩니다.
- 크기: 버튼의 높이는 28로, 너비는 80으로 설정되었습니다.
이 단계에서는 워크시트에 버튼이 성공적으로 추가되었지만 아직 끝나지 않았습니다. 버튼을 사용자 지정해 보겠습니다.
## 3단계: 버튼 속성 설정
이제 텍스트, 글꼴, 위치를 설정하여 버튼의 모양을 사용자 지정할 시간입니다.
```csharp
// 버튼의 캡션을 설정합니다.
button.Text = "Aspose";
// 버튼이 셀에 부착되는 방식인 배치 유형을 설정합니다.
button.Placement = PlacementType.FreeFloating;
```

- 텍스트: 버튼의 캡션을 "Aspose"로 설정했습니다.
-  배치: 워크시트 셀을 기준으로 버튼이 어떻게 배치될지 정의합니다.`FreeFloating` 버튼을 셀과 상관없이 움직일 수 있습니다.
이 단계에서는 버튼의 캡션과 위치를 개인화합니다.
## 4단계: 버튼 글꼴 사용자 지정
글꼴 속성을 사용자 정의하여 버튼에 약간의 멋을 더해 보겠습니다.
```csharp
// 글꼴 이름을 설정합니다.
button.Font.Name = "Tahoma";
// 캡션 문자열을 굵게 설정합니다.
button.Font.IsBold = true;
// 색상을 파란색으로 설정합니다.
button.Font.Color = Color.Blue;
```

- 글꼴 이름: 글꼴을 깔끔하고 현대적인 글꼴인 "Tahoma"로 변경합니다.
- 굵게: 강조를 위해 버튼 텍스트를 굵게 표시합니다.
- 색상: 글꼴 색상을 파란색으로 설정하여 버튼 텍스트가 눈에 띄도록 했습니다.
이 단계에서는 버튼의 모양을 개선하여 기능적이고 시각적으로 매력적으로 만들어줍니다.
## 5단계: 버튼에 하이퍼링크 추가
하이퍼링크를 추가하면 버튼을 더욱 유용하게 만들 수 있습니다.
```csharp
// 버튼에 대한 하이퍼링크를 설정합니다.
button.AddHyperlink("https://한국어: www.aspose.com/");
```

- AddHyperlink: 이 방법을 사용하여 버튼에 클릭 가능한 하이퍼링크를 추가합니다. 클릭하면 버튼이 Aspose 웹사이트로 이동합니다.
이 단계에서는 버튼에 상호 작용성이 추가되어 단순한 미적인 측면을 넘어 기능적인 측면이 생깁니다.
## 6단계: Excel 파일 저장
모든 것이 설정되면 변경 사항을 저장하는 것을 잊지 마세요!
```csharp
// 파일을 저장합니다.
workbook.Save(dataDir + "book1.out.xls");
```

-  저장 방법: 다음을 사용합니다.`Save` 수정된 통합 문서를 새 파일에 쓰는 방법입니다. 파일은 지정된 디렉토리에 저장됩니다.
축하합니다! 이제 Excel 워크시트에 완전히 사용자 지정된 버튼을 추가했습니다.
## 결론
Excel 워크시트에 버튼을 추가하면 스프레드시트의 기능을 크게 향상시켜 더욱 상호 작용적이고 사용자 친화적으로 만들 수 있습니다. Aspose.Cells for .NET을 사용하면 이 튜토리얼에서 보여준 것처럼 몇 줄의 코드만으로 이를 달성할 수 있습니다.
Aspose.Cells for .NET은 Excel 조작에 무한한 가능성을 제공하는 강력한 라이브러리입니다. 작업을 자동화하든 스프레드시트에 새로운 기능을 추가하든 이 라이브러리는 바로 여러분의 솔루션입니다.
 아직 그렇지 않은 경우,[.NET 라이브러리용 Aspose.Cells 다운로드](https://releases.aspose.com/cells/net/) Excel 파일을 강화해 보세요.
## 자주 묻는 질문
### Aspose.Cells for .NET에서 버튼 외에 다른 모양을 사용할 수 있나요?
네, Aspose.Cells를 사용하면 체크박스, 라디오 버튼 등 다양한 모양을 추가할 수 있습니다.
### Aspose.Cells를 통해 추가한 버튼에서 매크로를 트리거할 수 있나요?
네, 버튼을 매크로에 연결할 수는 있지만 Excel에서 매크로 코드를 별도로 처리해야 합니다.
### 셀에 맞춰 버튼 크기가 자동으로 조절되게 하려면 어떻게 해야 하나요?
 사용하세요`PlacementType.Move` 버튼의 크기를 셀에 맞게 조절할 수 있는 속성입니다.
### 하나의 워크시트에 여러 개의 버튼을 추가할 수 있나요?
 물론입니다! 필요한 만큼 버튼을 추가하려면 다음을 호출하세요.`AddButton` 방법을 여러 번 반복함.
### 버튼 모양을 더 세부적으로 사용자 지정할 수 있나요?
네, 배경색, 테두리 스타일 등 여러 속성을 수정할 수 있습니다.