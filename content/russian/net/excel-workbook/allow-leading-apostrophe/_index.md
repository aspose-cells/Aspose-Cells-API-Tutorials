---
title: Разрешить начальный апостроф
linktitle: Разрешить начальный апостроф
second_title: Справочник по Aspose.Cells для .NET API
description: Разрешить начальный апостроф в книгах Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 60
url: /ru/net/excel-workbook/allow-leading-apostrophe/
---
В этом пошаговом руководстве мы объясним предоставленный исходный код C#, который позволит вам разрешить использование начального апострофа в книге Excel с помощью Aspose.Cells для .NET. Выполните следующие шаги, чтобы выполнить эту операцию.

## Шаг 1: Установите исходный и выходной каталоги

```csharp
// исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
// Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
```

На этом первом шаге мы определяем исходные и выходные каталоги для файлов Excel.

## Шаг 2. Создайте экземпляр объекта WorkbookDesigner.

```csharp
// Создание экземпляра объекта WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Мы создаем экземпляр`WorkbookDesigner` класс из Aspose.Cells.

## Шаг 3: Загрузите книгу Excel

```csharp
//Загрузите книгу Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Загружаем книгу Excel из указанного файла и отключаем автоматическое преобразование начальных апострофов в стиль текста.

## Шаг 4: Установите источник данных

```csharp
// Определите источник данных для книги конструктора
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

## Шаг 5. Обработайте смарт-маркеры

```csharp
// Обработка интеллектуальных маркеров
designer. Process();
```

 Мы используем`Process` способ обработки смарт-маркеров в рабочей книге дизайнера.

## Шаг 6. Сохраните измененную книгу Excel.

```csharp
// Сохраните измененную книгу Excel.
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Сохраняем измененную книгу Excel с внесенными изменениями.

### Пример исходного кода для разрешения начального апострофа с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Создание экземпляра объекта WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Откройте электронную таблицу конструктора, содержащую смарт-маркеры.
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
// Установите источник данных для электронной таблицы конструктора
designer.SetDataSource("sampleData", list);
// Обработка смарт-маркеров
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Заключение

Поздравляем! Вы узнали, как разрешить использование начального апострофа в книге Excel с помощью Aspose.Cells для .NET. Поэкспериментируйте с собственными данными, чтобы дополнительно настроить книги Excel.

### Часто задаваемые вопросы

#### Вопрос. Что такое разрешение начального апострофа в книге Excel?

A: Разрешение начального апострофа в рабочей книге Excel позволяет правильно отображать данные, начинающиеся с апострофа, без преобразования их в текстовый стиль. Это полезно, когда вы хотите сохранить апостроф как часть данных.

#### Q: Почему мне нужно отключить автоматическое преобразование начальных апострофов?

О: Отключив автоматическое преобразование ведущих кавычек, вы можете сохранить их использование в ваших данных. Это позволяет избежать любого непреднамеренного изменения данных при открытии или манипулировании книгой Excel.

#### В: Как установить источник данных в книге дизайнера?

 A: Чтобы установить источник данных в книге дизайнера, вы можете использовать`SetDataSource` метод, указывающий имя источника данных и список соответствующих объектов данных.

#### В: Влияет ли разрешение начального апострофа на другие данные в книге Excel?

О: Нет, разрешение начального апострофа влияет только на данные, начинающиеся с апострофа. Другие данные в книге Excel остаются без изменений.

#### В: Могу ли я использовать эту функцию с другими форматами файлов Excel?

О: Да, вы можете использовать эту функцию с другими форматами файлов Excel, поддерживаемыми Aspose.Cells, такими как .xls, .xlsm и т. д.