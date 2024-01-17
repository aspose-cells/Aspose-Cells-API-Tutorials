---
title: Excel 워크시트에서 행 보호
linktitle: Excel 워크시트에서 행 보호
second_title: .NET API 참조용 Aspose.Cells
description: 이 튜토리얼에서 .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트의 행을 보호하는 방법을 알아보세요. C#의 단계별 튜토리얼입니다.
type: docs
weight: 60
url: /ko/net/protect-excel-file/protect-row-in-excel-worksheet/
---
이 자습서에서는 Aspose.Cells 라이브러리를 사용하여 Excel 스프레드시트의 행을 보호하는 일부 C# 소스 코드를 살펴보겠습니다. 코드의 각 단계를 살펴보고 작동 방식을 설명하겠습니다. 원하는 결과를 얻으려면 지침을 주의 깊게 따르십시오.

## 1단계: 전제조건

시작하기 전에 .NET용 Aspose.Cells 라이브러리를 설치했는지 확인하세요. Aspose 공식 홈페이지에서 받으실 수 있습니다. 또한 최신 버전의 Visual Studio 또는 기타 C# 개발 환경이 있는지 확인하세요.

## 2단계: 필수 네임스페이스 가져오기

Aspose.Cells 라이브러리를 사용하려면 필요한 네임스페이스를 코드로 가져와야 합니다. C# 소스 파일 맨 위에 다음 줄을 추가합니다.

```csharp
using Aspose.Cells;
```

## 3단계: Excel 통합 문서 만들기

이 단계에서는 새로운 Excel 통합 문서를 만듭니다. 다음 코드를 사용하여 Excel 통합 문서를 만듭니다.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// 새 통합 문서를 만듭니다.
Workbook wb = new Workbook();
```

 꼭 교체하세요`"YOUR_DOCUMENTS_DIR"` 문서 디렉토리에 대한 적절한 경로를 사용하십시오.

## 4단계: 스프레드시트 만들기

이제 Excel 통합 문서를 만들었으므로 워크시트를 만들고 첫 번째 시트를 가져옵니다. 다음 코드를 사용하세요.

```csharp
// 스프레드시트 개체를 만들고 첫 번째 시트를 가져옵니다.
Worksheet sheet = wb.Worksheets[0];
```

## 5단계: 스타일 정의

이 단계에서는 스프레드시트의 행에 적용할 스타일을 정의합니다. 다음 코드를 사용하세요.

```csharp
// 스타일 객체의 정의.
Styling styling;
```

## 6단계: 반복하여 모든 열 잠금 해제

이제 워크시트의 모든 열을 반복하여 잠금을 해제하겠습니다. 다음 코드를 사용하세요.

```csharp
// 워크시트의 모든 열을 반복하고 잠금을 해제합니다.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## 7단계: 첫 번째 줄 잠그기

이 단계에서는 워크시트의 첫 번째 행을 잠급니다. 다음 코드를 사용하세요.

```csharp
// 첫 번째 줄의 스타일을 가져옵니다.
style = sheet.Cells.Rows[0].Style;
// 스타일을 잠급니다.
style. IsLocked = true;
// 첫 번째 줄에 스타일을 적용합니다.
sheet.Cells.ApplyRowStyle(0, style);
```

## 8단계: 워크시트 보호

이제 스타일을 설정하고 행을 잠갔으므로 스프레드시트를 보호해 보겠습니다. 다음 코드를 사용하세요.

```csharp
// 워크시트를 보호하세요.
sheet.Protect(ProtectionType.All);
```

## 9단계: Excel 파일 저장

마지막으로 수정된 엑셀 파일을 저장하겠습니다. 다음 코드를 사용하세요.

```csharp
// 엑셀 파일을 저장합니다.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

수정된 Excel 파일을 저장하려면 올바른 경로를 지정해야 합니다.

### .NET용 Aspose.Cells를 사용하는 Excel 워크시트의 행 보호에 대한 샘플 소스 코드 
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

축하합니다! 이제 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 스프레드시트의 행을 보호할 수 있는 C# 소스 코드가 생겼습니다. 단계를 주의 깊게 따르고 특정 요구 사항에 맞게 코드를 사용자 정의하십시오.

### FAQ(자주 묻는 질문)

#### 이 코드는 최신 버전의 Excel에서 작동하나요?

예, 이 코드는 Excel 2010 이상 형식의 파일을 포함하여 최신 버전의 Excel에서 작동합니다.

#### 워크시트의 모든 행이 아닌 특정 행만 보호할 수 있나요?

예, 코드를 수정하여 보호하려는 특정 행을 지정할 수 있습니다. 이에 따라 루프와 인덱스를 조정해야 합니다.

#### 잠긴 회선을 다시 잠금 해제하려면 어떻게 해야 합니까?

 당신은 사용할 수 있습니다`IsLocked` 의 방법`Style` 값을 설정할 객체`false` 행의 잠금을 해제합니다.

#### 동일한 Excel 통합 문서에서 여러 워크시트를 보호할 수 있습니까?

예. 통합 문서의 각 워크시트에 대해 워크시트 만들기, 스타일 설정 및 보호 단계를 반복할 수 있습니다.

#### 스프레드시트 보호 비밀번호를 어떻게 변경할 수 있나요?

 다음을 사용하여 비밀번호를 변경할 수 있습니다.`Protect` 메서드를 사용하고 새 비밀번호를 인수로 지정합니다.