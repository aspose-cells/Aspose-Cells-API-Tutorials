---
title: Получить подробную информацию об Odata
linktitle: Получить подробную информацию об Odata
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как получить данные OData из книги Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 110
url: /ru/net/excel-workbook/get-odata-details/
---
Использование OData широко распространено, когда речь идет о получении структурированных данных из внешних источников данных. С помощью Aspose.Cells для .NET вы можете легко получить данные OData из книги Excel. Выполните следующие шаги, чтобы получить желаемые результаты:

## Шаг 1. Укажите исходный каталог.

Сначала вам необходимо указать исходный каталог, в котором находится файл Excel, содержащий сведения об OData. Вот как это сделать с помощью Aspose.Cells:

```csharp
// исходный каталог
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Шаг 2. Загрузите книгу

После указания исходного каталога вы можете загрузить книгу Excel из файла. Вот пример кода:

```csharp
// Загрузите книгу
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## Шаг 3. Получите сведения об OData

После загрузки книги вы можете получить доступ к сведениям OData с помощью коллекции PowerQueryFormulas. Вот как:

```csharp
// Получение коллекции формул Power Query.
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Ознакомьтесь с каждой формулой Power Query.
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Получение коллекции элементов формулы Power Query.
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Перебрать каждый элемент формулы Power Query.
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Пример исходного кода для получения сведений об Odata с помощью Aspose.Cells для .NET 
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

Извлечение данных OData из книги Excel теперь стало проще с помощью Aspose.Cells для .NET. Выполнив шаги, описанные в этом руководстве, вы сможете эффективно получать доступ к данным OData и обрабатывать их. Поэкспериментируйте с собственными файлами Excel, содержащими сведения об OData, и получите максимальную отдачу от этой мощной функции.

### Часто задаваемые вопросы

#### Вопрос: Поддерживает ли Aspose.Cells другие источники данных помимо OData?
    
О: Да, Aspose.Cells поддерживает несколько источников данных, таких как базы данных SQL, файлы CSV, веб-сервисы и т. д.

#### Вопрос: Как я могу использовать полученные данные OData в своем приложении?
    
О: После того, как вы получили данные OData с помощью Aspose.Cells, вы можете использовать их для анализа данных, создания отчетов или любых других манипуляций в вашем приложении.

#### Вопрос: Могу ли я фильтровать или сортировать данные OData при получении с помощью Aspose.Cells?
    
О: Да, Aspose.Cells предлагает расширенные функции для фильтрации, сортировки и управления данными OData в соответствии с вашими конкретными потребностями.

#### Вопрос: Могу ли я автоматизировать процесс получения сведений об OData с помощью Aspose.Cells?
    
О: Да, вы можете автоматизировать процесс получения сведений об OData, интегрировав Aspose.Cells в свои рабочие процессы или используя сценарии программирования.