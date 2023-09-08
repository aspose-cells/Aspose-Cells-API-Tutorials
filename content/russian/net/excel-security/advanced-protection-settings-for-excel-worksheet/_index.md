---
title: Параметры дополнительной защиты для листа Excel
linktitle: Параметры дополнительной защиты для листа Excel
second_title: Справочник по API Aspose.Cells для .NET
description: Защитите свои файлы Excel, установив расширенные настройки защиты с помощью Aspose.Cells для .NET.
type: docs
weight: 10
url: /ru/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
В этом руководстве мы покажем вам, как установить дополнительные параметры защиты для электронной таблицы Excel с помощью библиотеки Aspose.Cells для .NET. Следуйте инструкциям ниже, чтобы выполнить эту задачу.

## Шаг 1: Подготовка

Убедитесь, что вы установили Aspose.Cells для .NET и создали проект C# в предпочитаемой вами интегрированной среде разработки (IDE).

## Шаг 2. Установите путь к каталогу документов.

 Объявить`dataDir` переменную и инициализируйте ее путем к каталогу ваших документов. Например :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Обязательно замените`"YOUR_DOCUMENTS_DIRECTORY"` с фактическим путем к вашему каталогу.

## Шаг 3. Создайте поток файлов, чтобы открыть файл Excel.

 Создать`FileStream` объект, содержащий файл Excel, который нужно открыть:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Убедитесь, что у вас есть файл Excel`book1.xls` в каталоге документов или укажите правильное имя и местоположение файла.

## Шаг 4. Создайте экземпляр объекта Workbook и откройте файл Excel.

 Использовать`Workbook`класс из Aspose.Cells для создания экземпляра объекта Workbook и открытия указанного файла Excel через файловый поток:

```csharp
Workbook excel = new Workbook(fstream);
```

## Шаг 5. Доступ к первому листу

Перейдите к первому листу файла Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Шаг 6. Установите параметры защиты рабочего листа

Используйте свойства объекта листа, чтобы при необходимости установить параметры защиты листа. Например :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... При необходимости установите другие параметры защиты...
```

## Шаг 7. Сохраните измененный файл Excel.

 Сохраните измененный файл Excel, используя`Save` метод объекта Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Обязательно укажите желаемый путь и имя выходного файла.

## Шаг 8. Закройте файловый поток

После сохранения закройте поток файлов, чтобы освободить все связанные ресурсы:

```csharp
fstream.Close();
```
	
### Пример исходного кода для параметров дополнительной защиты для листа Excel с использованием Aspose.Cells для .NET 
```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание потока файлов, содержащего открываемый файл Excel.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook excel = new Workbook(fstream);
// Доступ к первому листу в файле Excel
Worksheet worksheet = excel.Worksheets[0];
// Запретить пользователям удалять столбцы листа
worksheet.Protection.AllowDeletingColumn = false;
// Запретить пользователям удалять строки рабочего листа
worksheet.Protection.AllowDeletingRow = false;
// Запретить пользователям редактировать содержимое листа
worksheet.Protection.AllowEditingContent = false;
// Ограничение пользователей на редактирование объектов рабочего листа
worksheet.Protection.AllowEditingObject = false;
// Ограничение пользователей на редактирование сценариев рабочего листа
worksheet.Protection.AllowEditingScenario = false;
//Ограничение пользователей на фильтрацию
worksheet.Protection.AllowFiltering = false;
// Разрешение пользователям форматировать ячейки рабочего листа
worksheet.Protection.AllowFormattingCell = true;
// Разрешение пользователям форматировать строки рабочего листа
worksheet.Protection.AllowFormattingRow = true;
// Разрешение пользователям вставлять столбцы на лист
worksheet.Protection.AllowFormattingColumn = true;
// Разрешение пользователям вставлять гиперссылки на лист
worksheet.Protection.AllowInsertingHyperlink = true;
// Разрешение пользователям вставлять строки на лист
worksheet.Protection.AllowInsertingRow = true;
// Разрешение пользователям выбирать заблокированные ячейки листа
worksheet.Protection.AllowSelectingLockedCell = true;
// Разрешение пользователям выбирать незаблокированные ячейки листа
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Разрешение пользователям сортировать
worksheet.Protection.AllowSorting = true;
// Разрешение пользователям использовать сводные таблицы на листе
worksheet.Protection.AllowUsingPivotTable = true;
// Сохранение измененного файла Excel
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close();
```

## Заключение

Поздравляем! Теперь вы узнали, как установить дополнительные параметры защиты для электронной таблицы Excel с помощью Aspose.Cells для .NET. Используйте эти знания, чтобы защитить файлы Excel и ограничить действия пользователей.

### Часто задаваемые вопросы

#### Вопрос: Как создать новый проект C# в своей IDE?

О: Действия по созданию нового проекта C# могут различаться в зависимости от используемой вами среды разработки. Подробные инструкции см. в документации вашей IDE.

#### Вопрос: Можно ли установить дополнительные параметры защиты, отличные от указанных в руководстве?

О: Да, Aspose.Cells предлагает широкий спектр настроек защиты, которые вы можете настроить в соответствии со своими потребностями. Дополнительную информацию см. в документации Aspose.Cells.

#### Вопрос: Какой формат файла используется для сохранения измененного файла Excel в примере кода?

Ответ: В примере кода измененный файл Excel сохраняется в формате Excel 97-2003 (.xls). При необходимости вы можете выбрать другие форматы, поддерживаемые Aspose.Cells.

#### Вопрос: Как получить доступ к другим листам в файле Excel?

 О: Вы можете получить доступ к другим листам, используя индекс или имя листа, например:`Worksheet worksheet = excel.Worksheets[1];` или`Worksheet worksheet = excel.Worksheets[" SheetName"];`.