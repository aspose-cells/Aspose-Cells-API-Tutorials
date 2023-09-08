---
title: Обновление элемента формулы Power Query
linktitle: Обновление элемента формулы Power Query
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как обновить элементы формулы Power Query в файлах Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 160
url: /ru/net/excel-workbook/update-power-query-formula-item/
---
Обновление элемента формулы Power Query — обычная операция при работе с данными в файлах Excel. С помощью Aspose.Cells для .NET вы можете легко обновить элемент формулы Power Query, выполнив следующие действия:

## Шаг 1. Укажите исходный и выходной каталоги.

Сначала вам необходимо указать исходный каталог, в котором находится файл Excel, содержащий обновляемые формулы Power Query, а также выходной каталог, в котором вы хотите сохранить измененный файл. Вот как это сделать с помощью Aspose.Cells:

```csharp
// исходный каталог
string SourceDir = RunExamples.Get_SourceDirectory();

// Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
```

## Шаг 2. Загрузите исходную книгу Excel.

Затем вам необходимо загрузить исходную книгу Excel, в которой вы хотите обновить элемент формулы Power Query. Вот как это сделать:

```csharp
// Загрузите исходную книгу Excel
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Шаг 3. Просмотр и обновление элементов формулы Power Query

После загрузки книги вы можете перейти к коллекции формул Power Query и просмотреть каждую формулу и ее элементы. В этом примере мы ищем элемент формулы с именем «Источник» и обновляем его значение. Вот пример кода для обновления элемента формулы Power Query:

```csharp
// Доступ к коллекции формул Power Query
DataMashup mashupData = workbook.DataMashup;

// Перебирать формулы Power Query и их элементы.
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Шаг 4. Сохраните выходную книгу Excel.

После обновления элемента формулы Power Query вы можете сохранить измененную книгу Excel в указанном выходном каталоге. Вот как это сделать:

```csharp
// Сохраните выходную книгу Excel.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Пример исходного кода для обновления элемента формулы Power Query с использованием Aspose.Cells для .NET 
```csharp
// Рабочие каталоги
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Сохраните выходную книгу.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Заключение

Обновление элементов формулы Power Query — важная операция при использовании Aspose.Cells для манипулирования и обработки данных в файлах Excel. Следуя инструкциям выше, вы можете легко обновить элементы формулы.

### Часто задаваемые вопросы

#### Вопрос: Что такое Power Query в Excel?
     
Ответ: Power Query — это функция Excel, которая помогает собирать, преобразовывать и загружать данные из разных источников. Он предлагает мощные инструменты для очистки, объединения и изменения данных перед их импортом в Excel.

#### Вопрос: Как узнать, был ли успешно обновлен элемент формулы Power Query?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Вопрос: Могу ли я обновить несколько элементов формулы Power Query одновременно?
    
О: Да, вы можете просмотреть коллекцию элементов формулы Power Query и обновить несколько элементов за один цикл, в зависимости от ваших конкретных потребностей.

#### Вопрос: Есть ли другие операции, которые я могу выполнять с формулами Power Query с помощью Aspose.Cells?
    
О: Да, Aspose.Cells предлагает полный набор функций для работы с формулами Power Query, включая создание, удаление, копирование и поиск формул в книге Excel.