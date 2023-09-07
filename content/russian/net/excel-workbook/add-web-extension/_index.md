---
title: Добавить веб-расширение
linktitle: Добавить веб-расширение
second_title: Справочник по Aspose.Cells для .NET API
description: Легко добавляйте веб-расширение в свои книги Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 40
url: /ru/net/excel-workbook/add-web-extension/
---
В этом пошаговом руководстве мы объясним предоставленный исходный код C#, который позволит вам добавить веб-расширение с помощью Aspose.Cells для .NET. Выполните следующие действия, чтобы добавить веб-расширение в книгу Excel.

## Шаг 1: Установите выходной каталог

```csharp
// Выходной каталог
string outDir = RunExamples.Get_OutputDirectory();
```

На этом первом шаге мы определяем выходной каталог, в котором будет сохранена измененная книга Excel.

## Шаг 2. Создайте новую книгу

```csharp
//Создать новую книгу
Workbook workbook = new Workbook();
```

 Здесь мы создаем новую книгу Excel, используя`Workbook` класс из Aspose.Cells.

## Шаг 3. Получите доступ к коллекции веб-расширений

```csharp
// Получите доступ к коллекции веб-расширений
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Мы получаем доступ к коллекции веб-расширений книги Excel, используя`WebExtensions` собственность`Worksheets` объект.

## Шаг 4. Добавьте новое веб-расширение

```csharp
// Добавить новое веб-расширение
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Мы добавляем новое веб-расширение в коллекцию расширений. Мы определяем идентификатор ссылки, имя хранилища и тип хранилища расширения.

## Шаг 5. Получите доступ к коллекции панели задач веб-расширения

```csharp
// Доступ к коллекции панели задач веб-расширения
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Мы получаем доступ к коллекции областей задач веб-расширения рабочей книги Excel, используя`WebExtensionTaskPanes` собственность`Worksheets` объект.

## Шаг 6. Добавьте новую область задач

```csharp
// Добавить новую область задач
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Мы добавляем новую панель задач в коллекцию панелей задач. Мы устанавливаем видимость панели, ее состояние закрепления и связанное веб-расширение.

## Шаг 7: Сохраните и закройте книгу

```csharp
// Сохраните и закройте книгу
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Мы сохраняем измененную книгу в указанный выходной каталог, а затем закрываем ее.

### Пример исходного кода для добавления веб-расширения с использованием Aspose.Cells для .NET 
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

Поздравляем! Теперь вы узнали, как добавить веб-расширение с помощью Aspose.Cells для .NET. Поэкспериментируйте с кодом и изучите дополнительные функции Aspose.Cells, чтобы получить максимальную отдачу от управления веб-расширениями в ваших книгах Excel.

## Часто задаваемые вопросы

#### Вопрос. Что такое веб-расширение в книге Excel?

Ответ. Веб-расширение в рабочей книге Excel — это компонент, который позволяет добавлять в Excel дополнительные функции за счет интеграции веб-приложений. Он может предлагать интерактивные функции, настраиваемые информационные панели, внешние интеграции и многое другое.

#### В: Как добавить веб-расширение в книгу Excel с помощью Aspose.Cells?

 О: Чтобы добавить веб-расширение в книгу Excel с помощью Aspose.Cells, выполните действия, описанные в нашем пошаговом руководстве. Использовать`WebExtensionCollection` и`WebExtensionTaskPaneCollection` классы для добавления и настройки веб-расширения и связанной панели задач.

#### Вопрос. Какая информация требуется для добавления веб-расширения?

О. При добавлении веб-расширения необходимо указать идентификатор SKU расширения, имя и тип магазина. Эта информация помогает правильно определить и загрузить расширение.

#### Вопрос. Можно ли добавить несколько веб-расширений в одну книгу Excel?

 О: Да, вы можете добавить несколько веб-расширений в одну книгу Excel. Использовать`Add` метод коллекции веб-расширений, чтобы добавить каждое расширение, а затем связать их с соответствующими областями задач.