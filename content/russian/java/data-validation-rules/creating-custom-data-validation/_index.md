---
title: Создание пользовательской проверки данных
linktitle: Создание пользовательской проверки данных
second_title: Aspose.Cells API обработки Java Excel
description: Узнайте, как создать собственную проверку данных с помощью Aspose.Cells для Java. Пошаговое руководство с исходным кодом.
type: docs
weight: 10
url: /ru/java/data-validation-rules/creating-custom-data-validation/
---

## Введение

Проверка данных помогает поддерживать целостность данных, не позволяя пользователям вводить неправильные или недействительные данные в электронные таблицы Excel. Хотя Excel предлагает встроенные параметры проверки данных, существуют сценарии, в которых вам необходимо определить собственные правила проверки. Aspose.Cells for Java позволяет вам эффективно добиться этого.

## Предварительные условия

Прежде чем углубляться в код, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.Cells для Java: загрузите и установите библиотеку с сайта[здесь](https://releases.aspose.com/cells/java/).

## Шаг 1. Настройка вашего Java-проекта

Для начала создайте новый проект Java в предпочитаемой вами интегрированной среде разработки (IDE). Добавьте библиотеку Aspose.Cells for Java в путь к классам вашего проекта.

## Шаг 2. Создание книги Excel

Начнем с создания новой книги Excel с использованием Aspose.Cells для Java.

```java
// Код Java для создания новой книги Excel
Workbook workbook = new Workbook();
```

## Шаг 3. Добавление рабочего листа

Теперь давайте добавим лист в книгу, где мы применим нашу пользовательскую проверку данных.

```java
// Java-код для добавления листа
Worksheet worksheet = workbook.getWorksheets().get(0);
```

## Шаг 4. Определение пользовательских критериев проверки

На этом этапе мы определим пользовательские критерии проверки, которым должны соответствовать наши данные. Допустим, мы хотим ограничить возраст, введенный в ячейку, диапазоном от 18 до 60 лет.

```java
// Код Java для определения пользовательских критериев проверки
Validation validation = worksheet.getValidations().add();
validation.setType(ValidationType.WHOLE);
validation.setOperator(OperatorType.BETWEEN);
validation.setFormula1("18");
validation.setFormula2("60");
validation.setShowError(true);
validation.setAlertStyle(ValidationAlertType.STOP);
validation.setErrorTitle("Invalid Age");
validation.setErrorMessage("Age must be between 18 and 60.");
```

## Шаг 5. Применение проверки данных к диапазону

Теперь, когда мы определили наши пользовательские критерии проверки, давайте применим их к определенному диапазону ячеек.

```java
// Код Java для применения проверки данных к диапазону
CellArea area = new CellArea();
area.startRow = 0;
area.startColumn = 0;
area.endRow = 9; // Применить проверку к первым десяти строкам
area.endColumn = 0;

validation.addArea(area);
```

## Шаг 6. Сохранение файла Excel

Наконец, сохраните файл Excel с примененными пользовательскими правилами проверки данных.

```java
// Java-код для сохранения файла Excel
workbook.save("CustomDataValidation.xlsx");
```

## Заключение

В этом руководстве мы рассмотрели, как создавать собственные правила проверки данных с помощью Aspose.Cells для Java. Выполнив эти шаги, вы можете гарантировать, что ваши данные Excel соответствуют определенным критериям, повышая целостность и точность данных.

## Часто задаваемые вопросы

### Как загрузить Aspose.Cells для Java?

 Вы можете скачать Aspose.Cells для Java с сайта по адресу[здесь](https://releases.aspose.com/cells/java/).

### Могу ли я применить пользовательскую проверку данных к нескольким диапазонам на одном листе?

Да, вы можете применить пользовательскую проверку данных к нескольким диапазонам на одном листе, повторяя шаг 5 для каждого желаемого диапазона.

### Существуют ли другие типы проверки данных, поддерживаемые Aspose.Cells для Java?

Да, Aspose.Cells для Java поддерживает различные типы проверки данных, включая целые числа, десятичные числа, дату, время, длину текста и многое другое.

### Как настроить сообщение об ошибке, отображаемое при сбое проверки данных?

 Вы можете настроить сообщение об ошибке, изменив`setErrorMessage` метод на шаге 4, где вы определяете критерии проверки.

### Работает ли Aspose.Cells for Java с файлами Excel в разных форматах?

Да, Aspose.Cells для Java поддерживает широкий спектр форматов файлов Excel, включая XLS, XLSX, XLSM и другие.