---
title: 워크시트의 기존 프린터 설정 제거
linktitle: 워크시트의 기존 프린터 설정 제거
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 Excel 스프레드시트에서 기존 프린터 설정을 제거하는 방법을 알아보세요.
type: docs
weight: 80
url: /ko/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 Excel 워크시트에서 기존 프린터 설정을 제거하는 방법을 단계별로 안내합니다. 프로세스를 설명하기 위해 C# 소스 코드를 사용하겠습니다.

## 1단계: 환경 설정

컴퓨터에 .NET용 Aspose.Cells가 설치되어 있는지 확인하세요. 또한 원하는 개발 환경에서 새 프로젝트를 만듭니다.

## 2단계: 필요한 라이브러리 가져오기

코드 파일에서 Aspose.Cells 작업에 필요한 라이브러리를 가져옵니다. 해당 코드는 다음과 같습니다.

```csharp
using Aspose.Cells;
```

## 3단계: 소스 및 출력 디렉터리 설정

원본 Excel 파일이 있는 소스 및 출력 디렉터리와 수정된 파일을 저장할 위치를 각각 설정합니다. 다음 코드를 사용하세요.

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

전체 디렉터리 경로를 지정해야 합니다.

## 4단계: 원본 Excel 파일 로드

다음 코드를 사용하여 소스 Excel 파일을 로드합니다.

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

그러면 지정된 Excel 파일이 통합 문서 개체로 로드됩니다.

## 5단계: 워크시트 탐색

루프를 사용하여 통합 문서의 모든 워크시트를 반복합니다. 다음 코드를 사용하세요.

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // 나머지 코드는 다음 단계에서 추가됩니다.
}
```

## 6단계: 기존 프린터 설정 삭제

각 워크시트에 프린터 설정이 있는지 확인하고 필요한 경우 삭제하세요. 다음 코드를 사용하세요.

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## 7단계: 수정된 통합 문서 저장

다음 코드를 사용하여 수정된 통합 문서를 저장합니다.

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

그러면 수정된 통합 문서가 지정된 출력 디렉터리에 저장됩니다.

### .NET용 Aspose.Cells를 사용하여 워크시트의 기존 프린터 설정 제거에 대한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
//출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
//소스 Excel 파일 로드
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//통합 문서의 시트 수를 가져옵니다.
int sheetCount = wb.Worksheets.Count;
//모든 시트 반복
for (int i = 0; i < sheetCount; i++)
{
    //i번째 워크시트에 액세스
    Worksheet ws = wb.Worksheets[i];
    //워크시트 페이지 설정에 액세스
    PageSetup ps = ws.PageSetup;
    //이 워크시트에 대한 프린터 설정이 있는지 확인하세요.
    if (ps.PrinterSettings != null)
    {
        //다음 메시지를 인쇄하세요
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //인쇄 시트 이름 및 용지 크기
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //null로 설정하여 프린터 설정을 제거합니다.
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//만약에
}//~을 위한
//통합 문서 저장
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## 결론

이제 Aspose.Cells for .NET을 사용하여 Excel 워크시트에서 기존 프린터 설정을 제거하는 방법을 배웠습니다. 이 자습서에서는 환경 설정부터 스프레드시트 탐색 및 프린터 설정 지우기에 이르기까지 프로세스의 모든 단계를 안내했습니다. 이제 이 지식을 사용하여 Excel 파일의 프린터 설정을 관리할 수 있습니다.

### FAQ

#### Q1: 스프레드시트에 기존 프린터 설정이 있는지 어떻게 알 수 있나요?

 A1: 다음 페이지에 액세스하여 워크시트에 대한 프린터 설정이 있는지 확인할 수 있습니다.`PrinterSettings` 의 재산`PageSetup` 물체. 값이 null이 아닌 경우 기존 프린터 설정이 있음을 의미합니다.

#### Q2: 특정 스프레드시트에 대해서만 프린터 설정을 삭제할 수 있나요?

 A2: 예, 동일한 접근 방식을 사용하여 해당 워크시트에 액세스하여 특정 워크시트에 대한 프린터 설정을 제거할 수 있습니다.`PageSetup` 물체.

#### Q3: 이 방법을 사용하면 다른 레이아웃 설정도 제거됩니까?

A3: 아니요. 이 방법은 프린터 설정만 삭제합니다. 여백, 용지 방향 등과 같은 기타 레이아웃 설정은 변경되지 않습니다.

#### 질문 4: 이 방법은 .xls 및 .xlsx와 같은 모든 Excel 파일 형식에 적용됩니까?

A4: 예, 이 방법은 .xls 및 .xlsx를 포함하여 Aspose.Cells에서 지원하는 모든 Excel 파일 형식에 작동합니다.

#### Q5: 편집된 Excel 파일에서 프린터 설정에 대한 변경 사항이 영구적으로 적용됩니까?

A5: 예, 프린터 설정 변경 사항은 편집된 Excel 파일에 영구적으로 저장됩니다.