---
title: Зафиксировать панели рабочего листа
linktitle: Зафиксировать панели рабочего листа
second_title: Справочник по API Aspose.Cells для .NET
description: Легко манипулируйте замороженными панелями листа Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 70
url: /ru/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
В этом уроке мы покажем вам, как заблокировать панели на листе Excel, используя исходный код C# с помощью Aspose.Cells для .NET. Следуйте инструкциям ниже, чтобы получить желаемый результат.

## Шаг 1. Импортируйте необходимые библиотеки.

Убедитесь, что вы установили библиотеку Aspose.Cells для .NET и импортировали необходимые библиотеки в свой проект C#.

```csharp
using Aspose.Cells;
```

## Шаг 2. Установите путь к каталогу и откройте файл Excel.

 Задайте путь к каталогу, содержащему файл Excel, затем откройте файл, создав экземпляр`Workbook` объект.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Шаг 3. Перейдите в электронную таблицу и примените настройки блокировки панели.

 Перейдите к первому листу файла Excel с помощью кнопки`Worksheet` объект. Затем используйте`FreezePanes` метод применения настроек блокировки панели.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

В приведенном выше примере панели привязаны к ячейке в строке 3 и столбце 2.

## Шаг 4. Сохраните изменения.

 После внесения необходимых изменений сохраните измененный файл Excel, используя`Save` метод`Workbook` объект.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Пример исходного кода для закрепления панелей рабочего листа с использованием Aspose.Cells для .NET 

```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание потока файлов, содержащего открываемый файл Excel.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook workbook = new Workbook(fstream);
// Доступ к первому листу в файле Excel
Worksheet worksheet = workbook.Worksheets[0];
// Применение настроек областей закрепления
worksheet.FreezePanes(3, 2, 3, 2);
// Сохранение измененного файла Excel
workbook.Save(dataDir + "output.xls");
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close();
```

## Заключение

В этом пошаговом руководстве показано, как заблокировать панели в электронной таблице Excel с помощью Aspose.Cells для .NET. Используя предоставленный исходный код C#, вы можете легко настроить параметры блокировки панели, чтобы лучше организовывать и визуализировать данные в файлах Excel.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это мощная библиотека для управления файлами Excel в приложениях .NET.

#### Как мне установить Aspose.Cells для .NET?

 Чтобы установить Aspose.Cells для .NET, вам необходимо скачать соответствующий пакет с сайта[Aspose Релизы](https://releases/aspose.com/cells/net/) и добавьте его в свой проект .NET.

#### Как заблокировать панели на листе Excel с помощью Aspose.Cells для .NET?

 Вы можете использовать`FreezePanes` метод`Worksheet` объект для блокировки панелей рабочего листа. Укажите ячейки для блокировки, указав индексы строк и столбцов.

#### Могу ли я настроить параметры блокировки панели с помощью Aspose.Cells для .NET?

 Да, используя`FreezePanes` вы можете указать, какие ячейки необходимо заблокировать, указав соответствующие индексы строк и столбцов.
