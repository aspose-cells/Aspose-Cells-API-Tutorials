---
title: Извлечь встроенный файл MOL
linktitle: Извлечь встроенный файл MOL
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как легко извлечь встроенные файлы MOL из книги Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 90
url: /ru/net/excel-workbook/extract-embedded-mol-file/
---
В этом руководстве мы пошагово расскажем, как извлечь встроенный файл MOL из книги Excel с помощью библиотеки Aspose.Cells для .NET. Вы узнаете, как просматривать листы рабочей книги, извлекать соответствующие объекты OLE и сохранять извлеченные файлы MOL. Выполните следующие действия, чтобы успешно выполнить эту задачу.

## Шаг 1: Определите исходный и выходной каталоги
Во-первых, нам нужно определить исходный и выходной каталоги в нашем коде. Эти каталоги указывают, где находится исходная книга Excel и где будут сохранены извлеченные файлы MOL. Вот соответствующий код:

```csharp
// Каталоги
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

При необходимости обязательно укажите соответствующие пути.

## Шаг 2. Загрузка книги Excel
Следующим шагом является загрузка рабочей книги Excel, содержащей встроенные объекты OLE и файлы MOL. Вот код для загрузки книги:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Убедитесь, что в коде правильно указано имя исходного файла.

## Шаг 3. Просмотрите листы и извлеките файлы MOL.
Теперь мы пройдемся по каждому листу рабочей книги и извлечем соответствующие объекты OLE, которые содержат файлы MOL. Вот соответствующий код:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Этот код перебирает каждый лист в рабочей книге, извлекает объекты OLE и сохраняет извлеченные файлы MOL в выходной каталог.

### Пример исходного кода для извлечения встроенного файла Mol с использованием Aspose.Cells для .NET 
```csharp
//каталоги
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Заключение
Поздравляем! Вы узнали, как извлечь встроенный файл MOL из книги Excel с помощью Aspose.Cells для .NET. Теперь вы можете применить эти знания для извлечения файлов MOL из ваших собственных книг Excel. Вы можете продолжить изучение библиотеки Aspose.Cells и узнать о других ее мощных функциях.

### Часто задаваемые вопросы

#### В: Что такое файл MOL?
 
A: Файл MOL — это формат файла, используемый для представления химических структур в вычислительной химии. Он содержит информацию об атомах, связях и других молекулярных свойствах.

#### В: Этот метод работает со всеми типами файлов Excel?

О: Да, этот метод работает со всеми типами файлов Excel, поддерживаемыми Aspose.Cells.

#### В: Могу ли я извлечь сразу несколько файлов MOL?

О: Да, вы можете одновременно извлечь несколько файлов MOL, перебирая объекты OLE на каждом листе рабочей книги.