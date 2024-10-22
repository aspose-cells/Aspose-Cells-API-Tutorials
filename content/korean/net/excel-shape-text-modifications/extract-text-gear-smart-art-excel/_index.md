---
title: Excel에서 기어 유형 스마트 아트에서 텍스트 추출
linktitle: Excel에서 기어 유형 스마트 아트에서 텍스트 추출
second_title: Aspose.Cells .NET Excel 처리 API
description: Aspose.Cells for .NET을 사용하여 Excel에서 기어 유형 SmartArt에서 텍스트를 추출하는 방법을 알아보세요. 단계별 가이드와 코드 예제가 포함되어 있습니다.
type: docs
weight: 10
url: /ko/net/excel-shape-text-modifications/extract-text-gear-smart-art-excel/
---
## 소개
Excel로 작업할 때 시각적으로 매력적인 방식으로 메시지를 전달하는 데 도움이 되는 SmartArt 그래픽을 접할 수 있습니다. 이러한 그래픽 중에서 기어 유형 SmartArt는 계층적이고 방향성 있는 흐름으로 인해 선호되며, 종종 프로젝트 관리 또는 시스템 모델링에 사용됩니다. 하지만 이러한 도형에서 프로그래밍 방식으로 텍스트를 추출해야 하는 경우는 어떨까요? 이때 Aspose.Cells for .NET이 유용합니다! 이 블로그 게시물에서는 Aspose.Cells for .NET을 사용하여 Excel에서 기어 유형 SmartArt 도형에서 텍스트를 추출하는 방법에 대한 단계별 가이드를 안내합니다.
## 필수 조건
들어가기 전에 꼭 갖춰야 할 필수 전제 조건이 있습니다. 걱정하지 마세요. 간단하며, 제가 안내해 드리겠습니다.
### .NET 환경
컴퓨터에 .NET 개발 환경이 설정되어 있는지 확인하세요. 이는 Visual Studio 또는 .NET 개발을 지원하는 선택한 IDE일 수 있습니다.
### .NET용 Aspose.Cells
 다음으로 Aspose.Cells 라이브러리를 설치해야 합니다. 이것은 Excel 파일을 원활하게 조작할 수 있게 해주는 강력한 라이브러리입니다. 다음에서 다운로드할 수 있습니다.[Aspose 릴리스 페이지](https://releases.aspose.com/cells/net/) . 먼저 탐색하고 싶다면 다음을 활용하세요.[무료 체험](https://releases.aspose.com/).
### C#의 기본 지식
이 튜토리얼을 따라가려면 C# 프로그래밍에 대한 기본적인 이해가 필요합니다. 처음 접하더라도 걱정하지 마세요. 가능한 한 초보자에게 친숙한 단계를 설계하겠습니다.
### 샘플 Excel 파일
이 튜토리얼에서는 기어 유형 SmartArt 모양이 포함된 샘플 Excel 파일도 필요합니다. 쉽게 만들거나 온라인에서 템플릿을 찾을 수 있습니다. SmartArt에 기어 유형 모양이 하나 이상 포함되어 있는지 확인하기만 하면 됩니다.
## 패키지 가져오기
코딩을 시작하려면 필요한 패키지를 가져와야 합니다. 방법은 다음과 같습니다.
### 새 프로젝트 만들기
1. .NET IDE를 엽니다.
2. 새 프로젝트를 만듭니다. 예를 들어, .NET 옵션에서 '콘솔 애플리케이션'을 선택합니다.
3. 프로젝트 이름을 지정하고 원하는 프레임워크를 설정합니다. 
### 참조 추가
Aspose.Cells를 사용하려면 프로젝트에 라이브러리 참조를 추가해야 합니다.
1. 솔루션 탐색기에서 프로젝트 이름을 마우스 오른쪽 버튼으로 클릭합니다.
2. “NuGet 패키지 관리”를 선택하세요.
3. "Aspose.Cells"를 검색하여 설치하세요.
설치가 완료되면 코딩을 시작할 준비가 완료됩니다!
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
이제 텍스트를 추출하는 데 사용할 코드를 분석해 보겠습니다. 단계별로 진행하겠습니다.
## 1단계: 소스 디렉토리 설정
먼저 Excel 파일이 있는 디렉토리를 정의합니다.
```csharp
// 소스 디렉토리
string sourceDir = "Your Document Directory";
```
 교체를 꼭 해주세요`"Your Document Directory"` Excel 파일의 실제 경로를 포함합니다.
## 2단계: Excel 통합 문서 로드
다음으로 Excel 통합 문서를 로드합니다. 이것이 우리가 그 내용에 접근할 수 있는 방법입니다:
```csharp
// 기어 유형의 스마트 아트 모양이 포함된 샘플 Excel 파일을 로드합니다.
Workbook wb = new Workbook(sourceDir + "sampleExtractTextFromGearTypeSmartArtShape.xlsx");
```
이 부분에서는 샘플 Excel 통합 문서를 로드합니다.
## 3단계: 첫 번째 워크시트에 액세스
이제 통합 문서를 로드했으므로 SmartArt가 있는 첫 번째 워크시트에 액세스해 보겠습니다.
```csharp
// 첫 번째 워크시트에 접근합니다.
Worksheet ws = wb.Worksheets[0];
```
이는 추가 조작을 위한 첫 번째 워크시트를 검색합니다.
## 4단계: 첫 번째 모양에 액세스
다음으로, 워크시트 내의 첫 번째 모양에 접근해야 합니다. 이렇게 하면 SmartArt 그래픽을 탐색할 수 있습니다.
```csharp
// 첫 번째 모양에 접근합니다.
Aspose.Cells.Drawing.Shape sh = ws.Shapes[0];
```
여기서는 SmartArt에 필요한 것으로 추정되는 첫 번째 모양에 초점을 맞춥니다.
## 5단계: 그룹 모양 얻기
모양이 정해지면 이제 SmartArt 표현의 결과를 얻을 차례입니다.
```csharp
// 그룹모양의 형태로 기어형 스마트아트 모양의 결과를 얻습니다.
Aspose.Cells.Drawing.GroupShape gs = sh.GetResultOfSmartArt();
```
이렇게 하면 기어 유형 SmartArt가 그룹화된 모양으로 검색됩니다.
## 6단계: 개별 모양 추출
이제 SmartArt를 구성하는 개별 모양을 추출해 보겠습니다.
```csharp
// 그룹 모양으로 구성된 개별 모양의 목록을 가져옵니다.
Aspose.Cells.Drawing.Shape[] shps = gs.GetGroupedShapes();
```
이 배열은 반복하는 데 필요한 모든 개별 모양을 보관합니다.
## 7단계: 텍스트 추출 및 인쇄
마지막으로, 우리는 모양 배열을 반복하고 기어 유형 모양에서 텍스트를 추출할 수 있습니다.
```csharp
// 기어 유형 모양의 텍스트를 추출하여 콘솔에 인쇄합니다.
for (int i = 0; i < shps.Length; i++)
{
    Aspose.Cells.Drawing.Shape s = shps[i];
    if (s.Type == Aspose.Cells.Drawing.AutoShapeType.Gear9 || s.Type == Aspose.Cells.Drawing.AutoShapeType.Gear6)
    {
        Console.WriteLine("Gear Type Shape Text: " + s.Text);
    }
}
```
이 루프에서 우리는 모양의 유형을 확인하고 그것이 기어 유형 모양이면 텍스트를 출력합니다.
## 8단계: 실행 확인
마지막으로, 프로세스가 성공적으로 완료되면 확인 메시지를 추가할 수 있습니다.
```csharp
Console.WriteLine("ExtractTextFromGearTypeSmartArtShape executed successfully.");
```
이것으로 추출이 완료되고 콘솔에서 텍스트 출력을 볼 수 있습니다!
## 결론
 축하합니다! 방금 Aspose.Cells for .NET을 사용하여 Excel에서 기어 유형 SmartArt 도형에서 텍스트를 추출하는 방법을 배웠습니다. 이 편리한 기술은 시각적 데이터 표현에 의존하는 보고서나 문서를 자동화하는 문을 열어줍니다. 노련한 개발자이든 초보자이든 SmartArt에서 정보를 제어하고 추출하면 워크플로를 간소화하고 효율성을 높일 수 있습니다. 자세한 내용을 살펴보는 것을 잊지 마세요.[Aspose.Cells 문서](https://reference.aspose.com/cells/net/) 추가 기능을 원하시면.
## 자주 묻는 질문
### Aspose.Cells란 무엇인가요?
Aspose.Cells는 개발자가 Excel 파일을 쉽게 만들고 조작할 수 있는 .NET 라이브러리입니다.
### Aspose.Cells를 다른 언어에서도 사용할 수 있나요?
네! Aspose.Cells는 Java와 Python을 포함한 여러 프로그래밍 언어로 제공됩니다.
### .NET용 Aspose.Cells를 구매해야 합니까?
 Aspose.Cells는 무료 체험판을 제공하지만, 장기 사용을 위해서는 구매가 필요합니다. 구매 옵션을 찾을 수 있습니다.[여기](https://purchase.aspose.com/buy).
### Aspose.Cells 사용자를 위한 지원이 제공되나요?
 물론입니다! 커뮤니티 지원을 찾을 수 있습니다.[Aspose.Cells 포럼](https://forum.aspose.com/c/cells/9).
### 이 방법을 사용하여 다른 SmartArt 유형을 추출할 수 있나요?
네, 약간의 수정만으로 코드의 조건을 변경하여 다양한 SmartArt 도형에서 텍스트를 추출할 수 있습니다.