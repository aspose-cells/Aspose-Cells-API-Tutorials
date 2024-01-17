---
title: Excel 워크시트에서 범위 편집
linktitle: Excel 워크시트에서 범위 편집
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 특정 범위를 편집하는 방법을 알아보세요. C#의 단계별 튜토리얼입니다.
type: docs
weight: 20
url: /ko/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel은 스프레드시트를 만들고 관리하기 위한 강력한 도구로, 데이터를 제어하고 보호하는 다양한 기능을 제공합니다. 그러한 기능 중 하나는 사용자가 다른 부분을 보호하면서 워크시트의 특정 범위를 편집할 수 있도록 하는 것입니다. 이 튜토리얼에서는 프로그래밍 방식으로 Excel 파일을 작업하는 데 널리 사용되는 라이브러리인 Aspose.Cells for .NET을 사용하여 이 기능을 구현하는 방법을 단계별로 안내합니다.

.NET용 Aspose.Cells를 사용하면 Excel 스프레드시트의 범위를 쉽게 조작할 수 있으며 사용자 친화적인 인터페이스와 고급 기능을 제공합니다. 사용자가 .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 특정 범위를 편집할 수 있도록 하려면 아래 단계를 따르세요.
## 1단계: 환경 설정

개발 환경에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. Aspose 공식 웹사이트에서 라이브러리를 다운로드하고 설치 지침에 대한 설명서를 확인하세요.

## 2단계: 통합 문서 및 워크시트 초기화

시작하려면 새 통합 문서를 만들고 범위 변경을 허용하려는 워크시트에 대한 참조를 가져와야 합니다. 이를 달성하려면 다음 코드를 사용하십시오.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// 디렉터리가 아직 없으면 만듭니다.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// 새 통합 문서 인스턴스화
Workbook workbook = new Workbook();

// 첫 번째 워크시트 가져오기(기본값)
Worksheet sheet = workbook.Worksheets[0];
```

 이 코드 조각에서는 먼저 Excel 파일이 저장될 디렉터리의 경로를 정의합니다. 다음으로, 새로운 인스턴스를 생성합니다.`Workbook` 클래스를 사용하여 첫 번째 워크시트에 대한 참조를 가져옵니다.`Worksheets` 재산.

## 3단계: 편집 가능한 범위 가져오기

이제 수정을 허용하려는 범위를 검색해야 합니다. 다음 코드를 사용하세요.

```csharp
// 수정 가능한 범위 가져오기
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## 4단계: 보호 범위 설정

범위 수정을 허용하기 전에 보호된 범위를 정의해야 합니다. 방법은 다음과 같습니다.

```csharp
// 보호된 범위 정의
ProtectedRange ProtectedRange;

// 범위 만들기
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 이 코드에서는`ProtectedRange` 클래스를 사용하고`Add` 보호할 범위를 지정하는 방법입니다.

## 5단계: 비밀번호 지정

보안을 강화하기 위해 보호된 범위에 대한 비밀번호를 지정할 수 있습니다. 방법은 다음과 같습니다.

```csharp
// 비밀번호 지정
protectedBeach.Password = "YOUR_PASSWORD";
```

## 6단계: 워크시트 보호

이제 보호 범위를 설정했으므로 무단 수정을 방지하기 위해 워크시트를 보호할 수 있습니다. 다음 코드를 사용하세요.

```csharp
// 워크시트를 보호하세요
leaf.Protect(ProtectionType.All);
```

## 7단계: Excel 파일 저장

마지막으로 변경 사항이 포함된 Excel 파일을 저장합니다. 필요한 코드는 다음과 같습니다.

```csharp
// 엑셀 파일을 저장하세요
workbook.Save(dataDir + "protectedrange.out.xls");
```

### .NET용 Aspose.Cells를 사용하여 Excel 워크시트에서 범위 편집을 위한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 디렉터리가 아직 없으면 만듭니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// 새 통합 문서 인스턴스화
Workbook book = new Workbook();

// 첫 번째(기본) 워크시트 가져오기
Worksheet sheet = book.Worksheets[0];

// 허용 편집 범위 가져오기
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// ProtectedRange 정의
ProtectedRange proteced_range;

// 범위 만들기
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// 비밀번호를 지정하세요
proteced_range.Password = "YOUR_PASSWORD";

// 시트를 보호하세요
sheet.Protect(ProtectionType.All);

// 엑셀 파일을 저장하세요
book.Save(dataDir + "protectedrange.out.xls");
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 사용자가 Excel 스프레드시트에서 특정 범위를 편집할 수 있도록 허용하는 방법을 배웠습니다. 이제 이 기술을 자신의 프로젝트에 적용하고 Excel 파일의 보안을 향상시킬 수 있습니다.


#### 자주 묻는 질문

#### Q: Excel 스프레드시트에서 범위를 편집하기 위해 Aspose.Cells for .NET을 사용해야 하는 이유는 무엇입니까?

A: Aspose.Cells for .NET은 Excel 파일 작업을 위한 강력하고 사용하기 쉬운 API를 제공합니다. 범위 조작, 워크시트 보호 등과 같은 고급 기능을 제공합니다.

#### Q: 워크시트에 편집 가능한 범위를 여러 개 설정할 수 있나요?

 A: 예, 다음을 사용하여 여러 편집 가능한 범위를 정의할 수 있습니다.`Add` 의 방법`ProtectedRangeCollection` 수집. 각 범위에는 고유한 보호 설정이 있을 수 있습니다.

####  Q: 편집 가능한 범위를 정의한 후 삭제할 수 있나요?

 A: 예, 다음을 사용할 수 있습니다.`RemoveAt` 의 방법`ProtectedRangeCollection` 인덱스를 지정하여 특정 편집 가능한 범위를 제거하는 컬렉션입니다.

#### Q: 보호된 Excel 파일을 저장한 후 어떻게 열 수 있나요?

A: 보호된 Excel 파일을 열려면 보호 범위를 생성할 때 지정된 비밀번호를 제공해야 합니다. 데이터에 접근할 수 있는 권한이 손실되지 않도록 비밀번호를 안전한 곳에 보관하세요.