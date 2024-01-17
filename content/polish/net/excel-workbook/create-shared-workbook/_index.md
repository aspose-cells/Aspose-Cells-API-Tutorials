---
title: Utwórz udostępniony skoroszyt
linktitle: Utwórz udostępniony skoroszyt
second_title: Aspose.Cells dla .NET API odniesienia
description: Utwórz udostępniony skoroszyt programu Excel za pomocą Aspose.Cells dla platformy .NET, aby umożliwić współbieżną współpracę w zakresie danych.
type: docs
weight: 70
url: /pl/net/excel-workbook/create-shared-workbook/
---
tym samouczku przeprowadzimy Cię przez dostarczony kod źródłowy C#, który umożliwi utworzenie udostępnionego skoroszytu przy użyciu Aspose.Cells dla .NET. Aby wykonać tę operację, wykonaj poniższe czynności.

## Krok 1: Ustaw katalog wyjściowy

```csharp
// Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
```

W tym pierwszym kroku definiujemy katalog wyjściowy, w którym zostanie zapisany udostępniony skoroszyt.

## Krok 2: Utwórz obiekt skoroszytu

```csharp
// Utwórz obiekt skoroszytu
Workbook wb = new Workbook();
```

Tworzymy nowy obiekt skoroszytu, który będzie reprezentował nasz skoroszyt programu Excel.

## Krok 3: Włącz udostępnianie skoroszytu

```csharp
// Udostępnij skoroszyt
wb.Settings.Shared = true;
```

 Włączamy funkcję udostępniania skoroszytu, ustawiając opcję`Shared` właściwość obiektu Workbook do`true`.

## Krok 4: Zapisz udostępniony skoroszyt

```csharp
// Zapisz udostępniony skoroszyt
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Zapisujemy udostępniony skoroszyt, podając ścieżkę i nazwę pliku wyjściowego.

### Przykładowy kod źródłowy narzędzia Utwórz skoroszyt udostępniony przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
//Utwórz obiekt skoroszytu
Workbook wb = new Workbook();
//Udostępnij skoroszyt
wb.Settings.Shared = true;
//Zapisz udostępniony skoroszyt
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Wniosek

Gratulacje! Nauczyłeś się, jak utworzyć udostępniony skoroszyt przy użyciu Aspose.Cells dla .NET. Udostępniony skoroszyt może być używany jednocześnie przez wielu użytkowników do współpracy nad danymi. Eksperymentuj z własnymi danymi i dokładniej eksploruj funkcje Aspose.Cells, aby tworzyć wydajne i spersonalizowane skoroszyty programu Excel.

### Często zadawane pytania

#### P: Co to jest skoroszyt udostępniony?

Odp.: Skoroszyt udostępniony to skoroszyt programu Excel, z którego może korzystać jednocześnie wielu użytkowników w celu współpracy nad danymi. Każdy użytkownik może wprowadzać zmiany w skoroszycie, a pozostali użytkownicy będą widzieć aktualizacje w czasie rzeczywistym.

#### P: Jak włączyć udostępnianie skoroszytu w Aspose.Cells dla .NET?

 Odp.: Aby umożliwić udostępnianie skoroszytu w Aspose.Cells dla .NET, musisz ustawić`Shared` właściwość obiektu Workbook do`true`. Umożliwi to użytkownikom jednoczesną pracę nad skoroszytem.

#### P: Czy mogę ograniczyć uprawnienia użytkownika w udostępnionym skoroszycie?

Odp.: Tak, możesz ograniczyć uprawnienia użytkownika w udostępnionym skoroszycie, korzystając z funkcji zabezpieczeń programu Excel. Możesz ustawić określone uprawnienia dla każdego użytkownika, takie jak możliwość edycji, tylko do odczytu itp.

#### P: Jak mogę udostępnić skoroszyt innym użytkownikom?

Odp.: Po utworzeniu udostępnionego skoroszytu możesz udostępnić go innym użytkownikom, wysyłając im plik Excel. Inni użytkownicy będą mogli jednocześnie otworzyć plik i pracować nad nim.

#### P: Czy wszystkie funkcje programu Excel są obsługiwane w udostępnionym skoroszycie?

Odp.: Większość funkcji programu Excel jest obsługiwana w udostępnionym skoroszycie. Jednak niektóre zaawansowane funkcje, takie jak makra i dodatki, mogą mieć ograniczenia lub ograniczenia, jeśli są używane w udostępnionym skoroszycie.