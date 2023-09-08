---
title: Получить ширину и высоту листа бумаги
linktitle: Получить ширину и высоту листа бумаги
second_title: Справочник по API Aspose.Cells для .NET
description: Создайте пошаговое руководство, объясняющее следующий исходный код C# для получения ширины и высоты листа электронной таблицы с помощью Aspose.Cells для .NET.
type: docs
weight: 80
url: /ru/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
В этом руководстве мы шаг за шагом объясним следующий исходный код C#, чтобы получить ширину и высоту листа с помощью Aspose.Cells для .NET. Выполните следующие действия:

## Шаг 1. Создайте книгу
 Начните с создания новой книги с помощью`Workbook` сорт:

```csharp
Workbook wb = new Workbook();
```

## Шаг 2. Доступ к первому листу
 Затем перейдите к первому листу в книге, используя`Worksheet` сорт:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Шаг 3. Установите размер бумаги A2 и укажите ширину и высоту бумаги в дюймах.
 Использовать`PaperSize` собственность`PageSetup` объект, чтобы установить размер бумаги A2, затем используйте`PaperWidth` и`PaperHeight` свойства, чтобы получить ширину и высоту бумаги соответственно. Отобразите эти значения с помощью`Console.WriteLine` метод:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Шаг 4. Повторите действия для бумаги других размеров.
Повторите предыдущие шаги, изменив размер бумаги на A3, A4 и Letter, а затем отобразив значения ширины и высоты бумаги для каждого размера:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Пример исходного кода для получения ширины и высоты листа с помощью Aspose.Cells для .NET 

```csharp
//Создать книгу
Workbook wb = new Workbook();
//Доступ к первому листу
Worksheet ws = wb.Worksheets[0];
//Установите размер бумаги A2 и напечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Установите размер бумаги A3 и напечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Установите размер бумаги A4 и напечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Установите размер бумаги Letter и напечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Заключение

Вы узнали, как использовать Aspose.Cells для .NET, чтобы получить ширину и высоту листа электронной таблицы. Эта функция может быть полезна для настройки и точного макета ваших документов Excel.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это мощная библиотека для управления и обработки файлов Excel в приложениях .NET. Он предлагает множество функций для создания, изменения, преобразования и анализа файлов Excel.

#### Как я могу получить размер бумаги электронной таблицы с помощью Aspose.Cells для .NET?

 Вы можете использовать`PageSetup` класс`Worksheet` объект для доступа к размеру бумаги. Использовать`PaperSize` свойство для установки размера бумаги и`PaperWidth` и`PaperHeight` свойства, чтобы получить ширину и высоту бумаги соответственно.

#### Какие размеры бумаги поддерживает Aspose.Cells for .NET?

Aspose.Cells для .NET поддерживает широкий диапазон часто используемых форматов бумаги, таких как A2, A3, A4 и Letter, а также множество других нестандартных размеров.

#### Могу ли я настроить размер бумаги электронной таблицы с помощью Aspose.Cells для .NET?

 Да, вы можете установить нестандартный размер бумаги, указав точные размеры ширины и высоты с помощью`PaperWidth` и`PaperHeight` свойства`PageSetup` сорт.