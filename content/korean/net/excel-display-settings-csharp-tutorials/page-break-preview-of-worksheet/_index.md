---
title: 워크시트의 페이지 나누기 미리보기
linktitle: 워크시트의 페이지 나누기 미리보기
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 워크시트의 페이지 나누기 미리 보기를 표시하는 단계별 가이드입니다.
type: docs
weight: 110
url: /ko/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 워크시트의 페이지 나누기 미리보기를 표시하는 방법을 설명하겠습니다. 원하는 결과를 얻으려면 다음 단계를 따르십시오.

## 1단계: 환경 설정

.NET용 Aspose.Cells를 설치하고 개발 환경을 설정했는지 확인하세요. 또한 페이지 나누기 미리 보기를 표시하려는 Excel 파일의 복사본이 있는지 확인하세요.

## 2단계: 필요한 종속성 가져오기

Aspose.Cells의 클래스를 사용하는 데 필요한 지시문을 추가합니다.

```csharp
using Aspose.Cells;
using System.IO;
```

## 3단계: 코드 초기화

Excel 문서가 포함된 디렉터리의 경로를 초기화하는 것부터 시작하세요.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 4단계: Excel 파일 열기

 만들기`FileStream` 열려는 Excel 파일이 포함된 개체:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 인스턴스화`Workbook` 개체를 만들고 파일 스트림을 사용하여 Excel 파일을 엽니다.

```csharp
Workbook workbook = new Workbook(fstream);
```

## 5단계: 스프레드시트에 액세스하기

Excel 파일의 첫 번째 워크시트로 이동합니다.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 6단계: 페이지별 미리보기 표시

스프레드시트에 대한 페이지별 미리보기를 활성화합니다.

```csharp
worksheet. IsPageBreakPreview = true;
```

## 7단계: 변경 사항 저장

Excel 파일의 변경 사항을 저장합니다.

```csharp
workbook.Save(dataDir + "output.xls");
```

## 8단계: 파일 스트림 닫기

모든 리소스를 해제하려면 파일 스트림을 닫습니다.

```csharp
fstream.Close();
```

### .NET용 Aspose.Cells를 사용하는 워크시트의 페이지 나누기 미리 보기에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 열려는 Excel 파일이 포함된 파일 스트림 생성
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// 통합 문서 개체 인스턴스화
// 파일 스트림을 통해 Excel 파일 열기
Workbook workbook = new Workbook(fstream);
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
// 페이지 나누기 미리 보기에 워크시트 표시
worksheet.IsPageBreakPreview = true;
// 수정된 엑셀 파일 저장
workbook.Save(dataDir + "output.xls");
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```

## 결론

이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 워크시트의 페이지 나누기 미리 보기를 표시하는 방법을 배웠습니다. 설명된 단계를 따르면 Excel 파일의 모양과 레이아웃을 쉽게 제어할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### .NET용 Aspose.Cells란 무엇입니까?

Aspose.Cells for .NET은 .NET 애플리케이션에서 Excel 파일을 조작하는 데 널리 사용되는 소프트웨어 라이브러리입니다.

#### 전체 워크시트 대신 특정 워크시트에 대한 페이지별 미리 보기를 표시할 수 있나요?

예, Aspose.Cells를 사용하면 해당 Worksheet 개체에 액세스하여 특정 워크시트에 대한 페이지 나누기 미리 보기를 활성화할 수 있습니다.

#### Aspose.Cells는 다른 Excel 파일 편집 기능을 지원합니까?

예, Aspose.Cells는 데이터 추가, 서식 지정, 차트 생성 등과 같이 Excel 파일을 편집하고 조작하기 위한 다양한 기능을 제공합니다.

#### Aspose.Cells는 .xls 형식의 Excel 파일에서만 작동합니까?

아니요, Aspose.Cells는 .xls 및 .xlsx를 포함한 다양한 Excel 파일 형식을 지원합니다.
	