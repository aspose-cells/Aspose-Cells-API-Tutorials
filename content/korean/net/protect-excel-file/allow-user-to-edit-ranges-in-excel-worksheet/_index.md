---
title: 사용자가 Excel 워크시트에서 범위를 편집하도록 허용
linktitle: 사용자가 Excel 워크시트에서 범위를 편집하도록 허용
second_title: .NET API 참조용 Aspose.Cells
description: 사용자가 .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 특정 범위를 편집할 수 있도록 허용합니다. C#의 소스 코드를 단계별로 안내합니다.
type: docs
weight: 10
url: /ko/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
이 가이드에서는 사용자가 Excel 스프레드시트에서 특정 범위를 편집할 수 있도록 .NET용 Aspose.Cells를 사용하는 방법을 안내합니다. 이 작업을 수행하려면 아래 단계를 따르십시오.

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

만들려는 Excel 통합 문서를 나타내는 새 Workbook 개체를 인스턴스화합니다.

```csharp
Workbook book = new Workbook();
```

## 5단계: 첫 번째 워크시트에 액세스

다음 코드를 사용하여 Excel 통합 문서의 첫 번째 워크시트로 이동합니다.

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 6단계: 승인된 수정 범위 검색

 다음을 사용하여 허용된 편집 범위 컬렉션을 가져옵니다.`AllowEditRanges` 재산:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## 7단계: 보호 범위 정의

 다음을 사용하여 보호된 범위를 정의합니다.`Add` 의 방법`AllowEditRanges` 수집:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

여기서는 A1 셀에서 C3 셀까지의 보호 범위 "r2"를 만들었습니다.

## 8단계: 비밀번호 지정

 다음을 사용하여 보호된 범위에 대한 비밀번호를 지정합니다.`Password` 재산:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 꼭 교체하세요`"YOUR_PASSWORD"` 원하는 비밀번호로.

## 9단계: 워크시트 보호

 다음을 사용하여 워크시트를 보호하세요.`Protect` 의 방법`Worksheet` 물체:

```csharp
sheet.Protect(ProtectionType.All);
```

이렇게 하면 허용된 범위를 벗어나는 수정을 방지하여 스프레드시트를 보호할 수 있습니다.

## 10단계: 등록

  엑셀 파일

 생성된 Excel 파일을 다음을 사용하여 저장합니다.`Save` 의 방법`Workbook` 물체:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

원하는 파일 이름과 올바른 경로를 지정하십시오.

### .NET용 Aspose.Cells를 사용하여 Excel 워크시트에서 사용자가 범위를 편집할 수 있도록 허용하는 샘플 소스 코드 
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
proteced_range.Password = "123";
// 시트를 보호하세요
sheet.Protect(ProtectionType.All);
// 엑셀 파일을 저장하세요
book.Save(dataDir + "protectedrange.out.xls");
```

## 결론

이제 사용자가 Excel 스프레드시트에서 특정 범위를 편집할 수 있도록 .NET용 Aspose.Cells를 사용하는 방법을 배웠습니다. 귀하의 특정 요구 사항을 충족하기 위해 Aspose.Cells가 제공하는 기능을 더 자세히 살펴보십시오.


### 자주 묻는 질문

#### 1. 사용자가 Excel 스프레드시트에서 특정 범위를 편집할 수 있도록 허용하는 방법은 무엇입니까?

 당신은 사용할 수 있습니다`ProtectedRangeCollection` 허용되는 수정 범위를 정의하는 클래스입니다. 사용`Add` 원하는 셀로 새 보호 범위를 만드는 방법입니다.

#### 2. 승인된 수정 범위에 대해 비밀번호를 설정할 수 있나요?

 예, 다음을 사용하여 비밀번호를 지정할 수 있습니다.`Password` 의 재산`ProtectedRange` 물체. 이렇게 하면 비밀번호를 아는 사용자에게만 액세스가 제한됩니다.

#### 3. 허용 범위가 설정된 후 스프레드시트를 어떻게 보호합니까?

 사용`Protect` 의 방법`Worksheet` 워크시트를 보호하기 위한 개체입니다. 이렇게 하면 허용된 범위를 벗어나는 변경이 방지되며, 비밀번호를 지정한 경우 비밀번호를 묻는 메시지가 나타날 수 있습니다.