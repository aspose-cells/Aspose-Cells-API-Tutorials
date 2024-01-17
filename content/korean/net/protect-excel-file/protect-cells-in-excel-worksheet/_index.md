---
title: Excel 워크시트에서 셀 보호
linktitle: Excel 워크시트에서 셀 보호
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel의 특정 셀을 보호하는 방법을 알아보세요. C#의 단계별 튜토리얼입니다.
type: docs
weight: 30
url: /ko/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel은 스프레드시트를 만들고 관리하는 데 널리 사용되는 도구입니다. Excel의 핵심 기능 중 하나는 데이터 무결성을 유지하기 위해 특정 셀을 보호하는 기능입니다. 이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 Excel 스프레드시트의 특정 셀을 보호하는 방법을 단계별로 안내합니다. Aspose.Cells for .NET은 뛰어난 유연성과 고급 기능을 통해 Excel 파일을 쉽게 조작할 수 있게 해주는 강력한 프로그래밍 라이브러리입니다. 중요한 세포를 보호하고 데이터를 안전하게 유지하는 방법을 배우려면 제공된 단계를 따르십시오.

## 1단계: 환경 설정

개발 환경에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. Aspose 공식 웹사이트에서 라이브러리를 다운로드하고 설치 지침에 대한 설명서를 확인하세요.

## 2단계: 통합 문서 및 워크시트 초기화

시작하려면 새 통합 문서를 만들고 셀을 보호하려는 워크시트에 대한 참조를 가져와야 합니다. 다음 코드를 사용하세요.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// 디렉터리가 아직 없으면 만듭니다.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// 새 통합 문서 만들기
Workbook workbook = new Workbook();

// 첫 번째 워크시트 가져오기
Worksheet sheet = workbook.Worksheets[0];
```

 이 코드 조각에서는 먼저 Excel 파일이 저장될 디렉터리의 경로를 정의합니다. 다음으로, 새로운 인스턴스를 생성합니다.`Workbook` 클래스를 사용하여 첫 번째 워크시트에 대한 참조를 가져옵니다.`Worksheets` 재산.

## 3단계: 셀 스타일 정의

이제 보호하려는 셀의 스타일을 정의해야 합니다. 다음 코드를 사용하세요.

```csharp
// 스타일 객체 정의
Styling styling;

// 워크시트의 모든 열을 반복하고 잠금을 해제합니다.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 이 코드에서는 루프를 사용하여 워크시트의 모든 열을 반복하고 스타일을 설정하여 해당 셀의 잠금을 해제합니다.`IsLocked` 재산`false` . 그런 다음`ApplyStyle` 스타일을 사용하여 열에 스타일을 적용하는 방법`StyleFlag` 셀을 잠그는 플래그입니다.

## 4단계: 특정 셀 보호

이제 잠그려는 특정 셀을 보호하겠습니다. 다음 코드를 사용하세요.

```csharp
// 세 개의 셀(A1, B1, C1)을 잠급니다.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

 이 코드에서는 다음을 사용하여 각 특정 셀의 스타일을 가져옵니다.`GetStyle` 방법을 선택한 다음`IsLocked` 스타일의 속성`true`셀을 잠그려면 마지막으로 다음을 사용하여 업데이트된 스타일을 각 셀에 적용합니다.`SetStyle` 방법.

## 5단계: 워크시트 보호

이제 보호할 셀을 정의했으므로 워크시트 자체를 보호할 수 있습니다. 다음 코드를 사용하세요.

```csharp
// 워크시트를 보호하세요
leaf.Protect(ProtectionType.All);
```

 이 코드는`Protect` 지정된 보호 유형으로 워크시트를 보호하는 방법(이 경우)`ProtectionType.All` 워크시트의 모든 항목을 보호합니다.

## 6단계: Excel 파일 저장

마지막으로 변경 사항이 포함된 Excel 파일을 저장합니다. 다음 코드를 사용하세요.

```csharp
// 엑셀 파일을 저장하세요
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 이 코드에서는`Save` 지정된 디렉터리에 통합 문서를 저장하는 방법`Excel97To2003` 체재.

### .NET용 Aspose.Cells를 사용하여 Excel 워크시트의 셀 보호에 대한 샘플 소스 코드 
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
// styleflag 객체 정의
StyleFlag styleflag;
// 워크시트의 모든 열을 반복하고 잠금을 해제합니다.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// A1, B1, C1 등 세 개의 셀을 잠급니다.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// 마지막으로 지금 시트를 보호하세요.
sheet.Protect(ProtectionType.All);
// 엑셀 파일을 저장합니다.
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트의 특정 셀을 보호하는 방법을 배웠습니다. 이제 이 기술을 자신의 프로젝트에 적용하고 Excel 파일의 보안을 향상시킬 수 있습니다.


### 자주 묻는 질문

#### Q: Excel 스프레드시트의 셀을 보호하기 위해 Aspose.Cells for .NET을 사용해야 하는 이유는 무엇입니까?

A: Aspose.Cells for .NET은 Excel 파일 작업을 쉽게 해주는 강력한 라이브러리입니다. 셀 보호, 범위 잠금 해제 등의 고급 기능을 제공합니다.

#### Q: 개별 셀이 아닌 셀 범위를 보호하는 것이 가능합니까?

 A: 예, 다음을 사용하여 보호할 특정 셀 범위를 정의할 수 있습니다.`ApplyStyle` 적절한 방법을 사용하여`StyleFlag`.

#### Q: 보호된 Excel 파일을 저장한 후 어떻게 열 수 있나요?

A: 보호된 Excel 파일을 열 때 워크시트 보호 시 지정한 비밀번호를 제공해야 합니다.

#### Q: Excel 스프레드시트에 적용할 수 있는 다른 유형의 보호가 있습니까?

A: 예, Aspose.Cells for .NET은 구조 보호, 창 보호 등과 같은 다양한 유형의 보호를 지원합니다. 필요에 따라 적절한 보호 유형을 선택할 수 있습니다.