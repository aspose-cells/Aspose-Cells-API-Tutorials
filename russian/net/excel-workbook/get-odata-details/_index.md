---
title: Получить сведения об Одате
linktitle: Получить сведения об Одате
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как получить данные OData из книги Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 110
url: /ru/net/excel-workbook/get-odata-details/
---
Использование OData распространено, когда речь идет о получении структурированных данных из внешних источников данных. С Aspose.Cells для .NET вы можете легко получить данные OData из книги Excel. Выполните следующие шаги, чтобы получить желаемые результаты:

## Шаг 1: Укажите исходный каталог

Во-первых, вам нужно указать исходный каталог, в котором находится файл Excel, содержащий данные OData. Вот как это сделать с помощью Aspose.Cells:

```csharp
// исходный каталог
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Шаг 2. Загрузите книгу

Как только исходный каталог указан, вы можете загрузить книгу Excel из файла. Вот пример кода:

```csharp
// Загрузите книгу
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## Шаг 3. Получите сведения об OData

После загрузки книги вы можете получить доступ к сведениям OData с помощью коллекции PowerQueryFormulas. Вот как:

```csharp
// Получить коллекцию формул Power Query
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Пройдитесь по каждой формуле Power Query
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Получить коллекцию элементов формулы Power Query.
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Итерация по каждому элементу формулы Power Query
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Пример исходного кода для получения сведений об Odata с использованием Aspose.Cells для .NET 
```csharp
// исходный каталог
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## Заключение

Получить данные OData из книги Excel теперь легко с помощью Aspose.Cells для .NET. Следуя шагам, описанным в этом руководстве, вы сможете эффективно получать доступ к данным OData и обрабатывать их. Поэкспериментируйте со своими собственными файлами Excel, содержащими данные OData, и получите максимальную отдачу от этой мощной функции.

### Часто задаваемые вопросы

#### В: Поддерживает ли Aspose.Cells другие источники данных помимо OData?
    
О: Да, Aspose.Cells поддерживает несколько источников данных, таких как базы данных SQL, файлы CSV, веб-сервисы и т. д.

#### Вопрос: Как я могу использовать полученные данные OData в своем приложении?
    
О: После того, как вы получили данные OData с помощью Aspose.Cells, вы можете использовать их для анализа данных, создания отчетов или любых других манипуляций в своем приложении.

#### Вопрос. Можно ли фильтровать или сортировать данные OData при извлечении с помощью Aspose.Cells?
    
О: Да, Aspose.Cells предлагает расширенные функции для фильтрации, сортировки и обработки данных OData в соответствии с вашими конкретными потребностями.

#### Вопрос. Можно ли автоматизировать процесс получения данных OData с помощью Aspose.Cells?
    
О: Да, вы можете автоматизировать процесс получения данных OData, интегрировав Aspose.Cells в свои рабочие процессы или используя сценарии программирования.