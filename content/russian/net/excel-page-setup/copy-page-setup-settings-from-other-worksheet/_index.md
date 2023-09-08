---
title: Копирование настроек страницы из другого листа
linktitle: Копирование настроек страницы из другого листа
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как скопировать настройки конфигурации страницы из одной электронной таблицы в другую с помощью Aspose.Cells для .NET. Пошаговое руководство по оптимизации использования этой библиотеки.
type: docs
weight: 10
url: /ru/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
В этой статье мы шаг за шагом объясним следующий исходный код C#: Скопируйте параметры конфигурации страницы из другой электронной таблицы с помощью Aspose.Cells для .NET. Для выполнения этой операции мы будем использовать библиотеку Aspose.Cells для .NET. Если вы хотите скопировать параметры настройки страницы с одного листа на другой, выполните следующие действия.

## Шаг 1. Создание книги
Первым шагом является создание рабочей книги. В нашем случае мы будем использовать класс Workbook, предоставленный библиотекой Aspose.Cells. Вот код для создания книги:

```csharp
Workbook wb = new Workbook();
```

## Шаг 2. Добавление тестовых листов
После создания книги нам нужно добавить тестовые листы. В этом примере мы добавим два листа. Вот код для добавления двух листов:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Шаг 3. Доступ к рабочим листам
Теперь, когда мы добавили рабочие листы, нам нужно получить к ним доступ, чтобы иметь возможность изменить их настройки. Мы получим доступ к листам «TestSheet1» и «TestSheet2», используя их имена. Вот код для доступа к нему:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Шаг 4. Установка размера бумаги
 На этом этапе мы установим размер бумаги листа «TestSheet1». Мы будем использовать`PageSetup.PaperSize` свойство для установки размера бумаги. Например, мы установим размер бумаги «PaperA3ExtraTransverse». Вот код для этого:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Шаг 5. Копирование настроек страницы
Теперь мы скопируем настройки конфигурации страницы из листа «TestSheet1» в «TestSheet2». Мы будем использовать`PageSetup.Copy` метод выполнения этой операции. Вот код для этого:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Шаг 6: Печать размеров бумаги
 После копирования настроек страницы мы напечатаем размеры бумаги двух листов. Мы будем использовать`Console.WriteLine` для отображения размеров бумаги. Вот код для этого:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Пример исходного кода для копирования настроек страницы из другого листа с использованием Aspose.Cells для .NET 
```csharp
//Создать книгу
Workbook wb = new Workbook();
//Добавьте два тестовых листа
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Получите доступ к обоим листам как TestSheet1 и TestSheet2.
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Установите размер бумаги TestSheet1 на PaperA3ExtraTransverse.
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Распечатайте размер бумаги обоих листов.
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Скопируйте PageSetup из TestSheet1 в TestSheet2.
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Распечатайте размер бумаги обоих листов.
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Заключение
В этой статье мы узнали, как скопировать настройки конфигурации страницы с одного листа на другой с помощью Aspose.Cells для .NET. Мы выполнили следующие шаги: создание книги, добавление тестовых листов, доступ к рабочим листам, установка размера бумаги, копирование параметров настройки страницы и печать размеров бумаги. Теперь вы можете использовать эти знания для копирования настроек конфигурации страницы в свои собственные проекты.

### Часто задаваемые вопросы

#### Вопрос: Могу ли я скопировать параметры конфигурации страницы между разными экземплярами книги?

 О: Да, вы можете скопировать параметры настройки страницы между разными экземплярами книги, используя`PageSetup.Copy` метод библиотеки Aspose.Cells.

#### Вопрос: Могу ли я скопировать другие настройки страницы, например ориентацию или поля?

 О: Да, вы можете скопировать другие настройки страницы, используя`PageSetup.Copy` метод с соответствующими опциями. Например, вы можете скопировать ориентацию, используя`CopyOptions.Orientation` и поля с использованием`CopyOptions.Margins`.

#### Вопрос: Как узнать, какие параметры доступны для формата бумаги?

О: Вы можете ознакомиться с Справочником по API библиотеки Aspose.Cells, чтобы узнать о доступных параметрах размера бумаги. Существует перечисление под названием`PaperSizeType` в котором перечислены различные поддерживаемые форматы бумаги.

#### Вопрос: Как загрузить библиотеку Aspose.Cells для .NET?

 О: Вы можете скачать библиотеку Aspose.Cells для .NET с сайта[Aspose Релизы](https://releases.aspose.com/cells/net). Доступны бесплатные пробные версии, а также платные лицензии для коммерческого использования.

#### Вопрос: Поддерживает ли библиотека Aspose.Cells другие языки программирования?

О: Да, библиотека Aspose.Cells поддерживает несколько языков программирования, включая C#, Java, Python и многие другие.