---
title: 내장된 Mol 파일 추출
linktitle: 내장된 Mol 파일 추출
second_title: .NET API 참조용 Aspose.Cells
description: Aspose.Cells for .NET을 사용하여 Excel 통합 문서에서 포함된 MOL 파일을 쉽게 추출하는 방법을 알아보세요.
type: docs
weight: 90
url: /ko/net/excel-workbook/extract-embedded-mol-file/
---
이 튜토리얼에서는 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 통합 문서에서 포함된 MOL 파일을 추출하는 방법을 단계별로 안내합니다. 통합 문서 시트를 탐색하고, 해당 OLE 개체를 추출하고, 추출된 MOL 파일을 저장하는 방법을 배우게 됩니다. 이 작업을 성공적으로 완료하려면 아래 단계를 따르세요.

## 1단계: 소스 및 출력 디렉터리 정의
먼저 코드에서 소스 및 출력 디렉터리를 정의해야 합니다. 이러한 디렉터리는 원본 Excel 통합 문서의 위치와 추출된 MOL 파일이 저장될 위치를 나타냅니다. 해당 코드는 다음과 같습니다.

```csharp
// 디렉토리
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

필요에 따라 적절한 경로를 지정하십시오.

## 2단계: Excel 통합 문서 로드
다음 단계는 포함된 OLE 개체와 MOL 파일이 포함된 Excel 통합 문서를 로드하는 것입니다. 통합 문서를 로드하는 코드는 다음과 같습니다.

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

코드에 소스 파일 이름을 올바르게 지정했는지 확인하세요.

## 3단계: 시트를 탐색하고 MOL 파일 추출
이제 통합 문서의 각 시트를 반복하고 MOL 파일이 포함된 해당 OLE 개체를 추출합니다. 해당 코드는 다음과 같습니다.

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

이 코드는 통합 문서의 각 시트를 반복하고 OLE 개체를 가져온 다음 추출된 MOL 파일을 출력 디렉터리에 저장합니다.

### .NET용 Aspose.Cells를 사용하여 임베디드 Mol 파일 추출을 위한 샘플 소스 코드 
```csharp
//디렉토리
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## 결론
축하합니다! Aspose.Cells for .NET을 사용하여 Excel 통합 문서에서 포함된 MOL 파일을 추출하는 방법을 배웠습니다. 이제 이 지식을 적용하여 Excel 통합 문서에서 MOL 파일을 추출할 수 있습니다. Aspose.Cells 라이브러리를 더 자세히 살펴보고 다른 강력한 기능에 대해 알아보세요.

### 자주 묻는 질문

#### Q: MOL 파일이 무엇인가요?
 
A: MOL 파일은 컴퓨터 화학에서 화학 구조를 표현하는 데 사용되는 파일 형식입니다. 여기에는 원자, 결합 및 기타 분자 특성에 대한 정보가 포함되어 있습니다.

#### Q: 이 방법은 모든 Excel 파일 형식에 적용됩니까?

A: 예, 이 방법은 Aspose.Cells가 지원하는 모든 Excel 파일 형식에서 작동합니다.

#### Q: 여러 MOL 파일을 한 번에 추출할 수 있나요?

A: 예, 통합 문서의 각 시트에 있는 OLE 개체를 반복하여 여러 MOL 파일을 한 번에 추출할 수 있습니다.