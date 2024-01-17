---
title: 정규식 바꾸기
linktitle: 정규식 바꾸기
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 파일에서 Regex 대체를 수행하는 방법을 알아보세요.
type: docs
weight: 140
url: /ko/net/excel-workbook/regex-replace/
---
정규식(Regex)을 기반으로 한 텍스트 바꾸기는 Excel 파일의 데이터를 조작할 때 흔히 수행되는 작업입니다. .NET용 Aspose.Cells를 사용하면 다음 단계에 따라 Regex 교체를 쉽게 수행할 수 있습니다.

## 1단계: 소스 디렉터리 및 출력 디렉터리 지정

먼저, 교체할 데이터가 포함된 Excel 파일이 있는 원본 디렉터리와 수정된 파일을 저장할 출력 디렉터리를 지정해야 합니다. Aspose.Cells를 사용하여 수행하는 방법은 다음과 같습니다.

```csharp
// 소스 디렉토리
string sourceDir = RunExamples.Get_SourceDirectory();

// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2단계: 원본 Excel 파일 로드

다음으로 Regex 대체를 수행하려는 소스 Excel 파일을 로드해야 합니다. 수행 방법은 다음과 같습니다.

```csharp
// 원본 Excel 파일 로드
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## 3단계: 정규식 대체 수행

파일을 업로드한 후 대소문자 구분 및 정확한 셀 내용 일치를 포함한 대체 옵션을 설정할 수 있습니다. 다음은 Regex 교체를 수행하는 샘플 코드입니다.

```csharp
// 교체 옵션 설정
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// 검색 키가 정규식인지 정의
replace. RegexKey = true;

// 정규식 교체 수행
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## 4단계: 출력 Excel 파일 저장

Regex 교체가 완료되면 수정된 Excel 파일을 지정된 출력 디렉터리에 저장할 수 있습니다. 수행 방법은 다음과 같습니다.

```csharp
// 출력 Excel 파일 저장
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### .NET용 Aspose.Cells를 사용한 Regex 바꾸기의 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
//출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// 검색된 키가 정규식임을 나타내려면 true로 설정하세요.
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## 결론

정규식 대체는 Excel 파일의 데이터를 동적으로 수정하는 강력한 기술입니다. .NET용 Aspose.Cells를 사용하면 위에 설명된 단계에 따라 Regex 교체를 쉽게 수행할 수 있습니다. 자신만의 정규 표현식을 실험하고 Aspose.Cells가 제공하는 유연성을 활용해 보세요.

### 자주 묻는 질문

#### Q: 정규식 대체란 무엇입니까?
    
A: 정규식 대체는 Excel 파일의 정규식을 기반으로 텍스트 패턴을 바꾸는 데 사용되는 기술입니다. 이를 통해 데이터를 빠르고 정확하게 변경할 수 있습니다.

#### Q: 정규 표현식 대체는 대소문자를 구분합니까?
    
A: 아니요. Aspose.Cells를 사용하면 Regex 대체가 대소문자를 구분해야 하는지 여부를 지정할 수 있습니다. 귀하는 이 기능을 완전히 제어할 수 있습니다.

#### Q: Regex를 바꿀 때 셀 내용의 정확한 일치를 지정하려면 어떻게 해야 합니까?
    
A: Aspose.Cells를 사용하면 Regex 대체가 셀 내용과 정확하게 일치해야 하는지 여부를 정의할 수 있습니다. 필요에 따라 이 옵션을 조정할 수 있습니다.

#### Q: Regex를 Aspose.Cells로 바꿀 때 고급 정규식을 사용할 수 있나요?
    
A: 예, Aspose.Cells는 고급 정규식을 지원하므로 Excel 파일에서 복잡하고 정교한 교체를 수행할 수 있습니다.

#### Q: Regex 교체가 성공했는지 어떻게 확인할 수 있나요?
    
A: Regex 교체를 수행한 후 출력을 확인하고 출력 Excel 파일이 올바르게 생성되었는지 확인하여 작업이 성공했는지 확인할 수 있습니다.
	