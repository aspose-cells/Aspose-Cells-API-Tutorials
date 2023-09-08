---
title: Отображение и скрытие полос прокрутки рабочего листа
linktitle: Отображение и скрытие полос прокрутки рабочего листа
second_title: Справочник по API Aspose.Cells для .NET
description: Отобразите или скройте полосы прокрутки на листе Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 50
url: /ru/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
В этом уроке мы покажем вам, как отображать или скрывать вертикальные и горизонтальные полосы прокрутки на листе Excel, используя исходный код C# с помощью Aspose.Cells для .NET. Следуйте инструкциям ниже, чтобы получить желаемый результат.

## Шаг 1. Импортируйте необходимые библиотеки.

Убедитесь, что вы установили библиотеку Aspose.Cells для .NET и импортировали необходимые библиотеки в свой проект C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Шаг 2. Установите путь к каталогу и откройте файл Excel.

 Задайте путь к каталогу, содержащему файл Excel, затем откройте файл, создав поток файлов и создав экземпляр`Workbook` объект.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Шаг 3. Скройте полосы прокрутки

 Использовать`IsVScrollBarVisible` и`IsHScrollBarVisible` свойства`Workbook.Settings` объект, чтобы скрыть вертикальную и горизонтальную полосы прокрутки листа.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Шаг 4. Сохраните изменения.

 После внесения необходимых изменений сохраните измененный файл Excel, используя`Save` метод`Workbook` объект.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Пример исходного кода для отображения и скрытия полос прокрутки рабочего листа с использованием Aspose.Cells для .NET 

```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание потока файлов, содержащего открываемый файл Excel.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook workbook = new Workbook(fstream);
// Скрытие вертикальной полосы прокрутки файла Excel
workbook.Settings.IsVScrollBarVisible = false;
// Скрытие горизонтальной полосы прокрутки файла Excel
workbook.Settings.IsHScrollBarVisible = false;
// Сохранение измененного файла Excel
workbook.Save(dataDir + "output.xls");
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close();
```

### Заключение

В этом пошаговом руководстве показано, как отображать или скрывать вертикальные и горизонтальные полосы прокрутки в электронной таблице Excel с помощью Aspose.Cells для .NET. Используя предоставленный исходный код C#, вы можете легко настроить отображение полос прокрутки в файлах Excel.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это мощная библиотека для управления файлами Excel в приложениях .NET.

#### Как мне установить Aspose.Cells для .NET?

 Чтобы установить Aspose.Cells для .NET, вам необходимо скачать соответствующий пакет с сайта[Aspose Релизы](https://releases/aspose.com/cells/net/) и добавьте его в свой проект .NET.

#### Как я могу отображать или скрывать полосы прокрутки в электронной таблице Excel с помощью Aspose.Cells для .NET?

 Вы можете использовать`IsVScrollBarVisible` и`IsHScrollBarVisible` свойства`Workbook.Settings` объект для отображения или скрытия вертикальной и горизонтальной полосы прокрутки соответственно на листе Excel.

#### Какие еще форматы файлов Excel поддерживаются Aspose.Cells для .NET?

Aspose.Cells для .NET поддерживает различные форматы файлов Excel, такие как XLS, XLSX, CSV, HTML, PDF и т. д.