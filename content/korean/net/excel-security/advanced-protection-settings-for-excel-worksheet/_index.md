---
title: Excel 워크시트에 대한 고급 보호 설정
linktitle: Excel 워크시트에 대한 고급 보호 설정
second_title: .NET API 참조용 Aspose.Cells
description: Aspose.Cells for .NET으로 고급 보호 설정을 지정하여 Excel 파일을 보호하세요.
type: docs
weight: 10
url: /ko/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
이 튜토리얼에서는 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 스프레드시트에 대한 고급 보호 설정을 지정하는 단계를 안내합니다. 이 작업을 완료하려면 아래 지침을 따르세요.

## 1단계: 준비

.NET용 Aspose.Cells를 설치하고 원하는 통합 개발 환경(IDE)에서 C# 프로젝트를 생성했는지 확인하세요.

## 2단계: 문서 디렉터리 경로 설정

 선언하다`dataDir` 변수를 지정하고 문서 디렉토리 경로로 초기화하세요. 예를 들어 :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 꼭 교체하세요`"YOUR_DOCUMENTS_DIRECTORY"` 디렉터리의 실제 경로를 사용합니다.

## 3단계: Excel 파일을 여는 파일 스트림 만들기

 만들기`FileStream` 열려는 Excel 파일이 포함된 개체:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 엑셀 파일이 있는지 확인하세요`book1.xls` 문서 디렉토리에 있거나 올바른 파일 이름과 위치를 지정하십시오.

## 4단계: 통합 문서 개체 인스턴스화 및 Excel 파일 열기

 사용`Workbook`Aspose.Cells의 클래스를 사용하여 통합 문서 개체를 인스턴스화하고 파일 스트림을 통해 지정된 Excel 파일을 엽니다.

```csharp
Workbook excel = new Workbook(fstream);
```

## 5단계: 첫 번째 워크시트에 액세스

Excel 파일의 첫 번째 워크시트로 이동합니다.

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## 6단계: 워크시트 보호 설정 지정

필요에 따라 워크시트 개체 속성을 사용하여 워크시트 보호 설정을 지정합니다. 예를 들어 :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... 필요에 따라 다른 보호 설정을 지정합니다...
```

## 7단계: 수정된 Excel 파일을 저장합니다.

 수정된 Excel 파일을 다음을 사용하여 저장합니다.`Save` Workbook 개체의 메서드:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

출력 파일에 대해 원하는 경로와 파일 이름을 지정해야 합니다.

## 8단계: 파일 스트림 닫기

저장한 후에는 파일 스트림을 닫아 관련된 모든 리소스를 해제합니다.

```csharp
fstream.Close();
```
	
### .NET용 Aspose.Cells를 사용하는 Excel 워크시트의 고급 보호 설정에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 열려는 Excel 파일이 포함된 파일 스트림 생성
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// 통합 문서 개체 인스턴스화
// 파일 스트림을 통해 Excel 파일 열기
Workbook excel = new Workbook(fstream);
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = excel.Worksheets[0];
// 사용자가 워크시트의 열을 삭제하도록 제한
worksheet.Protection.AllowDeletingColumn = false;
// 사용자가 워크시트의 행을 삭제하도록 제한
worksheet.Protection.AllowDeletingRow = false;
// 사용자가 워크시트 내용을 편집하도록 제한
worksheet.Protection.AllowEditingContent = false;
// 사용자가 워크시트의 개체를 편집하도록 제한
worksheet.Protection.AllowEditingObject = false;
// 워크시트의 시나리오를 편집할 수 있도록 사용자 제한
worksheet.Protection.AllowEditingScenario = false;
//사용자를 필터링하도록 제한
worksheet.Protection.AllowFiltering = false;
// 사용자가 워크시트의 셀 서식을 지정할 수 있도록 허용
worksheet.Protection.AllowFormattingCell = true;
// 사용자가 워크시트 행의 서식을 지정할 수 있도록 허용
worksheet.Protection.AllowFormattingRow = true;
// 사용자가 워크시트에 열을 삽입하도록 허용
worksheet.Protection.AllowFormattingColumn = true;
// 사용자가 워크시트에 하이퍼링크를 삽입하도록 허용
worksheet.Protection.AllowInsertingHyperlink = true;
// 사용자가 워크시트에 행을 삽입하도록 허용
worksheet.Protection.AllowInsertingRow = true;
// 사용자가 워크시트의 잠긴 셀을 선택할 수 있도록 허용
worksheet.Protection.AllowSelectingLockedCell = true;
// 사용자가 워크시트의 잠금 해제된 셀을 선택할 수 있도록 허용
worksheet.Protection.AllowSelectingUnlockedCell = true;
// 사용자가 정렬하도록 허용
worksheet.Protection.AllowSorting = true;
// 사용자가 워크시트에서 피벗 테이블을 사용하도록 허용
worksheet.Protection.AllowUsingPivotTable = true;
// 수정된 엑셀 파일 저장
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```

## 결론

축하합니다! 이제 Aspose.Cells for .NET을 사용하여 Excel 스프레드시트에 대한 고급 보호 설정을 지정하는 방법을 배웠습니다. 이 지식을 활용하여 Excel 파일을 보호하고 사용자 작업을 제한하세요.

### 자주 묻는 질문

#### Q: 내 IDE에서 새 C# 프로젝트를 만들려면 어떻게 해야 합니까?

A: 새 C# 프로젝트를 만드는 단계는 사용 중인 IDE에 따라 다를 수 있습니다. 자세한 지침은 IDE 설명서를 참조하세요.

#### Q: 튜토리얼에서 언급한 것 외에 사용자 정의 보호 설정을 지정할 수 있습니까?

A: 예, Aspose.Cells는 귀하의 특정 요구 사항에 맞게 사용자 정의할 수 있는 광범위한 보호 설정을 제공합니다. 자세한 내용은 Aspose.Cells 설명서를 참조하세요.

#### Q: 샘플 코드에서 수정된 엑셀 파일을 저장하는 데 사용된 파일 형식은 무엇인가요?

A: 샘플 코드에서는 수정된 엑셀 파일이 Excel 97-2003(.xls) 형식으로 저장됩니다. 필요한 경우 Aspose.Cells에서 지원하는 다른 형식을 선택할 수 있습니다.

#### Q: Excel 파일의 다른 워크시트에 어떻게 액세스할 수 있나요?

 A: 색인이나 시트 이름을 사용하여 다른 워크시트에 액세스할 수 있습니다. 예를 들면 다음과 같습니다.`Worksheet worksheet = excel.Worksheets[1];` 또는`Worksheet worksheet = excel.Worksheets[" SheetName"];`.