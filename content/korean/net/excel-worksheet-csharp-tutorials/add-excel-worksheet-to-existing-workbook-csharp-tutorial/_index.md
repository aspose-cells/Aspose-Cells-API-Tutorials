---
title: 기존 통합 문서에 Excel 워크시트 추가 C# 자습서
linktitle: 기존 통합 문서에 Excel 워크시트 추가
second_title: .NET API 참조용 Aspose.Cells
description: Aspose.Cells for .NET을 사용하여 기존 Excel 통합 문서에 새 시트를 쉽게 추가할 수 있습니다. 코드 예제가 포함된 단계별 튜토리얼입니다.
type: docs
weight: 10
url: /ko/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
이 튜토리얼에서는 .NET용 Aspose.Cells를 사용하여 기존 Excel 통합 문서에 새 시트를 추가하는 데 도움이 되는 아래 C# 소스 코드를 단계별로 설명합니다. 프로세스를 자세히 이해하는 데 도움이 되도록 각 단계에 대한 샘플 코드를 포함하겠습니다.

## 1단계: 문서 디렉터리 정의

시작하려면 Excel 파일이 있는 디렉터리 경로를 설정해야 합니다. 코드의 "YOUR DOCUMENT DIRECTORY"를 Excel 파일의 실제 경로로 바꾸십시오.

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## 2단계: 파일 스트림 생성 및 Excel 파일 열기

 다음으로 파일 스트림을 생성하고 다음을 사용하여 Excel 파일을 열어야 합니다.`FileStream` 수업.

```csharp
// 열려는 Excel 파일이 포함된 파일 스트림을 만듭니다.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## 3단계: 통합 문서 개체 인스턴스화

 Excel 파일을 연 후 인스턴스화해야 합니다.`Workbook`물체. 이 개체는 Excel 통합 문서를 나타내며 통합 문서를 조작하기 위한 다양한 메서드와 속성을 제공합니다.

```csharp
// 통합 문서 개체 인스턴스화
// 파일 흐름을 통해 Excel 파일 열기
Workbook workbook = new Workbook(fstream);
```

## 4단계: 통합 문서에 새 시트 추가

 통합 문서에 새 워크시트를 추가하려면`Worksheets.Add()` 의 방법`Workbook` 물체. 이 메서드는 새로 추가된 시트의 인덱스를 반환합니다.

```csharp
// 통합 문서 통합 문서에 새 시트 추가
int i = workbook. Worksheets. Add();
```

## 5단계: 새 시트 이름 설정

 새로 추가된 시트의 이름은 다음을 사용하여 설정할 수 있습니다.`Name` 의 재산`Worksheet` 물체.

```csharp
// 시트 인덱스를 전달하여 추가된 새 시트의 참조를 얻습니다.
Worksheet worksheet = workbook.Worksheets[i];
// 새 시트의 이름을 정의합니다.
worksheet.Name = "My Worksheet";
```

## 6단계: Excel 파일 저장

 새 시트를 추가하고 이름을 설정한 후에는 다음을 사용하여 수정된 Excel 파일을 저장할 수 있습니다.`Save()` 의 방법`Workbook` 물체.

```csharp
// 엑셀 파일을 저장하세요
workbook.Save(dataDir + "output.out.xls");
```

## 7단계: 파일 스트림 닫기 및 리소스 해제

마지막으로 파일 스트림을 닫아 관련된 모든 리소스를 해제하는 것이 중요합니다.

```csharp
// 모든 리소스를 해제하려면 파일 스트림을 닫으세요.
fstream.Close();
```

### 기존 통합 문서에 Excel 워크시트 추가를 위한 샘플 소스 코드 .NET용 Aspose.Cells를 사용하는 C# 자습서 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 열려는 Excel 파일이 포함된 파일 스트림 생성
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// 통합 문서 개체 인스턴스화
// 파일 스트림을 통해 Excel 파일 열기
Workbook workbook = new Workbook(fstream);
// 통합 문서 개체에 새 워크시트 추가
int i = workbook.Worksheets.Add();
// 시트 인덱스를 전달하여 새로 추가된 워크시트의 참조 얻기
Worksheet worksheet = workbook.Worksheets[i];
// 새로 추가된 워크시트 이름 설정
worksheet.Name = "My Worksheet";
// 엑셀 파일 저장
workbook.Save(dataDir + "output.out.xls");
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```

## 결론

이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 기존 Excel 통합 문서에 새로운 Fire Connect를 추가하는 단계별 프로세스를 다루었습니다. 제공된 코드 예제와 설명을 따르면 이제 C# 애플리케이션에서 이 작업을 수행하는 방법을 잘 이해할 수 있을 것입니다. Aspose.Cells for .NET은 Excel 파일 작업을 위한 포괄적인 기능 세트를 제공하므로 다양한 Excel 관련 작업을 효율적으로 자동화할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### .NET용 Aspose.Cells란 무엇입니까?

Aspose.Cells for .NET은 개발자가 애플리케이션에서 Excel 파일을 생성, 조작 및 변환할 수 있는 강력한 .NET 라이브러리입니다. 스프레드시트, 셀, 수식, 스타일 등을 사용하여 작업할 수 있는 다양한 기능을 제공합니다.

#### .NET용 Aspose.Cells를 어떻게 설치하나요?

.NET용 Aspose.Cells를 설치하려면 Aspose 릴리스(https://releases.aspose.com/cells/net) 제공된 설치 지침을 따르세요. 또한 애플리케이션에서 라이브러리를 사용하려면 유효한 라이센스가 필요합니다.

#### .NET용 Aspose.Cells를 사용하여 여러 스프레드시트를 추가할 수 있나요?

 예, Aspose.Cells for .NET을 사용하여 하나의 Excel 파일에 여러 워크시트를 추가할 수 있습니다. 당신은 사용할 수 있습니다`Worksheets.Add()` 의 방법`Workbook` 통합 문서의 다른 위치에 새 워크시트를 추가하려면 개체를 사용하세요.

#### Excel 파일의 셀 서식을 어떻게 지정합니까?

Aspose.Cells for .NET은 Excel 파일의 셀 서식을 지정하는 다양한 방법과 속성을 제공합니다. 셀 값을 설정하고 글꼴 스타일, 색상, 정렬, 테두리 등과 같은 서식 옵션을 적용할 수 있습니다. 셀 서식에 대한 자세한 내용은 Aspose.Cells에서 제공하는 설명서와 샘플 코드를 참조하세요.

#### .NET용 Aspose.Cells는 다른 Excel 버전과 호환됩니까?

예, Aspose.Cells for .NET은 Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019 및 Office 365용 Excel을 포함한 다양한 Excel 버전과 호환됩니다. .xls 형식과 최신 . xlsx 형식입니다.