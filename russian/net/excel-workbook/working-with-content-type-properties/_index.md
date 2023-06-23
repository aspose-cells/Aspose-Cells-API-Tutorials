---
title: Работа со свойствами типа контента
linktitle: Работа со свойствами типа контента
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как работать со свойствами типа контента с помощью Aspose.Cells для .NET.
type: docs
weight: 180
url: /ru/net/excel-workbook/working-with-content-type-properties/
---
Свойства типа содержимого играют жизненно важную роль в управлении файлами Excel и манипулировании ими с помощью библиотеки Aspose.Cells для .NET. Эти свойства позволяют определить дополнительные метаданные для файлов Excel, упрощая организацию и поиск данных. В этом руководстве мы пошагово познакомим вас со свойствами типа контента и поработаем с ними, используя пример кода C#.

## Предпосылки

Прежде чем начать, убедитесь, что у вас есть следующее:

- Aspose.Cells for .NET установлен на вашем компьютере для разработки.
- Интегрированная среда разработки (IDE), совместимая с C#, например Visual Studio.

## Шаг 1. Настройка среды

Прежде чем приступить к работе со свойствами типа контента, убедитесь, что вы настроили среду разработки с помощью Aspose.Cells для .NET. Вы можете добавить ссылку на библиотеку Aspose.Cells в свой проект и импортировать необходимое пространство имен в свой класс.

```csharp
using Aspose.Cells;
```

## Шаг 2. Создание новой книги Excel

 Сначала мы создадим новую книгу Excel, используя`Workbook`класс, предоставленный Aspose.Cells. В следующем коде показано, как создать новую книгу Excel и сохранить ее в указанном выходном каталоге.

```csharp
// Целевой каталог
string outputDir = RunExamples.Get_OutputDirectory();

// Создать новую книгу Excel
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## Шаг 3: Добавление свойств типа контента

 Теперь, когда у нас есть рабочая книга Excel, мы можем добавить свойства типа контента с помощью`Add` метод`ContentTypeProperties` коллекция`Workbook` сорт. Каждое свойство представлено именем и значением. ТЫ

  Вы также можете указать тип данных свойства.

```csharp
// Добавьте первое свойство типа контента
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// Добавьте второе свойство типа контента
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## Шаг 4. Сохранение книги Excel

 После добавления свойств типа контента мы можем сохранить книгу Excel с изменениями. Использовать`Save` метод`Workbook` класс, чтобы указать выходной каталог и имя файла.

```csharp
// Сохраните книгу Excel
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### Пример исходного кода для работы со свойствами типа контента с использованием Aspose.Cells для .NET 
```csharp
//исходный каталог
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## Заключение

Поздравляем! Вы узнали, как работать со свойствами типа контента, используя Aspose.Cells для .NET. Теперь вы можете добавлять собственные метаданные в файлы Excel и более эффективно управлять ими.

### Часто задаваемые вопросы

#### Вопрос. Совместимы ли свойства типа содержимого со всеми версиями Excel?

О: Да, свойства типа содержимого совместимы с файлами Excel, созданными во всех версиях Excel.

#### Вопрос. Можно ли изменить свойства типа контента после их добавления в книгу Excel?

 О: Да, вы можете изменить свойства типа контента в любое время, перейдя в`ContentTypeProperties` коллекция`Workbook` class и с помощью соответствующих свойств методов и p.

#### В: Поддерживаются ли свойства типа содержимого при сохранении в PDF?

О: Нет, свойства типа содержимого не поддерживаются при сохранении в PDF. Они специфичны для файлов Excel.