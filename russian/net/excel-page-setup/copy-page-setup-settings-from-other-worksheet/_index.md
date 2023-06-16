---
title: Копировать настройки параметров страницы из другого рабочего листа
linktitle: Копировать настройки параметров страницы из другого рабочего листа
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как копировать параметры конфигурации страницы из одной электронной таблицы в другую с помощью Aspose.Cells для .NET. Пошаговое руководство по оптимизации использования этой библиотеки.
type: docs
weight: 10
url: /ru/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
В этой статье мы шаг за шагом объясним следующий исходный код C#: Скопируйте параметры конфигурации страницы из другой электронной таблицы, используя Aspose.Cells для .NET. Мы будем использовать библиотеку Aspose.Cells для .NET для выполнения этой операции. Если вы хотите скопировать параметры настройки страницы с одного рабочего листа на другой, выполните следующие действия.

## Шаг 1: Создание рабочей книги
Первым шагом является создание рабочей книги. В нашем случае мы будем использовать класс Workbook, предоставляемый библиотекой Aspose.Cells. Вот код для создания книги:

```csharp
Workbook wb = new Workbook();
```

## Шаг 2: Добавление тестовых листов
После создания книги нам нужно добавить тестовые листы. В этом примере мы добавим два рабочих листа. Вот код для добавления двух листов:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Шаг 3: Доступ к рабочим листам
Теперь, когда мы добавили рабочие листы, нам нужно получить к ним доступ, чтобы иметь возможность изменять их настройки. Мы получим доступ к рабочим листам «TestSheet1» и «TestSheet2», используя их имена. Вот код для доступа к нему:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Шаг 4: Установка размера бумаги
 На этом шаге мы установим размер бумаги рабочего листа «TestSheet1». Мы будем использовать`PageSetup.PaperSize` свойство для установки размера бумаги. Например, мы установим размер бумаги «PaperA3ExtraTransverse». Вот код для этого:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Шаг 5: Копирование настроек параметров страницы
 Теперь мы скопируем параметры конфигурации страницы из рабочего листа «TestSheet1» в «TestSheet2». Мы будем использовать`PageSetup.Copy` способ выполнения этой операции. Вот код для этого:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Шаг 6: Печать размеров бумаги
 После копирования параметров настройки страницы мы распечатаем размеры бумаги двух рабочих листов. Мы будем использовать`Console.WriteLine` для отображения размеров бумаги. Вот код для этого:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Пример исходного кода для копирования параметров настройки страницы из другого рабочего листа с использованием Aspose.Cells для .NET 
```csharp
//Создать книгу
Workbook wb = new Workbook();
//Добавьте два тестовых листа
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Доступ к обоим листам как TestSheet1 и TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Установите для размера бумаги TestSheet1 значение PaperA3ExtraTransverse.
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Распечатайте размер бумаги обоих рабочих листов
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Скопируйте PageSetup из TestSheet1 в TestSheet2.
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Распечатайте размер бумаги обоих рабочих листов
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Заключение
В этой статье мы узнали, как копировать параметры конфигурации страницы с одного рабочего листа на другой с помощью Aspose.Cells для .NET. Мы прошли следующие этапы: создание рабочей книги, добавление тестовых рабочих листов, доступ к рабочим листам, установка размера бумаги, копирование параметров настройки страницы и печать размеров бумаги. Теперь вы можете использовать эти знания для копирования настроек конфигурации страницы в свои собственные проекты.

### Часто задаваемые вопросы

Вопрос. Можно ли копировать параметры конфигурации страницы между разными экземплярами книги?

 О: Да, вы можете копировать параметры настройки страницы между разными экземплярами книги, используя`PageSetup.Copy` метод библиотеки Aspose.Cells.

В: Могу ли я скопировать другие параметры настройки страницы, такие как ориентация или поля?

 О: Да, вы можете скопировать другие параметры настройки страницы, используя`PageSetup.Copy` метод с соответствующими параметрами. Например, вы можете скопировать ориентацию, используя`CopyOptions.Orientation` и поля с использованием`CopyOptions.Margins`.

В: Как узнать, какие параметры доступны для размера бумаги?

 О: Вы можете проверить Справочник по API библиотеки Aspose.Cells, чтобы узнать о доступных параметрах размера бумаги. Существует перечисление под названием`PaperSizeType` в котором перечислены различные поддерживаемые форматы бумаги.

В: Как я могу скачать библиотеку Aspose.Cells для .NET?

 О: Вы можете скачать библиотеку Aspose.Cells для .NET с[Aspose выпускает](https://releases.aspose.com/cells/net). Доступны бесплатные пробные версии, а также платные лицензии для коммерческого использования.

Q: Поддерживает ли библиотека Aspose.Cells другие языки программирования?

О: Да, библиотека Aspose.Cells поддерживает несколько языков программирования, включая C#, Java, Python и многие другие.