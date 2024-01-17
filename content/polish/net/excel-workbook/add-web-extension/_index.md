---
title: Dodaj rozszerzenie internetowe
linktitle: Dodaj rozszerzenie internetowe
second_title: Aspose.Cells dla .NET API odniesienia
description: Z łatwością dodawaj rozszerzenia internetowe do skoroszytów programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 40
url: /pl/net/excel-workbook/add-web-extension/
---
W tym samouczku krok po kroku wyjaśnimy dostarczony kod źródłowy C#, który pozwoli Ci dodać rozszerzenie internetowe za pomocą Aspose.Cells dla .NET. Wykonaj poniższe czynności, aby dodać rozszerzenie internetowe do skoroszytu programu Excel.

## Krok 1: Ustaw katalog wyjściowy

```csharp
// Katalog wyjściowy
string outDir = RunExamples.Get_OutputDirectory();
```

W tym pierwszym kroku definiujemy katalog wyjściowy, w którym zostanie zapisany zmodyfikowany skoroszyt Excela.

## Krok 2: Utwórz nowy skoroszyt

```csharp
// Utwórz nowy skoroszyt
Workbook workbook = new Workbook();
```

Tutaj tworzymy nowy skoroszyt programu Excel za pomocą`Workbook` klasa z Aspose.Cells.

## Krok 3: Uzyskaj dostęp do kolekcji rozszerzeń internetowych

```csharp
// Uzyskaj dostęp do kolekcji rozszerzeń internetowych
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Dostęp do kolekcji rozszerzeń internetowych skoroszytu programu Excel uzyskujemy za pomocą`WebExtensions` własność`Worksheets` obiekt.

## Krok 4: Dodaj nowe rozszerzenie internetowe

```csharp
// Dodaj nowe rozszerzenie internetowe
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Do kolekcji rozszerzeń dodajemy nowe rozszerzenie internetowe. Definiujemy identyfikator referencyjny, nazwę sklepu i typ sklepu rozszerzenia.

## Krok 5: Uzyskaj dostęp do kolekcji okienka zadań rozszerzenia sieciowego

```csharp
// Uzyskaj dostęp do kolekcji okienek zadań rozszerzenia internetowego
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Dostęp do kolekcji okienek zadań rozszerzenia internetowego skoroszytu programu Excel uzyskujemy za pomocą`WebExtensionTaskPanes` własność`Worksheets` obiekt.

## Krok 6: Dodaj nowe okienko zadań

```csharp
// Dodaj nowe okienko zadań
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Do kolekcji okienek zadań dodajemy nowe okienko zadań. Ustawiamy widoczność panelu, jego stan dokowania i powiązane z nim rozszerzenie internetowe.

## Krok 7: Zapisz i zamknij skoroszyt

```csharp
// Zapisz i zamknij skoroszyt
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Zapisujemy zmodyfikowany skoroszyt w określonym katalogu wyjściowym, a następnie go zamykamy.

### Przykładowy kod źródłowy dla Dodaj rozszerzenie sieciowe przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
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

## Wniosek

Gratulacje! Nauczyłeś się teraz, jak dodać rozszerzenie internetowe za pomocą Aspose.Cells dla .NET. Eksperymentuj z kodem i odkrywaj dodatkowe funkcje Aspose.Cells, aby w pełni wykorzystać możliwości manipulowania rozszerzeniami internetowymi w skoroszytach programu Excel.

## Często zadawane pytania

#### P: Co to jest rozszerzenie internetowe w skoroszycie programu Excel?

Odp.: Rozszerzenie internetowe w skoroszycie programu Excel to składnik umożliwiający dodanie dodatkowych funkcji do programu Excel poprzez integrację aplikacji internetowych. Może oferować funkcje interaktywne, niestandardowe pulpity nawigacyjne, integracje zewnętrzne i wiele więcej.

#### P: Jak dodać rozszerzenie internetowe do skoroszytu programu Excel za pomocą Aspose.Cells?

 Odp.: Aby dodać rozszerzenie internetowe do skoroszytu programu Excel za pomocą Aspose.Cells, możesz wykonać kroki opisane w naszym przewodniku krok po kroku. Użyj`WebExtensionCollection` I`WebExtensionTaskPaneCollection` klas, aby dodać i skonfigurować rozszerzenie internetowe i powiązane okienko zadań.

#### P: Jakie informacje są wymagane, aby dodać rozszerzenie internetowe?

Odp.: Dodając rozszerzenie internetowe, musisz podać identyfikator SKU rozszerzenia, nazwę sklepu i typ sklepu. Informacje te pomagają prawidłowo zidentyfikować i załadować rozszerzenie.

#### P: Czy mogę dodać wiele rozszerzeń internetowych do jednego skoroszytu programu Excel?

 Odp.: Tak, możesz dodać wiele rozszerzeń internetowych do jednego skoroszytu programu Excel. Użyj`Add` metodę kolekcji rozszerzeń internetowych, aby dodać każde rozszerzenie, a następnie powiązać je z odpowiednimi okienkami zadań.