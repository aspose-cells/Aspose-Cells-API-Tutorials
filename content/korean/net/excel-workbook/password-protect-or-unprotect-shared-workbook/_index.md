---
title: 비밀번호 보호 또는 공유 통합 문서 보호 해제
linktitle: 비밀번호 보호 또는 공유 통합 문서 보호 해제
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 공유 통합 문서를 비밀번호로 보호하거나 보호 해제하는 방법을 알아보세요.
type: docs
weight: 120
url: /ko/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
데이터 개인정보 보호를 위해서는 공유 통합 문서를 비밀번호로 보호하는 것이 중요합니다. Aspose.Cells for .NET을 사용하면 비밀번호를 사용하여 공유 통합 문서를 쉽게 보호하거나 보호 해제할 수 있습니다. 원하는 결과를 얻으려면 아래 단계를 따르십시오.

## 1단계: 출력 디렉터리 지정

먼저 보호된 Excel 파일이 저장될 출력 디렉터리를 지정해야 합니다. Aspose.Cells를 사용하여 수행하는 방법은 다음과 같습니다.

```csharp
// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2단계: 빈 Excel 파일 만들기

그런 다음 보호 또는 보호 해제를 적용하려는 빈 Excel 파일을 만들 수 있습니다. 다음은 샘플 코드입니다.

```csharp
// 빈 Excel 통합 문서 만들기
Workbook wb = new Workbook();
```

## 3단계: 공유 통합 문서 보호 또는 보호 해제

통합 문서를 만든 후 적절한 암호를 지정하여 공유 통합 문서를 보호하거나 보호 해제할 수 있습니다. 방법은 다음과 같습니다.

```csharp
// 비밀번호로 공유 통합 문서를 보호하세요
wb.ProtectSharedWorkbook("1234");

// 공유 통합 문서의 보호를 해제하려면 이 줄의 주석 처리를 해제하세요.
// wb.UnprotectSharedWorkbook("1234");
```

## 4단계: 출력 Excel 파일 저장

보호 또는 보호 해제를 적용하면 보호된 Excel 파일을 지정된 출력 디렉터리에 저장할 수 있습니다. 수행 방법은 다음과 같습니다.

```csharp
// 출력 Excel 파일 저장
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### .NET용 Aspose.Cells를 사용하여 공유 통합 문서를 암호로 보호하거나 보호 해제하는 샘플 소스 코드 
```csharp
//출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
//빈 Excel 파일 만들기
Workbook wb = new Workbook();
//비밀번호로 공유 통합 문서 보호
wb.ProtectSharedWorkbook("1234");
//공유 통합 문서 보호를 해제하려면 이 줄의 주석 처리를 해제하세요.
//wb.UnprotectSharedWorkbook("1234");
//출력 Excel 파일 저장
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## 결론

데이터 보안을 보장하려면 공유 통합 문서를 비밀번호로 보호하거나 보호 해제하는 것이 필수적입니다. .NET용 Aspose.Cells를 사용하면 이 기능을 Excel 파일에 쉽게 추가할 수 있습니다. 이 가이드의 단계를 따르면 암호를 사용하여 공유 통합 문서를 효과적으로 보호하거나 보호 해제할 수 있습니다. 자신의 Excel 파일을 시험해보고 중요한 데이터의 보안을 유지하세요.

### 자주 묻는 질문

#### Q: Aspose.Cells와 공유된 통합 문서에는 어떤 유형의 보호를 적용할 수 있나요?
    
A: Aspose.Cells를 사용하면 데이터의 무단 액세스, 수정 또는 삭제를 방지하기 위해 비밀번호를 지정하여 공유 통합 문서를 보호할 수 있습니다.

#### Q: 암호를 지정하지 않고 공유 통합 문서를 보호할 수 있나요?
    
A: 예, 비밀번호를 지정하지 않고도 공유 통합 문서를 보호할 수 있습니다. 그러나 더 나은 보안을 위해 강력한 비밀번호를 사용하는 것이 좋습니다.

#### Q: Aspose.Cells와 공유된 통합 문서의 보호를 해제하려면 어떻게 해야 합니까?
    
A: 공유 통합 문서의 보호를 해제하려면 통합 문서를 보호할 때 사용한 것과 동일한 비밀번호를 지정해야 합니다. 이를 통해 보호 기능이 제거되고 데이터에 자유롭게 접근할 수 있습니다.

#### Q: 공유 통합 문서를 보호하면 통합 문서의 기능과 수식이 영향을 받나요?
    
A: 공유 통합 문서를 보호하면 사용자는 통합 문서에 있는 기능과 수식에 계속 액세스할 수 있습니다. 보호는 통합 문서의 구조적 변경에만 영향을 미칩니다.