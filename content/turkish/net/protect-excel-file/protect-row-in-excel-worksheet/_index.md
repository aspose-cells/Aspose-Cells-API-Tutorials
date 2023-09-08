---
title: Excel Çalışma Sayfasındaki Satırı Koru
linktitle: Excel Çalışma Sayfasındaki Satırı Koru
second_title: Aspose.Cells for .NET API Referansı
description: Bu eğitimde Aspose.Cells for .NET kullanarak bir Excel tablosunun satırlarını nasıl koruyacağınızı keşfedin. C#'ta adım adım eğitim.
type: docs
weight: 60
url: /tr/net/protect-excel-file/protect-row-in-excel-worksheet/
---
Bu eğitimde, bir Excel elektronik tablosundaki satırları korumak için Aspose.Cells kütüphanesini kullanan bazı C# kaynak kodlarına bakacağız. Kodun her adımını inceleyeceğiz ve nasıl çalıştığını açıklayacağız. İstenilen sonuçları elde etmek için talimatları dikkatlice izleyin.

## 1. Adım: Önkoşullar

Başlamadan önce .NET için Aspose.Cells kütüphanesini kurduğunuzdan emin olun. Aspose'un resmi web sitesinden alabilirsiniz. Ayrıca Visual Studio'nun veya başka bir C# geliştirme ortamının güncel bir sürümüne sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells kütüphanesini kullanmak için gerekli ad alanlarını kodumuza aktarmamız gerekiyor. C# kaynak dosyanızın en üstüne aşağıdaki satırları ekleyin:

```csharp
using Aspose.Cells;
```

## 3. Adım: Excel çalışma kitabı oluşturma

Bu adımda yeni bir Excel çalışma kitabı oluşturacağız. Excel çalışma kitabı oluşturmak için aşağıdaki kodu kullanın:

```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Yeni bir çalışma kitabı oluşturun.
Workbook wb = new Workbook();
```

 Değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIR"` Belgeler dizininize uygun yol ile.

## 4. Adım: Elektronik tablo oluşturma

Artık Excel çalışma kitabını oluşturduğumuza göre, bir çalışma sayfası oluşturup ilk sayfayı alalım. Aşağıdaki kodu kullanın:

```csharp
// Bir elektronik tablo nesnesi oluşturun ve ilk sayfayı alın.
Worksheet sheet = wb.Worksheets[0];
```

## Adım 5: Stili Tanımlama

Bu adımda elektronik tablonun satırlarına uygulanacak stili tanımlayacağız. Aşağıdaki kodu kullanın:

```csharp
// Stil nesnesinin tanımı.
Styling styling;
```

## Adım 6: Tüm sütunların kilidini açmak için döngü yapın

Şimdi çalışma sayfasındaki tüm sütunlar arasında dolaşıp bunların kilidini açacağız. Aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasındaki tüm sütunlar arasında dolaşın ve bunların kilidini açın.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Adım 7: İlk satırı kilitleme

Bu adımda çalışma sayfasının ilk satırını kilitleyeceğiz. Aşağıdaki kodu kullanın:

```csharp
// İlk satırın stilini alın.
style = sheet.Cells.Rows[0].Style;
// Stili kilitle.
style. IsLocked = true;
// Stili ilk satıra uygulayın.
sheet.Cells.ApplyRowStyle(0, style);
```

## Adım 8: Çalışma sayfasını koruma

Artık stilleri ayarladığımıza ve satırları kilitlediğimize göre e-tabloyu korumaya geçelim. Aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasını koruyun.
sheet.Protect(ProtectionType.All);
```

## Adım 9: Excel dosyasını kaydetme

Son olarak değiştirilen Excel dosyasını kaydedeceğiz. Aşağıdaki kodu kullanın:

```csharp
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Değiştirilen Excel dosyasını kaydetmek için doğru yolu belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfasındaki Satırı Koru için örnek kaynak kodu 
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
// İlk satır stilini alın.
style = sheet.Cells.Rows[0].Style;
// Kilitle.
style.IsLocked = true;
//Bayrağı somutlaştırın.
flag = new StyleFlag();
// Kilit ayarını yapın.
flag.Locked = true;
// Stili ilk satıra uygulayın.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Sayfayı koruyun.
sheet.Protect(ProtectionType.All);
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Çözüm

Tebrikler! Artık .NET için Aspose.Cells kütüphanesini kullanarak bir Excel elektronik tablosundaki satırları korumanıza olanak tanıyan C# kaynak kodunuz var. Adımları dikkatlice takip ettiğinizden ve kodu özel ihtiyaçlarınıza göre özelleştirdiğinizden emin olun.

### SSS (Sık Sorulan Sorular)

#### Bu kod Excel'in son sürümleriyle çalışıyor mu?

Evet, bu kod, Excel 2010 ve üzeri formattaki dosyalar da dahil olmak üzere Excel'in son sürümleriyle çalışır.

#### Çalışma sayfasındaki tüm satırlar yerine yalnızca belirli satırları koruyabilir miyim?

Evet, korumak istediğiniz belirli satırları belirtmek için kodu değiştirebilirsiniz. Döngüyü ve indeksleri buna göre ayarlamanız gerekecektir.

#### Kilitli hatların kilidini tekrar nasıl açabilirim?

 Şunu kullanabilirsiniz:`IsLocked` yöntemi`Style` Değerin ayarlanacağı nesne`false` ve satırların kilidini açın.

#### Aynı Excel çalışma kitabında birden fazla çalışma sayfasını korumak mümkün müdür?

Evet, çalışma kitabındaki her çalışma sayfası için çalışma sayfası oluşturma, stili ayarlama ve koruma adımlarını tekrarlayabilirsiniz.

#### Elektronik tablo koruma parolasını nasıl değiştirebilirim?

 Şifreyi kullanarak değiştirebilirsiniz.`Protect` yöntemi ve argüman olarak yeni bir parolanın belirtilmesi.