---
title: Добавить веб-расширение
linktitle: Добавить веб-расширение
second_title: Справочник по API Aspose.Cells для .NET
description: Легко добавляйте веб-расширения в свои книги Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 40
url: /ru/net/excel-workbook/add-web-extension/
---
В этом пошаговом руководстве мы объясним предоставленный исходный код C#, который позволит вам добавить веб-расширение с помощью Aspose.Cells для .NET. Выполните следующие действия, чтобы добавить веб-расширение в книгу Excel.

## Шаг 1. Установите выходной каталог.

```csharp
// Выходной каталог
string outDir = RunExamples.Get_OutputDirectory();
```

На этом первом этапе мы определяем выходной каталог, в котором будет сохранена измененная книга Excel.

## Шаг 2. Создайте новую книгу

```csharp
// Создать новую книгу
Workbook workbook = new Workbook();
```

Здесь мы создаем новую книгу Excel, используя`Workbook` класс из Aspose.Cells.

## Шаг 3. Доступ к коллекции веб-расширений

```csharp
// Доступ к коллекции веб-расширений
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Мы получаем доступ к коллекции веб-расширений книги Excel с помощью`WebExtensions` собственность`Worksheets` объект.

## Шаг 4. Добавьте новое веб-расширение

```csharp
// Добавить новое веб-расширение
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Мы добавляем новое веб-расширение в коллекцию расширений. Мы определяем идентификатор ссылки, имя магазина и тип магазина расширения.

## Шаг 5. Доступ к коллекции панели задач веб-расширения

```csharp
// Доступ к коллекции панели задач веб-расширения.
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Мы получаем доступ к коллекции панелей задач веб-расширения книги Excel с помощью`WebExtensionTaskPanes` собственность`Worksheets` объект.

## Шаг 6. Добавьте новую панель задач.

```csharp
// Добавить новую панель задач
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Мы добавляем новую область задач в коллекцию панелей задач. Мы устанавливаем видимость панели, ее состояние закрепления и соответствующее веб-расширение.

## Шаг 7. Сохраните и закройте книгу.

```csharp
// Сохраните и закройте книгу
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Мы сохраняем измененную книгу в указанном выходном каталоге, а затем закрываем ее.

### Пример исходного кода для добавления веб-расширения с помощью Aspose.Cells для .NET 
```csharp
//Исходный каталог
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Заключение

Поздравляем! Теперь вы узнали, как добавить веб-расширение с помощью Aspose.Cells для .NET. Поэкспериментируйте с кодом и изучите дополнительные возможности Aspose.Cells, чтобы получить максимальную отдачу от управления веб-расширениями в книгах Excel.

## Часто задаваемые вопросы

#### Вопрос: Что такое веб-расширение в книге Excel?

О: Веб-расширение в книге Excel — это компонент, который позволяет добавлять в Excel дополнительные функции путем интеграции веб-приложений. Он может предлагать интерактивные функции, настраиваемые информационные панели, внешнюю интеграцию и многое другое.

#### Вопрос: Как добавить веб-расширение в книгу Excel с помощью Aspose.Cells?

 О: Чтобы добавить веб-расширение в книгу Excel с помощью Aspose.Cells, вы можете выполнить действия, описанные в нашем пошаговом руководстве. Использовать`WebExtensionCollection` и`WebExtensionTaskPaneCollection` классы для добавления и настройки веб-расширения и связанной с ним области задач.

#### Вопрос: Какая информация необходима для добавления веб-расширения?

О: При добавлении веб-расширения вы должны указать идентификатор SKU расширения, название и тип магазина. Эта информация помогает правильно идентифицировать и загрузить расширение.

#### Вопрос: Могу ли я добавить несколько веб-расширений в одну книгу Excel?

 О: Да, вы можете добавить несколько веб-расширений в одну книгу Excel. Использовать`Add` метод коллекции веб-расширений, чтобы добавить каждое расширение, а затем связать их с соответствующими панелями задач.