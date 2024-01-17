---
title: 파워 쿼리 수식 항목 업데이트
linktitle: 파워 쿼리 수식 항목 업데이트
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 파일의 파워 쿼리 수식 요소를 업데이트하는 방법을 알아보세요.
type: docs
weight: 160
url: /ko/net/excel-workbook/update-power-query-formula-item/
---
파워 쿼리 수식 항목 업데이트는 Excel 파일의 데이터로 작업할 때 일반적인 작업입니다. .NET용 Aspose.Cells를 사용하면 다음 단계에 따라 파워 쿼리 수식 항목을 쉽게 업데이트할 수 있습니다.

## 1단계: 소스 및 출력 디렉터리 지정

먼저, 업데이트할 파워 쿼리 수식이 포함된 Excel 파일이 있는 원본 디렉터리와 수정된 파일을 저장할 출력 디렉터리를 지정해야 합니다. Aspose.Cells를 사용하여 수행하는 방법은 다음과 같습니다.

```csharp
// 소스 디렉토리
string SourceDir = RunExamples.Get_SourceDirectory();

// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2단계: 원본 Excel 통합 문서 로드

다음으로 파워 쿼리 수식 항목을 업데이트하려는 원본 Excel 통합 문서를 로드해야 합니다. 수행 방법은 다음과 같습니다.

```csharp
// 원본 Excel 통합 문서 로드
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## 3단계: 파워 쿼리 수식 항목 찾아보기 및 업데이트

통합 문서를 로드한 후 파워 쿼리 수식 컬렉션으로 이동하여 각 수식과 해당 요소를 찾아볼 수 있습니다. 이 예에서는 이름이 "Source"인 수식 항목을 찾고 해당 값을 업데이트합니다. 파워 쿼리 수식 항목을 업데이트하는 샘플 코드는 다음과 같습니다.

```csharp
// 파워 쿼리 수식 컬렉션에 액세스
DataMashup mashupData = workbook.DataMashup;

// 파워 쿼리 수식 및 해당 요소를 반복합니다.
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## 4단계: 출력 Excel 통합 문서 저장

파워 쿼리 수식 항목을 업데이트한 후에는 수정된 Excel 통합 문서를 지정된 출력 디렉터리에 저장할 수 있습니다. 수행 방법은 다음과 같습니다.

```csharp
// 출력 Excel 통합 문서 저장
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### .NET용 Aspose.Cells를 사용하여 파워 쿼리 수식 항목 업데이트에 대한 샘플 소스 코드 
```csharp
// 작업 디렉토리
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// 출력 통합 문서를 저장합니다.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## 결론

파워 쿼리 수식 요소를 업데이트하는 것은 Aspose.Cells를 사용하여 Excel 파일의 데이터를 조작하고 처리할 때 필수적인 작업입니다. 위에 제공된 단계를 따르면 수식 요소를 쉽게 업데이트할 수 있습니다.

### 자주 묻는 질문

#### Q: Excel의 파워 쿼리란 무엇입니까?
     
A: 파워 쿼리는 다양한 원본에서 데이터를 수집, 변환 및 로드하는 데 도움이 되는 Excel의 기능입니다. Excel로 가져오기 전에 데이터를 정리, 결합 및 재구성하는 강력한 도구를 제공합니다.

#### Q: 파워 쿼리 수식 항목이 성공적으로 업데이트되었는지 어떻게 알 수 있나요?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Q: 여러 파워 쿼리 수식 항목을 한 번에 업데이트할 수 있나요?
    
A: 예, 특정 요구 사항에 따라 파워 쿼리 수식 항목 컬렉션을 반복하고 단일 루프에서 여러 항목을 업데이트할 수 있습니다.

#### Q: Aspose.Cells를 사용하여 파워 쿼리 수식에 대해 수행할 수 있는 다른 작업이 있습니까?
    
A: 예, Aspose.Cells는 Excel 통합 문서에서 수식 생성, 삭제, 복사 및 검색을 포함하여 파워 쿼리 수식 작업을 위한 모든 기능을 제공합니다.