---
title: Определите, является ли размер бумаги рабочего листа автоматическим
linktitle: Определите, является ли размер бумаги рабочего листа автоматическим
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как определить, является ли размер бумаги электронной таблицы автоматическим, с помощью Aspose.Cells для .NET.
type: docs
weight: 20
url: /ru/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
В этой статье мы шаг за шагом объясним следующий исходный код C#: Определите, является ли размер бумаги на листе автоматическим, с помощью Aspose.Cells для .NET. Для выполнения этой операции мы будем использовать библиотеку Aspose.Cells для .NET. Выполните следующие действия, чтобы определить, является ли размер бумаги на листе автоматическим.

## Шаг 1. Загрузка книг
Первым шагом является загрузка книг. У нас будет две книги: одна с отключенным автоматическим размером бумаги, а другая с включенным автоматическим размером бумаги. Вот код для загрузки книг:

```csharp
// исходный каталог
string sourceDir = "YOUR_SOURCE_DIR";
// Выходной каталог
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Загрузите первую книгу с отключенным автоматическим размером бумаги.
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Загрузить вторую книгу с включенным автоматическим размером бумаги
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Шаг 2. Доступ к электронным таблицам
Теперь, когда мы загрузили рабочие книги, нам нужен доступ к рабочим листам, чтобы мы могли проверить автоматический размер бумаги. Мы перейдем к первому листу из двух книг. Вот код для доступа к нему:

```csharp
//Перейти к первому листу первой книги
Worksheet ws11 = wb1.Worksheets[0];

// Перейти к первому листу второй книги
Worksheet ws12 = wb2.Worksheets[0];
```

## Шаг 3. Проверьте автоматический размер бумаги
 На этом этапе мы проверим, является ли размер бумаги рабочего листа автоматическим. Мы будем использовать`PageSetup.IsAutomaticPaperSize` свойство, чтобы получить эту информацию. Затем мы отобразим результат. Вот код для этого:

```csharp
// Отображение свойства IsAutomaticPaperSize первого листа в первой книге.
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Отображение свойства IsAutomaticPaperSize первого листа во второй книге.
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Пример исходного кода для автоматического определения размера бумаги рабочего листа с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Выходной каталог
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Загрузите первую книгу с автоматическим размером бумаги false
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Загрузите вторую книгу с автоматическим размером бумаги true.
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Доступ к первому листу обеих книг
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Распечатайте свойство PageSetup.IsAutomaticPaperSize обоих листов.
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Заключение
В этой статье мы узнали, как определить, является ли размер листа автоматическим, с помощью Aspose.Cells для .NET. Мы выполнили следующие шаги: загрузили рабочие книги,

доступ к электронным таблицам и автоматическая проверка формата бумаги. Теперь вы можете использовать эти знания, чтобы определить, является ли размер бумаги ваших электронных таблиц автоматическим.

### Часто задаваемые вопросы

#### Вопрос: Как загрузить книги с помощью Aspose.Cells для .NET?

О: Вы можете загружать книги, используя класс Workbook из библиотеки Aspose.Cells. Используйте метод Workbook.Load для загрузки книги из файла.

#### Вопрос: Могу ли я проверить автоматический размер бумаги для других таблиц?

О: Да, вы можете проверить автоматический размер бумаги для любого листа, обратившись к свойству PageSetup.IsAutomaticPaperSize соответствующего объекта Worksheet.

#### Вопрос: Как изменить автоматический размер бумаги электронной таблицы?

О: Чтобы изменить автоматический размер бумаги листа, вы можете использовать свойство PageSetup.IsAutomaticPaperSize и установить для него нужное значение (истина или ложь).

#### Вопрос: Какие еще функции предлагает Aspose.Cells для .NET?

О: Aspose.Cells for .NET предлагает множество функций для работы с электронными таблицами, таких как создание, изменение и преобразование книг, а также манипулирование данными, формулами и форматированием.