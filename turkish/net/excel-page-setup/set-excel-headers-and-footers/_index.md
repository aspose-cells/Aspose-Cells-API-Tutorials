---
title: Excel Üst Bilgilerini ve Alt Bilgilerini Ayarlama
linktitle: Excel Üst Bilgilerini ve Alt Bilgilerini Ayarlama
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel'de üst bilgileri ve alt bilgileri nasıl ayarlayacağınızı öğrenin.
type: docs
weight: 100
url: /tr/net/excel-page-setup/set-excel-headers-and-footers/
---

Bu eğitimde, Aspose.Cells for .NET kullanarak Excel'de üst bilgileri ve alt bilgileri nasıl ayarlayacağınızı adım adım göstereceğiz. Süreci göstermek için C# kaynak kodunu kullanacağız.

## 1. Adım: Ortamı ayarlama

Makinenizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Kod dosyanızda, Aspose.Cells ile çalışmak için gereken kütüphaneleri içe aktarın. İşte ilgili kod:

```csharp
using Aspose.Cells;
```

## 3. Adım: Veri Dizinini Ayarlayın

Değiştirilen Excel dosyasını kaydetmek istediğiniz veri dizinini ayarlayın. Aşağıdaki kodu kullanın:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Tam dizin yolunu belirttiğinizden emin olun.

## Adım 4: Çalışma kitabını ve çalışma sayfasını oluşturma

Yeni bir Çalışma Kitabı nesnesi oluşturun ve aşağıdaki kodu kullanarak çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Bu, çalışma sayfası içeren boş bir çalışma kitabı oluşturacak ve o çalışma sayfasının PageSetup nesnesine erişim sağlayacaktır.

## Adım 5: Başlıkları Ayarlama

 kullanarak elektronik tablo başlıklarını ayarlayın.`SetHeader` PageSetup nesnesinin yöntemleri. İşte örnek bir kod:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Bu, sırasıyla başlıklardaki çalışma sayfası adını, geçerli tarih ve saati ve dosya adını ayarlayacaktır.

## 6. Adım: Alt bilgileri tanımlama

 kullanarak elektronik tablo altbilgilerini ayarlayın.`SetFooter` PageSetup nesnesinin yöntemleri. İşte örnek bir kod:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Bu, sırasıyla bir metin dizesi, geçerli sayfa numarası ve altbilgilerdeki toplam sayfa sayısını ayarlayacaktır.

## 7. Adım: Değiştirilmiş Çalışma Kitabını Kaydetme

Değiştirilen çalışma kitabını aşağıdaki kodu kullanarak kaydedin:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Bu, değiştirilen çalışma kitabını belirtilen veri dizinine kaydedecektir.

### Aspose.Cells for .NET kullanarak Excel Üst Bilgilerini ve Alt Bilgilerini Ayarlamak için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook excel = new Workbook();
// Çalışma sayfasının PageSetup referansını alma
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Çalışma sayfası adını başlığın sol kısmında ayarlama
pageSetup.SetHeader(0, "&A");
//Başlığın orta bölümünde geçerli tarihi ve geçerli saati ayarlama
// ve başlığın yazı tipini değiştirme
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Geçerli dosya adını başlığın sağ bölümünde ayarlama ve değiştirme
// başlığın yazı tipi
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Altbilginin sol kısmında bir dize ayarlama ve yazı tipini değiştirme
// bu dizenin bir bölümünün ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Geçerli sayfa numarasını altbilginin orta bölümünde ayarlama
pageSetup.SetFooter(1, "&P");
// Sayfa sayısını altbilginin sağ kısmında ayarlama
pageSetup.SetFooter(2, "&N");
// Çalışma Kitabını kaydedin.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Çözüm

Artık Aspose.Cells for .NET kullanarak Excel'de üst bilgileri ve alt bilgileri nasıl ayarlayacağınızı öğrendiniz. Bu öğretici, ortamın ayarlanmasından değiştirilen çalışma kitabının kaydedilmesine kadar sürecin her adımında size yol gösterdi. Excel dosyalarınızda daha fazla değişiklik yapmak için Aspose.Cells'in özelliklerini daha fazla keşfetmekten çekinmeyin.

### Sık Sorulan Sorular (SSS)

#### 1. Aspose.Cells for .NET'i sistemime nasıl kurabilirim?
Aspose.Cells for .NET'i kurmak için kurulum paketini Aspose resmi web sitesinden indirmeniz ve belgelerde verilen talimatları izlemeniz gerekir.

#### 2. Bu yöntem Excel'in tüm sürümlerinde çalışır mı?
Evet, Aspose.Cells for .NET ile üst bilgileri ve alt bilgileri ayarlama yöntemi, desteklenen tüm Excel sürümleriyle çalışır.

#### 3. Üst bilgileri ve alt bilgileri daha fazla özelleştirebilir miyim?
Evet, Aspose.Cells üst bilgileri ve alt bilgileri özelleştirmek için metin yerleşimi, renk, yazı tipi, sayfa numaraları ve daha fazlası dahil olmak üzere kapsamlı bir özellik yelpazesi sunar.

#### 4. Üstbilgilere ve altbilgilere nasıl dinamik bilgi ekleyebilirim?
Geçerli tarih, saat, dosya adı, sayfa numarası gibi dinamik bilgileri üstbilgilere ve altbilgilere eklemek için özel değişkenleri ve biçimlendirme kodlarını kullanabilirsiniz.

#### 5. Üst bilgileri ve alt bilgileri ayarladıktan sonra kaldırabilir miyim?
 Evet, kullanarak üstbilgileri ve altbilgileri kaldırabilirsiniz.`ClearHeaderFooter` yöntemi`PageSetup` nesne. Bu, varsayılan üst bilgileri ve alt bilgileri geri yükleyecektir.