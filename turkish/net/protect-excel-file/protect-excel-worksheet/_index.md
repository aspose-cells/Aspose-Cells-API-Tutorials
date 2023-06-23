---
title: Excel Çalışma Sayfasını Koruyun
linktitle: Excel Çalışma Sayfasını Koruyun
second_title: Aspose.Cells for .NET API Referansı
description: Bu eğitimde Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunu nasıl koruyacağınızı keşfedin. C# ile adım adım kılavuz.
type: docs
weight: 50
url: /tr/net/protect-excel-file/protect-excel-worksheet/
---
Bu öğreticide, bir Excel elektronik tablosunu korumak için Aspose.Cells kitaplığını kullanan bazı C# kaynak kodlarına bakacağız. Kodun her adımını inceleyeceğiz ve nasıl çalıştığını açıklayacağız. İstenen sonuçları elde etmek için talimatları dikkatlice uyguladığınızdan emin olun.

## 1. Adım: Önkoşullar

Başlamadan önce, .NET için Aspose.Cells kitaplığını kurduğunuzdan emin olun. Aspose resmi sitesinden temin edebilirsiniz. Ayrıca, Visual Studio'nun veya başka herhangi bir C# geliştirme ortamının yeni bir sürümüne sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells kütüphanesini kullanmak için gerekli namespace'leri kodumuza import etmemiz gerekiyor. C# kaynak dosyanızın en üstüne aşağıdaki satırları ekleyin:

```csharp
using Aspose.Cells;
using System.IO;
```

## 3. Adım: Excel dosyasını yükleyin

Bu adımda korumak istediğimiz Excel dosyasını yükleyeceğiz. Excel dosyasını içeren dizine doğru yolu belirttiğinizden emin olun. Dosyayı yüklemek için aşağıdaki kodu kullanın:

```csharp
// Belgeler dizinine giden yol.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Açılacak Excel dosyasını içeren bir dosya akışı oluşturun.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Bir Çalışma Kitabı nesnesi örneği oluşturun.
//Dosya akışı aracılığıyla Excel dosyasını açın.
Workbook excel = new Workbook(fstream);
```

 değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIR"` belgeler dizininize uygun yolla.

## 4. Adım: Elektronik tabloya erişin

Artık Excel dosyasını yüklediğimize göre, ilk çalışma sayfasına erişebiliriz. İlk çalışma sayfasına erişmek için aşağıdaki kodu kullanın:

```csharp
// Excel dosyasındaki ilk çalışma sayfasına erişim.
Worksheet worksheet = excel.Worksheets[0];
```

## 5. Adım: Çalışma sayfasını koruyun

Bu adımda elektronik tabloyu bir parola kullanarak koruyacağız. Elektronik tabloyu korumak için aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasını bir parola ile koruyun.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Yer değiştirmek`"YOUR_PASSWORD"` e-tabloyu korumak için kullanmak istediğiniz parola ile.

## 6. Adım: Artık koruduğumuza göre Değiştirilmiş Excel Dosyasını kaydedin

elektronik tablo olarak, değiştirilen Excel dosyasını varsayılan biçimde kaydedeceğiz. Excel dosyasını kaydetmek için aşağıdaki kodu kullanın:

```csharp
// Değiştirilen Excel dosyasını varsayılan biçimde kaydedin.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Değiştirilen Excel dosyasını kaydetmek için doğru yolu belirttiğinizden emin olun.

## 7. Adım: Dosya Akışını Kapatın

Tüm kaynakları serbest bırakmak için, Excel dosyasını yüklemek için kullanılan dosya akışını kapatmamız gerekiyor. Dosya akışını kapatmak için aşağıdaki kodu kullanın:

```csharp
// Tüm kaynakları serbest bırakmak için dosya akışını kapatın.
fstream.Close();
```

Bu adımı kodunuzun sonuna eklediğinizden emin olun.


### Aspose.Cells for .NET kullanan Protect Excel Worksheet için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
// Excel dosyasını dosya akışı aracılığıyla açma
Workbook excel = new Workbook(fstream);
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = excel.Worksheets[0];
// Çalışma sayfasını bir parola ile koruma
worksheet.Protect(ProtectionType.All, "aspose", null);
// Değiştirilen Excel dosyasını varsayılan biçimde kaydetme
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Tebrikler! Artık bir Excel elektronik tablosunu Aspose.Cells library for .NET kullanarak korumanıza izin veren C# kaynak kodunuz var. Adımları dikkatli bir şekilde uyguladığınızdan ve kodu özel ihtiyaçlarınıza göre özelleştirdiğinizden emin olun.

### SSS (Sıkça Sorulan Sorular)

#### Birden çok çalışma sayfasını tek bir Excel dosyasında korumak mümkün müdür?

Y: Evet, her çalışma sayfası için 4-6. adımları tekrarlayarak tek bir Excel dosyasında birden çok çalışma sayfasını koruyabilirsiniz.

#### Yetkili kullanıcılar için belirli izinleri nasıl belirleyebilirim?

 C: tarafından sağlanan ek seçenekleri kullanabilirsiniz.`Protect`yetkili kullanıcılar için belirli izinleri belirleme yöntemi. Daha fazla bilgi için Aspose.Cells belgelerine bakın.

#### Excel dosyasının kendisini bir parola ile koruyabilir miyim?

C: Evet, Aspose.Cells kitaplığı tarafından sağlanan diğer yöntemleri kullanarak Excel dosyasının kendisini parola ile koruyabilirsiniz. Belirli örnekler için lütfen belgelere bakın.

#### Aspose.Cells kütüphanesi diğer Excel dosya formatlarını destekliyor mu?

C: Evet, Aspose.Cells kitaplığı, XLSX, XLSM, XLSB, CSV, vb. dahil olmak üzere çok çeşitli Excel dosya formatlarını destekler.