---
title: Получить ширину бумаги и высоту листа
linktitle: Получить ширину бумаги и высоту листа
second_title: Справочник по Aspose.Cells для .NET API
description: Создайте пошаговое руководство, чтобы объяснить следующий исходный код C#, чтобы получить ширину и высоту бумаги электронной таблицы с помощью Aspose.Cells для .NET.
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

## Шаг 2: доступ к первому рабочему листу
 Затем перейдите к первому рабочему листу в рабочей книге с помощью`Worksheet` сорт:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Шаг 3. Установите размер бумаги на A2 и укажите ширину и высоту бумаги в дюймах.
 Использовать`PaperSize` собственность`PageSetup` объект, чтобы установить размер бумаги на A2, затем используйте`PaperWidth` и`PaperHeight` свойства, чтобы получить ширину и высоту бумаги соответственно. Отобразите эти значения с помощью`Console.WriteLine` метод:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Шаг 4. Повторите шаги для других форматов бумаги.
Повторите предыдущие шаги, изменив размер бумаги на A3, A4 и Letter, а затем отобразив значения ширины и высоты бумаги для каждого размера:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Пример исходного кода для получения ширины и высоты листа бумаги с использованием Aspose.Cells для .NET 

```csharp
//Создать книгу
Workbook wb = new Workbook();
//Доступ к первому рабочему листу
Worksheet ws = wb.Worksheets[0];
//Установите размер бумаги на A2 и распечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Установите размер бумаги на A3 и распечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Установите размер бумаги на A4 и распечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Установите размер бумаги на Letter и напечатайте ширину и высоту бумаги в дюймах.
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Заключение

Вы узнали, как использовать Aspose.Cells для .NET, чтобы получить ширину и высоту бумаги электронной таблицы. Эта функция может быть полезна для настройки и точной компоновки ваших документов Excel.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это мощная библиотека для управления и обработки файлов Excel в приложениях .NET. Он предлагает множество функций для создания, изменения, преобразования и анализа файлов Excel.

#### Как я могу получить размер листа электронной таблицы с помощью Aspose.Cells для .NET?

 Вы можете использовать`PageSetup` класс`Worksheet` объекта для доступа к размеру бумаги. Использовать`PaperSize` свойство для установки размера бумаги и`PaperWidth` и`PaperHeight` свойства, чтобы получить ширину и высоту бумаги соответственно.

#### Какие форматы бумаги поддерживает Aspose.Cells for .NET?

Aspose.Cells для .NET поддерживает широкий диапазон широко используемых форматов бумаги, таких как A2, A3, A4 и Letter, а также многие другие нестандартные форматы.

#### Могу ли я настроить размер листа электронной таблицы с помощью Aspose.Cells для .NET?

Да, вы можете установить пользовательский размер бумаги, указав точные размеры ширины и высоты с помощью`PaperWidth` и`PaperHeight` свойства`PageSetup` сорт.