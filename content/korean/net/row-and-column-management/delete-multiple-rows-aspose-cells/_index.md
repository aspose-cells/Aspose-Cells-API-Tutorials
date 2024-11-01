---
title: Aspose.Cells .NET에서 여러 행 삭제
linktitle: Aspose.Cells .NET에서 여러 행 삭제
second_title: Aspose.Cells .NET Excel 처리 API
description: Aspose.Cells for .NET을 사용하여 Excel에서 여러 행을 삭제하는 방법을 알아보세요. 이 자세한 단계별 가이드는 개발자를 위한 필수 조건, 코딩 예제 및 FAQ를 다룹니다.
type: docs
weight: 21
url: /ko/net/row-and-column-management/delete-multiple-rows-aspose-cells/
---
## 소개
Excel을 사용해 본 적이 있다면, 특히 여러 행을 빠르게 삭제해야 할 때 대용량 데이터 세트를 조작하는 데 얼마나 많은 시간이 소요되는지 알 것입니다. 다행히도 Aspose.Cells for .NET을 사용하면 이 프로세스가 간소화되고 프로그래밍 방식으로 쉽게 관리할 수 있습니다. 데이터를 정리하든, 반복되는 행을 관리하든, 단순히 분석을 위해 파일을 준비하든, Aspose.Cells는 이러한 작업을 번거롭지 않게 해주는 강력한 도구를 제공합니다.
이 가이드에서는 Aspose.Cells for .NET을 사용하여 Excel에서 여러 행을 삭제하는 단계를 안내해 드리겠습니다. 필수 조건, 필요한 가져오기를 다루고 각 단계를 쉽게 따르고 구현할 수 있는 방식으로 세분화합니다. 그럼, 시작해 볼까요!
## 필수 조건
시작하기 전에 다음 사항을 준비하세요.
1.  .NET 라이브러리용 Aspose.Cells: 여기에서 다운로드하여 설치하세요.[여기](https://releases.aspose.com/cells/net/).
2. IDE: Visual Studio나 호환되는 .NET 환경을 사용하세요.
3.  라이센스: Aspose.Cells에 대한 유효한 라이센스를 구매하세요.[여기](https://purchase.aspose.com/buy) 또는 다음을 시도하세요[임시 면허](https://purchase.aspose.com/temporary-license/).
4. C#과 .NET에 대한 기본 지식: 이 튜토리얼은 사용자가 C#에 익숙하다고 가정합니다.
## 패키지 가져오기
코딩을 시작하기 전에 필요한 네임스페이스를 가져와 보겠습니다.
```csharp
using System.IO;
using Aspose.Cells;
```
이러한 네임스페이스는 Excel 파일을 다루고 파일 스트림을 처리하는 데 필요한 필수 클래스에 대한 액세스를 제공합니다.
코드로 들어가 봅시다. 각 단계를 나누어서 따라가고 Aspose.Cells for .NET에서 행을 삭제하는 방법을 이해할 수 있도록 하겠습니다.
## 1단계: 디렉토리 경로 설정
코드에서 파일을 찾아 저장할 위치를 알 수 있도록 디렉토리 경로를 설정해야 합니다.
```csharp
// 문서 디렉토리의 경로입니다.
string dataDir = "Your Document Directory";
```
이 줄을 사용하면 Excel 파일이 저장되는 경로와 수정된 버전을 저장할 위치를 정의할 수 있습니다.
## 2단계: 파일 스트림으로 Excel 파일 열기
Excel 파일을 열고 조작하려면 먼저 Excel 문서에 연결되는 파일 스트림을 만듭니다. 파일 스트림을 사용하면 Excel 통합 문서를 열고 편집할 수 있습니다.
```csharp
// 열려는 Excel 파일을 포함하는 파일 스트림 생성
FileStream fstream = new FileStream(dataDir + "Book1.xlsx", FileMode.OpenOrCreate);
```
 이 코드는 다음을 생성합니다.`FileStream` Excel 파일(이 경우 "Book1.xlsx")에 대한 개체입니다.`FileMode.OpenOrCreate`인수를 사용하면 파일이 존재하지 않을 경우 파일을 생성합니다.
## 3단계: 통합 문서 개체 초기화
이제 파일 스트림이 있으니 Excel 파일을 작업할 통합 문서 개체를 초기화해 보겠습니다. 이 개체는 메모리에 있는 전체 Excel 파일을 나타내므로 다양한 수정을 할 수 있습니다.
```csharp
// Workbook 개체를 인스턴스화하고 파일 스트림을 통해 Excel 파일 열기
Workbook workbook = new Workbook(fstream);
```
 여기서 우리는 통과합니다`fstream` 물체에`Workbook` Excel 파일을 열고 그 내용을 메모리에 로드하는 생성자입니다.
## 4단계: 타겟 워크시트에 접근
이제 워크북이 준비되었으니, 어떤 워크시트를 작업할지 지정해야 합니다. 첫 번째 워크시트를 타겟으로 삼겠지만, 인덱스를 수정하여 아무 워크시트나 선택할 수 있습니다.
```csharp
// Excel 파일의 첫 번째 워크시트에 액세스하기
Worksheet worksheet = workbook.Worksheets[0];
```
 설정하여`workbook.Worksheets[0]` , Excel 파일에서 첫 번째 시트를 선택하고 있습니다. 다른 워크시트가 필요한 경우 인덱스를 변경합니다(예:`Worksheets[1]` (두 번째 워크시트의 경우)
## 5단계: 여러 행 삭제
 이 튜토리얼의 주요 부분인 여러 행 삭제에 대해 알아보겠습니다.`DeleteRows` 이 방법을 사용하면 워크시트의 특정 위치에서 지정된 수의 행을 제거할 수 있습니다.
```csharp
//워크시트에서 3번째 행부터 10개 행 삭제
worksheet.Cells.DeleteRows(2, 10);
```
이 줄에서:
- `2` 삭제가 시작될 행의 인덱스입니다(0부터 시작하므로`2` 실제로는 3번째 줄입니다).
- `10` 해당 인덱스에서 시작하여 삭제할 행의 개수입니다.
이 코드 줄은 3~12행을 삭제하여 데이터의 공간을 비우고 잠재적으로 데이터 세트를 간소화하는 데 도움이 됩니다.
## 6단계: 수정된 파일 저장
이제 행이 삭제되었으므로 업데이트된 통합 문서를 저장할 차례입니다. 원본을 덮어쓰지 않도록 새 이름으로 파일을 저장합니다.
```csharp
// 수정된 Excel 파일 저장하기
workbook.Save(dataDir + "output.xlsx");
```
이 코드는 통합 문서를 같은 디렉토리에 새 이름인 "output.xlsx"로 저장합니다. 원래 파일을 대체하려면 여기에서 같은 파일 이름을 사용할 수 있습니다.
## 7단계: 파일 스트림 닫기
모든 작업이 완료되면 파일 스트림을 닫는 것을 잊지 마세요. 이 단계는 시스템 리소스를 확보하고 잠재적인 메모리 누수를 방지하는 데 필수적입니다.
```csharp
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```
 닫기`fstream`여기서 코드를 마무리합니다. 파일 스트림이 열려 있으면, 특히 큰 파일로 작업할 때 프로그램이 시스템에 리소스를 다시 릴리스하지 못하게 할 수 있습니다.
## 결론
그리고 그게 전부입니다! 이제 Aspose.Cells for .NET을 사용하여 Excel 파일에서 여러 행을 삭제하는 방법을 배웠습니다. 이러한 단계를 따르면 행을 조작하고 데이터 구성을 빠르게 최적화할 수 있습니다. Aspose.Cells는 Excel 파일을 프로그래밍 방식으로 처리하기 위한 강력한 도구 세트를 제공하므로 동적 데이터로 작업하는 개발자에게 매우 귀중합니다.
데이터 정리, 추가 분석을 위한 파일 준비 또는 반복적인 데이터 세트 관리 등 Aspose.Cells는 프로세스를 간소화합니다. 이제 직접 파일에서 시도해 보고 Aspose.Cells를 사용하여 Excel 작업을 더 쉽게 만드는 방법을 알아보세요!
## 자주 묻는 질문
### Aspose.Cells for .NET을 사용하여 행 대신 열을 삭제할 수 있나요?  
 예, Aspose.Cells는 다음을 제공합니다.`DeleteColumns` 행을 삭제하는 것과 비슷한 방식으로 열을 제거할 수 있는 방법입니다.
### 존재하는 행보다 많은 행을 삭제하려고 하면 어떻게 되나요?  
존재하는 것보다 많은 행을 지정하면 Aspose.Cells는 오류를 발생시키지 않고 워크시트 끝까지의 모든 행을 삭제합니다.
### 연속되지 않은 행을 삭제할 수 있나요?  
 예, 하지만 개별적으로 또는 여러 번의 호출로 삭제해야 합니다.`DeleteRows`연속된 행에만 작동합니다.
### Aspose.Cells를 사용하려면 라이선스가 필요한가요?  
 예, 상업적 사용을 위해서는 유효한 라이선스가 필요합니다. 라이선스를 구매하거나 시도할 수 있습니다.[임시 면허](https://purchase.aspose.com/temporary-license/) 도서관을 평가하는 경우.
### 실수로 잘못된 행을 제거한 경우 삭제를 취소하려면 어떻게 해야 하나요?  
Aspose.Cells에는 내장된 실행 취소 기능이 없습니다. 수정하기 전에 원본 파일의 백업을 보관하는 것이 가장 좋습니다.