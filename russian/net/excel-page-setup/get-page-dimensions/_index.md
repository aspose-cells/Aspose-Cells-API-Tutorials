---
title: Получить размеры страницы
linktitle: Получить размеры страницы
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как получить размеры страницы в Excel с помощью Aspose.Cells для .NET. Пошаговое руководство с исходным кодом на C#.
type: docs
weight: 40
url: /ru/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET — это мощная библиотека, позволяющая разработчикам программно работать с файлами Microsoft Excel. Он предлагает широкий спектр функций для работы с документами Excel, включая возможность получения размеров страницы. В этом руководстве мы покажем вам, как получить размеры страницы с помощью Aspose.Cells для .NET.

## Шаг 1. Создайте экземпляр класса Workbook.

Для начала нам нужно создать экземпляр класса Workbook, который представляет книгу Excel. Этого можно добиться с помощью следующего кода:

```csharp
Workbook book = new Workbook();
```

## Шаг 2. Доступ к электронной таблице

Затем нам нужно перейти к рабочему листу в рабочей книге, где мы хотим установить размеры страницы. В этом примере предположим, что мы хотим работать с первым рабочим листом. Мы можем получить к нему доступ, используя следующий код:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Шаг 3. Установите размер бумаги на A2, а также ширину и высоту печати в дюймах.

Теперь мы установим размер бумаги на A2 и напечатаем ширину и высоту страницы в дюймах. Этого можно добиться с помощью следующего кода:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Шаг 4. Установите размер бумаги на A3 и ширину и высоту печати в дюймах.

Далее мы установим размер бумаги на A3 и напечатаем ширину и высоту страницы в дюймах. Вот соответствующий код:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Шаг 5. Установите размер бумаги на A4, а также ширину и высоту печати в дюймах.

Теперь мы установим размер бумаги на A4 и напечатаем ширину и высоту страницы в дюймах. Вот код:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Шаг 6. Установите размер бумаги Letter и напечатайте ширину и высоту в дюймах.

Наконец, мы установим размер бумаги на Letter и напечатаем ширину и высоту страницы в дюймах. Вот код:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Пример исходного кода для получения параметров страницы с использованием Aspose.Cells для .NET 
```csharp
// Создайте экземпляр класса Workbook
Workbook book = new Workbook();
// Доступ к первому рабочему листу
Worksheet sheet = book.Worksheets[0];
// Установите размер бумаги на A2 и распечатайте ширину и высоту бумаги в дюймах.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Установите размер бумаги на A3 и распечатайте ширину и высоту бумаги в дюймах.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Установите размер бумаги на A4 и распечатайте ширину и высоту бумаги в дюймах.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Установите размер бумаги на Letter и напечатайте ширину и высоту бумаги в дюймах.
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Заключение

Поздравляем! Вы узнали, как получить размеры страницы с помощью Aspose.Cells для .NET. Эта функция может быть полезна, когда вам нужно выполнить определенные операции на основе размеров страницы в ваших файлах Excel.

Не забудьте дополнительно изучить документацию Aspose.Cells, чтобы узнать обо всех его мощных функциях.

### Часто задаваемые вопросы

#### 1. Какие еще форматы бумаги поддерживает Aspose.Cells для .NET?

Aspose.Cells для .NET поддерживает различные форматы бумаги, включая A1, A5, B4, B5, Executive, Legal, Letter и многие другие. Полный список поддерживаемых форматов бумаги можно найти в документации.

#### 2. Могу ли я установить пользовательские размеры страницы с помощью Aspose.Cells для .NET?

Да, вы можете установить пользовательские размеры страницы, указав желаемую ширину и высоту. Aspose.Cells предлагает полную гибкость настройки размеров страницы в соответствии с вашими потребностями.

#### 3. Могу ли я получить размеры страницы в других единицах измерения, кроме дюймов?

Да, Aspose.Cells для .NET позволяет получать размеры страницы в различных единицах измерения, включая дюймы, сантиметры, миллиметры и пункты.

#### 4. Поддерживает ли Aspose.Cells for .NET другие функции редактирования параметров страницы?

Да, Aspose.Cells предлагает полный набор функций для редактирования настроек страницы, включая настройку полей, ориентации, верхних и нижних колонтитулов и т. д.