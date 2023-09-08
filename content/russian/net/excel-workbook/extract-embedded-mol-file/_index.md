---
title: Извлечь встроенный файл Mol
linktitle: Извлечь встроенный файл Mol
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как легко извлечь внедренные файлы MOL из книги Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 90
url: /ru/net/excel-workbook/extract-embedded-mol-file/
---
В этом уроке мы шаг за шагом покажем вам, как извлечь внедренный файл MOL из книги Excel с помощью библиотеки Aspose.Cells для .NET. Вы научитесь просматривать листы книги, извлекать соответствующие объекты OLE и сохранять извлеченные файлы MOL. Выполните следующие действия, чтобы успешно выполнить эту задачу.

## Шаг 1. Определите исходный и выходной каталоги.
Во-первых, нам нужно определить исходный и выходной каталоги в нашем коде. Эти каталоги указывают, где находится исходная книга Excel и где будут сохранены извлеченные файлы MOL. Вот соответствующий код:

```csharp
// Каталоги
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Обязательно укажите соответствующие пути по мере необходимости.

## Шаг 2. Загрузка книги Excel
Следующим шагом является загрузка книги Excel, содержащей внедренные объекты OLE и файлы MOL. Вот код для загрузки книги:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Обязательно правильно укажите имя исходного файла в коде.

## Шаг 3. Просмотрите листы и извлеките файлы MOL.
Теперь мы пройдемся по каждому листу книги и извлечем соответствующие объекты OLE, содержащие файлы MOL. Вот соответствующий код:

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

Этот код проходит по каждому листу книги, извлекает объекты OLE и сохраняет извлеченные файлы MOL в выходной каталог.

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
Поздравляем! Вы узнали, как извлечь внедренный файл MOL из книги Excel с помощью Aspose.Cells для .NET. Теперь вы можете применить эти знания для извлечения файлов MOL из ваших собственных книг Excel. Не стесняйтесь продолжить изучение библиотеки Aspose.Cells и узнать о других ее мощных функциях.

### Часто задаваемые вопросы

#### Вопрос: Что такое файл MOL?
 
Ответ: Файл MOL — это формат файла, используемый для представления химических структур в вычислительной химии. Он содержит информацию об атомах, связях и других молекулярных свойствах.

#### Вопрос: Этот метод работает со всеми типами файлов Excel?

О: Да, этот метод работает со всеми типами файлов Excel, поддерживаемыми Aspose.Cells.

#### Вопрос: Могу ли я извлечь несколько файлов MOL одновременно?

О: Да, вы можете извлечь несколько файлов MOL одновременно, перебирая объекты OLE на каждом листе книги.