---
title: 워크시트의 스크롤 막대 표시 및 숨기기
linktitle: 워크시트의 스크롤 막대 표시 및 숨기기
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 워크시트에서 스크롤 막대를 표시하거나 숨깁니다.
type: docs
weight: 50
url: /ko/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
이 튜토리얼에서는 Aspose.Cells for .NET과 함께 C# 소스 코드를 사용하여 Excel 워크시트에서 수직 및 수평 스크롤 막대를 표시하거나 숨기는 방법을 보여줍니다. 원하는 결과를 얻으려면 아래 단계를 따르십시오.

## 1단계: 필요한 라이브러리 가져오기

.NET용 Aspose.Cells 라이브러리를 설치했는지 확인하고 필요한 라이브러리를 C# 프로젝트로 가져옵니다.

```csharp
using Aspose.Cells;
using System.IO;
```

## 2단계: 디렉터리 경로 설정 및 Excel 파일 열기

 Excel 파일이 포함된 디렉터리로 경로를 설정한 다음, 파일 스트림을 생성하고 인스턴스화하여 파일을 엽니다.`Workbook` 물체.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 3단계: 스크롤바 숨기기

 사용`IsVScrollBarVisible` 그리고`IsHScrollBarVisible` 의 속성`Workbook.Settings` 워크시트의 세로 및 가로 스크롤 막대를 숨기려면 개체를 사용하세요.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## 4단계: 변경 사항 저장

 필요한 사항을 변경한 후 다음을 사용하여 수정된 Excel 파일을 저장합니다.`Save` 의 방법`Workbook` 물체.

```csharp
workbook.Save(dataDir + "output.xls");
```

### .NET용 Aspose.Cells를 사용하여 워크시트의 스크롤 막대 표시 및 숨기기에 대한 샘플 소스 코드 

```csharp
//문서 디렉터리의 경로입니다.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// 열려는 Excel 파일이 포함된 파일 스트림 생성
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// 통합 문서 개체 인스턴스화
// 파일 스트림을 통해 Excel 파일 열기
Workbook workbook = new Workbook(fstream);
// Excel 파일의 세로 스크롤 막대 숨기기
workbook.Settings.IsVScrollBarVisible = false;
// Excel 파일의 가로 스크롤 막대 숨기기
workbook.Settings.IsHScrollBarVisible = false;
// 수정된 엑셀 파일 저장
workbook.Save(dataDir + "output.xls");
// 모든 리소스를 해제하기 위해 파일 스트림을 닫습니다.
fstream.Close();
```

### 결론

이 단계별 가이드에서는 Aspose.Cells for .NET을 사용하여 Excel 스프레드시트에서 수직 및 수평 스크롤 막대를 표시하거나 숨기는 방법을 보여주었습니다. 제공된 C# 소스 코드를 사용하면 Excel 파일의 스크롤 막대 표시를 쉽게 사용자 지정할 수 있습니다.

### 자주 묻는 질문(FAQ)

#### .NET용 Aspose.Cells란 무엇입니까?

Aspose.Cells for .NET은 .NET 애플리케이션에서 Excel 파일을 조작하기 위한 강력한 라이브러리입니다.

#### .NET용 Aspose.Cells를 어떻게 설치하나요?

 .NET용 Aspose.Cells를 설치하려면 다음에서 관련 패키지를 다운로드해야 합니다.[Aspose 릴리스](https://releases/aspose.com/cells/net/) .NET 프로젝트에 추가하세요.

#### .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 스크롤 막대를 표시하거나 숨기려면 어떻게 해야 합니까?

 당신은 사용할 수 있습니다`IsVScrollBarVisible` 그리고`IsHScrollBarVisible` 의 속성`Workbook.Settings` Excel 워크시트에서 각각 수직 및 수평 스크롤 막대를 표시하거나 숨기려면 개체입니다.

#### .NET용 Aspose.Cells는 어떤 다른 Excel 파일 형식을 지원합니까?

Aspose.Cells for .NET은 XLS, XLSX, CSV, HTML, PDF 등과 같은 다양한 Excel 파일 형식을 지원합니다.