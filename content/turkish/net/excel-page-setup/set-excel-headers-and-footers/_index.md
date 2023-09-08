---
title: Excel Üstbilgilerini ve Altbilgilerini Ayarlama
linktitle: Excel Üstbilgilerini ve Altbilgilerini Ayarlama
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak Excel'de üstbilgi ve altbilgileri nasıl ayarlayacağınızı öğrenin.
type: docs
weight: 100
url: /tr/net/excel-page-setup/set-excel-headers-and-footers/
---

Bu eğitimde size Aspose.Cells for .NET kullanarak Excel'de üstbilgi ve altbilgilerin nasıl ayarlanacağını adım adım göstereceğiz. Süreci göstermek için C# kaynak kodunu kullanacağız.

## 1. Adım: Ortamı ayarlama

Aspose.Cells for .NET'in makinenizde kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Aspose.Cells ile çalışmak için gereken kütüphaneleri kod dosyanıza aktarın. İşte ilgili kod:

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

Bu, çalışma sayfası içeren boş bir çalışma kitabı oluşturacak ve bu çalışma sayfasının PageSetup nesnesine erişim sağlayacaktır.

## Adım 5: Başlıkları Ayarlama

 Elektronik tablo başlıklarını kullanarak ayarlayın.`SetHeader` PageSetup nesnesinin yöntemleri. İşte örnek bir kod:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Bu, sırasıyla başlıklardaki çalışma sayfası adını, geçerli tarih ve saati ve dosya adını ayarlayacaktır.

## Adım 6: Altbilgileri tanımlama

 Elektronik tablo altbilgilerini şunu kullanarak ayarlayın:`SetFooter` PageSetup nesnesinin yöntemleri. İşte örnek bir kod:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Bu sırasıyla bir metin dizesini, geçerli sayfa numarasını ve altbilgilerdeki toplam sayfa sayısını ayarlayacaktır.

## Adım 7: Değiştirilen Çalışma Kitabını Kaydetme

Değiştirilen çalışma kitabını aşağıdaki kodu kullanarak kaydedin:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Bu, değiştirilen çalışma kitabını belirtilen veri dizinine kaydedecektir.

### Aspose.Cells for .NET kullanarak Excel Üstbilgilerini ve Altbilgilerini Ayarlama için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook excel = new Workbook();
// Çalışma sayfasının PageSetup referansının alınması
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Başlığın sol bölümünde çalışma sayfası adının ayarlanması
pageSetup.SetHeader(0, "&A");
//Başlığın orta bölümünde geçerli tarihi ve geçerli saati ayarlama
// ve başlığın yazı tipini değiştirme
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Geçerli dosya adını başlığın sağ kısmında ayarlamak ve değiştirmek
// başlığın yazı tipi
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Alt bilginin sol kısmına bir dize ayarlama ve yazı tipini değiştirme
// bu dizenin bir kısmının ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Geçerli sayfa numarasını altbilginin orta bölümünde ayarlama
pageSetup.SetFooter(1, "&P");
// Altbilginin sağ bölümünde sayfa sayısını ayarlama
pageSetup.SetFooter(2, "&N");
// Çalışma Kitabını kaydedin.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Çözüm

Artık Aspose.Cells for .NET'i kullanarak Excel'de üstbilgi ve altbilgileri nasıl ayarlayacağınızı öğrendiniz. Bu eğitim, ortamın ayarlanmasından değiştirilen çalışma kitabının kaydedilmesine kadar sürecin her adımında size yol gösterdi. Excel dosyalarınızda daha fazla değişiklik yapmak için Aspose.Cells'in özelliklerini daha fazla keşfetmekten çekinmeyin.

### Sık Sorulan Sorular (SSS)

#### 1. Aspose.Cells for .NET'i sistemime nasıl kurabilirim?
Aspose.Cells for .NET'i yüklemek için Aspose resmi web sitesinden kurulum paketini indirmeniz ve belgelerde verilen talimatları izlemeniz gerekir.

#### 2. Bu yöntem Excel'in tüm sürümlerinde çalışır mı?
Evet, Aspose.Cells for .NET ile üstbilgi ve altbilgileri ayarlama yöntemi, desteklenen tüm Excel sürümleriyle çalışır.

#### 3. Üstbilgileri ve altbilgileri daha da özelleştirebilir miyim?
Evet, Aspose.Cells üstbilgileri ve altbilgileri özelleştirmek için metin yerleşimi, renk, yazı tipi, sayfa numaraları ve daha fazlası dahil olmak üzere çok çeşitli özellikler sunar.

#### 4. Üstbilgilere ve altbilgilere dinamik bilgileri nasıl ekleyebilirim?
Üstbilgilere ve altbilgilere geçerli tarih, saat, dosya adı, sayfa numarası vb. gibi dinamik bilgiler eklemek için özel değişkenleri ve biçimlendirme kodlarını kullanabilirsiniz.

#### 5. Üstbilgileri ve altbilgileri ayarladıktan sonra kaldırabilir miyim?
 Evet, üstbilgileri ve altbilgileri şunu kullanarak kaldırabilirsiniz:`ClearHeaderFooter` yöntemi`PageSetup` nesne. Bu, varsayılan üstbilgileri ve altbilgileri geri yükleyecektir.