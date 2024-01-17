---
title: 공유 통합 문서 만들기
linktitle: 공유 통합 문서 만들기
second_title: .NET API 참조용 Aspose.Cells
description: Aspose.Cells for .NET으로 Excel 공유 통합 문서를 만들어 동시 데이터 공동 작업을 활성화하세요.
type: docs
weight: 70
url: /ko/net/excel-workbook/create-shared-workbook/
---
이 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 공유 통합 문서를 생성할 수 있는 제공된 C# 소스 코드를 안내합니다. 이 작업을 수행하려면 아래 단계를 따르십시오.

## 1단계: 출력 디렉터리 설정

```csharp
// 출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
```

이 첫 번째 단계에서는 공유 통합 문서가 저장될 출력 디렉터리를 정의합니다.

## 2단계: 통합 문서 개체 만들기

```csharp
// 통합 문서 개체 만들기
Workbook wb = new Workbook();
```

Excel 통합 문서를 나타내는 새 통합 문서 개체를 만들고 있습니다.

## 3단계: 통합 문서 공유 활성화

```csharp
// 통합 문서 공유
wb.Settings.Shared = true;
```

 다음을 설정하여 통합 문서의 공유 기능을 활성화합니다.`Shared` Workbook 개체의 속성을`true`.

## 4단계: 공유 통합 문서 저장

```csharp
// 공유 통합 문서 저장
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

출력 파일의 경로와 이름을 지정하여 공유 통합 문서를 저장합니다.

### .NET용 Aspose.Cells를 사용하여 공유 통합 문서 만들기에 대한 샘플 소스 코드 
```csharp
//출력 디렉토리
string outputDir = RunExamples.Get_OutputDirectory();
//통합 문서 개체 만들기
Workbook wb = new Workbook();
//통합 문서 공유
wb.Settings.Shared = true;
//공유 통합 문서 저장
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## 결론

축하합니다! .NET용 Aspose.Cells를 사용하여 공유 통합 문서를 만드는 방법을 배웠습니다. 공유 통합 문서는 여러 사용자가 동시에 데이터 공동 작업을 위해 사용할 수 있습니다. 자신의 데이터를 실험하고 Aspose.Cells의 기능을 추가로 탐색하여 강력하고 개인화된 Excel 통합 문서를 만드세요.

### 자주 묻는 질문

#### Q: 공유 통합 문서란 무엇입니까?

A: 공유 통합 문서는 여러 사용자가 동시에 데이터 공동 작업을 위해 사용할 수 있는 Excel 통합 문서입니다. 각 사용자는 통합 문서를 변경할 수 있으며 다른 사용자는 실시간으로 업데이트를 볼 수 있습니다.

#### Q: .NET용 Aspose.Cells에서 통합 문서 공유를 활성화하는 방법은 무엇입니까?

 A: .NET용 Aspose.Cells에서 통합 문서 공유를 활성화하려면`Shared` Workbook 개체의 속성을`true`. 이를 통해 사용자는 통합 문서에서 동시에 작업할 수 있습니다.

#### Q: 공유 통합 문서에서 사용자 권한을 제한할 수 있나요?

A: 예, Excel의 보안 기능을 사용하여 공유 통합 문서에서 사용자 권한을 제한할 수 있습니다. 편집, 읽기 전용 등 각 사용자에 대한 특정 권한을 설정할 수 있습니다.

#### Q: 통합 문서를 다른 사용자와 공유하려면 어떻게 해야 합니까?

A: 공유 통합 문서를 만든 후에는 다른 사용자에게 Excel 파일을 보내 공유할 수 있습니다. 다른 사용자가 파일을 열고 동시에 작업할 수 있습니다.

#### Q: 공유 통합 문서에서는 모든 Excel 기능이 지원됩니까?

A: 대부분의 Excel 기능은 공유 통합 문서에서 지원됩니다. 그러나 매크로 및 추가 기능과 같은 일부 고급 기능은 공유 통합 문서에서 사용할 때 제한 사항이 있을 수 있습니다.