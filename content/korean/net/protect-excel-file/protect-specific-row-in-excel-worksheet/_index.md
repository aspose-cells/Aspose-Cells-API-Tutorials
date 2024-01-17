---
title: Excel 워크시트의 특정 행 보호
linktitle: Excel 워크시트의 특정 행 보호
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel의 특정 행을 보호하세요. 기밀 데이터 보안을 위한 단계별 가이드입니다.
type: docs
weight: 90
url: /ko/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
정보 보안을 보장하려면 Excel 스프레드시트의 기밀 데이터를 보호하는 것이 필수적입니다. Aspose.Cells for .NET은 Excel 스프레드시트의 특정 행을 보호하는 강력한 솔루션을 제공합니다. 이 가이드에서는 제공된 C# 소스 코드를 사용하여 Excel 워크시트의 특정 행을 보호하는 방법을 안내합니다. Excel 파일에서 행 보호를 설정하려면 다음의 간단한 단계를 따르세요.

## 1단계: 필수 라이브러리 가져오기

시작하려면 시스템에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. 또한 Aspose.Cells의 기능을 사용하려면 C# 프로젝트에 적절한 참조를 추가해야 합니다. 필요한 라이브러리를 가져오는 코드는 다음과 같습니다.

```csharp
// 필요한 참조 추가
using Aspose.Cells;
```

## 2단계: Excel 통합 문서 및 스프레드시트 만들기

필요한 라이브러리를 가져온 후 새 Excel 통합 문서와 새 워크시트를 만들 수 있습니다. 수행 방법은 다음과 같습니다.

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// 디렉터리가 아직 없으면 만듭니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// 새 통합 문서를 만듭니다.
Workbook wb = new Workbook();

// 스프레드시트 개체를 만들고 첫 번째 시트를 가져옵니다.
Worksheet sheet = wb.Worksheets[0];
```

## 3단계: 스타일 및 스타일 플래그 설정

이제 워크시트의 모든 열을 잠금 해제하기 위해 셀 스타일과 스타일 플래그를 설정하겠습니다. 필요한 코드는 다음과 같습니다.

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
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## 4단계: 특정 회선 보호

이제 워크시트의 특정 행을 보호하겠습니다. 수정을 방지하기 위해 첫 번째 행을 잠그겠습니다. 방법은 다음과 같습니다.

```csharp
// 첫 번째 줄의 스타일을 가져옵니다.
style = sheet.Cells.Rows[0].Style;

// 잠그세요.
style. IsLocked = true;

//플래그를 인스턴스화합니다.
flag = new StyleFlag();

// 잠금 매개변수를 설정합니다.
flag. Locked = true;

// 첫 번째 줄에 스타일을 적용합니다.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## 5단계: 워크시트 보호

마지막으로, 무단 수정을 방지하기 위해 Excel 워크시트 전체를 보호하겠습니다. 방법은 다음과 같습니다.

```csharp
// 워크시트를 보호하세요.
sheet.Protect(ProtectionType.All);
```

## 6단계: 보호된 Excel 파일 저장

Excel 워크시트의 특정 행 보호를 완료하면 보호된 Excel 파일을 시스템에 저장할 수 있습니다. 방법은 다음과 같습니다.

```csharp
// 엑셀 파일을 저장합니다.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

이 단계를 수행하면 Aspose.Cells for .NET을 사용하여 Excel 스프레드시트의 특정 행을 성공적으로 보호하게 됩니다.

### .NET용 Aspose.Cells를 사용하여 Excel 워크시트의 특정 행 보호에 대한 샘플 소스 코드 
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
// 첫 번째 행 스타일을 가져옵니다.
style = sheet.Cells.Rows[0].Style;
// 잠그세요.
style.IsLocked = true;
//플래그를 인스턴스화합니다.
flag = new StyleFlag();
// 잠금 설정을 설정하세요.
flag.Locked = true;
// 첫 번째 행에 스타일을 적용합니다.
sheet.Cells.ApplyRowStyle(0, style, flag);
// 시트를 보호하세요.
sheet.Protect(ProtectionType.All);
// 엑셀 파일을 저장합니다.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 결론

무단 액세스나 원치 않는 수정을 방지하려면 Excel 파일의 데이터를 보호하는 것이 중요합니다. .NET용 Aspose.Cells 라이브러리를 사용하면 제공된 C# 소스 코드를 사용하여 Excel 스프레드시트의 특정 행을 쉽게 보호할 수 있습니다. Excel 파일에 추가 보안 계층을 추가하려면 이 단계별 가이드를 따르세요.

### 자주 묻는 질문

#### 모든 버전의 Excel에서 특정 행 보호가 작동하나요?

예, .NET용 Aspose.Cells를 사용한 특정 행 보호는 지원되는 모든 Excel 버전에서 작동합니다.

#### Excel 스프레드시트의 여러 특정 행을 보호할 수 있나요?

예, 이 가이드에 설명된 유사한 방법을 사용하여 여러 특정 행을 보호할 수 있습니다.

#### Excel 스프레드시트에서 특정 행의 잠금을 해제하려면 어떻게 해야 하나요?

 특정 행을 잠금 해제하려면 다음을 사용하여 그에 따라 소스 코드를 수정해야 합니다.`IsLocked` 의 방법`Style` 물체.