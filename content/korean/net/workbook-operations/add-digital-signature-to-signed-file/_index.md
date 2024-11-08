---
title: 서명된 Excel 파일에 디지털 서명 추가
linktitle: 서명된 Excel 파일에 디지털 서명 추가
second_title: Aspose.Cells .NET Excel 처리 API
description: 이 단계별 가이드에서 Aspose.Cells for .NET을 사용하여 이미 서명된 Excel 파일에 디지털 서명을 추가하는 방법을 알아보세요. 문서를 보호하세요.
type: docs
weight: 12
url: /ko/net/workbook-operations/add-digital-signature-to-signed-file/
---
## 소개
오늘날의 디지털 세계에서 문서의 진위성과 무결성을 보장하는 것은 매우 중요합니다. 디지털 서명은 문서가 변경되지 않았고 합법적인 출처에서 왔는지 확인하는 강력한 수단으로 사용됩니다. .NET에서 Excel 파일을 사용하고 이미 서명된 파일에 디지털 서명을 추가하려는 경우 올바른 위치에 있습니다! 이 가이드에서는 Aspose.Cells for .NET을 사용하여 기존에 서명된 Excel 파일에 새 디지털 서명을 추가하는 과정을 안내합니다. 
## 필수 조건
자세한 내용을 알아보기 전에 시작하는 데 필요한 모든 것이 있는지 확인해 보겠습니다.
1.  .NET용 Aspose.Cells: 무엇보다도 .NET 환경에 Aspose.Cells를 설치해야 합니다. 다음에서 다운로드할 수 있습니다.[릴리스 페이지](https://releases.aspose.com/cells/net/).
2. .NET Framework: 컴퓨터에 .NET Framework가 설치되어 있는지 확인하세요. 이 가이드에서는 기본 .NET 프로그래밍 개념에 익숙하다고 가정합니다.
3. 디지털 인증서: 디지털 서명을 만들려면 유효한 디지털 인증서(.pfx 형식)가 필요합니다. 인증서가 없으면 테스트 목적으로 자체 서명 인증서를 만들 수 있습니다.
4. 개발 환경: C# 코드를 작성하고 실행할 수 있는 Visual Studio와 같은 코드 편집기나 IDE.
5. 샘플 Excel 파일: 이미 디지털 서명된 기존 Excel 파일이 있어야 합니다. 이 파일에 다른 서명을 추가할 것입니다.
이러한 전제 조건을 갖추었으니, 이제 코드로 들어가 보겠습니다!
## 패키지 가져오기
코딩을 시작하기 전에 필요한 네임스페이스를 가져오세요. C# 파일 맨 위에 포함해야 할 내용은 다음과 같습니다.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
이러한 네임스페이스를 사용하면 Excel 파일을 조작하고 디지털 서명을 처리하는 데 필요한 클래스와 메서드에 액세스할 수 있습니다.
이제 프로세스를 관리 가능한 단계로 나누어 보겠습니다. 각 단계를 살펴보고 이미 서명된 Excel 파일에 디지털 서명을 추가하는 방법을 이해하도록 하겠습니다.
## 1단계: 디렉토리 정의
먼저, 소스 파일의 위치와 출력 파일을 저장할 위치를 지정해야 합니다. 간단하지만 중요합니다.
```csharp
// 소스 디렉토리
string sourceDir = "Your Document Directory"; // 실제 디렉토리로 바꾸세요
// 출력 디렉토리
string outputDir = "Your Document Directory"; // 실제 디렉토리로 바꾸세요
```
 바꾸다`"Your Document Directory"` 파일이 저장된 실제 경로와 함께. 이것은 파일 작업의 무대를 설정합니다.
## 2단계: 기존 서명된 통합 문서 로드
다음으로, 이미 서명된 기존 Excel 통합 문서를 로드합니다. 여기서 마법이 시작됩니다.
```csharp
// 새로운 디지털 서명을 추가하려면 이미 디지털 서명된 통합 문서를 로드하세요.
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```
 이 줄은 새로운 것을 초기화합니다`Workbook` 지정된 파일이 있는 개체입니다. 파일 이름이 기존 서명된 Excel 파일과 일치하는지 확인하세요.
## 3단계: 디지털 서명 컬렉션 만들기
디지털 서명을 관리하려면 컬렉션을 만들어야 합니다. 이렇게 하면 필요한 경우 여러 서명을 보관할 수 있습니다.
```csharp
// 디지털 서명 컬렉션 만들기
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```
이 컬렉션은 통합 문서에 적용하기 전에 새로운 디지털 서명을 추가하는 곳입니다.
## 4단계: 인증서 로드
이제 디지털 인증서를 로드할 시간입니다. 이 인증서는 새 서명을 만드는 데 사용됩니다.
```csharp
// 인증서 파일 및 비밀번호
string certFileName = sourceDir + "AsposeDemo.pfx"; // 귀하의 인증서 파일
string password = "aspose"; //귀하의 인증서 비밀번호
// 새로운 인증서 생성
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```
 교체를 꼭 해주세요`AsposeDemo.pfx` 인증서 파일 이름을 입력하고 그에 따라 비밀번호를 업데이트합니다. 이 단계는 올바른 인증서 없이는 유효한 서명을 만들 수 없기 때문에 매우 중요합니다.
## 5단계: 새 디지털 서명 만들기
인증서가 로드되었으므로 이제 새 디지털 서명을 만들 수 있습니다. 이 서명은 컬렉션에 추가됩니다.
```csharp
// 새로운 디지털 서명을 만들어 디지털 서명 컬렉션에 추가하세요
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
```
여기서는 서명을 설명하는 메시지를 제공하는데, 이는 기록 보관에 도움이 될 수 있습니다. 타임스탬프는 서명이 올바른 시점과 연관되어 있는지 확인합니다.
## 6단계: 통합 문서에 서명 컬렉션 추가
서명을 만든 후에는 전체 컬렉션을 통합 문서에 추가할 차례입니다.
```csharp
// 통합 문서 내에 디지털 서명 컬렉션 추가
workbook.AddDigitalSignature(dsCollection);
```
이 단계에서는 통합 문서에 새로운 디지털 서명을 효과적으로 적용하여 신뢰성을 더해줍니다.
## 7단계: 통합 문서 저장
마지막으로, 새로운 디지털 서명이 포함된 통합 문서를 저장합니다. 이제 모든 노고가 보상받는 순간입니다.
```csharp
//통합 문서를 저장하고 폐기하세요.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```
출력 파일의 이름을 지정해야 합니다. 이는 추가 디지털 서명이 포함된 Excel 파일의 새 버전이 됩니다.
## 8단계: 성공 확인
요약하자면, 작업이 성공적으로 완료되면 피드백을 제공하는 것이 좋습니다.
```csharp
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```
이 줄은 콘솔에 확인 메시지를 출력해서 모든 것이 순조롭게 진행되었음을 알려줍니다.
## 결론
이제 다 됐습니다! Aspose.Cells for .NET을 사용하여 이미 서명된 Excel 파일에 새 디지털 서명을 성공적으로 추가했습니다. 이 프로세스는 문서의 보안을 강화할 뿐만 아니라 신뢰할 수 있고 검증 가능한지 확인합니다. 
디지털 서명은 오늘날의 디지털 환경에서 필수적이며, 특히 문서의 무결성을 유지해야 하는 기업과 전문가에게 필수적입니다. 이 가이드를 따르면 Excel 파일에서 디지털 서명을 쉽게 관리하여 데이터가 안전하고 진짜임을 보장할 수 있습니다.
## 자주 묻는 질문
### 디지털 서명이란 무엇인가요?
디지털 서명은 디지털 메시지나 문서의 진위성과 무결성을 검증하기 위한 수학적 체계입니다. 문서가 변경되지 않았는지 확인하고 서명자의 신원을 확인합니다.
### 디지털 서명을 만들려면 특별한 인증서가 필요합니까?
네, 유효한 디지털 서명을 만들려면 신뢰할 수 있는 인증 기관(CA)에서 발급한 디지털 인증서가 필요합니다.
### 테스트에 자체 서명된 인증서를 사용할 수 있나요?
물론입니다! 개발 및 테스트 목적으로 자체 서명 인증서를 만들 수 있지만 프로덕션의 경우 신뢰할 수 있는 CA의 인증서를 사용하는 것이 가장 좋습니다.
### 서명되지 않은 문서에 서명을 추가하려고 하면 어떻게 되나요?
아직 서명되지 않은 문서에 디지털 서명을 추가하려고 하면 문제없이 작동하지만 원래 서명은 존재하지 않습니다.
### Aspose.Cells에 대한 자세한 정보는 어디에서 볼 수 있나요?
 확인할 수 있습니다[Aspose.Cells 설명서](https://reference.aspose.com/cells/net/) 자세한 가이드와 API 참조는 여기에서 확인하세요.