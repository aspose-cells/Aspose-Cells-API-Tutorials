---
title: 압축 수준 조정
linktitle: 압축 수준 조정
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells로 압축 수준을 조정하여 Excel 통합 문서의 크기를 줄이세요.
type: docs
weight: 50
url: /ko/net/excel-workbook/adjust-compression-level/
---
이 단계별 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 압축 수준을 조정할 수 있는 제공된 C# 소스 코드를 설명합니다. Excel 통합 문서의 압축 수준을 조정하려면 아래 단계를 따르세요.

## 1단계: 소스 및 출력 디렉터리 설정

```csharp
// 소스 디렉토리
string sourceDir = RunExamples.Get_SourceDirectory();
// 출력 디렉토리
string outDir = RunExamples.Get_OutputDirectory();
```

이 첫 번째 단계에서는 Excel 파일의 소스 및 출력 디렉터리를 정의합니다.

## 2단계: Excel 통합 문서 로드

```csharp
// Excel 통합 문서 로드
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

다음을 사용하여 지정된 파일에서 Excel 통합 문서를 로드합니다.`Workbook` Aspose.Cells의 클래스입니다.

## 3단계: 백업 옵션 설정

```csharp
// 백업 옵션 정의
XlsbSaveOptions options = new XlsbSaveOptions();
```

 우리는`XlsbSaveOptions` 저장 옵션을 설정하는 클래스입니다.

## 4단계: 압축 수준 조정(수준 1)

```csharp
// 압축 수준 조정(레벨 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 설정하여 압축 수준을 조정합니다.`CompressionType` 에게`Level1`. 그런 다음 이 압축 옵션을 지정하여 Excel 통합 문서를 저장합니다.

## 5단계: 압축 수준 조정(수준 6)

```csharp
// 압축 수준 조정(레벨 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 압축 수준을 조정하는 과정을 반복합니다.`Level6` 이 옵션을 사용하여 Excel 통합 문서를 저장하십시오.

## 6단계: 압축 수준 조정(수준 9)

```csharp
// 압축 수준 조정(레벨 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 마지막으로 프로세스를 반복하여 압축 수준을 다음으로 조정합니다.`Level9` 이 옵션을 사용하여 Excel 통합 문서를 저장하십시오.

### .NET용 Aspose.Cells를 사용하여 압축 수준 조정에 대한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 Excel 통합 문서에서 압축 수준을 조정하는 방법을 배웠습니다. 다양한 수준의 압축을 실험하여 요구 사항에 가장 적합한 압축 수준을 찾으십시오.

### 자주 묻는 질문

#### Q: Excel 통합 문서의 압축이란 무엇입니까?

A: Excel 통합 문서의 압축은 압축 알고리즘을 사용하여 파일 크기를 줄이는 프로세스입니다. 이렇게 하면 필요한 저장 공간이 줄어들고 파일을 로드하고 조작할 때 성능이 향상됩니다.

#### Q: Aspose.Cells에서는 어떤 수준의 압축을 사용할 수 있나요?

A: Aspose.Cells를 사용하면 압축 수준을 1에서 9까지 조정할 수 있습니다. 압축 수준이 높을수록 파일 크기는 작아지지만 처리 시간도 늘어날 수 있습니다.

#### Q: Excel 통합 문서에 적합한 압축 수준을 어떻게 선택합니까?

A: 압축 수준 선택은 특정 요구 사항에 따라 다릅니다. 최대 압축을 원하고 처리 시간이 문제가 되지 않는다면 레벨 9로 갈 수 있습니다. 파일 크기와 처리 시간 사이의 절충안을 선호한다면 중간 레벨을 선택할 수 있습니다.

#### Q: 압축이 Excel 통합 문서의 데이터 품질에 영향을 미치나요?

A: 아니요. 압축은 Excel 통합 문서의 데이터 품질에 영향을 미치지 않습니다. 데이터 자체를 변경하지 않고 압축 기술을 사용하여 파일 크기를 줄입니다.

#### Q: 엑셀 파일을 저장한 후 압축 수준을 조정할 수 있나요?

A: 아니요. 특정 압축 수준으로 Excel 파일을 저장하면 나중에 압축 수준을 조정할 수 없습니다. 파일을 수정하려면 새 압축 수준으로 파일을 다시 저장해야 합니다.