---
title: 워크시트에 스레드 댓글 추가
linktitle: 워크시트에 스레드 댓글 추가
second_title: Aspose.Cells .NET Excel 처리 API
description: 이 단계별 튜토리얼을 통해 Aspose.Cells for .NET을 사용하여 Excel 워크시트에 스레드 주석을 추가하는 방법을 알아보세요. 손쉽게 협업을 강화하세요.
type: docs
weight: 10
url: /ko/net/worksheet-operations/add-threaded-comments/
---
## 소개
스레드 주석으로 Excel 워크시트를 개선하고 싶으신가요? Aspose.Cells for .NET을 사용하는 개발자라면 운이 좋으시네요! 스레드 주석을 사용하면 Excel 시트 내에서 보다 체계적인 토론이 가능하여 사용자가 효과적으로 협업할 수 있습니다. 피드백이 필요한 프로젝트를 진행 중이든 단순히 데이터에 주석을 달고 싶든, 이 튜토리얼은 Aspose.Cells를 사용하여 Excel 워크시트에 스레드 주석을 추가하는 과정을 안내합니다. 
## 필수 조건
시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
1. Visual Studio: .NET 개발을 위한 가장 일반적인 IDE인 Visual Studio가 컴퓨터에 설치되어 있는지 확인하세요.
2.  Aspose.Cells for .NET: Aspose.Cells for .NET 라이브러리가 설치되어 있어야 합니다. 아직 설치하지 않았다면 사이트에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cells/net/).
3. C#에 대한 기본 지식: 이 튜토리얼은 C#로 작성되므로 C# 프로그래밍에 대한 지식이 필수적입니다.
4. .NET Framework: 프로젝트가 호환되는 .NET Framework 버전으로 설정되어 있는지 확인하세요.
## 패키지 가져오기
Aspose.Cells를 사용하려면 프로젝트에 필요한 네임스페이스를 가져와야 합니다. 방법은 다음과 같습니다.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
이러한 네임스페이스를 사용하면 Excel 파일을 조작하고 스레드된 댓글을 관리하는 데 필요한 클래스와 메서드에 액세스할 수 있습니다.
이제 필수 구성 요소가 설정되고 필요한 패키지가 가져왔으니 명확성을 위해 스레드 댓글을 추가하는 과정을 여러 단계로 나누어 보겠습니다.
## 1단계: 새 통합 문서 만들기
우선, 스레드 댓글을 추가할 새로운 통합 문서를 만들어야 합니다.
```csharp
string outDir = "Your Document Directory"; // 출력 디렉토리 설정
Workbook workbook = new Workbook(); // 새 통합 문서 만들기
```
 이 단계에서는 Excel 파일이 저장될 출력 디렉토리를 설정합니다.`Workbook` 클래스는 Aspose.Cells에서 Excel 파일을 만들고 조작하기 위한 진입점입니다.
## 2단계: 댓글 작성자 추가
댓글을 추가하기 전에 작성자를 정의해야 합니다. 이 작성자는 귀하가 만든 댓글과 연관됩니다. 지금 작성자를 추가해 보겠습니다.
```csharp
int authorIndex = workbook.Worksheets.ThreadedCommentAuthors.Add("Aspose Test", "", ""); // 작성자 추가
ThreadedCommentAuthor author = workbook.Worksheets.ThreadedCommentAuthors[authorIndex]; // 저자를 얻으십시오
```
 여기서 우리는 다음을 사용합니다.`Add` 새로운 작성자를 만드는 방법입니다. 매개변수에서 작성자 이름과 기타 선택 사항(예: 이메일)을 지정할 수 있습니다. 이 작성자는 나중에 댓글을 추가할 때 참조됩니다.
## 3단계: 스레드 댓글 추가
이제 작성자가 설정되었으니, 워크시트의 특정 셀에 스레드된 댓글을 추가할 차례입니다. 
```csharp
workbook.Worksheets[0].Comments.AddThreadedComment("A1", "Test Threaded Comment", author); // 스레드 댓글 추가
```
 이 단계에서는 첫 번째 워크시트의 셀 A1에 주석을 추가합니다. 다음을 바꿀 수 있습니다.`"A1"` 주석을 추가하려는 셀 참조와 함께. 따옴표로 묶인 메시지는 주석의 내용입니다.
## 4단계: 통합 문서 저장
스레드에 댓글을 추가한 후에는 변경 사항이 유지되도록 통합 문서를 저장해야 합니다.
```csharp
workbook.Save(outDir + "AddThreadedComments_out.xlsx"); // 통합 문서 저장
```
 여기서 통합 문서는 지정된 출력 디렉토리에 이름으로 저장됩니다.`AddThreadedComments_out.xlsx`디렉토리가 존재하는지 확인하세요. 그렇지 않으면 파일을 찾을 수 없다는 오류가 발생합니다.
## 5단계: 성공 확인
마지막으로, 작업이 성공적이었음을 나타내는 메시지를 콘솔에 출력해 보겠습니다.
```csharp
Console.WriteLine("AddThreadedComments executed successfully."); // 확인 메시지
```
이 단계는 선택 사항이지만 디버깅에 유용합니다. 코드가 오류 없이 실행되었음을 알려줍니다.
## 결론
이제 다 됐습니다! Aspose.Cells for .NET을 사용하여 Excel 워크시트에 스레드 주석을 성공적으로 추가했습니다. 이 기능은 여러 사용자가 같은 문서에서 작업할 때 협업을 크게 향상시키고 커뮤니케이션의 명확성을 제공할 수 있습니다.
스레드 댓글은 문서 내에서 더 풍부한 토론을 할 수 있을 뿐만 아니라 주석을 체계적으로 정리할 수 있습니다. 다양한 셀, 작성자, 댓글을 실험하여 통합 문서에 어떻게 나타나는지 확인하세요.
## 자주 묻는 질문
### Excel에서 스레드된 댓글이란 무엇인가요?  
스레드 댓글은 댓글 내에서 답변과 토론을 할 수 있는 댓글로, 협업을 더욱 쉽게 만들어줍니다.
### 하나의 셀에 여러 개의 댓글을 추가할 수 있나요?  
네, 하나의 셀에 여러 개의 스레드 댓글을 추가하여 광범위한 토론을 진행할 수 있습니다.
### Aspose.Cells를 사용하려면 라이선스가 필요한가요?  
 무료 평가판으로 Aspose.Cells를 사용해 볼 수 있지만 프로덕션 사용에는 라이선스가 필요합니다.[여기](https://purchase.aspose.com/buy).
### Excel에서 주석을 보려면 어떻게 해야 하나요?  
댓글을 추가한 후에는 댓글이 있는 셀 위에 마우스를 올리거나 댓글 창을 통해 댓글을 볼 수 있습니다.
### Aspose.Cells에 대한 자세한 정보는 어디에서 볼 수 있나요?  
 참조하실 수 있습니다[Aspose.Cells 설명서](https://reference.aspose.com/cells/net/) 더 많은 정보와 자세한 예를 보려면.