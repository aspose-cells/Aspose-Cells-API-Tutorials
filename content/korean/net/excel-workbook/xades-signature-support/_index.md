---
title: Xades 서명 지원
linktitle: Xades 서명 지원
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 파일에 Xades 서명을 추가하는 방법을 알아보세요.
type: docs
weight: 190
url: /ko/net/excel-workbook/xades-signature-support/
---
이 기사에서는 .NET용 Aspose.Cells 라이브러리를 사용한 Xades 서명 지원에 대한 아래 C# 소스 코드를 단계별로 설명합니다. 이 라이브러리를 사용하여 Xades 디지털 서명을 Excel 파일에 추가하는 방법을 알아봅니다. 또한 서명 프로세스 및 실행에 대한 개요를 제공합니다. 확실한 결과를 얻으려면 아래 단계를 따르십시오.

## 1단계: 소스 및 출력 디렉터리 정의
시작하려면 코드에서 소스 및 출력 디렉터리를 정의해야 합니다. 이러한 디렉터리는 소스 파일이 있는 위치와 출력 파일이 저장될 위치를 나타냅니다. 해당 코드는 다음과 같습니다.

```csharp
// 소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

필요에 따라 디렉토리 경로를 조정하십시오.

## 2단계: Excel 통합 문서 로드
다음 단계는 Xades 디지털 서명을 추가하려는 Excel 통합 문서를 로드하는 것입니다. 통합 문서를 로드하는 코드는 다음과 같습니다.

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

코드에 소스 파일 이름을 올바르게 지정했는지 확인하세요.

## 3단계: 디지털 서명 구성
이제 필요한 정보를 제공하여 Xades 디지털 서명을 구성하겠습니다. 디지털 인증서와 관련 비밀번호가 포함된 PFX 파일을 지정해야 합니다. 해당 코드는 다음과 같습니다.

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

"pfxPassword"를 실제 비밀번호로 바꾸고 "pfxFile"을 PFX 파일 경로로 바꾸십시오.

## 4단계: 디지털 서명 추가
이제 디지털 서명을 구성했으므로 이를 Excel 통합 문서에 추가할 수 있습니다. 해당 코드는 다음과 같습니다.

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

이 단계에서는 Xades 디지털 서명을 Excel 통합 문서에 추가합니다.

## 5단계: 서명이 포함된 통합 문서 저장
마지막으로 디지털 서명이 추가된 Excel 통합 문서를 저장합니다. 해당 코드는 다음과 같습니다.

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

필요에 따라 출력 파일의 이름을 조정하십시오.

### .NET용 Aspose.Cells를 사용하는 Xades 서명 지원을 위한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
//출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## 결론
축하합니다! .NET용 Aspose.Cells 라이브러리를 사용하여 Xades 디지털 서명을 Excel 파일에 추가하는 방법을 배웠습니다. 이 문서에 제공된 단계를 따르면 자신의 프로젝트에서 이 기능을 구현할 수 있습니다. 자유롭게 라이브러리를 더 많이 실험해보고 라이브러리가 제공하는 다른 강력한 기능을 찾아보세요.

### 자주 묻는 질문

#### Q: Xades가 무엇인가요?

A: Xades는 디지털 문서의 무결성과 신뢰성을 보장하는 데 사용되는 고급 전자 서명 표준입니다.

#### Q: Aspose.Cells에 다른 유형의 디지털 서명을 사용할 수 있나요?

A: 예, Aspose.Cells는 XMLDSig 서명 및 PKCS#7 서명과 같은 다른 유형의 디지털 서명도 지원합니다.

#### Q: Excel 파일이 아닌 다른 파일 형식에 서명을 적용할 수 있나요?
 
A: 예, Aspose.Cells에서는 Word, PDF, PowerPoint 파일과 같은 지원되는 다른 파일 형식에도 디지털 서명을 적용할 수 있습니다.