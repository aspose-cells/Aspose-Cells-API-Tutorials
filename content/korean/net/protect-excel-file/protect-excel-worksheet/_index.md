---
title: Excel 워크시트 보호
linktitle: Excel 워크시트 보호
second_title: .NET API 참조용 Aspose.Cells
description: 이 튜토리얼에서 .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트를 보호하는 방법을 알아보세요. C#의 단계별 가이드입니다.
type: docs
weight: 50
url: /ko/net/protect-excel-file/protect-excel-worksheet/
---
이 튜토리얼에서는 Aspose.Cells 라이브러리를 사용하여 Excel 스프레드시트를 보호하는 일부 C# 소스 코드를 살펴보겠습니다. 코드의 각 단계를 살펴보고 작동 방식을 설명하겠습니다. 원하는 결과를 얻으려면 지침을 주의 깊게 따르십시오.

## 1단계: 전제조건

시작하기 전에 .NET용 Aspose.Cells 라이브러리를 설치했는지 확인하세요. Aspose 공식 홈페이지에서 받으실 수 있습니다. 또한 최신 버전의 Visual Studio 또는 기타 C# 개발 환경이 있는지 확인하세요.

## 2단계: 필수 네임스페이스 가져오기

Aspose.Cells 라이브러리를 사용하려면 필요한 네임스페이스를 코드로 가져와야 합니다. C# 소스 파일 맨 위에 다음 줄을 추가합니다.

```csharp
using Aspose.Cells;
using System.IO;
```

## 3단계: Excel 파일 로드

이 단계에서는 보호하려는 Excel 파일을 로드합니다. Excel 파일이 포함된 디렉터리에 대한 올바른 경로를 지정해야 합니다. 파일을 업로드하려면 다음 코드를 사용하세요.

```csharp
// 문서 디렉터리의 경로입니다.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// 열려는 Excel 파일이 포함된 파일 스트림을 만듭니다.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// 통합 문서 개체를 인스턴스화합니다.
//파일 스트림을 통해 Excel 파일을 엽니다.
Workbook excel = new Workbook(fstream);
```

 꼭 교체하세요`"YOUR_DOCUMENTS_DIR"` 문서 디렉토리에 대한 적절한 경로를 사용하십시오.

## 4단계: 스프레드시트에 액세스

이제 Excel 파일을 로드했으므로 첫 번째 워크시트에 액세스할 수 있습니다. 다음 코드를 사용하여 첫 번째 워크시트에 액세스합니다.

```csharp
// Excel 파일의 첫 번째 워크시트에 액세스합니다.
Worksheet worksheet = excel.Worksheets[0];
```

## 5단계: 워크시트 보호

이 단계에서는 비밀번호를 사용하여 스프레드시트를 보호합니다. 스프레드시트를 보호하려면 다음 코드를 사용하세요.

```csharp
// 워크시트를 비밀번호로 보호하세요.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 바꾸다`"YOUR_PASSWORD"` 스프레드시트를 보호하는 데 사용하려는 비밀번호를 입력하세요.

## 6단계: 수정된 Excel 파일 저장 이제 보호가 완료되었습니다.

é 스프레드시트에서는 수정된 Excel 파일을 기본 형식으로 저장합니다. 다음 코드를 사용하여 Excel 파일을 저장합니다.

```csharp
// 수정된 Excel 파일을 기본 형식으로 저장합니다.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

수정된 Excel 파일을 저장하려면 올바른 경로를 지정해야 합니다.

## 7단계: 파일 스트림 닫기

모든 리소스를 해제하려면 Excel 파일을 로드하는 데 사용된 파일 스트림을 닫아야 합니다. 파일 스트림을 닫으려면 다음 코드를 사용하십시오.

```csharp
// 모든 리소스를 해제하려면 파일 스트림을 닫으세요.
fstream.Close();
```

코드 끝에 이 단계를 포함해야 합니다.


### .NET용 Aspose.Cells를 사용하여 Excel 워크시트 보호를 위한 샘플 소스 코드 
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
// 비밀번호로 워크시트 보호하기
worksheet.Protect(ProtectionType.All, "aspose", null);
// 수정된 Excel 파일을 기본 형식으로 저장
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```

## 결론

축하합니다! 이제 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 스프레드시트를 보호할 수 있는 C# 소스 코드가 생겼습니다. 단계를 주의 깊게 따르고 특정 요구 사항에 맞게 코드를 사용자 정의하십시오.

### FAQ(자주 묻는 질문)

#### 하나의 Excel 파일에서 여러 워크시트를 보호할 수 있습니까?

A: 예, 각 워크시트에 대해 4~6단계를 반복하여 하나의 Excel 파일에 있는 여러 워크시트를 보호할 수 있습니다.

#### 인증된 사용자에 대한 특정 권한을 어떻게 지정합니까?

 A: 에서 제공하는 추가 옵션을 사용할 수 있습니다.`Protect`인증된 사용자에게 특정 권한을 지정하는 방법입니다. 자세한 내용은 Aspose.Cells 설명서를 참조하세요.

#### Excel 파일 자체를 비밀번호로 보호할 수 있나요?

A: 예, Aspose.Cells 라이브러리에서 제공하는 다른 방법을 사용하여 Excel 파일 자체를 비밀번호로 보호할 수 있습니다. 구체적인 예는 설명서를 참조하세요.

#### Aspose.Cells 라이브러리는 다른 Excel 파일 형식을 지원합니까?

A: 예, Aspose.Cells 라이브러리는 XLSX, XLSM, XLSB, CSV 등을 포함한 광범위한 Excel 파일 형식을 지원합니다.