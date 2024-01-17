---
title: XLSB 파일의 외부 연결 읽기 및 쓰기
linktitle: XLSB 파일의 외부 연결 읽기 및 쓰기
second_title: .NET API 참조용 Aspose.Cells
description: .NET용 Aspose.Cells를 사용하여 XLSB 파일의 외부 연결을 읽고 수정하는 방법을 알아보세요.
type: docs
weight: 130
url: /ko/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Excel 통합 문서에서 외부 소스의 데이터를 조작하려면 XLSB 파일에 대한 외부 연결을 읽고 쓰는 것이 필수적입니다. .NET용 Aspose.Cells를 사용하면 다음 단계에 따라 외부 연결을 쉽게 읽고 쓸 수 있습니다.

## 1단계: 소스 디렉터리 및 출력 디렉터리 지정

먼저, 외부 연결이 포함된 XLSB 파일이 있는 소스 디렉터리와 수정된 파일을 저장할 출력 디렉터리를 지정해야 합니다. Aspose.Cells를 사용하여 수행하는 방법은 다음과 같습니다.

```csharp
// 소스 디렉토리
string sourceDir = RunExamples.Get_SourceDirectory();

// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2단계: 원본 Excel XLSB 파일 로드

다음으로 외부 연결 읽기 및 쓰기 작업을 수행하려는 원본 Excel XLSB 파일을 로드해야 합니다. 다음은 샘플 코드입니다.

```csharp
// 원본 Excel XLSB 파일 로드
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## 3단계: 외부 연결 읽기 및 수정

파일을 로드한 후 실제로 데이터베이스 연결인 첫 번째 외부 연결에 액세스할 수 있습니다. 외부 연결의 다양한 속성을 읽고 수정할 수 있습니다. 방법은 다음과 같습니다.

```csharp
// 데이터베이스 연결인 첫 번째 외부 연결을 읽습니다.
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// 데이터베이스 연결 이름, 명령 및 연결 정보를 표시합니다.
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// 연결 이름 수정
dbCon.Name = "NewCustomer";
```

## 4단계: 출력 Excel XLSB 파일 저장

필요한 사항을 변경한 후에는 수정된 Excel XLSB 파일을 지정된 출력 디렉터리에 저장할 수 있습니다. 수행 방법은 다음과 같습니다.

```csharp
// 출력 Excel XLSB 파일을 저장합니다.
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### .NET용 Aspose.Cells를 사용하여 XLSB 파일의 읽기 및 쓰기 외부 연결을 위한 샘플 소스 코드 
```csharp
//소스 디렉터리
string sourceDir = RunExamples.Get_SourceDirectory();
//출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
//원본 Excel Xlsb 파일 로드
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//실제로 DB 연결인 첫 번째 외부 연결을 읽습니다.
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//DB-Connection의 이름, 명령어, 연결정보를 출력합니다.
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//연결 이름 수정
dbCon.Name = "NewCust";
//Excel Xlsb 파일 저장
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## 결론

XLSB 파일에 대한 외부 연결을 읽고 쓰면 Excel 통합 문서에 있는 외부 소스의 데이터를 조작할 수 있습니다. Aspose.Cells for .NET을 사용하면 쉽게 외부 연결에 액세스하고 연결 정보를 읽고 수정하며 변경 사항을 저장할 수 있습니다. 자신만의 XLSB 파일을 시험해보고 Excel 응용프로그램에서 외부 연결의 강력한 기능을 활용해 보세요.

### 자주 묻는 질문

#### Q: XLSB 파일의 외부 연결이란 무엇입니까?
    
A: XLSB 파일의 외부 연결은 데이터베이스와 같은 외부 데이터 소스와 설정된 연결을 의미합니다. 이 외부 소스의 데이터를 Excel 통합 문서로 가져올 수 있습니다.

#### Q: XLSB 파일에 여러 외부 연결을 가질 수 있습니까?
     
A: 예, XLSB 파일에는 여러 외부 연결이 있을 수 있습니다. 각 연결 개체에 액세스하여 개별적으로 관리할 수 있습니다.

#### Q: Aspose.Cells를 사용하여 XLSB 파일에서 외부 연결 세부 정보를 어떻게 읽을 수 있나요?
     
A: Aspose.Cells에서 제공하는 기능을 사용하여 연결 이름, 관련 명령 및 연결 정보와 같은 외부 연결 속성에 액세스할 수 있습니다.

#### Q: Aspose.Cells를 사용하여 XLSB 파일의 외부 연결을 수정할 수 있습니까?
     
A: 예, 특정 요구 사항에 맞게 연결 이름과 같은 외부 연결 속성을 수정할 수 있습니다. Aspose.Cells는 이러한 변경을 수행하는 방법을 제공합니다.

#### Q: Aspose.Cells를 사용하여 외부 연결의 변경 사항을 XLSB 파일에 어떻게 저장할 수 있나요?
     
A: 외부 연결에 필요한 사항을 변경한 후에는 Aspose.Cells에서 제공하는 적절한 방법을 사용하여 수정된 Excel XLSB 파일을 간단히 저장할 수 있습니다.