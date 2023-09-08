---
title: Защитите определенные ячейки на листе Excel
linktitle: Защитите определенные ячейки на листе Excel
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как защитить определенные ячейки в Excel с помощью Aspose.Cells для .NET. Пошаговое руководство по C#.
type: docs
weight: 70
url: /ru/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
В этом уроке мы рассмотрим исходный код C#, который использует библиотеку Aspose.Cells для защиты определенных ячеек в электронной таблице Excel. Мы рассмотрим каждый шаг кода и объясним, как он работает. Внимательно следуйте инструкциям, чтобы получить желаемые результаты.

## Шаг 1: Предварительные условия

Прежде чем начать, убедитесь, что у вас установлена библиотека Aspose.Cells для .NET. Вы можете получить его на официальном сайте Aspose. Также убедитесь, что у вас установлена последняя версия Visual Studio или любой другой среды разработки C#.

## Шаг 2. Импортируйте необходимые пространства имен.

Чтобы использовать библиотеку Aspose.Cells, нам необходимо импортировать необходимые пространства имен в наш код. Добавьте следующие строки в начало исходного файла C#:

```csharp
using Aspose.Cells;
```

## Шаг 3. Создание книги Excel

На этом этапе мы создадим новую книгу Excel. Используйте следующий код для создания книги Excel:

```csharp
// Путь к каталогу документов.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Создайте новую книгу.
Workbook wb = new Workbook();
```

 Обязательно замените`"YOUR_DOCUMENTS_DIR"` с соответствующим путем к каталогу ваших документов.

## Шаг 4. Создание электронной таблицы

Теперь, когда мы создали книгу Excel, давайте создадим рабочий лист и получим первый лист. Используйте следующий код:

```csharp
// Создайте объект электронной таблицы и получите первый лист.
Worksheet sheet = wb.Worksheets[0];
```

## Шаг 5: Определение стиля

На этом этапе мы определим стиль, который будет применяться к конкретным ячейкам. Используйте следующий код:

```csharp
// Определение объекта стиля.
Styling styling;
```

## Шаг 6. Повторите цикл, чтобы разблокировать все столбцы.

Теперь мы пройдемся по всем столбцам на листе и разблокируем их. Используйте следующий код:

```csharp
// Просмотрите все столбцы на листе и разблокируйте их.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Шаг 7. Блокировка определенных ячеек

На этом этапе мы заблокируем определенные ячейки. Используйте следующий код:

```csharp
//Блокировка всех трех ячеек... т.е. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Шаг 8. Защита листа

Наконец, мы защитим рабочий лист, чтобы предотвратить изменение определенных ячеек. Используйте следующий код:

```csharp
// Защитите рабочий лист.
sheet.Protect(ProtectionType.All);
```

## Шаг 9: Сохранение файла Excel

Теперь мы сохраним измененный файл Excel. Используйте следующий код:

```csharp
// Сохраните файл Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Обязательно укажите правильный путь для сохранения измененного файла Excel.

### Пример исходного кода для защиты определенных ячеек на листе Excel с использованием Aspose.Cells для .NET 
```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создайте каталог, если он еще не существует.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Создайте новую книгу.
Workbook wb = new Workbook();
// Создайте объект рабочего листа и получите первый лист.
Worksheet sheet = wb.Worksheets[0];
// Определите объект стиля.
Style style;
// Определите объект styleflag
StyleFlag styleflag;
// Просмотрите все столбцы на листе и разблокируйте их.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Заблокируйте три ячейки... т.е. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Наконец, защитите лист сейчас.
sheet.Protect(ProtectionType.All);
// Сохраните файл Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Заключение

Поздравляем! Теперь у вас есть исходный код C#, который позволяет защитить определенные ячейки на листе Excel с помощью библиотеки Aspose.Cells для .NET. Не стесняйтесь настраивать код в соответствии с вашими конкретными потребностями.

### Часто задаваемые вопросы (часто задаваемые вопросы)

#### Работает ли этот код с последними версиями Excel?

Да, этот код работает с последними версиями Excel, включая файлы в формате Excel 2010 и более поздних версий.

#### Могу ли я защитить другие ячейки, кроме A1, B1 и C1?

Да, вы можете изменить код, чтобы заблокировать другие конкретные ячейки, изменив ссылки на ячейки в соответствующих строках кода.

#### Как я могу снова разблокировать заблокированные ячейки?

 Вы можете использовать`SetStyle` метод с`IsLocked` установлен в`false` чтобы разблокировать ячейки.

#### Могу ли я добавить в книгу дополнительные листы?

 Да, вы можете добавить в книгу другие листы, используя`Worksheets.Add()`метод и повторите шаги защиты ячеек для каждого листа.

#### Как изменить формат сохранения файла Excel?

 Вы можете изменить формат сохранения с помощью`SaveFormat` метод с нужным форматом, например`SaveFormat.Xlsx` для Excel 2007 и более поздних версий.