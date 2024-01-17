---
title: 이미 서명된 Excel 파일에 디지털 서명 추가
linktitle: 이미 서명된 Excel 파일에 디지털 서명 추가
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 기존 Excel 파일에 디지털 서명을 쉽게 추가할 수 있습니다.
type: docs
weight: 30
url: /ko/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
이 단계별 가이드에서는 Aspose.Cells for .NET을 사용하여 이미 서명된 Excel 파일에 디지털 서명을 추가할 수 있는 제공된 C# 소스 코드를 설명합니다. 기존 Excel 파일에 새 디지털 서명을 추가하려면 아래 단계를 따르세요.

## 1단계: 소스 및 출력 디렉터리 설정

```csharp
// 소스 디렉토리
string sourceDir = RunExamples.Get_SourceDirectory();

// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

이 첫 번째 단계에서는 기존 Excel 파일을 로드하고 새 디지털 서명으로 파일을 저장하는 데 사용할 소스 및 출력 디렉터리를 정의합니다.

## 2단계: 기존 Excel 파일 로드

```csharp
// 이미 서명된 Excel 통합 문서 로드
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 여기서는 이미 서명된 Excel 파일을 로드합니다.`Workbook` Aspose.Cells의 클래스입니다.

## 3단계: 디지털 서명 컬렉션 만들기

```csharp
// 디지털 서명 컬렉션 만들기
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 우리는 다음을 사용하여 새로운 디지털 서명 컬렉션을 만듭니다.`DigitalSignatureCollection` 수업.

## 4단계: 새 인증서 만들기

```csharp
// 새 인증서 만들기
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

여기서는 제공된 파일과 비밀번호로 새 인증서를 만듭니다.

## 5단계: 컬렉션에 새 디지털 서명 추가

```csharp
// 새 디지털 서명 만들기
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// 컬렉션에 디지털 서명 추가
dsCollection.Add(signature);
```

 우리는 다음을 사용하여 새로운 디지털 서명을 만듭니다.`DigitalSignature` 클래스를 만들어 디지털 서명 컬렉션에 추가합니다.

## 6단계: 통합 문서에 디지털 서명 컬렉션 추가

```csharp
//통합 문서에 디지털 서명 모음 추가
workbook.AddDigitalSignature(dsCollection);
```

 다음을 사용하여 기존 Excel 통합 문서에 디지털 서명 모음을 추가합니다.`AddDigitalSignature()` 방법.

## 7단계: 통합 문서 저장 및 닫기

```csharp
// 통합 문서를 저장하고 닫습니다.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

새 디지털 서명이 포함된 통합 문서를 지정된 출력 디렉터리에 저장한 다음 이를 닫고 관련 리소스를 해제합니다.

### .NET용 Aspose.Cells를 사용하여 이미 서명된 Excel 파일에 디지털 서명을 추가하기 위한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
//출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
//인증서 파일 및 비밀번호
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//새 디지털 서명을 추가하려면 이미 디지털 서명된 통합 문서를 로드하세요.
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//디지털 서명 컬렉션 만들기
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//새 인증서 만들기
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//새로운 디지털 서명을 생성하고 디지털 서명 컬렉션에 추가
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//통합 문서 내부에 디지털 서명 수집 추가
workbook.AddDigitalSignature(dsCollection);
//통합 문서를 저장하고 폐기합니다.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## 결론

축하합니다! 이제 Aspose.Cells for .NET을 사용하여 이미 서명된 Excel 파일에 디지털 서명을 추가하는 방법을 배웠습니다. 디지털 서명은 Excel 파일에 추가 보안 계층을 추가하여 신뢰성과 무결성을 보장합니다.

### 자주 묻는 질문

#### Q: .NET용 Aspose.Cells이 무엇인가요?

A: Aspose.Cells for .NET은 .NET 개발자가 Excel 파일을 쉽게 생성, 수정, 변환 및 조작할 수 있게 해주는 강력한 클래스 라이브러리입니다.

#### Q: Excel 파일의 디지털 서명이란 무엇입니까?

A: Excel 파일의 디지털 서명은 문서의 신뢰성, 무결성 및 출처를 보장하는 전자 표시입니다. 파일이 서명된 이후 수정되지 않았으며 신뢰할 수 있는 소스에서 가져온 것인지 확인하는 데 사용됩니다.

#### Q: Excel 파일에 디지털 서명을 추가하면 어떤 이점이 있나요?

A: Excel 파일에 디지털 서명을 추가하면 무단 변경으로부터 보호하고, 데이터 무결성을 보장하고, 문서 작성자를 인증하고, 문서에 포함된 정보에 대한 신뢰성을 제공하는 등 여러 가지 이점을 제공합니다.

#### Q: Excel 파일에 여러 디지털 서명을 추가할 수 있나요?

A: 예, Aspose.Cells를 사용하면 Excel 파일에 여러 디지털 서명을 추가할 수 있습니다. 한 번의 작업으로 디지털 서명 모음을 생성하고 이를 파일에 추가할 수 있습니다.

#### Q: Excel 파일에 디지털 서명을 추가하기 위한 요구 사항은 무엇입니까?

A: Excel 파일에 디지털 서명을 추가하려면 문서 서명에 사용할 유효한 디지털 인증서가 필요합니다. 디지털 서명을 추가하기 전에 올바른 인증서와 비밀번호가 있는지 확인하세요.