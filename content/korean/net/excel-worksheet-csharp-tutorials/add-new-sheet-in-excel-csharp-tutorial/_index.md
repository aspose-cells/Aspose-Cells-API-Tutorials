---
title: Excel C# 자습서에 새 시트 추가
linktitle: Excel에 새 시트 추가
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel에 새 시트를 추가하는 방법을 알아보세요. C#의 소스 코드가 포함된 단계별 튜토리얼입니다.
type: docs
weight: 20
url: /ko/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 Excel에 새 시트를 추가하는 C# 소스 코드를 단계별로 설명합니다. Excel 통합 문서에 새 워크시트를 추가하는 것은 보고서를 생성하거나 데이터를 조작할 때 일반적인 작업입니다. Aspose.Cells는 .NET을 사용하여 Excel 파일을 쉽게 조작하고 생성할 수 있게 해주는 강력한 라이브러리입니다. 이 코드를 이해하고 구현하려면 아래 단계를 따르세요.

## 1단계: 문서 디렉터리 설정

첫 번째 단계는 Excel 파일이 저장될 문서 디렉터리를 정의하는 것입니다. 디렉터리가 존재하지 않으면 다음 코드를 사용하여 디렉터리를 만듭니다.

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// 디렉터리가 아직 없으면 만듭니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

"YOUR DOCUMENTS DIRECTORY"를 문서 디렉토리에 대한 적절한 경로로 바꾸십시오.

## 2단계: 통합 문서 개체 인스턴스화

두 번째 단계는 Excel 통합 문서를 나타내는 Workbook 개체를 인스턴스화하는 것입니다. 다음 코드를 사용하세요.

```csharp
Workbook workbook = new Workbook();
```

이 개체는 새 워크시트를 추가하고 Excel 통합 문서에서 다른 작업을 수행하는 데 사용됩니다.

## 3단계: 새 워크시트 추가

세 번째 단계는 통합 문서 개체에 새 워크시트를 추가하는 것입니다. 다음 코드를 사용하세요.

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

그러면 통합 문서 개체에 새 워크시트가 추가되고 해당 색인을 사용하여 이 워크시트에 대한 참조를 얻게 됩니다.

## 4단계: 새 워크시트 이름 설정

네 번째 단계는 새 워크시트에 이름을 지정하는 것입니다. 다음 코드를 사용하여 워크시트 이름을 설정할 수 있습니다.

```csharp
worksheet.Name = "My Worksheet";
```

"내 스프레드시트"를 원하는 새 시트 이름으로 바꾸세요.

## 5단계: Excel 파일 저장

마지막 단계는 Excel 파일을 저장하는 것입니다. 다음 코드를 사용하세요.

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

그러면 새 워크시트가 포함된 Excel 통합 문서가 지정한 문서 디렉터리에 저장됩니다.

### .NET용 Aspose.Cells를 사용하는 Excel C# 자습서의 새 시트 추가에 대한 샘플 소스 코드 
```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 디렉터리가 아직 없으면 만듭니다.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook();
// 통합 문서 개체에 새 워크시트 추가
int i = workbook.Worksheets.Add();
// 시트 인덱스를 전달하여 새로 추가된 워크시트의 참조 얻기
Worksheet worksheet = workbook.Worksheets[i];
// 새로 추가된 워크시트 이름 설정
worksheet.Name = "My Worksheet";
// 엑셀 파일 저장
workbook.Save(dataDir + "output.out.xls");
```

## 결론

이제 Aspose.Cells for .NET을 사용하여 Excel에 새 워크시트를 추가하는 방법을 배웠습니다. 이 방법을 사용하면 C#을 사용하여 Excel 파일을 조작하고 생성할 수 있습니다. Aspose.Cells는 애플리케이션에서 Excel 파일 처리를 단순화하는 많은 강력한 기능을 제공합니다.

### 자주 묻는 질문(FAQ)

#### C#이 아닌 다른 프로그래밍 언어로 Aspose.Cells를 사용할 수 있나요?

예, Aspose.Cells는 Java, Python, Ruby 등과 같은 여러 프로그래밍 언어를 지원합니다.

#### 새로 생성된 워크시트의 셀에 서식을 추가할 수 있나요?

예, Aspose.Cells의 Worksheet 클래스에서 제공하는 메서드를 사용하여 셀에 서식을 적용할 수 있습니다. 셀 스타일 설정, 배경색 변경, 테두리 적용 등을 할 수 있습니다.

#### 새 워크시트에서 셀 데이터에 어떻게 액세스할 수 있나요?

Aspose.Cells의 Worksheet 클래스에서 제공하는 속성과 메서드를 사용하여 셀 데이터에 액세스할 수 있습니다. 예를 들어 Cells 속성을 사용하여 특정 셀에 액세스하고 해당 값을 검색하거나 수정할 수 있습니다.

#### Aspose.Cells는 Excel에서 수식을 지원합니까?

예, Aspose.Cells는 Excel 수식을 지원합니다. Cell 클래스의 SetFormula 메서드를 사용하여 워크시트 셀에 수식을 설정할 수 있습니다.
