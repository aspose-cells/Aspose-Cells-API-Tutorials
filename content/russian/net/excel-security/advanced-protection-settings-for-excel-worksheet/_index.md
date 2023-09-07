---
title: Дополнительные параметры защиты для рабочего листа Excel
linktitle: Дополнительные параметры защиты для рабочего листа Excel
second_title: Справочник по Aspose.Cells для .NET API
description: Защитите свои файлы Excel, установив дополнительные параметры защиты с помощью Aspose.Cells для .NET.
type: docs
weight: 10
url: /ru/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
В этом руководстве мы покажем вам, как установить дополнительные параметры защиты для электронной таблицы Excel с помощью библиотеки Aspose.Cells для .NET. Следуйте приведенным ниже инструкциям, чтобы выполнить эту задачу.

## Шаг 1: Подготовка

Убедитесь, что вы установили Aspose.Cells для .NET и создали проект C# в выбранной вами интегрированной среде разработки (IDE).

## Шаг 2. Задайте путь к каталогу документов

 объявить`dataDir` переменную и инициализируйте ее путем к каталогу ваших документов. Например :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Обязательно замените`"YOUR_DOCUMENTS_DIRECTORY"` с фактическим путем к вашему каталогу.

## Шаг 3. Создайте файловый поток, чтобы открыть файл Excel.

 Создать`FileStream` объект, содержащий файл Excel для открытия:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Убедитесь, что у вас есть файл Excel`book1.xls` в каталоге документов или укажите правильное имя файла и местоположение.

## Шаг 4. Создайте экземпляр объекта Workbook и откройте файл Excel.

 Использовать`Workbook`class из Aspose.Cells, чтобы создать экземпляр объекта Workbook и открыть указанный файл Excel через файловый поток:

```csharp
Workbook excel = new Workbook(fstream);
```

## Шаг 5: Получите доступ к первому рабочему листу

Перейдите к первому рабочему листу файла Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Шаг 6. Установите параметры защиты рабочего листа

Используйте свойства объекта рабочего листа, чтобы настроить параметры защиты рабочего листа по мере необходимости. Например :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... При необходимости установите другие параметры защиты...
```

## Шаг 7: Сохраните измененный файл Excel

 Сохраните измененный файл Excel с помощью`Save` метод объекта Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Обязательно укажите желаемый путь и имя файла для выходного файла.

## Шаг 8: Закройте файловый поток

После сохранения закройте файловый поток, чтобы освободить все связанные ресурсы:

```csharp
fstream.Close();
```
	
### Пример исходного кода для параметров дополнительной защиты для рабочего листа Excel с использованием Aspose.Cells для .NET 
```csharp
// Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание файлового потока, содержащего открываемый файл Excel
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook excel = new Workbook(fstream);
// Доступ к первому рабочему листу в файле Excel
Worksheet worksheet = excel.Worksheets[0];
// Ограничение пользователей на удаление столбцов рабочего листа
worksheet.Protection.AllowDeletingColumn = false;
// Ограничение пользователей на удаление строки рабочего листа
worksheet.Protection.AllowDeletingRow = false;
// Ограничение пользователей на редактирование содержимого рабочего листа
worksheet.Protection.AllowEditingContent = false;
// Ограничение пользователей на редактирование объектов рабочего листа
worksheet.Protection.AllowEditingObject = false;
// Ограничение пользователей на редактирование сценариев рабочего листа
worksheet.Protection.AllowEditingScenario = false;
//Ограничение пользователей для фильтрации
worksheet.Protection.AllowFiltering = false;
// Разрешение пользователям форматировать ячейки рабочего листа
worksheet.Protection.AllowFormattingCell = true;
// Разрешение пользователям форматировать строки рабочего листа
worksheet.Protection.AllowFormattingRow = true;
// Разрешение пользователям вставлять столбцы на листе
worksheet.Protection.AllowFormattingColumn = true;
// Разрешение пользователям вставлять гиперссылки на лист
worksheet.Protection.AllowInsertingHyperlink = true;
// Разрешение пользователям вставлять строки на листе
worksheet.Protection.AllowInsertingRow = true;
// Разрешение пользователям выбирать заблокированные ячейки рабочего листа
worksheet.Protection.AllowSelectingLockedCell = true;
// Разрешение пользователям выбирать разблокированные ячейки рабочего листа
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Разрешить пользователям сортировать
worksheet.Protection.AllowSorting = true;
// Разрешение пользователям использовать сводные таблицы на листе
worksheet.Protection.AllowUsingPivotTable = true;
// Сохранение измененного файла Excel
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close();
```

## Заключение

Поздравляем! Теперь вы узнали, как установить дополнительные параметры защиты для электронной таблицы Excel с помощью Aspose.Cells для .NET. Используйте эти знания для защиты файлов Excel и ограничения действий пользователей.

### Часто задаваемые вопросы

#### Вопрос: Как мне создать новый проект C# в моей среде IDE?

О: Шаги по созданию нового проекта C# могут различаться в зависимости от используемой вами IDE. Обратитесь к документации вашей IDE для получения подробных инструкций.

#### В: Можно ли установить собственные параметры защиты, отличные от указанных в руководстве?

О: Да, Aspose.Cells предлагает широкий спектр настроек защиты, которые вы можете настроить в соответствии со своими потребностями. Дополнительные сведения см. в документации Aspose.Cells.

#### В: Какой формат файла используется для сохранения измененного файла Excel в примере кода?

О: В примере кода измененный файл Excel сохраняется в формате Excel 97-2003 (.xls). При необходимости вы можете выбрать другие форматы, поддерживаемые Aspose.Cells.

#### Q: Как я могу получить доступ к другим листам в файле Excel?

 A: Вы можете получить доступ к другим рабочим листам, используя индекс или имя листа, например:`Worksheet worksheet = excel.Worksheets[1];` или`Worksheet worksheet = excel.Worksheets[" SheetName"];`.