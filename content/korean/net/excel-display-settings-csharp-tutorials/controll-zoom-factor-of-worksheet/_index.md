---
title: 워크시트의 확대/축소 비율 제어
linktitle: 워크시트의 확대/축소 비율 제어
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 워크시트의 확대/축소 비율을 제어합니다.
type: docs
weight: 20
url: /ko/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
워크시트의 확대/축소 비율을 제어하는 것은 .NET용 Aspose.Cells 라이브러리를 사용하여 Excel 파일로 작업할 때 필수적인 기능입니다. 이 가이드에서는 Aspose.Cells를 사용하여 C# 소스 코드를 사용하여 워크시트의 확대/축소 비율을 단계별로 제어하는 방법을 보여줍니다.

## 1단계: 필수 라이브러리 가져오기

시작하기 전에 .NET용 Aspose.Cells 라이브러리를 설치했는지 확인하고 필요한 라이브러리를 C# 프로젝트로 가져오세요.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## 2단계: 디렉터리 경로 설정 및 Excel 파일 열기

 시작하려면 Excel 파일이 포함된 디렉터리에 대한 경로를 설정한 다음`FileStream` 객체를 생성하고 인스턴스화`Workbook` Excel 통합 문서를 나타내는 개체입니다.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 3단계: 스프레드시트에 액세스하여 확대/축소 비율 변경

이 단계에서는 인덱스를 사용하여 Excel 통합 문서의 첫 번째 워크시트에 액세스합니다.`0` 워크시트 확대/축소 비율을 다음으로 설정합니다.`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## 4단계: 변경 사항을 저장하고 파일 닫기

 워크시트 확대/축소 비율을 변경한 후에는 다음을 사용하여 변경 사항을 Excel 파일에 저장합니다.`Save` 의 방법`Workbook` 물체. 그런 다음 파일 스트림을 닫아 사용된 모든 리소스를 해제합니다.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### .NET용 Aspose.Cells를 사용하여 워크시트의 확대/축소 비율 제어에 대한 샘플 소스 코드 

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 열려는 Excel 파일이 포함된 파일 스트림 생성
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// 통합 문서 개체 인스턴스화
// 파일 스트림을 통해 Excel 파일 열기
Workbook workbook = new Workbook(fstream);
// Excel 파일의 첫 번째 워크시트에 액세스
Worksheet worksheet = workbook.Worksheets[0];
// 워크시트의 확대/축소 비율을 75로 설정
worksheet.Zoom = 75;
// 수정된 엑셀 파일 저장
workbook.Save(dataDir + "output.xls");
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```

## 결론

이 단계별 가이드에서는 Aspose.Cells for .NET을 사용하여 워크시트의 확대/축소 비율을 제어하는 방법을 보여주었습니다. 제공된 C# 소스 코드를 사용하면 .NET 애플리케이션에서 워크시트의 확대/축소 비율을 쉽게 조정할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### .NET용 Aspose.Cells란 무엇입니까?

Aspose.Cells for .NET은 .NET 애플리케이션에서 Excel 파일을 조작하기 위한 풍부한 기능의 파일링 라이브러리입니다.

#### .NET용 Aspose.Cells를 어떻게 설치하나요?

 .NET용 Aspose.Cells를 설치하려면 다음에서 해당 NuGet 패키지를 다운로드해야 합니다.[Aspose 릴리스](https://releases/aspose.com/cells/net/) .NET 프로젝트에 추가하세요.

#### .NET용 Aspose.Cells는 어떤 기능을 제공합니까?

Aspose.Cells for .NET은 Excel 파일 생성, 편집, 변환 및 고급 조작과 같은 기능을 제공합니다.

#### .NET용 Aspose.Cells는 어떤 파일 형식을 지원합니까?

.NET용 Aspose.Cells는 XLSX, XLSM, CSV, HTML, PDF 등을 포함한 다양한 파일 형식을 지원합니다.
