---
title: Excel Çalışma Sayfasını Koruyun
linktitle: Excel Çalışma Sayfasını Koruyun
second_title: Aspose.Cells for .NET API Referansı
description: Bu eğitimde Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunu nasıl koruyacağınızı keşfedin. C#'ta adım adım kılavuz.
type: docs
weight: 50
url: /tr/net/protect-excel-file/protect-excel-worksheet/
---
Bu eğitimde, bir Excel elektronik tablosunu korumak için Aspose.Cells kütüphanesini kullanan bazı C# kaynak kodlarına bakacağız. Kodun her adımını inceleyeceğiz ve nasıl çalıştığını açıklayacağız. İstenilen sonuçları elde etmek için talimatları dikkatlice takip ettiğinizden emin olun.

## 1. Adım: Önkoşullar

Başlamadan önce .NET için Aspose.Cells kütüphanesini kurduğunuzdan emin olun. Aspose'un resmi web sitesinden alabilirsiniz. Ayrıca Visual Studio'nun veya başka bir C# geliştirme ortamının güncel bir sürümüne sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells kütüphanesini kullanmak için gerekli ad alanlarını kodumuza aktarmamız gerekiyor. C# kaynak dosyanızın en üstüne aşağıdaki satırları ekleyin:

```csharp
using Aspose.Cells;
using System.IO;
```

## 3. Adım: Excel dosyasını yükleyin

Bu adımda korumak istediğimiz Excel dosyasını yükleyeceğiz. Excel dosyasını içeren dizinin doğru yolunu belirttiğinizden emin olun. Dosyayı yüklemek için aşağıdaki kodu kullanın:

```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Açılacak Excel dosyasını içeren bir dosya akışı oluşturun.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Bir Çalışma Kitabı nesnesinin örneğini oluşturun.
//Excel dosyasını dosya akışı yoluyla açın.
Workbook excel = new Workbook(fstream);
```

 Değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIR"` Belgeler dizininize uygun yol ile.

## 4. Adım: E-tabloya erişin

Artık Excel dosyasını yüklediğimize göre ilk çalışma sayfasına erişebiliriz. İlk çalışma sayfasına erişmek için aşağıdaki kodu kullanın:

```csharp
// Excel dosyasındaki ilk çalışma sayfasına erişim.
Worksheet worksheet = excel.Worksheets[0];
```

## 5. Adım: Çalışma sayfasını koruyun

Bu adımda elektronik tabloyu bir şifre kullanarak koruyacağız. Elektronik tabloyu korumak için aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasını bir parolayla koruyun.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Yer değiştirmek`"YOUR_PASSWORD"` e-tabloyu korumak için kullanmak istediğiniz şifreyle.

## Adım 6: Artık koruduğumuza göre Değiştirilmiş Excel Dosyasını Kaydedin

e-tabloda, değiştirilen Excel dosyasını varsayılan formatta kaydedeceğiz. Excel dosyasını kaydetmek için aşağıdaki kodu kullanın:

```csharp
// Değiştirilen Excel dosyasını varsayılan biçimde kaydedin.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Değiştirilen Excel dosyasını kaydetmek için doğru yolu belirttiğinizden emin olun.

## 7. Adım: Dosya Akışını Kapatın

Tüm kaynakları serbest bırakmak için Excel dosyasını yüklemek için kullanılan dosya akışını kapatmamız gerekir. Dosya akışını kapatmak için aşağıdaki kodu kullanın:

```csharp
// Tüm kaynakları serbest bırakmak için dosya akışını kapatın.
fstream.Close();
```

Bu adımı kodunuzun sonuna eklediğinizden emin olun.


### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfasını Koru için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
// Excel dosyasını dosya akışı aracılığıyla açma
Workbook excel = new Workbook(fstream);
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = excel.Worksheets[0];
// Çalışma sayfasını parolayla koruma
worksheet.Protect(ProtectionType.All, "aspose", null);
// Değiştirilen Excel dosyasını varsayılan formatta kaydetme
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Tebrikler! Artık .NET için Aspose.Cells kütüphanesini kullanarak bir Excel elektronik tablosunu korumanıza olanak tanıyan C# kaynak kodunuz var. Adımları dikkatlice takip ettiğinizden ve kodu özel ihtiyaçlarınıza göre özelleştirdiğinizden emin olun.

### SSS (Sık Sorulan Sorular)

#### Birden fazla çalışma sayfasını tek bir Excel dosyasında korumak mümkün mü?

C: Evet, her çalışma sayfası için 4-6 arasındaki adımları tekrarlayarak birden fazla çalışma sayfasını tek bir Excel dosyasında koruyabilirsiniz.

#### Yetkili kullanıcılar için belirli izinleri nasıl belirleyebilirim?

 C: Sağlanan ek seçenekleri kullanabilirsiniz.`Protect`Yetkili kullanıcılar için belirli izinleri belirtme yöntemi. Daha fazla bilgi için Aspose.Cells belgelerine bakın.

#### Excel dosyasının kendisini bir parola ile koruyabilir miyim?

C: Evet, Aspose.Cells kütüphanesinin sağladığı diğer yöntemleri kullanarak Excel dosyasını şifreyle koruyabilirsiniz. Belirli örnekler için lütfen belgelere bakın.

#### Aspose.Cells kütüphanesi diğer Excel dosya formatlarını destekliyor mu?

C: Evet, Aspose.Cells kütüphanesi XLSX, XLSM, XLSB, CSV vb. dahil çok çeşitli Excel dosya formatlarını destekler.