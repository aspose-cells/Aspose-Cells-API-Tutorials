---
title: 선행 아포스트로피 허용
linktitle: 선행 아포스트로피 허용
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 통합 문서에서 선행 아포스트로피를 허용합니다.
type: docs
weight: 60
url: /ko/net/excel-workbook/allow-leading-apostrophe/
---
이 단계별 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 Excel 통합 문서에서 선행 아포스트로피를 사용할 수 있도록 허용하는 제공된 C# 소스 코드를 설명합니다. 이 작업을 수행하려면 아래 단계를 따르십시오.

## 1단계: 소스 및 출력 디렉터리 설정

```csharp
// 소스 디렉토리
string sourceDir = RunExamples.Get_SourceDirectory();
// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

이 첫 번째 단계에서는 Excel 파일의 소스 및 출력 디렉터리를 정의합니다.

## 2단계: WorkbookDesigner 개체 인스턴스화

```csharp
// WorkbookDesigner 개체 인스턴스화
WorkbookDesigner designer = new WorkbookDesigner();
```

 우리는`WorkbookDesigner` Aspose.Cells의 클래스입니다.

## 3단계: Excel 통합 문서 로드

```csharp
// Excel 통합 문서 로드
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

지정된 파일에서 Excel 통합 문서를 로드하고 초기 아포스트로피를 텍스트 스타일로 자동 변환하는 기능을 비활성화합니다.

## 4단계: 데이터 소스 설정

```csharp
// 디자이너 통합 문서의 데이터 원본 정의
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 우리는 데이터 객체의 목록을 정의하고`SetDataSource` 디자이너 통합 문서의 데이터 소스를 설정하는 방법입니다.

## 5단계: 스마트 마커 처리

```csharp
// 스마트 마커 처리
designer. Process();
```

 우리는`Process` 디자이너 워크북에서 스마트 마커를 처리하는 방법입니다.

## 6단계: 수정된 Excel 통합 문서 저장

```csharp
// 수정된 Excel 통합 문서 저장
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

수정된 Excel 통합 문서를 변경 사항과 함께 저장합니다.

### .NET용 Aspose.Cells를 사용하여 선행 아포스트로피 허용에 대한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// WorkbookDesigner 개체 인스턴스화
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// 스마트 마커가 포함된 디자이너 스프레드시트 열기
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// 디자이너 스프레드시트의 데이터 소스 설정
designer.SetDataSource("sampleData", list);
// 스마트 마커 처리
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 Excel 통합 문서에서 선행 아포스트로피 사용을 허용하는 방법을 배웠습니다. Excel 통합 문서를 추가로 사용자 지정하려면 자신의 데이터를 실험해 보세요.

### 자주 묻는 질문

#### Q: Excel 통합 문서에서 선행 아포스트로피 권한이란 무엇입니까?

A: Excel 통합 문서에서 초기 아포스트로피를 허용하면 아포스트로피로 시작하는 데이터를 텍스트 스타일로 변환하지 않고도 올바르게 표시할 수 있습니다. 이는 아포스트로피를 데이터의 일부로 유지하려는 경우에 유용합니다.

#### Q: 초기 아포스트로피 자동 변환을 꺼야 하는 이유는 무엇입니까?

A: 선행 인용문의 자동 변환을 비활성화하면 데이터에서 그대로 사용할 수 있습니다. 이렇게 하면 Excel 통합 문서를 열거나 조작하는 동안 의도하지 않은 데이터 수정을 방지할 수 있습니다.

#### Q: 디자이너 통합 문서에서 데이터 소스를 설정하는 방법은 무엇입니까?

 A: 디자이너 통합 문서에서 데이터 원본을 설정하려면`SetDataSource` 데이터 소스의 이름과 해당 데이터 개체 목록을 지정하는 메서드입니다.

#### Q: 선행 아포스트로피를 허용하면 Excel 통합 문서의 다른 데이터에 영향을 미치나요?

A: 아니요. 선행 아포스트로피를 허용하면 아포스트로피로 시작하는 데이터에만 영향을 미칩니다. Excel 통합 문서의 다른 데이터는 변경되지 않습니다.

#### Q: 이 기능을 다른 Excel 파일 형식과 함께 사용할 수 있나요?

A: 예, .xls, .xlsm 등과 같이 Aspose.Cells가 지원하는 다른 Excel 파일 형식과 함께 이 기능을 사용할 수 있습니다.