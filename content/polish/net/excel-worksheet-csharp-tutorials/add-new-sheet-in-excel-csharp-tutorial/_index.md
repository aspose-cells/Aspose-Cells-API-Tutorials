---
title: Dodaj nowy arkusz w samouczku Excel C#
linktitle: Dodaj nowy arkusz w programie Excel
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak dodać nowy arkusz w programie Excel za pomocą Aspose.Cells dla .NET. Samouczek krok po kroku z kodem źródłowym w języku C#.
type: docs
weight: 20
url: /pl/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
tym samouczku wyjaśnimy krok po kroku kod źródłowy C#, aby dodać nowy arkusz w Excelu za pomocą Aspose.Cells dla .NET. Dodawanie nowego arkusza do skoroszytu programu Excel jest typową operacją podczas tworzenia raportów lub manipulowania danymi. Aspose.Cells to potężna biblioteka, która ułatwia manipulowanie i generowanie plików Excel przy użyciu platformy .NET. Wykonaj poniższe kroki, aby zrozumieć i zaimplementować ten kod.

## Krok 1: Konfiguracja katalogu dokumentów

Pierwszym krokiem jest zdefiniowanie katalogu dokumentu, w którym zostanie zapisany plik Excel. Jeśli katalog nie istnieje, tworzymy go za pomocą następującego kodu:

```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Utwórz katalog, jeśli jeszcze nie istnieje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

Pamiętaj, aby zastąpić „TWOJ KATALOG DOKUMENTÓW” odpowiednią ścieżką do katalogu dokumentów.

## Krok 2: Tworzenie instancji obiektu skoroszytu

Drugim krokiem jest utworzenie instancji obiektu Workbook, który reprezentuje skoroszyt programu Excel. Użyj następującego kodu:

```csharp
Workbook workbook = new Workbook();
```

Obiekt ten posłuży do dodania nowego arkusza i wykonania innych operacji na skoroszycie programu Excel.

## Krok 3: Dodanie nowego arkusza

Trzecim krokiem jest dodanie nowego arkusza do obiektu Workbook. Użyj następującego kodu:

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

Spowoduje to dodanie nowego arkusza do obiektu Workbook i otrzymasz odniesienie do tego arkusza za pomocą jego indeksu.

## Krok 4: Ustawianie nazwy nowego arkusza

Czwartym krokiem jest nadanie nazwy nowemu arkuszowi. Aby ustawić nazwę arkusza, możesz użyć następującego kodu:

```csharp
worksheet.Name = "My Worksheet";
```

Zastąp „Mój arkusz kalkulacyjny” żądaną nazwą nowego arkusza.

## Krok 5: Zapisywanie pliku Excel

Wreszcie ostatnim krokiem jest zapisanie pliku Excel. Użyj następującego kodu:

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

Spowoduje to zapisanie skoroszytu programu Excel z nowym arkuszem w określonym katalogu dokumentów.

### Przykładowy kod źródłowy dla samouczka Dodaj nowy arkusz w programie Excel C# przy użyciu Aspose.Cells dla .NET 
```csharp
//Ścieżka do katalogu dokumentów.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Utwórz katalog, jeśli jeszcze nie istnieje.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// Tworzenie instancji obiektu skoroszytu
Workbook workbook = new Workbook();
// Dodanie nowego arkusza do obiektu Workbook
int i = workbook.Worksheets.Add();
// Uzyskanie odniesienia do nowo dodanego arkusza poprzez przekazanie jego indeksu arkusza
Worksheet worksheet = workbook.Worksheets[i];
// Ustawianie nazwy nowo dodanego arkusza
worksheet.Name = "My Worksheet";
// Zapisywanie pliku Excel
workbook.Save(dataDir + "output.out.xls");
```

## Wniosek

Nauczyłeś się teraz, jak dodać nowy arkusz w programie Excel przy użyciu Aspose.Cells dla .NET. Za pomocą tej metody można manipulować plikami Excel i generować je przy użyciu języka C#. Aspose.Cells oferuje wiele zaawansowanych funkcji upraszczających obsługę plików Excel w aplikacjach.

### Często zadawane pytania (FAQ)

#### Czy mogę używać Aspose.Cells z innymi językami programowania niż C#?

Tak, Aspose.Cells obsługuje wiele języków programowania, takich jak Java, Python, Ruby i wiele innych.

#### Czy mogę dodać formatowanie do komórek w nowo utworzonym arkuszu?

Tak, możesz zastosować formatowanie do komórek, korzystając z metod udostępnianych przez klasę Worksheet Aspose.Cells. Możesz ustawić styl komórki, zmienić kolor tła, zastosować obramowania itp.

#### Jak uzyskać dostęp do danych komórkowych z nowego arkusza?

Dostęp do danych komórkowych można uzyskać, korzystając z właściwości i metod udostępnianych przez klasę Worksheet Aspose.Cells. Na przykład możesz użyć właściwości Cells, aby uzyskać dostęp do określonej komórki i pobrać lub zmodyfikować jej wartość.

#### Czy Aspose.Cells obsługuje formuły w programie Excel?

Tak, Aspose.Cells obsługuje formuły Excela. Formuły można ustawiać w komórkach arkusza za pomocą metody SetFormula klasy Cell.
