---
title: 통합 문서를 로드하는 동안 정의된 이름 필터링
linktitle: 통합 문서를 로드하는 동안 정의된 이름 필터링
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 통합 문서를 로드할 때 정의된 이름을 필터링하는 방법을 알아보세요.
type: docs
weight: 100
url: /ko/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
.NET 애플리케이션에서 Excel 통합 문서로 작업할 때 로드 시 데이터를 필터링해야 하는 경우가 많습니다. Aspose.Cells for .NET은 Excel 통합 문서를 쉽게 조작할 수 있는 강력한 라이브러리입니다. 이 가이드에서는 .NET용 Aspose.Cells를 사용하여 통합 문서를 로드할 때 정의된 이름을 필터링하는 방법을 보여줍니다. 원하는 결과를 얻으려면 다음의 간단한 단계를 따르십시오.

## 1단계: 로드 옵션 지정

먼저 통합 문서의 로드 동작을 정의하기 위한 로드 옵션을 지정해야 합니다. 우리의 경우 로드 시 설정된 이름을 무시하려고 합니다. Aspose.Cells를 사용하여 수행하는 방법은 다음과 같습니다.

```csharp
// 로딩 옵션을 지정합니다
LoadOptions opts = new LoadOptions();

// 정의된 이름을 로드하지 마세요
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## 2단계: 통합 문서 로드

로드 옵션이 구성되면 원본 파일에서 Excel 통합 문서를 로드할 수 있습니다. 올바른 파일 경로를 지정하십시오. 다음은 샘플 코드입니다.

```csharp
// 통합 문서 로드
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## 3단계: 필터링된 통합 문서 저장

통합 문서를 로드한 후 필요에 따라 다른 작업이나 편집을 수행할 수 있습니다. 그런 다음 필터링된 통합 문서를 출력 파일에 저장할 수 있습니다. 방법은 다음과 같습니다.

```csharp
// 필터링된 Excel 통합 문서 저장
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### .NET용 Aspose.Cells를 사용하여 통합 문서를 로드하는 동안 정의된 이름 필터에 대한 샘플 소스 코드 
```csharp
//로드 옵션 지정
LoadOptions opts = new LoadOptions();
//정의된 이름을 로드하고 싶지 않습니다.
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//통합 문서 로드
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//출력 Excel 파일을 저장하면 C1의 수식이 깨집니다.
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## 결론

Excel 통합 문서를 로드할 때 정의된 이름을 필터링하는 것은 많은 응용 프로그램에서 매우 중요할 수 있습니다. .NET용 Aspose.Cells는 데이터 로드 및 필터링을 위한 유연한 옵션을 제공하여 이 작업을 더 쉽게 만듭니다. 이 가이드의 단계를 따르면 정의된 이름을 효과적으로 필터링하고 Excel 통합 문서에서 원하는 결과를 얻을 수 있습니다.


### 자주 묻는 질문

#### Q: Aspose.Cells는 C# 외에 다른 프로그래밍 언어를 지원합니까?
    
A: 예, Aspose.Cells는 Java, Python, C와 같은 다양한 프로그래밍 언어를 지원하는 크로스 플랫폼 라이브러리입니다.++그리고 더 많은.

#### Q: Aspose.Cells를 사용하여 통합 문서를 로드할 때 다른 데이터 유형을 필터링할 수 있나요?
    
A: 예, Aspose.Cells는 수식, 스타일, 매크로 등을 포함한 데이터에 대한 다양한 필터링 옵션을 제공합니다.

#### Q: Aspose.Cells는 원본 통합 문서의 형식과 속성을 유지합니까?
    
A: 예, Aspose.Cells는 Excel 파일로 작업할 때 원본 통합 문서의 서식, 스타일, 수식 및 기타 속성을 유지합니다.