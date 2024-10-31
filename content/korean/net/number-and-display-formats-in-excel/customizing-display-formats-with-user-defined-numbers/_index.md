---
title: 사용자 정의 숫자로 표시 형식 사용자 정의
linktitle: 사용자 정의 숫자로 표시 형식 사용자 정의
second_title: Aspose.Cells .NET Excel 처리 API
description: Aspose.Cells for .NET으로 표시 형식을 사용자 지정하는 방법을 알아보세요. 이 단계별 가이드를 사용하여 날짜, 백분율 및 통화를 형식화하세요.
type: docs
weight: 11
url: /ko/net/number-and-display-formats-in-excel/customizing-display-formats-with-user-defined-numbers/
---
## 소개
Excel 파일을 사용하면 데이터를 보다 의미 있고 사용자 친화적인 방식으로 표시하기 위해 셀의 사용자 지정 서식이 필요한 경우가 많습니다. 보고서용 Excel 파일을 작성한다고 가정해 보겠습니다. 단순히 숫자만 원하는 것은 아닙니다. 날짜, 백분율, 통화를 세련되고 전문적으로 보이게 하고 싶을 것입니다. 바로 여기서 사용자 지정 표시 형식이 중요합니다. 이 자습서에서는 Aspose.Cells for .NET을 자세히 살펴보고 사용자 정의 설정을 사용하여 숫자의 표시 형식을 사용자 지정하는 방법을 보여드리겠습니다.
## 필수 조건
시작하기 전에 이 튜토리얼을 따라할 모든 것을 준비했는지 확인하세요. 필요한 것은 다음과 같습니다.
-  .NET용 Aspose.Cells가 설치되었습니다.[여기에서 다운로드하세요](https://releases.aspose.com/cells/net/).
- C# 및 .NET 프레임워크에 대한 기본 지식.
-  Aspose.Cells에 대한 유효한 라이센스입니다. 라이센스가 없으면 다음을 얻으세요.[무료 체험](https://releases.aspose.com/) 또는 요청[임시 면허](https://purchase.aspose.com/temporary-license/).
- Visual Studio와 같은 IDE.
- .NET Framework 4.0 이상.
 무언가 빠진 것이 있다면 걱정하지 마세요. 언제든지 이 링크를 다시 방문하여 필요한 파일을 다운로드하거나 도움을 요청할 수 있습니다.[Aspose 지원 포럼](https://forum.aspose.com/c/cells/9).
## 네임스페이스 가져오기
코드로 들어가기 전에 Aspose.Cells의 모든 필수 기능에 액세스하는 데 필요한 네임스페이스를 가져와야 합니다.
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
이 두 네임스페이스는 이 튜토리얼에서 핵심 도구가 될 것입니다. 이제 재미있는 부분으로 넘어가겠습니다.
## 1단계: 프로젝트 디렉토리 설정
먼저, 파일을 저장할 장소가 필요하죠? 출력 Excel 파일을 저장할 디렉토리를 만들어 보겠습니다. 이 단계에서는 아무것도 저장하기 전에 디렉토리가 있는지도 확인합니다.
```csharp
// 문서 디렉토리의 경로입니다.
string dataDir = "Your Document Directory";
// 디렉토리가 없으면 디렉토리를 생성합니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
-  우리는 정의하고 있습니다`dataDir` 출력 Excel 파일이 저장될 경로를 저장하는 변수입니다.
-  그런 다음 다음을 사용하여 디렉토리가 존재하는지 확인합니다.`System.IO.Directory.Exists()`.
-  디렉토리가 존재하지 않으면 다음을 사용하여 생성됩니다.`System.IO.Directory.CreateDirectory()`.
## 2단계: 새 통합 문서 만들기 및 워크시트 추가
이제 디렉토리가 생겼으니 새로운 Excel 통합 문서를 만들고 여기에 워크시트를 추가해 보겠습니다.
```csharp
// Workbook 개체 인스턴스화
Workbook workbook = new Workbook();
// Excel 개체에 새 워크시트 추가
int i = workbook.Worksheets.Add();
// 새로 추가된 워크시트의 시트 인덱스를 전달하여 해당 워크시트의 참조를 얻습니다.
Worksheet worksheet = workbook.Worksheets[i];
```
-  첫째, 우리는 새로운 것을 만듭니다`Workbook` 객체입니다. 이것을 Excel 파일이라고 생각하세요.
-  이 통합 문서에 새 워크시트를 추가합니다.`Add()`방법과 변수에 인덱스를 저장합니다.`i`.
-  이 워크시트를 참조하려면 다음을 사용합니다.`workbook.Worksheets[i]`.
## 3단계: 셀에 날짜 추가 및 형식 사용자 지정
 이제 현재 날짜를 셀에 삽입하고 사용자 지정 방식으로 표시되도록 서식을 지정해 보겠습니다. 기본 날짜 형식 대신 다음과 같은 사용자 지정 형식을 설정합니다.`d-mmm-yy`.
```csharp
// 현재 시스템 날짜를 "A1" 셀에 추가합니다.
worksheet.Cells["A1"].PutValue(DateTime.Now);
// A1 셀의 스타일 얻기
Style style = worksheet.Cells["A1"].GetStyle();
// 사용자 정의 표시 형식을 설정하여 날짜를 "d-mmm-yy"로 표시합니다.
style.Custom = "d-mmm-yy";
// A1 셀에 스타일 적용하기
worksheet.Cells["A1"].SetStyle(style);
```
-  현재 시스템 날짜를 셀에 추가합니다.`A1` 사용 중`PutValue(DateTime.Now)`.
-  우리는 셀의 현재 스타일을 검색합니다`A1` 사용 중`GetStyle()`.
-  셀의 스타일을 설정하여 수정합니다.`style.Custom = "d-mmm-yy"`, 날짜를 일, 월, 년도 순으로 표시합니다.
-  마지막으로 셀에 새 스타일을 적용합니다.`SetStyle()`.
## 4단계: 셀을 백분율로 서식 지정
 다음으로 숫자를 다루어 보겠습니다. 다른 셀에 숫자 값을 추가합니다.`A2`, 백분율로 서식을 지정합니다.
```csharp
//"A2" 셀에 숫자 값 추가
worksheet.Cells["A2"].PutValue(20);
// A2 셀의 스타일 얻기
style = worksheet.Cells["A2"].GetStyle();
// 값을 백분율로 표시하도록 사용자 정의 표시 형식 설정
style.Custom = "0.0%";
// A2 셀에 스타일 적용하기
worksheet.Cells["A2"].SetStyle(style);
```
-  우리는 가치를 더합니다`20` 세포로`A2`.
-  우리는 셀의 스타일을 검색합니다`A2` 사용자 정의 형식을 설정합니다.`0.0%` 값을 백분율(예: 20%)로 표시합니다.
-  마지막으로 다음을 사용하여 셀에 스타일을 적용합니다.`SetStyle()`.
## 5단계: 셀을 통화로 서식 지정
 셀에 다른 값을 추가해 보겠습니다.`A3`, 그리고 통화로 표시되도록 포맷합니다. 더 흥미로운 것을 만들기 위해 양수 값을 파운드로, 음수 값을 달러로 표시하는 포맷을 사용하겠습니다.
```csharp
// "A3" 셀에 숫자 값 추가
worksheet.Cells["A3"].PutValue(2546);
// A3 셀의 스타일 얻기
style = worksheet.Cells["A3"].GetStyle();
// 값을 통화로 표시하도록 사용자 정의 표시 형식 설정
style.Custom = "£#,##0;[Red]$-#,##0";
// A3 셀에 스타일 적용하기
worksheet.Cells["A3"].SetStyle(style);
```
-  우리는 가치를 더합니다`2546` 세포로`A3`.
-  사용자 정의 형식을 설정합니다`£#,##0;[Red]$-#,##0`양수 값은 파운드 기호와 함께 표시되고, 음수 값은 빨간색으로 달러 기호와 함께 표시됩니다.
- 우리는 셀에 스타일을 적용합니다`SetStyle()`.
## 6단계: 통합 문서 저장
마지막 단계는 통합 문서를 Excel 파일로 저장하는 것입니다. 이 튜토리얼에서는 Excel 97-2003 형식을 사용합니다.
```csharp
// Excel 파일 저장하기
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
-  그만큼`Save()` 이 방법은 지정된 디렉토리에 통합 문서를 저장합니다.
-  우리는 선택한다`SaveFormat.Excel97To2003` 이전 버전의 Excel과의 호환성을 보장합니다.
## 결론
이제 다 봤습니다! 방금 Excel 파일을 만들고 Aspose.Cells for .NET을 사용하여 특정 셀에 사용자 지정 날짜, 백분율 및 통화 서식을 추가하고 파일을 저장했습니다. 사용자 지정 서식을 사용하면 Excel 파일을 훨씬 더 읽기 쉽고 전문적으로 만들 수 있습니다. Aspose.Cells의 다른 서식 옵션(예: 조건부 서식)을 탐색하여 데이터 모양을 더욱 세부적으로 제어하는 것을 잊지 마세요.
## 자주 묻는 질문
### Aspose.Cells에서 더 복잡한 서식 옵션을 어떻게 적용할 수 있나요?
사용자 정의 숫자 서식을 사용하면 글꼴 색상, 테두리, 배경색 등 다양한 서식 스타일을 결합할 수 있습니다.
### 사용자 지정 숫자 서식을 셀 범위에 적용할 수 있나요?
예, Aspose.Cells를 사용하면 다음을 사용하여 셀 범위에 스타일을 적용할 수 있습니다.`Range.SetStyle()` 방법.
### 통합 문서를 어떤 다른 파일 형식으로 저장할 수 있나요?
 Aspose.Cells는 XLSX, CSV, PDF를 포함한 다양한 형식을 지원합니다. 간단히 변경하세요.`SaveFormat` 에서`Save()` 방법.
### 음수를 다른 형식으로 표시할 수 있나요?
물론입니다! 사용자 지정 숫자 형식을 사용하여 음수를 다른 색상이나 기호로 표시할 수 있습니다.
### Aspose.Cells for .NET은 무료인가요?
 Aspose.Cells는 무료 체험판을 제공하지만 모든 기능을 사용하려면 유효한 라이선스가 필요합니다.[여기 임시 면허증](https://purchase.aspose.com/temporary-license/).