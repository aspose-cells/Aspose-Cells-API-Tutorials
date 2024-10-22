---
title: Добавить поле со списком на рабочий лист в Excel
linktitle: Добавить поле со списком на рабочий лист в Excel
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как добавить поле со списком в лист Excel программным способом с помощью Aspose.Cells для .NET. Это пошаговое руководство проведет вас через каждую деталь.
type: docs
weight: 21
url: /ru/net/excel-shapes-controls/add-combo-box-to-worksheet-excel/
---
## Введение
Создание интерактивных электронных таблиц Excel может значительно улучшить пользовательский опыт, особенно при добавлении элементов формы, таких как поля со списком. Поля со списком позволяют пользователям выбирать параметры из предопределенного списка, что добавляет простоту и эффективность вводу данных. С Aspose.Cells для .NET вы можете программно создавать поля со списком в таблицах Excel без использования Excel напрямую. Эта мощная библиотека позволяет разработчикам манипулировать файлами Excel различными способами, включая возможность автоматизировать элементы управления формами.
В этом уроке мы проведем вас через процесс добавления поля со списком на лист в Excel с помощью Aspose.Cells для .NET. Если вы хотите создавать динамические, удобные для пользователя электронные таблицы, это руководство поможет вам начать.
## Предпосылки
Прежде чем погрузиться в код, давайте убедимся, что у вас есть все необходимое:
- Aspose.Cells для .NET: Загрузите и установите библиотеку Aspose.Cells для .NET с сайта[страница загрузки](https://releases.aspose.com/cells/net/).
- .NET Framework: Убедитесь, что на вашем компьютере установлен .NET Framework. Подойдет любая версия, поддерживаемая Aspose.Cells.
- Среда разработки: используйте IDE, например Visual Studio, для управления проектом и написания кода.
-  Лицензия Aspose: Вы можете работать без лицензии в ознакомительном режиме, но для полной версии вам необходимо применить лицензию. Получить[временная лицензия](https://purchase.aspose.com/temporary-license/) если необходимо.
## Импортные пакеты
Для начала вам нужно импортировать требуемые пространства имен в ваш проект. Вот что вам нужно:
```csharp
using System.IO;
using Aspose.Cells;
```
Они необходимы для взаимодействия с файлами Excel и управления элементами формы, такими как поля со списками в рабочей книге.
Давайте разберем процесс добавления поля со списком на несколько простых шагов для простоты понимания.
## Шаг 1: Настройте каталог документов
Первый шаг — создать каталог, в котором будут сохраняться ваши файлы Excel. Вы можете создать новую папку, если она еще не существует.
```csharp
// Путь к каталогу документов.
string dataDir = "Your Document Directory";
//Создайте каталог, если его еще нет.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
- dataDir: Указывает место сохранения выходного файла.
- System.IO.Directory.Exists: проверяет, существует ли уже каталог.
- System.IO.Directory.CreateDirectory: Создает каталог, если он отсутствует.
## Шаг 2: Создайте новую рабочую книгу
Теперь создайте новую книгу Excel, в которую вы добавите поле со списком.

```csharp
// Создайте новую рабочую книгу.
Workbook workbook = new Workbook();
```

- Workbook workbook: Инициализирует новый экземпляр класса Workbook, представляющий файл Excel.
## Шаг 3: Получите рабочий лист и ячейки
Затем откройте первый рабочий лист рабочей книги и извлеките набор ячеек, в которые вы будете вводить данные.

```csharp
// Получите первый рабочий лист.
Worksheet sheet = workbook.Worksheets[0];
// Получите коллекцию ячеек рабочего листа.
Cells cells = sheet.Cells;
```

- Лист рабочего листа: извлекает первый рабочий лист из рабочей книги.
- Ячейки ячеек: Получает коллекцию ячеек с рабочего листа.
## Шаг 4: Введите значения для поля со списком
Теперь нам нужно ввести некоторые значения в ячейки. Эти значения будут служить параметрами для поля со списком.

```csharp
// Введите значение.
cells["B3"].PutValue("Employee:");
// Выделите его жирным шрифтом.
cells["B3"].GetStyle().Font.IsBold = true;
// Введите несколько значений, обозначающих диапазон ввода для поля со списком.
cells["A2"].PutValue("Emp001");
cells["A3"].PutValue("Emp002");
cells["A4"].PutValue("Emp003");
cells["A5"].PutValue("Emp004");
cells["A6"].PutValue("Emp005");
cells["A7"].PutValue("Emp006");
```

- клетки["B3"].PutValue: помещает метку "Сотрудник" в ячейку B3.
- Font.IsBold = true: делает текст жирным, чтобы он выделялся.
- Диапазон ввода: Вводит несколько идентификаторов сотрудников в ячейки от A2 до A7. Они появятся в раскрывающемся списке.
## Шаг 5: Добавьте поле со списком на рабочий лист
Следующий шаг — добавить элемент управления combo box на ваш рабочий лист. Этот combo box позволит пользователям выбрать один из идентификаторов сотрудников, которые вы ввели ранее.

```csharp
// Добавьте новое поле со списком.
Aspose.Cells.Drawing.ComboBox comboBox = sheet.Shapes.AddComboBox(2, 0, 2, 0, 22, 100);
```

- AddComboBox: добавляет новый комбинированный список на рабочий лист. Числа (2, 0, 2, 0, 22, 100) представляют положение и размеры комбинированного списка.
## Шаг 6: Свяжите поле со списком с ячейкой и задайте диапазон ввода
Чтобы сделать поле со списком функциональным, нам нужно связать его с определенной ячейкой и определить диапазон ячеек, из которых оно будет извлекать свои варианты.

```csharp
// Установите связанную ячейку.
comboBox.LinkedCell = "A1";
// Установите диапазон ввода.
comboBox.InputRange = "A2:A7";
```

- LinkedCell: Связывает выбор поля со списком с ячейкой A1. Выбранное значение из поля со списком появится в этой ячейке.
- InputRange: определяет диапазон ячеек (A2:A7), содержащий значения, которые будут заполнять параметры поля со списком.
## Шаг 7: Настройте внешний вид поля со списком
Вы можете дополнительно настроить поле со списком, указав количество раскрывающихся строк и включив 3D-затенение для улучшения эстетики.

```csharp
// Установите количество строк списка, отображаемых в списковой части поля со списком.
comboBox.DropDownLines = 5;
// Установите комбинированный список с 3-D затенением.
comboBox.Shadow = true;
```

- DropDownLines: управляет количеством вариантов, которые будут видны в раскрывающемся списке одновременно.
- Тень: добавляет эффект 3D-тени к полю со списком.
## Шаг 8: Автоматическая подгонка столбцов и сохранение книги
Наконец, давайте автоматически подгоним столбцы для создания аккуратного макета и сохраним книгу.

```csharp
// Автоподбор столбцов
sheet.AutoFitColumns();
// Сохраняет файл.
workbook.Save(dataDir + "book1.out.xls");
```

- AutoFitColumns: Автоматически регулирует ширину столбцов в соответствии с содержимым.
- Сохранить: сохраняет книгу как файл Excel в указанном каталоге.

## Заключение
Добавление поля со списком в рабочие листы Excel с помощью Aspose.Cells для .NET — это простой процесс, который значительно повышает гибкость ввода данных. Программно создавая элементы управления формами, вы можете легко создавать интерактивные электронные таблицы. В этом руководстве показано, как добавить поле со списком, связать его с ячейкой и настроить его диапазон ввода, используя Aspose.Cells.
 Aspose.Cells предоставляет широкий спектр функций для работы с файлами Excel, что делает его идеальным выбором для разработчиков, желающих автоматизировать задачи с электронными таблицами. Попробуйте его с[бесплатная пробная версия](https://releases.aspose.com/).
## Часто задаваемые вопросы
### Могу ли я использовать Aspose.Cells без установленного Excel?
Да, Aspose.Cells работает независимо от Excel и не требует установки Excel.
### Как применить лицензию в Aspose.Cells?
 Вы можете подать заявку на получение лицензии, получив ее у[здесь](https://purchase.aspose.com/buy) и звонок`License.SetLicense()` в вашем коде.
### Какие форматы сохранения файлов поддерживает Aspose.Cells?
Aspose.Cells поддерживает сохранение файлов в различных форматах, таких как XLSX, XLS, CSV, PDF и другие.
### Есть ли ограничение на количество добавляемых полей со списком?
Нет, строгих ограничений нет; вы можете добавить столько полей со списком, сколько требуется вашему проекту.
### Как получить поддержку по Aspose.Cells?
 Вы можете получить поддержку от[Форум Aspose](https://forum.aspose.com/c/cells/9).