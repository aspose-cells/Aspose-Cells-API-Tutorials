---
title: Excel Çalışma Sayfasındaki Belirli Sütunu Koruyun
linktitle: Excel Çalışma Sayfasındaki Belirli Sütunu Koruyun
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak bir Excel sayfasındaki belirli bir sütunu nasıl koruyacağınızı öğrenin. C#'ta adım adım kılavuz.
type: docs
weight: 80
url: /tr/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
C#'ta Excel çalışma sayfalarıyla çalışırken, yanlışlıkla yapılan değişiklikleri önlemek için genellikle belirli sütunların korunması gerekir. Bu eğitimde, Aspose.Cells for .NET kütüphanesini kullanarak bir Excel çalışma sayfasındaki belirli bir sütunu koruma sürecinde size rehberlik edeceğiz. Bu görev için gereken C# kaynak kodunun adım adım açıklamasını size sunacağız. Öyleyse başlayalım!

## Excel Çalışma Sayfasındaki Belirli Sütunları Korumaya Genel Bakış

Bir Excel çalışma sayfasındaki belirli sütunların korunması, bu sütunların kilitli kalmasını ve uygun yetkilendirme olmadan değiştirilememesini sağlar. Bu, özellikle kullanıcıların çalışma sayfasının geri kalanıyla etkileşimde bulunmasına izin verirken belirli verilere veya formüllere düzenleme erişimini kısıtlamak istediğinizde kullanışlıdır. Aspose.Cells for .NET kitaplığı, Excel dosyalarını programlı olarak yönetmek için sütun koruması da dahil olmak üzere kapsamlı bir dizi özellik sunar.

## Ortamın Ayarlanması

Başlamadan önce, geliştirme ortamınızda Aspose.Cells for .NET kütüphanesinin kurulu olduğundan emin olun. Kütüphaneyi resmi Aspose web sitesinden indirebilir ve sağlanan yükleyiciyi kullanarak kurabilirsiniz.

## Yeni Bir Çalışma Kitabı ve Çalışma Sayfası Oluşturma

Belirli sütunları korumaya başlamak için Aspose.Cells for .NET'i kullanarak yeni bir çalışma kitabı ve çalışma sayfası oluşturmamız gerekiyor. İşte kod pasajı:

```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";

// Henüz mevcut değilse dizin oluşturun.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Yeni bir çalışma kitabı oluşturun.
Workbook wb = new Workbook();

// Bir çalışma sayfası nesnesi oluşturun ve ilk sayfayı edinin.
Worksheet sheet = wb.Worksheets[0];
```

"BELGE DİZİNİ"ni, Excel dosyasını kaydetmek istediğiniz gerçek dizin yolu ile değiştirdiğinizden emin olun.

## Stil ve Stil Bayrağı Nesnelerini Tanımlama

Sütunlara özel stiller ve koruma bayrakları ayarlamak için stil ve stil bayrağı nesnelerini tanımlamamız gerekir. İşte kod pasajı:

```csharp
// Stil nesnesini tanımlayın.
Style style;

// Stil bayrağı nesnesini tanımlayın.
StyleFlag flag;
```

## Sütunlar Arasında Döngü Yapmak ve Bunların Kilidini Açmak

Daha sonra, çalışma sayfasındaki tüm sütunlar arasında dolaşıp bunların kilidini açmamız gerekiyor. Bu, korumak istediğimiz sütun dışındaki tüm sütunların düzenlenebilir olmasını sağlayacaktır. İşte kod pasajı:

```csharp
// Çalışma sayfasındaki tüm sütunlar arasında dolaşın ve bunların kilidini açın.
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

Şimdi belirli bir sütunu kilitleyelim. Bu örnekte ilk sütunu kilitleyeceğiz (sütun dizini 0). İşte kod pasajı:

```csharp
// İlk sütun stilini alın.
style = sheet.Cells.Columns[0].Style;

// Kilitle.
style.IsLocked = true;
```

## Sütunlara Stil Uygulamak

Belirli bir sütunu kilitledikten sonra stili ve bayrağı o sütuna uygulamamız gerekir. İşte kod pasajı:

```csharp
//Bayrağı somutlaştırın.
flag = new StyleFlag();

// Kilit ayarını yapın.
flag.Locked = true;

// Stili ilk sütuna uygulayın.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## Çalışma Sayfasını Korumak

Korumayı sonlandırmak için, kilitli sütunların değiştirilememesini sağlamak üzere çalışma sayfasını korumamız gerekir. İşte kod pasajı:

```csharp
// Sayfayı koruyun.
sheet.Protect(ProtectionType.All);
```

## Excel Dosyasını Kaydetme

Son olarak değiştirdiğimiz Excel dosyasını istenilen konuma kaydedeceğiz. İşte kod pasajı:

```csharp
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

"output.out.xls" dosyasını istediğiniz dosya adı ve uzantısıyla değiştirdiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfasındaki Belirli Sütunu Korumak için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Henüz mevcut değilse dizin oluşturun.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Yeni bir çalışma kitabı oluşturun.
Workbook wb = new Workbook();
// Bir çalışma sayfası nesnesi oluşturun ve ilk sayfayı edinin.
Worksheet sheet = wb.Worksheets[0];
// Stil nesnesini tanımlayın.
Style style;
// Styleflag nesnesini tanımlayın.
StyleFlag flag;
// Çalışma sayfasındaki tüm sütunlar arasında dolaşın ve bunların kilidini açın.
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
//Bayrağı somutlaştırın.
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

Bu eğitimde, Aspose.Cells for .NET kütüphanesini kullanarak bir Excel çalışma sayfasındaki belirli bir sütunu korumanın adım adım sürecini açıkladık. Yeni bir çalışma kitabı ve çalışma sayfası oluşturarak, stil ve stil bayrağı nesnelerini tanımlayarak başladık ve ardından belirli sütunların kilidini açıp kilitlemeye başladık. Son olarak çalışma sayfasını koruma altına aldık ve değiştirilen Excel dosyasını kaydettik. Bu kılavuzu takip ederek artık C# ve Aspose.Cells for .NET kullanarak Excel çalışma sayfalarındaki belirli sütunları koruyabileceksiniz.

### Sıkça Sorulan Sorular (SSS)

#### Bu yöntemi kullanarak birden fazla sütunu koruyabilir miyim?

Evet, kodu uygun şekilde değiştirerek birden fazla sütunu koruyabilirsiniz. İstediğiniz sütun aralığında dolaşın ve kilitleme stillerini ve bayraklarını uygulayın.

#### Korunan çalışma sayfasını parolayla korumak mümkün mü?

 Evet, korumalı çalışma sayfasına parolayı arayarak parola koruması ekleyebilirsiniz.`Protect` yöntem.

#### Aspose.Cells for .NET diğer Excel dosya formatlarını destekliyor mu?

Evet, Aspose.Cells for .NET, XLS, XLSX, XLSM ve daha fazlası dahil olmak üzere çeşitli Excel dosya formatlarını destekler.

#### Sütunlar yerine belirli satırları koruyabilir miyim?

Evet, stilleri ve bayrakları sütun hücreleri yerine satır hücrelerine uygulayarak, sütunlar yerine belirli satırları korumak için kodu değiştirebilirsiniz.