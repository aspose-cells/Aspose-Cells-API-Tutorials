---
title: 웹 확장 추가
linktitle: 웹 확장 추가
second_title: .NET API 참조용 Aspose.Cells
description: Aspose.Cells for .NET을 사용하여 Excel 통합 문서에 웹 확장을 쉽게 추가하세요.
type: docs
weight: 40
url: /ko/net/excel-workbook/add-web-extension/
---
이 단계별 튜토리얼에서는 Aspose.Cells for .NET을 사용하여 웹 확장을 추가할 수 있는 제공된 C# 소스 코드를 설명합니다. Excel 통합 문서에 웹 확장을 추가하려면 아래 단계를 따르세요.

## 1단계: 출력 디렉터리 설정

```csharp
// 출력 디렉토리
string outDir = RunExamples.Get_OutputDirectory();
```

이 첫 번째 단계에서는 수정된 Excel 통합 문서가 저장될 출력 디렉터리를 정의합니다.

## 2단계: 새 통합 문서 만들기

```csharp
// 새 통합 문서 만들기
Workbook workbook = new Workbook();
```

여기서는 다음을 사용하여 새로운 Excel 통합 문서를 만듭니다.`Workbook` Aspose.Cells의 클래스입니다.

## 3단계: 웹 확장 컬렉션에 액세스

```csharp
// 웹 확장 컬렉션에 액세스
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 우리는 다음을 사용하여 Excel 통합 문서의 웹 확장 컬렉션에 액세스합니다.`WebExtensions` 의 재산`Worksheets` 물체.

## 4단계: 새 웹 확장 추가

```csharp
// 새 웹 확장 추가
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

확장 컬렉션에 새로운 웹 확장을 추가하고 있습니다. 확장 프로그램의 참조 ID, 매장 이름, 매장 유형을 정의합니다.

## 5단계: 웹 확장 작업창 컬렉션에 액세스

```csharp
// 웹 확장의 작업창 컬렉션에 액세스
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 다음을 사용하여 Excel 통합 문서 웹 확장 작업창 컬렉션에 액세스합니다.`WebExtensionTaskPanes` 의 재산`Worksheets` 물체.

## 6단계: 새 작업창 추가

```csharp
// 새 작업창 추가
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

작업창 컬렉션에 새 작업창을 추가하고 있습니다. 창의 가시성, 도킹 상태 및 관련 웹 확장을 설정합니다.

## 7단계: 통합 문서 저장 및 닫기

```csharp
// 통합 문서 저장 및 닫기
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

수정된 통합 문서를 지정된 출력 디렉터리에 저장한 다음 닫습니다.

### .NET용 Aspose.Cells를 사용하여 웹 확장 추가에 대한 샘플 소스 코드 
```csharp
//소스 디렉터리
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## 결론

축하합니다! 이제 .NET용 Aspose.Cells를 사용하여 웹 확장을 추가하는 방법을 배웠습니다. 코드를 실험하고 Aspose.Cells의 추가 기능을 탐색하여 Excel 통합 문서에서 웹 확장 기능을 최대한 활용하세요.

## 자주 묻는 질문

#### Q: Excel 통합 문서의 웹 확장이란 무엇입니까?

A: Excel 통합 문서의 웹 확장은 웹 응용 프로그램을 통합하여 Excel에 추가 기능을 추가할 수 있는 구성 요소입니다. 대화형 기능, 사용자 정의 대시보드, 외부 통합 등을 제공할 수 있습니다.

#### Q: Aspose.Cells를 사용하여 Excel 통합 문서에 웹 확장을 추가하는 방법은 무엇입니까?

 A: Aspose.Cells를 사용하여 Excel 통합 문서에 웹 확장을 추가하려면 단계별 가이드에 제공된 단계를 따르세요. 사용`WebExtensionCollection` 그리고`WebExtensionTaskPaneCollection` 웹 확장 및 관련 작업창을 추가하고 구성하는 클래스입니다.

#### Q: 웹 확장 프로그램을 추가하려면 어떤 정보가 필요합니까?

A: 웹 확장을 추가할 때 확장 SKU ID, 매장 이름, 매장 유형을 제공해야 합니다. 이 정보는 확장 프로그램을 올바르게 식별하고 로드하는 데 도움이 됩니다.

#### Q: 단일 Excel 통합 문서에 여러 웹 확장을 추가할 수 있나요?

 A: 예, 단일 Excel 통합 문서에 여러 웹 확장을 추가할 수 있습니다. 사용`Add` 웹 확장 컬렉션의 메서드를 사용하여 각 확장을 추가한 다음 이를 해당 작업창과 연결합니다.