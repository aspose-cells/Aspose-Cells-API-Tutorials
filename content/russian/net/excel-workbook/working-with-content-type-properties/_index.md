---
title: Работа со свойствами типа контента
linktitle: Работа со свойствами типа контента
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как работать со свойствами типа контента с помощью Aspose.Cells для .NET.
type: docs
weight: 180
url: /ru/net/excel-workbook/working-with-content-type-properties/
---
Свойства типа контента играют жизненно важную роль в управлении файлами Excel и манипулировании ими с использованием библиотеки Aspose.Cells для .NET. Эти свойства позволяют определять дополнительные метаданные для файлов Excel, упрощая организацию и поиск данных. В этом руководстве мы шаг за шагом покажем вам, как понять свойства типа контента и работать с ними, используя пример кода C#.

## Предварительные условия

Прежде чем начать, убедитесь, что у вас есть следующее:

- Aspose.Cells для .NET установлен на вашей машине разработки.
- Интегрированная среда разработки (IDE), совместимая с C#, например Visual Studio.

## Шаг 1. Настройка среды

Прежде чем приступить к работе со свойствами типа контента, убедитесь, что вы настроили свою среду разработки с помощью Aspose.Cells для .NET. Вы можете добавить ссылку на библиотеку Aspose.Cells в свой проект и импортировать необходимое пространство имен в свой класс.

```csharp
using Aspose.Cells;
```

## Шаг 2. Создание новой книги Excel

 Сначала мы создадим новую книгу Excel, используя`Workbook`класс, предоставленный Aspose.Cells. Следующий код показывает, как создать новую книгу Excel и сохранить ее в указанном выходном каталоге.

```csharp
// Каталог назначения
string outputDir = RunExamples.Get_OutputDirectory();

// Создайте новую книгу Excel
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## Шаг 3. Добавление свойств типа контента

 Теперь, когда у нас есть книга Excel, мы можем добавить свойства типа контента, используя`Add` метод`ContentTypeProperties` коллекция`Workbook` сорт. Каждое свойство представлено именем и значением. ТЫ

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

 После добавления свойств типа контента мы можем сохранить книгу Excel с изменениями. Использовать`Save` метод`Workbook` class, чтобы указать выходной каталог и имя файла.

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

Поздравляем! Вы узнали, как работать со свойствами типа контента с помощью Aspose.Cells для .NET. Теперь вы можете добавлять собственные метаданные в файлы Excel и управлять ими более эффективно.

### Часто задаваемые вопросы

#### Вопрос. Совместимы ли свойства типа контента со всеми версиями Excel?

О: Да, свойства типа контента совместимы с файлами Excel, созданными во всех версиях Excel.

#### Вопрос: Могу ли я редактировать свойства типа контента после добавления их в книгу Excel?

 О: Да, вы можете изменить свойства типа контента в любое время, перейдя в`ContentTypeProperties` коллекция`Workbook` class и используя методы и p соответствующие свойства.

#### Вопрос: Поддерживаются ли свойства типа контента при сохранении в PDF?

О: Нет, свойства типа контента не поддерживаются при сохранении в PDF. Они специфичны для файлов Excel.