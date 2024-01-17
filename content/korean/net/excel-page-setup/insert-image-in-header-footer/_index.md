---
title: 머리글 바닥글에 이미지 삽입
linktitle: 머리글 바닥글에 이미지 삽입
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 문서의 머리글이나 바닥글에 이미지를 삽입하는 방법을 알아보세요. C#의 소스 코드를 단계별로 안내합니다.
type: docs
weight: 60
url: /ko/net/excel-page-setup/insert-image-in-header-footer/
---
Excel 문서의 머리글이나 바닥글에 이미지를 삽입하는 기능은 보고서를 사용자 지정하거나 회사 로고를 추가하는 데 매우 유용할 수 있습니다. 이 문서에서는 Aspose.Cells for .NET을 사용하여 Excel 문서의 머리글이나 바닥글에 이미지를 삽입하는 방법을 단계별로 안내합니다. C# 소스 코드를 사용하여 이를 수행하는 방법을 배우게 됩니다.

## 1단계: 환경 설정

시작하기 전에 컴퓨터에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. 또한 원하는 개발 환경에서 새 프로젝트를 만듭니다.

## 2단계: 필요한 라이브러리 가져오기

코드 파일에서 Aspose.Cells 작업에 필요한 라이브러리를 가져옵니다. 해당 코드는 다음과 같습니다.

```csharp
using Aspose.Cells;
```

## 3단계: 문서 디렉터리 설정

작업하려는 Excel 문서가 있는 디렉터리를 설정합니다. 다음 코드를 사용하여 디렉터리를 설정합니다.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

전체 디렉터리 경로를 지정해야 합니다.

## 4단계: 통합 문서 개체 만들기

Workbook 개체는 작업할 Excel 문서를 나타냅니다. 다음 코드를 사용하여 만들 수 있습니다.

```csharp
Workbook workbook = new Workbook();
```

그러면 새로운 빈 통합 문서 개체가 생성됩니다.

## 5단계: 이미지 URL 저장

머리글이나 바닥글에 삽입하려는 이미지의 URL 또는 경로를 정의합니다. 다음 코드를 사용하여 이미지 URL을 저장합니다.

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

지정된 경로가 올바른지, 해당 위치에 이미지가 있는지 확인하세요.

## 6단계: 이미지 파일 열기

이미지 파일을 열기 위해 FileStream 개체를 사용하고 이미지에서 이진 데이터를 읽습니다. 해당 코드는 다음과 같습니다.

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

이미지 경로가 올바른지, 해당 경로에 액세스할 수 있는 올바른 권한이 있는지 확인하세요.

## 7단계: PageSetup 구성

PageSetup 개체는 머리글과 바닥글을 포함한 Excel 문서 페이지 설정을 지정하는 데 사용됩니다. 다음 코드를 사용하여 첫 번째 워크시트의 PageSetup 개체를 가져옵니다.

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

이렇게 하면 통합 문서의 첫 번째 워크시트에 대한 페이지 설정에 액세스할 수 있습니다.

## 8단계: 헤더에 이미지 추가

PageSetup 개체의 SetHeaderPicture() 메서드를 사용하여 페이지 머리글의 중간 부분에 이미지를 설정합니다. 해당 코드는 다음과 같습니다.

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

그러면 지정된 이미지가 페이지 헤더에 추가됩니다.

## 9단계: 헤더에 스크립트 추가

페이지 헤더에 스크립트를 추가하려면 PageSetup 개체의 SetHeader() 메서드를 사용합니다. 해당 코드는 다음과 같습니다.

```csharp
pageSetup.SetHeader(1, "&G");
```

그러면 지정된 스크립트가 페이지 헤더에 추가됩니다. 이 예에서 "&G" 스크립트는 페이지 번호를 표시합니다.

## 10단계: 헤더에 시트 이름 추가

페이지 머리글에 시트 이름을 표시하려면 PageSetup 개체의 SetHeader() 메서드를 다시 사용하십시오. 해당 코드는 다음과 같습니다.

```csharp
pageSetup.SetHeader(2, "&A");
```

페이지 헤더에 시트 이름이 추가됩니다. "&A" 스크립트는 시트 이름을 나타내는 데 사용됩니다.

## 11단계: 통합 문서 저장

통합 문서에 대한 변경 사항을 저장하려면 Workbook 개체의 Save() 메서드를 사용합니다. 해당 코드는 다음과 같습니다.

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

그러면 지정된 디렉터리에 대한 변경 사항이 포함된 통합 문서가 저장됩니다.

## 12단계: FileStream 닫기

이미지에서 이진 데이터를 읽은 후 FileStream을 닫아 리소스를 해제해야 합니다. FileStream을 닫으려면 다음 코드를 사용하십시오.

```csharp
inFile.Close();
```

FileStream 사용을 마친 후에는 항상 FileStream을 닫아야 합니다.

### .NET용 Aspose.Cells를 사용하여 머리글 바닥글에 이미지 삽입을 위한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//통합 문서 개체 만들기
Workbook workbook = new Workbook();
// 로고/그림의 URL을 저장하는 문자열 변수 만들기
string logo_url = dataDir + "aspose-logo.jpg";
// FileStream 객체 선언
FileStream inFile;
// 바이트 배열 선언
byte[] binaryData;
// 스트림에서 로고/그림을 열기 위해 FileStream 개체의 인스턴스 만들기
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// FileStream 객체 크기의 바이트 배열 인스턴스화
binaryData = new Byte[inFile.Length];
// 스트림에서 바이트 블록을 읽고 바이트 배열의 지정된 버퍼에 데이터를 씁니다.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// 통합 문서의 첫 번째 워크시트의 페이지 설정을 가져오기 위한 PageSetup 개체 만들기
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// 페이지 헤더 중앙 섹션에 로고/그림 설정
pageSetup.SetHeaderPicture(1, binaryData);
// 로고/그림에 대한 스크립트 설정
pageSetup.SetHeader(1, "&G");
// 스크립트를 사용하여 페이지 헤더의 오른쪽 섹션에 시트 이름 설정
pageSetup.SetHeader(2, "&A");
// 통합 문서 저장
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//FileStream 객체 닫기
inFile.Close();       
```
## 결론

축하합니다! 이제 Aspose.Cells for .NET을 사용하여 Excel 문서의 머리글이나 바닥글에 이미지를 삽입하는 방법을 알았습니다. 이 자습서에서는 환경 설정부터 수정된 통합 문서 저장까지 프로세스의 모든 단계를 안내했습니다. Aspose.Cells의 기능을 더 많이 실험해 보고 개인화되고 전문적인 Excel 문서를 만들어 보세요.

### FAQ

#### Q1: Excel 문서의 머리글이나 바닥글에 여러 이미지를 삽입할 수 있나요?

A1: 예, 각 추가 이미지에 대해 8단계와 9단계를 반복하여 Excel 문서의 머리글이나 바닥글에 여러 이미지를 삽입할 수 있습니다.

#### Q2: 머리글이나 바닥글에 삽입할 수 있는 이미지 형식은 무엇입니까?
A2: Aspose.Cells는 JPEG, PNG, GIF, BMP 등과 같은 다양한 일반 이미지 형식을 지원합니다.

#### 질문3: 머리글이나 바닥글의 모양을 추가로 사용자 정의할 수 있나요?

A3: 예, 특수 스크립트와 코드를 사용하여 머리글이나 바닥글의 모양을 추가로 형식화하고 사용자 정의할 수 있습니다. 사용자 정의 옵션에 대한 자세한 내용은 Aspose.Cells 설명서를 참조하세요.

#### Q4: Aspose.Cells는 다른 버전의 Excel에서 작동합니까?

A4: 예, Aspose.Cells는 Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 및 Excel 2019를 포함한 다양한 Excel 버전과 호환됩니다.

#### Q5: 셀이나 차트 등 Excel 문서의 다른 부분에 이미지를 삽입할 수 있나요?

A5: 예, Aspose.Cells는 셀, 차트 및 그리기 개체를 포함하여 Excel 문서의 다양한 부분에 이미지를 삽입할 수 있는 광범위한 기능을 제공합니다.