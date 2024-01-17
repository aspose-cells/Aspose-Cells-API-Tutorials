---
title: 워크시트 숨기기 및 숨기기 취소
linktitle: 워크시트 숨기기 및 숨기기 취소
second_title: .NET API 참조용 Aspose.Cells
description: 데이터 생성, 수정, 조작을 포함하여 Excel 파일 작업을 위한 강력한 라이브러리입니다.
type: docs
weight: 90
url: /ko/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 워크시트를 숨기고 표시하는 데 사용되는 다음 C# 소스 코드를 단계별로 설명합니다. 아래 단계를 따르십시오.

## 1단계: 환경 준비

시작하기 전에 시스템에 Aspose.Cells for .NET이 설치되어 있는지 확인하세요. 아직 설치하지 않았다면 Aspose 공식 웹사이트에서 다운로드할 수 있습니다. 설치가 완료되면 원하는 통합 개발 환경(IDE)에서 새 프로젝트를 생성할 수 있습니다.

## 2단계: 필수 네임스페이스 가져오기

C# 소스 파일에서 Aspose.Cells의 기능을 사용하는 데 필요한 네임스페이스를 추가합니다. 파일 시작 부분에 다음 줄을 추가합니다.

```csharp
using Aspose.Cells;
using System.IO;
```

## 3단계: Excel 파일 로드

워크시트를 숨기거나 숨김을 해제하기 전에 Excel 파일을 응용 프로그램에 로드해야 합니다. 프로젝트와 동일한 디렉터리에 사용하려는 Excel 파일이 있는지 확인하세요. 다음 코드를 사용하여 Excel 파일을 로드합니다.

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

"문서 디렉토리 경로"를 Excel 파일이 포함된 디렉토리의 실제 경로로 바꾸십시오.

## 4단계: 스프레드시트에 액세스

Excel 파일이 로드되면 숨기거나 숨기기를 취소하려는 워크시트로 이동할 수 있습니다. 다음 코드를 사용하여 파일의 첫 번째 워크시트에 액세스합니다.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 5단계: 워크시트 숨기기

 이제 워크시트에 액세스했으므로 다음을 사용하여 워크시트를 숨길 수 있습니다.`IsVisible` 재산. 파일의 첫 번째 워크시트를 숨기려면 다음 코드를 사용합니다.

```csharp
worksheet. IsVisible = false;
```

## 6단계: 워크시트 다시 표시

이전에 숨겨진 워크시트를 다시 표시하려면`IsVisible` 재산. 첫 번째 워크시트를 다시 표시하려면 다음 코드를 사용합니다.

```csharp
worksheet. IsVisible = true;
```

## 7단계: 변경 사항 저장

일단 당신은

  필요에 따라 워크시트를 숨기거나 숨김을 해제한 경우 변경 사항을 Excel 파일에 저장해야 합니다. 변경 사항을 저장하려면 다음 코드를 사용하십시오.

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

수정된 Excel 파일을 저장하려면 올바른 출력 경로를 지정해야 합니다.

### .NET용 Aspose.Cells를 사용하여 워크시트 숨기기 및 숨기기 해제에 대한 샘플 소스 코드 

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 열려는 Excel 파일이 포함된 파일 스트림 생성
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// 파일 스트림을 통해 Excel 파일을 열어 통합 문서 개체 인스턴스화
Workbook workbook = new Workbook(fstream);
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
// Excel 파일의 첫 번째 워크시트 숨기기
worksheet.IsVisible = false;
// Excel 파일의 첫 번째 워크시트를 표시합니다.
//Worksheet.IsVisible = true;
// 수정된 Excel 파일을 기본(Excel 2003) 형식으로 저장
workbook.Save(dataDir + "output.out.xls");
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 스프레드시트를 숨기고 표시하는 방법을 배웠습니다. 이제 이 기능을 사용하여 Excel 파일에서 스프레드시트의 가시성을 제어할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### .NET용 Aspose.Cells를 어떻게 설치하나요?

 다음에서 관련 NuGet 패키지를 다운로드하여 .NET용 Aspose.Cells를 설치할 수 있습니다.[Aspose 릴리스](https://releases/aspose.com/cells/net/) Visual Studio 프로젝트에 추가합니다.

#### .NET용 Aspose.Cells를 사용하는 데 필요한 최소 .NET Framework 버전은 무엇입니까?

.NET용 Aspose.Cells는 .NET Framework 2.0 이상을 지원합니다.

#### .NET용 Aspose.Cells를 사용하여 기존 Excel 파일을 열고 편집할 수 있나요?

예, Aspose.Cells for .NET을 사용하여 기존 Excel 파일을 열고 편집할 수 있습니다. Excel 파일의 워크시트, 셀, 수식 및 기타 요소에 액세스할 수 있습니다.

#### .NET용 Aspose.Cells는 보고 및 다른 파일 형식으로 내보내기를 지원합니까?

예, .NET용 Aspose.Cells는 보고서 생성을 지원하고 PDF, HTML, CSV, TXT 등과 같은 형식으로 내보내기를 지원합니다.

#### Excel 파일 수정은 영구적인가요?

예, Excel 파일 편집은 일단 저장하면 영구적입니다. 원본 파일을 변경하기 전에 백업 복사본을 저장하십시오.