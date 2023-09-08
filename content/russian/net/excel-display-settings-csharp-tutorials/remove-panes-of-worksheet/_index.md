---
title: Удалить панели рабочего листа
linktitle: Удалить панели рабочего листа
second_title: Справочник по API Aspose.Cells для .NET
description: Пошаговое руководство по удалению панелей из листа Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 120
url: /ru/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
В этом уроке мы объясним, как удалить панели из листа Excel с помощью Aspose.Cells для .NET. Выполните следующие шаги, чтобы получить желаемый результат:

## Шаг 1. Настройка среды

Убедитесь, что вы установили Aspose.Cells для .NET и настроили среду разработки. Также убедитесь, что у вас есть копия файла Excel, из которого вы хотите удалить панели.

## Шаг 2. Импортируйте необходимые зависимости

Добавьте необходимые директивы для использования классов из Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Шаг 3. Инициализация кода

Начните с инициализации пути к каталогу, содержащему ваши документы Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Шаг 4. Открытие файла Excel

 Создать экземпляр нового`Workbook` объект и откройте файл Excel с помощью`Open` метод:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Шаг 5. Определите активную ячейку

 Установите активную ячейку рабочего листа с помощью`ActiveCell` свойство:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Шаг 6. Удаление панелей

 Удалите панели из окна рабочего листа с помощью`RemoveSplit` метод:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Шаг 7: Сохранение изменений

Сохраните внесенные изменения в файл Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Пример исходного кода для удаления панелей рабочего листа с использованием Aspose.Cells для .NET 
```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создайте экземпляр новой книги и откройте файл шаблона.
Workbook book = new Workbook(dataDir + "Book1.xls");
// Установить активную ячейку
book.Worksheets[0].ActiveCell = "A20";
// Разделить окно рабочего листа
book.Worksheets[0].RemoveSplit();
// Сохраните файл Excel
book.Save(dataDir + "output.xls");
```

## Заключение

В этом уроке вы узнали, как удалить панели из листа Excel с помощью Aspose.Cells для .NET. Следуя описанным шагам, вы сможете легко настроить внешний вид и поведение файлов Excel.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это популярная программная библиотека для работы с файлами Excel в приложениях .NET.

#### Как установить активную ячейку листа в Aspose.Cells?

 Вы можете установить активную ячейку с помощью`ActiveCell`свойство объекта Worksheet.

#### Могу ли я удалить из окна листа только горизонтальные или вертикальные панели?

 Да, используя Aspose.Cells, вы можете удалить только горизонтальные или вертикальные панели, используя соответствующие методы, такие как`RemoveHorizontalSplit` или`RemoveVerticalSplit`.

#### Работает ли Aspose.Cells только с файлами Excel в формате .xls?

Нет, Aspose.Cells поддерживает различные форматы файлов Excel, включая .xls и .xlsx.
	