---
title: Excel 워크시트의 특정 열 보호
linktitle: Excel 워크시트의 특정 열 보호
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 시트의 특정 열을 보호하는 방법을 알아보세요. C#의 단계별 가이드입니다.
type: docs
weight: 80
url: /ko/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
C#에서 Excel 워크시트로 작업할 때 실수로 수정되는 것을 방지하기 위해 특정 열을 보호해야 하는 경우가 많습니다. 이 튜토리얼에서는 Aspose.Cells for .NET 라이브러리를 사용하여 Excel 워크시트의 특정 열을 보호하는 과정을 안내합니다. 이 작업에 필요한 C# 소스 코드에 대한 단계별 설명을 제공합니다. 자, 시작해 봅시다!

## Excel 워크시트의 특정 열 보호 개요

Excel 워크시트의 특정 열을 보호하면 해당 열이 잠긴 상태로 유지되며 적절한 인증 없이는 수정할 수 없습니다. 이는 사용자가 워크시트의 나머지 부분과 상호 작용할 수 있도록 허용하면서 특정 데이터나 수식에 대한 편집 액세스를 제한하려는 경우 특히 유용합니다. .NET용 Aspose.Cells 라이브러리는 열 보호를 포함하여 Excel 파일을 프로그래밍 방식으로 조작할 수 있는 포괄적인 기능 세트를 제공합니다.

## 환경 설정

시작하기 전에 개발 환경에 .NET용 Aspose.Cells 라이브러리가 설치되어 있는지 확인하세요. 공식 Aspose 웹사이트에서 라이브러리를 다운로드하고 제공된 설치 프로그램을 사용하여 설치할 수 있습니다.

## 새 통합 문서 및 워크시트 만들기

특정 열 보호를 시작하려면 Aspose.Cells for .NET을 사용하여 새 통합 문서와 워크시트를 만들어야 합니다. 코드 조각은 다음과 같습니다.

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";

// 디렉터리가 아직 없으면 만듭니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// 새 통합 문서를 만듭니다.
Workbook wb = new Workbook();

// 워크시트 개체를 만들고 첫 번째 시트를 얻습니다.
Worksheet sheet = wb.Worksheets[0];
```

"YOUR DOCUMENT DIRECTORY"를 Excel 파일을 저장하려는 실제 디렉터리 경로로 바꾸십시오.

## 스타일 및 스타일 플래그 객체 정의

열에 대한 특정 스타일과 보호 플래그를 설정하려면 스타일 및 스타일 플래그 개체를 정의해야 합니다. 코드 조각은 다음과 같습니다.

```csharp
// 스타일 객체를 정의합니다.
Style style;

// 스타일 플래그 객체를 정의합니다.
StyleFlag flag;
```

## 열을 반복하고 잠금 해제하기

다음으로 워크시트의 모든 열을 반복하여 잠금을 해제해야 합니다. 이렇게 하면 보호하려는 열을 제외한 모든 열을 편집할 수 있습니다. 코드 조각은 다음과 같습니다.

```csharp
// 워크시트의 모든 열을 반복하고 잠금을 해제합니다.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## 특정 열 잠금

이제 특정 열을 잠그겠습니다. 이 예에서는 첫 번째 열(열 인덱스 0)을 잠급니다. 코드 조각은 다음과 같습니다.

```csharp
// 첫 번째 열 스타일을 가져옵니다.
style = sheet.Cells.Columns[0].Style;

// 잠그세요.
style.IsLocked = true;
```

## 열에 스타일 적용

특정 열을 잠근 후 해당 열에 스타일과 플래그를 적용해야 합니다. 코드 조각은 다음과 같습니다.

```csharp
//플래그를 인스턴스화합니다.
flag = new StyleFlag();

// 잠금 설정을 설정하세요.
flag.Locked = true;

// 첫 번째 열에 스타일을 적용합니다.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## 워크시트 보호

보호를 완료하려면 잠긴 열을 수정할 수 없도록 워크시트를 보호해야 합니다. 코드 조각은 다음과 같습니다.

```csharp
// 시트를 보호하세요.
sheet.Protect(ProtectionType.All);
```

## 엑셀 파일 저장

마지막으로 수정된 엑셀 파일을 원하는 위치에 저장하겠습니다. 코드 조각은 다음과 같습니다.

```csharp
// 엑셀 파일을 저장합니다.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

"output.out.xls"를 원하는 파일 이름과 확장자로 바꾸십시오.

### .NET용 Aspose.Cells를 사용하는 Excel 워크시트의 특정 열 보호에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 디렉터리가 아직 없으면 만듭니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// 새 통합 문서를 만듭니다.
Workbook wb = new Workbook();
// 워크시트 개체를 만들고 첫 번째 시트를 얻습니다.
Worksheet sheet = wb.Worksheets[0];
// 스타일 객체를 정의합니다.
Style style;
// styleflag 개체를 정의합니다.
StyleFlag flag;
// 워크시트의 모든 열을 반복하고 잠금을 해제합니다.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// 첫 번째 열 스타일을 가져옵니다.
style = sheet.Cells.Columns[0].Style;
// 잠그세요.
style.IsLocked = true;
//플래그를 인스턴스화합니다.
flag = new StyleFlag();
// 잠금 설정을 설정하세요.
flag.Locked = true;
// 첫 번째 열에 스타일을 적용합니다.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// 시트를 보호하세요.
sheet.Protect(ProtectionType.All);
// 엑셀 파일을 저장합니다.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 결론

이 튜토리얼에서는 Aspose.Cells for .NET 라이브러리를 사용하여 Excel 워크시트의 특정 열을 보호하는 단계별 프로세스를 설명했습니다. 먼저 새 통합 문서와 워크시트를 만들고 스타일과 스타일 플래그 개체를 정의한 다음 특정 열의 잠금을 해제하고 잠그는 작업을 진행했습니다. 마지막으로 워크시트를 보호하고 수정된 Excel 파일을 저장했습니다. 이 가이드를 따르면 이제 C# 및 .NET용 Aspose.Cells를 사용하여 Excel 워크시트의 특정 열을 보호할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### 이 방법을 사용하여 여러 열을 보호할 수 있나요?

예, 그에 따라 코드를 수정하여 여러 열을 보호할 수 있습니다. 원하는 열 범위를 반복하고 잠금 스타일과 플래그를 적용하기만 하면 됩니다.

#### 보호된 워크시트를 비밀번호로 보호할 수 있나요?

 예, 전화를 걸 때 비밀번호를 지정하여 보호된 워크시트에 비밀번호 보호를 추가할 수 있습니다.`Protect` 방법.

#### .NET용 Aspose.Cells는 다른 Excel 파일 형식을 지원합니까?

예, .NET용 Aspose.Cells는 XLS, XLSX, XLSM 등을 포함한 다양한 Excel 파일 형식을 지원합니다.

#### 열 대신 특정 행을 보호할 수 있나요?

예, 열 셀 대신 행 셀에 스타일과 플래그를 적용하여 열 대신 특정 행을 보호하도록 코드를 수정할 수 있습니다.