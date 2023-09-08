---
title: Разрешить начальный апостроф
linktitle: Разрешить начальный апостроф
second_title: Справочник по API Aspose.Cells для .NET
description: Разрешите начальный апостроф в книгах Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 60
url: /ru/net/excel-workbook/allow-leading-apostrophe/
---
В этом пошаговом руководстве мы объясним предоставленный исходный код C#, который позволит вам разрешить использование начального апострофа в книге Excel с помощью Aspose.Cells для .NET. Для выполнения этой операции выполните следующие действия.

## Шаг 1. Установите исходный и выходной каталоги.

```csharp
// исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
// Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
```

На этом первом этапе мы определяем исходный и выходной каталоги для файлов Excel.

## Шаг 2. Создайте экземпляр объекта WorkbookDesigner.

```csharp
// Создание экземпляра объекта WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Мы создаем экземпляр`WorkbookDesigner` класс из Aspose.Cells.

## Шаг 3. Загрузите книгу Excel

```csharp
// Загрузите книгу Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Загружаем книгу Excel из указанного файла и отключаем автоматическое преобразование начальных апострофов в текстовый стиль.

## Шаг 4. Установите источник данных

```csharp
// Определите источник данных для книги дизайнера
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Мы определяем список объектов данных и используем`SetDataSource` метод для установки источника данных для книги дизайнера.

## Шаг 5. Обработка интеллектуальных маркеров

```csharp
// Обработка интеллектуальных маркеров
designer. Process();
```

 Мы используем`Process` метод обработки смарт-маркеров в книге дизайнера.

## Шаг 6. Сохраните измененную книгу Excel.

```csharp
// Сохраните измененную книгу Excel.
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Сохраняем модифицированную книгу Excel с внесенными изменениями.

### Пример исходного кода для разрешения ведущего апострофа с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Создание экземпляра объекта WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Откройте таблицу дизайнера, содержащую интеллектуальные маркеры.
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Установите источник данных для электронной таблицы дизайнера
designer.SetDataSource("sampleData", list);
// Обработка смарт-маркеров
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Заключение

Поздравляем! Вы узнали, как разрешить использование начального апострофа в книге Excel с помощью Aspose.Cells для .NET. Поэкспериментируйте с собственными данными для дальнейшей настройки книг Excel.

### Часто задаваемые вопросы

#### Вопрос: Что такое разрешение на апостроф в книге Excel?

Ответ: Разрешение начального апострофа в книге Excel позволяет корректно отображать данные, начинающиеся с апострофа, без преобразования их в текстовый стиль. Это полезно, если вы хотите сохранить апостроф как часть данных.

#### Вопрос: Зачем мне отключать автоматическое преобразование начальных апострофов?

О: Отключив автоматическое преобразование опережающих котировок, вы сможете сохранить их использование в том виде, в каком оно есть в ваших данных. Это позволяет избежать непреднамеренного изменения данных при открытии книги Excel или работе с ней.

#### Вопрос: Как установить источник данных в книге дизайнера?

 О: Чтобы установить источник данных в книге дизайнера, вы можете использовать команду`SetDataSource` метод, указывающий имя источника данных и список соответствующих объектов данных.

#### Вопрос: Влияет ли разрешение апострофа в начале на другие данные в книге Excel?

О: Нет, разрешение ведущего апострофа влияет только на данные, начинающиеся с апострофа. Остальные данные в книге Excel остаются без изменений.

#### Вопрос: Могу ли я использовать эту функцию с другими форматами файлов Excel?

О: Да, вы можете использовать эту функцию с другими форматами файлов Excel, поддерживаемыми Aspose.Cells, такими как .xls, .xlsm и т. д.