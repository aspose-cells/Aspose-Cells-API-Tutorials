---
title: Добавить цифровую подпись к подписанному файлу Excel
linktitle: Добавить цифровую подпись к подписанному файлу Excel
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как добавить цифровую подпись к уже подписанному файлу Excel с помощью Aspose.Cells for .NET в этом пошаговом руководстве. Защитите свои документы.
type: docs
weight: 12
url: /ru/net/workbook-operations/add-digital-signature-to-signed-file/
---
## Введение
В современном цифровом мире обеспечение подлинности и целостности документов имеет решающее значение. Цифровые подписи служат надежным средством проверки того, что документ не был изменен и что он получен из законного источника. Если вы работаете с файлами Excel в .NET и хотите добавить цифровую подпись в уже подписанный файл, вы попали по адресу! В этом руководстве мы проведем вас через процесс добавления новой цифровой подписи в существующий подписанный файл Excel с помощью Aspose.Cells для .NET. 
## Предпосылки
Прежде чем углубиться в детали, давайте убедимся, что у вас есть все необходимое для начала работы:
1.  Aspose.Cells для .NET: Прежде всего, вам необходимо установить Aspose.Cells в вашей среде .NET. Вы можете загрузить его с[страница релиза](https://releases.aspose.com/cells/net/).
2. .NET Framework: Убедитесь, что на вашем компьютере установлен .NET Framework. Это руководство предполагает, что вы знакомы с основными концепциями программирования .NET.
3. Цифровой сертификат: Вам понадобится действительный цифровой сертификат (в формате .pfx) для создания цифровой подписи. Если у вас его нет, вы можете создать самоподписанный сертификат для целей тестирования.
4. Среда разработки: редактор кода или IDE, например Visual Studio, где вы можете писать и выполнять свой код C#.
5. Образец файла Excel: У вас должен быть существующий файл Excel, который уже имеет цифровую подпись. Это будет файл, к которому мы добавим еще одну подпись.
Выполнив эти предварительные условия, давайте перейдем к коду!
## Импортные пакеты
Прежде чем начать кодирование, убедитесь, что вы импортировали необходимые пространства имен. Вот что вам нужно включить в начало вашего файла C#:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
Эти пространства имен предоставят вам доступ к классам и методам, необходимым для работы с файлами Excel и обработки цифровых подписей.
Теперь давайте разобьем процесс на управляемые шаги. Мы рассмотрим каждый шаг, чтобы убедиться, что вы понимаете, как добавить цифровую подпись в уже подписанный файл Excel.
## Шаг 1: Определите свои каталоги
Во-первых, вам нужно указать, где находятся ваши исходные файлы и где сохранить выходной файл. Это просто, но важно:
```csharp
// Исходный каталог
string sourceDir = "Your Document Directory"; // Замените на ваш реальный каталог
// Выходной каталог
string outputDir = "Your Document Directory"; // Замените на ваш реальный каталог
```
 Заменять`"Your Document Directory"` с фактическим путем, где хранятся ваши файлы. Это задает тон для ваших файловых операций.
## Шаг 2: Загрузите существующую подписанную рабочую книгу
Далее вы загрузите существующую книгу Excel, которая уже подписана. Вот тут-то и начинается волшебство:
```csharp
// Загрузите книгу, которая уже имеет цифровую подпись, чтобы добавить новую цифровую подпись.
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```
 Эта строка инициализирует новый`Workbook` объект с указанным файлом. Убедитесь, что имя файла соответствует вашему существующему подписанному файлу Excel.
## Шаг 3: Создайте коллекцию цифровых подписей
Для управления цифровыми подписями вам необходимо создать коллекцию. Это позволяет вам хранить несколько подписей, если это необходимо:
```csharp
// Создать коллекцию цифровых подписей
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```
В эту коллекцию вы добавите свою новую цифровую подпись перед ее применением к рабочей книге.
## Шаг 4: Загрузите свой сертификат
Теперь пришло время загрузить ваш цифровой сертификат. Этот сертификат будет использоваться для создания новой подписи:
```csharp
// Файл сертификата и его пароль
string certFileName = sourceDir + "AsposeDemo.pfx"; // Ваш файл сертификата
string password = "aspose"; //Ваш пароль сертификата
// Создать новый сертификат
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```
 Обязательно замените`AsposeDemo.pfx` с именем вашего файла сертификата и обновите пароль соответственно. Этот шаг имеет решающее значение, поскольку без правильного сертификата вы не сможете создать действительную подпись.
## Шаг 5: Создайте новую цифровую подпись
Загрузив сертификат, вы теперь можете создать новую цифровую подпись. Эта подпись будет добавлена в вашу коллекцию:
```csharp
// Создайте новую цифровую подпись и добавьте ее в коллекцию цифровых подписей.
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
```
Здесь вы предоставляете сообщение, описывающее подпись, что может быть полезно для ведения учета. Метка времени гарантирует, что подпись связана с правильным моментом времени.
## Шаг 6: Добавьте коллекцию подписей в рабочую книгу
После создания подписи пришло время добавить всю коллекцию в рабочую книгу:
```csharp
// Добавить коллекцию цифровых подписей в рабочую книгу
workbook.AddDigitalSignature(dsCollection);
```
На этом этапе ваша новая цифровая подпись эффективно применяется к рабочей книге, придавая ей дополнительную подлинность.
## Шаг 7: Сохраните рабочую книгу
Наконец, сохраните книгу с новой цифровой подписью. Это момент, когда вся ваша тяжелая работа окупается:
```csharp
//Сохраните рабочую книгу и утилизируйте ее.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```
Обязательно укажите имя для вашего выходного файла. Это будет новая версия вашего файла Excel, дополненная дополнительной цифровой подписью.
## Шаг 8: Подтвердите успех
В заключение будет хорошей идеей предоставить отзыв после успешного завершения операции:
```csharp
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```
Эта строка выведет на консоль подтверждающее сообщение, сообщающее, что все прошло гладко.
## Заключение
И вот оно! Вы успешно добавили новую цифровую подпись в уже подписанный файл Excel с помощью Aspose.Cells for .NET. Этот процесс не только повышает безопасность ваших документов, но и гарантирует, что они надежны и проверяемы. 
Цифровые подписи необходимы в современном цифровом ландшафте, особенно для предприятий и профессионалов, которым необходимо поддерживать целостность своих документов. Следуя этому руководству, вы сможете легко управлять цифровыми подписями в файлах Excel, гарантируя, что ваши данные останутся защищенными и подлинными.
## Часто задаваемые вопросы
### Что такое цифровая подпись?
Цифровая подпись — это математическая схема для проверки подлинности и целостности цифровых сообщений или документов. Она гарантирует, что документ не был изменен, и подтверждает личность подписавшего.
### Нужен ли мне специальный сертификат для создания цифровой подписи?
Да, для создания действительной цифровой подписи вам необходим цифровой сертификат, выданный доверенным центром сертификации (ЦС).
### Могу ли я использовать самоподписанный сертификат для тестирования?
Конечно! Вы можете создать самоподписанный сертификат для целей разработки и тестирования, но для производства лучше всего использовать сертификат от доверенного центра сертификации.
### Что произойдет, если я попытаюсь добавить подпись к неподписанному документу?
Если вы попытаетесь добавить цифровую подпись к документу, который еще не подписан, это сработает без проблем, но исходная подпись будет отсутствовать.
### Где я могу найти более подробную информацию об Aspose.Cells?
 Вы можете проверить[Документация Aspose.Cells](https://reference.aspose.com/cells/net/) для получения подробных руководств и ссылок на API.