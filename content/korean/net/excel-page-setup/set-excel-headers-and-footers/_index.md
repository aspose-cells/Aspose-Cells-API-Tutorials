---
title: Excel 머리글 및 바닥글 설정
linktitle: Excel 머리글 및 바닥글 설정
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel에서 머리글과 바닥글을 설정하는 방법을 알아보세요.
type: docs
weight: 100
url: /ko/net/excel-page-setup/set-excel-headers-and-footers/
---

이 튜토리얼에서는 .NET용 Aspose.Cells를 사용하여 Excel에서 머리글과 바닥글을 설정하는 방법을 단계별로 보여 드리겠습니다. 프로세스를 설명하기 위해 C# 소스 코드를 사용하겠습니다.

## 1단계: 환경 설정

컴퓨터에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. 또한 원하는 개발 환경에서 새 프로젝트를 만듭니다.

## 2단계: 필요한 라이브러리 가져오기

코드 파일에서 Aspose.Cells 작업에 필요한 라이브러리를 가져옵니다. 해당 코드는 다음과 같습니다.

```csharp
using Aspose.Cells;
```

## 3단계: 데이터 디렉터리 설정

수정된 엑셀 파일을 저장할 데이터 디렉터리를 설정합니다. 다음 코드를 사용하세요.

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

전체 디렉터리 경로를 지정해야 합니다.

## 4단계: 통합 문서 및 워크시트 만들기

새 Workbook 개체를 만들고 다음 코드를 사용하여 통합 문서의 첫 번째 워크시트로 이동합니다.

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

그러면 워크시트가 포함된 빈 통합 문서가 생성되고 해당 워크시트의 PageSetup 개체에 대한 액세스가 제공됩니다.

## 5단계: 헤더 설정

 다음을 사용하여 스프레드시트 헤더를 설정합니다.`SetHeader` PageSetup 개체의 메서드입니다. 다음은 샘플 코드입니다.

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

그러면 헤더에 워크시트 이름, 현재 날짜 및 시간, 파일 이름이 각각 설정됩니다.

## 6단계: 바닥글 정의

 다음을 사용하여 스프레드시트 바닥글을 설정합니다.`SetFooter` PageSetup 개체의 메서드입니다. 다음은 샘플 코드입니다.

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

그러면 바닥글의 텍스트 문자열, 현재 페이지 번호 및 총 페이지 수가 각각 설정됩니다.

## 7단계: 수정된 통합 문서 저장

다음 코드를 사용하여 수정된 통합 문서를 저장합니다.

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

그러면 수정된 통합 문서가 지정된 데이터 디렉터리에 저장됩니다.

### .NET용 Aspose.Cells를 사용하여 Excel 머리글 및 바닥글 설정에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 통합 문서 개체 인스턴스화
Workbook excel = new Workbook();
// 워크시트의 PageSetup 참조 가져오기
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// 헤더 왼쪽 부분에 워크시트 이름 설정
pageSetup.SetHeader(0, "&A");
//헤더 중앙 부분에 현재 날짜와 현재 시간 설정
// 헤더의 글꼴을 변경하면
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// 헤더 오른쪽 부분에 현재 파일 이름을 설정하고
// 헤더의 글꼴
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// 바닥글 왼쪽 문자열 설정 및 글꼴 변경
// 이 문자열의 일부("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// 바닥글 중앙 부분에 현재 페이지 번호 설정
pageSetup.SetFooter(1, "&P");
// 바닥글 오른쪽 부분에 페이지 수 설정
pageSetup.SetFooter(2, "&N");
// 통합 문서를 저장합니다.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## 결론

이제 .NET용 Aspose.Cells를 사용하여 Excel에서 머리글과 바닥글을 설정하는 방법을 배웠습니다. 이 자습서에서는 환경 설정부터 수정된 통합 문서 저장까지 프로세스의 모든 단계를 안내했습니다. Excel 파일에서 추가 조작을 수행하려면 Aspose.Cells의 기능을 더 자세히 살펴보세요.

### 자주 묻는 질문(FAQ)

#### 1. 내 시스템에 Aspose.Cells for .NET을 어떻게 설치하나요?
.NET용 Aspose.Cells를 설치하려면 Aspose 공식 웹사이트에서 설치 패키지를 다운로드하고 설명서에 제공된 지침을 따라야 합니다.

#### 2. 이 방법은 모든 버전의 Excel에서 작동합니까?
예, Aspose.Cells for .NET을 사용하여 머리글과 바닥글을 설정하는 방법은 지원되는 모든 Excel 버전에서 작동합니다.

#### 3. 머리글과 바닥글을 추가로 맞춤설정할 수 있나요?
예, Aspose.Cells는 텍스트 배치, 색상, 글꼴, 페이지 번호 등을 포함하여 머리글과 바닥글을 사용자 정의할 수 있는 광범위한 기능을 제공합니다.

#### 4. 머리글과 바닥글에 동적 정보를 어떻게 추가하나요?
특수 변수와 서식 지정 코드를 사용하여 현재 날짜, 시간, 파일 이름, 페이지 번호 등과 같은 동적 정보를 머리글과 바닥글에 추가할 수 있습니다.

#### 5. 머리글과 바닥글을 설정한 후 삭제할 수 있나요?
 예, 다음을 사용하여 머리글과 바닥글을 제거할 수 있습니다.`ClearHeaderFooter` 의 방법`PageSetup` 물체. 그러면 기본 머리글과 바닥글이 복원됩니다.