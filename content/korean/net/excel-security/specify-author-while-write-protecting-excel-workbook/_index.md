---
title: Excel 통합 문서 쓰기를 보호하는 동안 작성자 지정
linktitle: Excel 통합 문서 쓰기를 보호하는 동안 작성자 지정
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 통합 문서를 보호하고 사용자 지정하는 방법을 알아보세요. C#의 단계별 튜토리얼입니다.
type: docs
weight: 30
url: /ko/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

이 튜토리얼에서는 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 통합 문서 쓰기 보호 시 작성자를 지정하는 방법을 보여줍니다.

## 1단계: 환경 준비

시작하기 전에 컴퓨터에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. Aspose 공식 웹사이트에서 라이브러리를 다운로드하고 제공된 설치 지침을 따르세요.

## 2단계: 소스 및 출력 디렉터리 구성

제공된 소스 코드에서 소스 및 출력 디렉터리를 지정해야 합니다. 수정하다`sourceDir` 그리고`outputDir` "YOUR SOURCE DIRECTORY" 및 "YOUR OUTPUT DIRECTORY"를 컴퓨터의 해당 절대 경로로 대체하여 변수를 변경합니다.

```csharp
// 소스 디렉터리
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// 출력 디렉토리
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## 3단계: 빈 Excel 통합 문서 만들기

시작하려면 빈 Excel 통합 문서를 나타내는 Workbook 개체를 만듭니다.

```csharp
// 빈 통합 문서를 만듭니다.
Workbook wb = new Workbook();
```

## 4단계: 비밀번호로 쓰기 방지

 다음으로, 다음을 사용하여 Excel 통합 문서 쓰기를 보호하기 위한 비밀번호를 지정합니다.`WriteProtection.Password` 통합 문서 개체의 속성입니다.

```csharp
// 비밀번호로 통합 문서를 보호하세요.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## 5단계: 작성자 사양

 이제 다음을 사용하여 Excel 통합 문서의 작성자를 지정합니다.`WriteProtection.Author` 통합 문서 개체의 속성입니다.

```csharp
// 통합 문서 쓰기를 보호하는 동안 작성자를 지정하세요.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## 6단계: 보호된 Excel 통합 문서 백업

 쓰기 방지 및 작성자가 지정되면 다음을 사용하여 Excel 통합 문서를 XLSX 형식으로 저장할 수 있습니다.`Save()` 방법.

```csharp
// 통합 문서를 XLSX 형식으로 저장합니다.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### .NET용 Aspose.Cells를 사용하여 쓰기 보호하는 동안 작성자 지정 Excel 통합 문서에 대한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = "YOUR SOURCE DIRECTORY";

//출력 디렉토리
string outputDir = "YOUR OUTPUT DIRECTORY";

// 빈 통합 문서를 만듭니다.
Workbook wb = new Workbook();

// 비밀번호로 통합 문서를 보호하세요.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// 통합 문서 쓰기를 보호하는 동안 작성자를 지정하세요.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// 통합 문서를 XLSX 형식으로 저장합니다.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## 결론

축하합니다! 이제 Aspose.Cells for .NET을 사용하여 Excel 통합 문서 쓰기 보호 시 작성자를 지정하는 방법을 배웠습니다. 이러한 단계를 자신의 프로젝트에 적용하여 Excel 통합 문서를 보호하고 사용자 지정할 수 있습니다.

Excel 파일에 대한 고급 작업을 수행하려면 .NET용 Aspose.Cells의 기능을 더 자세히 살펴보세요.

## 자주 묻는 질문

#### Q: 비밀번호를 지정하지 않고 Excel 통합 문서 쓰기를 보호할 수 있나요?

 A: 예, 통합 문서 개체의`WriteProtect()` Excel 통합 문서 쓰기를 보호하려면 암호를 지정하지 않고 메서드를 사용하세요. 이렇게 하면 비밀번호를 요구하지 않고 통합 문서에 대한 변경이 제한됩니다.

#### Q: Excel 통합 문서에서 쓰기 방지를 어떻게 제거합니까?

 A: Excel 통합 문서에서 쓰기 금지를 제거하려면 다음을 사용할 수 있습니다.`Unprotect()` Worksheet 개체의 메서드 또는`RemoveWriteProtection()` 특정 사용 사례에 따라 Workbook 개체의 메서드를 사용합니다. .

#### Q: Excel 통합 문서를 보호하기 위한 비밀번호를 잊어버렸습니다. 어떡해 ?

A: Excel 통합 문서를 보호하기 위한 비밀번호를 잊어버린 경우 비밀번호를 직접 제거할 수 없습니다. 그러나 보호된 Excel 파일에 대한 암호 복구 기능을 제공하는 전문적인 타사 도구를 사용해 볼 수 있습니다.

#### Q: Excel 통합 문서 쓰기 금지 시 작성자를 여러 명 지정할 수 있나요?

A: 아니요. .NET용 Aspose.Cells 라이브러리를 사용하면 Excel 통합 문서 쓰기 금지 시 단일 작성자를 지정할 수 있습니다. 여러 명의 작성자를 지정하려면 엑셀 파일을 직접 조작하는 방식의 맞춤형 솔루션을 고려해야 합니다.