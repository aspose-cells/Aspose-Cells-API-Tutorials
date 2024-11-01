---
title: Aspose.Cells에서 시트 전체에 데이터 자동 채우기
linktitle: Aspose.Cells에서 시트 전체에 데이터 자동 채우기
second_title: Aspose.Cells .NET Excel 처리 API
description: Aspose.Cells for .NET 라이브러리를 사용하여 Excel에서 여러 워크시트에 데이터를 자동으로 채우는 방법을 알아보세요. 데이터 관리 작업을 간소화하는 단계별 프로세스를 알아보세요.
type: docs
weight: 11
url: /ko/net/smart-markers-dynamic-data/auto-populate-data-smart-markers/
---
## 소개
데이터 관리 및 자동화의 세계에서 여러 워크시트에 효율적으로 데이터를 채우는 기능은 중요한 작업입니다. Aspose.Cells for .NET은 이 문제에 대한 강력한 솔루션을 제공하여 데이터 소스에서 Excel 통합 문서 내의 여러 시트로 데이터를 원활하게 전송할 수 있도록 합니다. 이 자습서에서는 Aspose.Cells 라이브러리를 사용하여 시트 간에 데이터를 자동으로 채우는 단계별 프로세스를 안내합니다.
## 필수 조건
튜토리얼을 시작하기에 앞서 다음 필수 조건이 충족되었는지 확인하세요.
1. [마이크로소프트 비주얼 스튜디오](https://visualstudio.microsoft.com/downloads/) - 이것은 .NET용 Aspose.Cells 작업을 위한 기본 개발 환경입니다.
2. [.NET용 Aspose.Cells](https://releases.aspose.com/cells/net/) - Aspose 웹사이트에서 최신 버전의 라이브러리를 다운로드할 수 있습니다.
 시작하려면 다음 중 하나를 사용할 수 있습니다.[무료 체험**](https://releases.aspose.com/) 또는[**purchase a license](https://purchase.aspose.com/buy) .NET용 Aspose.Cells.
## 패키지 가져오기
먼저 C# 프로젝트에서 필요한 패키지를 가져옵니다.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Data;
```
## 1단계: 데이터 테이블 만들기
첫 번째 단계는 워크시트의 데이터 소스로 사용할 데이터 테이블을 만드는 것입니다. 이 예에서는 단일 열 "EmployeeID"가 있는 "Employees"라는 간단한 데이터 테이블을 만듭니다.
```csharp
//출력 디렉토리
string outputDir = "Your Document Directory";
//직원 데이터 테이블 생성
DataTable dt = new DataTable("Employees");
dt.Columns.Add("EmployeeID", typeof(int));
//데이터 테이블 내부에 행 추가
dt.Rows.Add(1230);
dt.Rows.Add(1231);
dt.Rows.Add(1232);
dt.Rows.Add(1233);
dt.Rows.Add(1234);
dt.Rows.Add(1235);
dt.Rows.Add(1236);
dt.Rows.Add(1237);
dt.Rows.Add(1238);
dt.Rows.Add(1239);
dt.Rows.Add(1240);
dt.Rows.Add(1241);
dt.Rows.Add(1242);
dt.Rows.Add(1243);
dt.Rows.Add(1244);
dt.Rows.Add(1245);
dt.Rows.Add(1246);
dt.Rows.Add(1247);
dt.Rows.Add(1248);
dt.Rows.Add(1249);
dt.Rows.Add(1250);
```
## 2단계: 데이터 테이블에서 데이터 리더 만들기
 다음으로, 우리는 다음을 만들 것입니다.`DataTableReader` 방금 만든 데이터 테이블에서. 이렇게 하면 Aspose.Cells 라이브러리의 데이터 소스로 데이터 테이블을 사용할 수 있습니다.
```csharp
//데이터 테이블에서 데이터 리더 생성
DataTableReader dtReader = dt.CreateDataReader();
```
## 3단계: 새 통합 문서 만들기
 이제 다음을 사용하여 새 통합 문서를 만들어 보겠습니다.`Workbook` Aspose.Cells에서 제공하는 클래스:
```csharp
//빈 통합 문서 만들기
Workbook wb = new Workbook();
```
## 4단계: 워크시트에 스마트 마커 추가
이 단계에서는 통합 문서의 첫 번째 및 두 번째 워크시트에 있는 셀에 스마트 마커를 추가합니다. 이러한 스마트 마커는 데이터 테이블의 데이터를 채우는 데 사용됩니다.
```csharp
//첫 번째 워크시트에 액세스하여 셀 A1에 스마트 마커를 추가합니다.
Worksheet ws = wb.Worksheets[0];
ws.Cells["A1"].PutValue("&=Employees.EmployeeID");
//두 번째 워크시트를 추가하고 셀 A1에 스마트 마커를 추가합니다.
wb.Worksheets.Add();
ws = wb.Worksheets[1];
ws.Cells["A1"].PutValue("&=Employees.EmployeeID");
```
## 5단계: 통합 문서 디자이너 만들기
 이제 우리는 다음을 생성할 것입니다.`WorkbookDesigner` 데이터 소스를 설정하고 스마트 마커를 처리하는 데 도움이 되는 개체:
```csharp
//워크북 디자이너 만들기
WorkbookDesigner wd = new WorkbookDesigner(wb);
```
## 6단계: 데이터 소스 설정
 다음으로, 통합 문서 디자이너의 데이터 소스를 설정합니다.`DataTableReader` 이전에 생성한 다음 처리할 행의 수를 지정합니다.
```csharp
//데이터 리더로 데이터 소스 설정
wd.SetDataSource("Employees", dtReader, 15);
```
## 7단계: 스마트 마커 처리
마지막으로, 첫 번째와 두 번째 워크시트의 스마트 마커를 처리합니다.
```csharp
//첫 번째 및 두 번째 워크시트에서 스마트 마커 태그 처리
wd.Process(0, false);
wd.Process(1, false);
```
## 8단계: 통합 문서 저장
마지막 단계는 지정된 출력 디렉토리에 통합 문서를 저장하는 것입니다.
```csharp
//통합 문서 저장
wb.Save(outputDir + "outputAutoPopulateSmartMarkerDataToOtherWorksheets.xlsx");
Console.WriteLine("AutoPopulateSmartMarkerDataToOtherWorksheets executed successfully.");
```
그리고 그게 전부입니다! Aspose.Cells for .NET을 성공적으로 사용하여 Excel 통합 문서의 여러 워크시트에 데이터를 자동으로 채웠습니다.
## 결론
이 튜토리얼에서는 Aspose.Cells for .NET 라이브러리를 사용하여 Excel 통합 문서의 여러 워크시트에 데이터를 자동으로 채우는 방법을 배웠습니다. 스마트 마커와`WorkbookDesigner` 클래스를 사용하면 데이터 소스의 데이터를 통합 문서 내의 다양한 시트로 효율적으로 전송할 수 있습니다.
## 자주 묻는 질문
### Aspose.Cells for .NET을 사용하면 워크시트뿐 아니라 여러 통합 문서에 데이터를 자동으로 채울 수 있나요?
 네, Aspose.Cells를 사용하여 여러 통합 문서에 데이터를 자동으로 채울 수도 있습니다. 이 프로세스는 이 튜토리얼에서 다룬 것과 비슷하지만 여러`Workbook` 하나의 객체 대신에 여러 객체를 사용합니다.
### 자동으로 채워지는 데이터의 모양과 서식을 어떻게 사용자 지정할 수 있나요?
Aspose.Cells는 자동 채우기 데이터에 적용할 수 있는 광범위한 서식 옵션을 제공합니다. 라이브러리에서 사용 가능한 다양한 속성과 메서드를 사용하여 글꼴, 크기, 색상, 테두리 등을 설정할 수 있습니다.
### 데이터를 자동으로 채울 때 대용량 데이터 세트를 효율적으로 처리할 방법이 있나요?
 네, Aspose.Cells는 대용량 데이터 세트를 보다 효율적으로 작업하는 데 도움이 되는 지연 로딩 및 청킹과 같은 기능을 제공합니다. 이러한 옵션은 다음에서 탐색할 수 있습니다.[선적 서류 비치](https://reference.aspose.com/cells/net/).
### Aspose.Cells를 사용하면 데이터 테이블 대신 데이터베이스에서 데이터를 자동으로 채울 수 있나요?
 물론입니다! Aspose.Cells는 데이터베이스를 포함한 다양한 데이터 소스와 함께 작동할 수 있습니다. 다음을 사용할 수 있습니다.`DataTableReader` 또는`DataReader` 데이터베이스에 연결하고 데이터를 자동으로 채우는 클래스입니다.
### 시트 전체에 걸쳐 데이터를 자동으로 채우는 전체 프로세스를 자동화할 방법이 있나요?
네, 이 튜토리얼에서 다룬 단계를 캡슐화하는 재사용 가능한 구성 요소나 메서드를 만들 수 있습니다. 이렇게 하면 자동 채우기 논리를 애플리케이션이나 스크립트에 쉽게 통합하여 매끄럽고 자동화된 프로세스를 만들 수 있습니다.