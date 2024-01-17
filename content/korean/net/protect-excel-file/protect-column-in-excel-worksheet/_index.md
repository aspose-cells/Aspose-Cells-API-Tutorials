---
title: Excel 워크시트의 열 보호
linktitle: Excel 워크시트의 열 보호
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel의 특정 열을 보호하는 방법을 알아보세요. 자세한 단계와 소스 코드가 포함되어 있습니다.
type: docs
weight: 40
url: /ko/net/protect-excel-file/protect-column-in-excel-worksheet/
---
Microsoft Excel은 스프레드시트 형식으로 데이터를 관리하고 분석하는 데 널리 사용되는 응용 프로그램입니다. 정보의 무결성과 기밀성을 보장하려면 민감한 데이터를 보호하는 것이 필수적입니다. 이 튜토리얼에서는 Aspose.Cells for .NET 라이브러리를 사용하여 Excel 스프레드시트의 특정 열을 보호하는 방법을 단계별로 안내합니다. Aspose.Cells for .NET은 Excel 파일을 처리하고 보호하기 위한 강력한 기능을 제공합니다. 특정 열의 데이터를 보호하고 Excel 스프레드시트를 보호하는 방법을 알아보려면 제공된 단계를 따르세요.
## 1단계: 디렉터리 설정

Excel 파일을 저장할 디렉터리를 정의하는 것부터 시작하세요. 다음 코드를 사용하세요.

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// 디렉터리가 없으면 만듭니다.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);
```

이 코드는 디렉터리가 이미 존재하는지 확인하고, 없으면 디렉터리를 생성합니다.

## 2단계: 새 통합 문서 만들기

다음으로 새 Excel 통합 문서를 만들고 첫 번째 워크시트를 가져옵니다. 다음 코드를 사용하세요.

```csharp
// 새 통합 문서를 만듭니다.
Workbook workbook = new Workbook();
// 스프레드시트 개체를 만들고 첫 번째 시트를 가져옵니다.
Worksheet sheet = workbook.Worksheets[0];
```

 이 코드는 새로운`Workbook` 개체를 사용하여 첫 번째 워크시트를 가져옵니다.`Worksheets[0]`.

## 3단계: 열 잠금 해제

워크시트의 모든 열을 잠금 해제하기 위해 루프를 사용하여 모든 열을 반복하고 잠금 해제 스타일을 적용합니다. 다음 코드를 사용하세요.

```csharp
// 스타일 개체를 설정합니다.
Styling styling;
// styleflag 개체를 설정합니다.
StyleFlag flag;
// 워크시트의 모든 열을 반복하고 잠금을 해제합니다.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

 이 코드는 워크시트의 각 열을 반복하고 다음을 설정하여 스타일의 잠금을 해제합니다.`IsLocked` 에게`false`.

## 4단계: 특정 열 잠금

이제 잠긴 스타일을 적용하여 특정 열을 잠그겠습니다. 다음 코드를 사용하세요.

```csharp
// 첫 번째 열의 스타일을 가져옵니다.
style = sheet.Cells.Columns[0].Style;
// 잠그세요.
style. IsLocked = true;
// 플래그 객체를 인스턴스화합니다.
flag = new StyleFlag();
// 잠금 매개변수를 설정합니다.
flag. Locked = true;
// 첫 번째 열에 스타일을 적용합니다.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

 이 코드는 다음을 사용하여 첫 번째 열을 선택합니다.`Columns[0]` 을 선택한 다음 스타일을 설정합니다.`IsLocked` 에게`true` 열을 잠그려면 마지막으로 다음을 사용하여 첫 번째 열에 스타일을 적용합니다.`ApplyStyle` 방법.

## 5단계: 워크시트 보호

이제 특정 열을 잠갔으므로 워크시트 자체를 보호할 수 있습니다. 다음 코드를 사용하세요.



```csharp
// 워크시트를 보호하세요.
leaf.Protect(ProtectionType.All);
```

 이 코드는`Protect` 보호 유형을 지정하여 워크시트를 보호하는 방법입니다.

## 6단계: Excel 파일 저장

마지막으로 원하는 디렉토리 경로와 파일 이름을 사용하여 Excel 파일을 저장합니다. 다음 코드를 사용하세요.

```csharp
// 엑셀 파일을 저장합니다.
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

 이 코드는`Save` 의 방법`Workbook` 지정된 이름과 파일 형식으로 Excel 파일을 저장하는 개체입니다.

### .NET용 Aspose.Cells를 사용하는 Excel 워크시트의 열 보호에 대한 샘플 소스 코드 
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

.NET용 Aspose.Cells를 사용하여 Excel 스프레드시트의 열을 보호하기 위한 단계별 튜토리얼을 따라하셨습니다. 모든 열을 잠금 해제하고, 특정 열을 잠그고, 워크시트 자체를 보호하는 방법을 배웠습니다. 이제 이러한 개념을 자신의 프로젝트에 적용하고 Excel 데이터를 보호할 수 있습니다.

## 자주 묻는 질문

#### Q: Excel 스프레드시트의 특정 열을 보호하는 것이 왜 중요한가요?

A: Excel 스프레드시트의 특정 열을 보호하면 중요한 데이터의 액세스 및 수정을 제한하여 정보 무결성과 기밀성을 보장할 수 있습니다.

#### Q: Aspose.Cells for .NET은 Excel 파일 처리를 위한 다른 기능을 지원합니까?

A: 예, Aspose.Cells for .NET은 Excel 파일 생성, 편집, 변환 및 보고를 포함한 광범위한 기능을 제공합니다.

#### Q: Excel 스프레드시트의 모든 열을 잠금 해제하려면 어떻게 해야 합니까?

A: .NET용 Aspose.Cells에서는 루프를 사용하여 모든 열을 반복하고 잠금 스타일을 "false"로 설정하여 모든 열을 잠금 해제할 수 있습니다.

#### Q: .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트를 어떻게 보호할 수 있나요?

 A: 다음을 사용할 수 있습니다.`Protect` 구조 보호, 셀 보호 등 다양한 보호 수준으로 시트를 보호하는 워크시트 개체 방법입니다.

#### Q: 다른 유형의 Excel 파일에 이러한 열 보호 개념을 적용할 수 있나요?

A: 예, Aspose.Cells for .NET의 열 보호 개념은 Excel 97-2003 파일(.xls) 및 최신 Excel 파일(.xlsx)과 같은 모든 유형의 Excel 파일에 적용 가능합니다.