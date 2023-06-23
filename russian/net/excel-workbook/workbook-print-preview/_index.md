---
title: Предварительный просмотр рабочей книги
linktitle: Предварительный просмотр рабочей книги
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как создать предварительный просмотр книги с помощью Aspose.Cells для .NET.
type: docs
weight: 170
url: /ru/net/excel-workbook/workbook-print-preview/
---
Предварительный просмотр рабочей книги — важная функция при работе с файлами Excel с помощью Aspose.Cells для .NET. Вы можете легко создать предварительный просмотр печати, выполнив следующие действия:

## Шаг 1: Укажите исходный каталог

Во-первых, вам нужно указать исходный каталог, в котором находится файл Excel, который вы хотите просмотреть. Вот как это сделать:

```csharp
// исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Шаг 2: Загрузите книгу

Затем вам нужно загрузить рабочую книгу Workbook из указанного файла Excel. Вот как это сделать:

```csharp
// Загрузите книгу Workbook
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Шаг 3. Настройте параметры изображения и печати

Перед созданием предварительного просмотра печати вы можете настроить параметры изображения и печати по мере необходимости. В этом примере мы используем параметры по умолчанию. Вот как это сделать:

```csharp
// Параметры изображения и печати
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Шаг 4. Создайте предварительный просмотр книги

Теперь вы можете создать предварительный просмотр книги Workbook с помощью класса WorkbookPrintingPreview. Вот как это сделать:

```csharp
// Предварительный просмотр рабочей книги
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Шаг 5: Создайте предварительный просмотр листа для печати

Если вы хотите создать предварительный просмотр для печати определенного рабочего листа, вы можете использовать класс SheetPrintingPreview. Вот пример:

```csharp
// Предварительный просмотр рабочего листа
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Пример исходного кода для предварительного просмотра рабочей книги с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Заключение

Создание предварительного просмотра книги — мощная функция, предлагаемая Aspose.Cells для .NET. Следуя приведенным выше шагам, вы можете легко просмотреть свою книгу Excel и получить информацию о количестве страниц для печати.

### Часто задаваемые вопросы

#### В: Как я могу указать другой исходный каталог для загрузки моей книги?
    
 О: Вы можете использовать`Set_SourceDirectory` метод, чтобы указать другой исходный каталог. Например:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### В: Могу ли я настроить параметры изображения и печати при создании предварительного просмотра?
    
 О: Да, вы можете настроить параметры изображения и печати, изменив свойства`ImageOrPrintOptions` объект. Например, вы можете установить разрешение изображения, формат выходного файла и т. д.

#### В: Можно ли создать предварительный просмотр для печати нескольких листов в книге?
    
О: Да, вы можете перебирать разные рабочие листы в рабочей книге и создавать предварительный просмотр печати для каждого листа, используя`SheetPrintingPreview` сорт.

#### В: Как сохранить предварительный просмотр в виде изображения или файла PDF?
    
 О: Вы можете использовать`ToImage` или`ToPdf` метод`WorkbookPrintingPreview` или`SheetPrintingPreview` объект для сохранения предварительного просмотра в виде изображения или файла PDF.

#### Q: Что я могу сделать с предварительным просмотром печати после создания?
    
О: Создав предварительный просмотр перед печатью, вы можете просмотреть его на экране, сохранить в виде изображения или файла PDF или использовать для других операций, таких как отправка по электронной почте или печать.
	