---
title: Excel Çalışma Sayfasında Belirli Sütunu Koru
linktitle: Excel Çalışma Sayfasında Belirli Sütunu Koru
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel sayfasındaki belirli bir sütunu nasıl koruyacağınızı öğrenin. C# ile adım adım kılavuz.
type: docs
weight: 80
url: /tr/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
C# dilinde Excel çalışma sayfalarıyla çalışırken, yanlışlıkla yapılan değişiklikleri önlemek için genellikle belirli sütunları korumak gerekir. Bu öğreticide, Aspose.Cells for .NET kitaplığını kullanarak bir Excel çalışma sayfasındaki belirli bir sütunu koruma sürecinde size rehberlik edeceğiz. Bu görev için gerekli olan C# kaynak kodunun adım adım açıklamasını size sağlayacağız. Öyleyse başlayalım!

## Bir Excel Çalışma Sayfasında Belirli Sütunları Korumaya Genel Bakış

Bir Excel çalışma sayfasındaki belirli sütunların korunması, bu sütunların kilitli kalmasını ve uygun yetkilendirme olmadan değiştirilememesini sağlar. Bu, kullanıcıların çalışma sayfasının geri kalanıyla etkileşime girmesine izin verirken belirli verilere veya formüllere düzenleme erişimini kısıtlamak istediğinizde özellikle kullanışlıdır. Aspose.Cells for .NET kitaplığı, sütun koruması da dahil olmak üzere, Excel dosyalarını program aracılığıyla işlemek için kapsamlı bir dizi özellik sağlar.

## Ortamı Kurma

Başlamadan önce, geliştirme ortamınızda Aspose.Cells for .NET kitaplığının kurulu olduğundan emin olun. Kütüphaneyi resmi Aspose web sitesinden indirebilir ve sağlanan yükleyiciyi kullanarak kurabilirsiniz.

## Yeni Bir Çalışma Kitabı ve Çalışma Sayfası Oluşturma

Belirli sütunları korumaya başlamak için Aspose.Cells for .NET kullanarak yeni bir çalışma kitabı ve çalışma sayfası oluşturmamız gerekiyor. İşte kod parçacığı:

```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";

// Halihazırda mevcut değilse, dizin oluşturun.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Yeni bir çalışma kitabı oluşturun.
Workbook wb = new Workbook();

// Bir çalışma sayfası nesnesi oluşturun ve ilk sayfayı alın.
Worksheet sheet = wb.Worksheets[0];
```

"BELGE DİZİNİNİZİ" Excel dosyasını kaydetmek istediğiniz gerçek dizin yolu ile değiştirdiğinizden emin olun.

## Stil ve Stil Bayrak Nesnelerini Tanımlama

Sütunlar için belirli stiller ve koruma bayrakları ayarlamak için, stil ve stil bayrağı nesnelerini tanımlamamız gerekir. İşte kod parçacığı:

```csharp
// Stil nesnesini tanımlayın.
Style style;

// Stil bayrağı nesnesini tanımlayın.
StyleFlag flag;
```

## Sütunlar Arasında Döngü Yapma ve Bunların Kilidini Açma

Ardından, çalışma sayfasındaki tüm sütunları dolaşıp kilidini açmamız gerekiyor. Bu, korumak istediğimiz dışındaki tüm sütunların düzenlenebilir olmasını sağlayacaktır. İşte kod parçacığı:

```csharp
// Çalışma sayfasındaki tüm sütunlarda dolaşın ve bunların kilidini açın.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Belirli Bir Sütunu Kilitleme

Şimdi belirli bir sütunu kilitleyelim. Bu örnekte, ilk sütunu kilitleyeceğiz (sütun dizini 0). İşte kod parçacığı:

```csharp
// İlk sütun stilini alın.
style = sheet.Cells.Columns[0].Style;

// Kilitle.
style.IsLocked = true;
```

## Stilleri Sütunlara Uygulamak

Belirli bir sütunu kilitledikten sonra, stili ve bayrağı o sütuna uygulamamız gerekir. İşte kod parçacığı:

```csharp
// Bayrağı somutlaştırın.
flag = new StyleFlag();

// Kilit ayarını yapın.
flag.Locked = true;

// Stili ilk sütuna uygulayın.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## Çalışma Sayfasını Koruma

Korumayı sonlandırmak için, kilitli sütunların değiştirilememesini sağlamak için çalışma sayfasını korumamız gerekir. İşte kod parçacığı:

```csharp
// Sayfayı koruyun.
sheet.Protect(ProtectionType.All);
```

## Excel Dosyasını Kaydetme

Son olarak, değiştirilen Excel dosyasını istenen konuma kaydedeceğiz. İşte kod parçacığı:

```csharp
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

"output.out.xls" dosyasını istenen dosya adı ve uzantısıyla değiştirdiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfasında Belirli Sütunu Koru için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Halihazırda mevcut değilse, dizin oluşturun.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Yeni bir çalışma kitabı oluşturun.
Workbook wb = new Workbook();
// Bir çalışma sayfası nesnesi oluşturun ve ilk sayfayı alın.
Worksheet sheet = wb.Worksheets[0];
// Stil nesnesini tanımlayın.
Style style;
//styleflag nesnesini tanımlayın.
StyleFlag flag;
// Çalışma sayfasındaki tüm sütunlarda dolaşın ve bunların kilidini açın.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// İlk sütun stilini alın.
style = sheet.Cells.Columns[0].Style;
// Kilitle.
style.IsLocked = true;
// Bayrağı somutlaştırın.
flag = new StyleFlag();
// Kilit ayarını yapın.
flag.Locked = true;
// Stili ilk sütuna uygulayın.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// Sayfayı koruyun.
sheet.Protect(ProtectionType.All);
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Çözüm

Bu eğitimde, Aspose.Cells for .NET kitaplığını kullanarak bir Excel çalışma sayfasındaki belirli bir sütunu koruma sürecini adım adım açıkladık. Stil ve stil bayrağı nesnelerini tanımlayarak yeni bir çalışma kitabı ve çalışma sayfası oluşturarak başladık ve ardından belirli sütunların kilidini açıp kilitlemeye devam ettik. Son olarak, çalışma sayfasını koruduk ve değiştirilen Excel dosyasını kaydettik. Bu kılavuzu takip ederek, artık C# ve Aspose.Cells for .NET kullanarak Excel çalışma sayfalarındaki belirli sütunları koruyabilirsiniz.

### Sıkça Sorulan Sorular (SSS)

#### Bu yöntemi kullanarak birden çok sütunu koruyabilir miyim?
Evet, kodu uygun şekilde değiştirerek birden çok sütunu koruyabilirsiniz. İstenen sütun aralığında dolaşın ve kilitleme stillerini ve işaretlerini uygulayın.

#### Korumalı çalışma sayfasını parola ile korumak mümkün müdür?
 Evet, korumalı çalışma sayfasına parolayı çağırırken parolayı belirterek parola koruması ekleyebilirsiniz.`Protect` yöntem.

#### Aspose.Cells for .NET diğer Excel dosya formatlarını destekliyor mu?
Evet, Aspose.Cells for .NET, XLS, XLSX, XLSM ve daha fazlasını içeren çeşitli Excel dosya formatlarını destekler.

#### Sütunlar yerine belirli satırları koruyabilir miyim?
Evet, stilleri ve bayrakları sütun hücreleri yerine satır hücrelerine uygulayarak, sütunlar yerine belirli satırları korumak için kodu değiştirebilirsiniz.