---
title: Excel Çalışma Sayfasındaki Belirli Hücreleri Koruyun
linktitle: Excel Çalışma Sayfasındaki Belirli Hücreleri Koruyun
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel'deki belirli hücreleri nasıl koruyacağınızı öğrenin. C#'ta adım adım eğitim.
type: docs
weight: 70
url: /tr/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
Bu eğitimde, bir Excel elektronik tablosundaki belirli hücreleri korumak için Aspose.Cells kütüphanesini kullanan C# kaynak koduna bakacağız. Kodun her adımını inceleyeceğiz ve nasıl çalıştığını açıklayacağız. İstenilen sonuçları elde etmek için talimatları dikkatlice izleyin.

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

Bu adımda belirli hücrelere uygulanacak stili tanımlayacağız. Aşağıdaki kodu kullanın:

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

## Adım 7: Belirli Hücreleri Kilitleme

Bu adımda belirli hücreleri kilitleyeceğiz. Aşağıdaki kodu kullanın:

```csharp
//Üç hücrenin tümü kilitleniyor... yani A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Adım 8: Çalışma sayfasını koruma

Son olarak, belirli hücrelerin değiştirilmesini önlemek için çalışma sayfasını koruyacağız. Aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasını koruyun.
sheet.Protect(ProtectionType.All);
```

## Adım 9: Excel dosyasını kaydetme

Şimdi değiştirilen Excel dosyasını kaydedeceğiz. Aşağıdaki kodu kullanın:

```csharp
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Değiştirilen Excel dosyasını kaydetmek için doğru yolu belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfasındaki Belirli Hücreleri Korumak için örnek kaynak kodu 
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
// Stil bayrağı nesnesini tanımlayın
StyleFlag styleflag;
// Çalışma sayfasındaki tüm sütunlar arasında dolaşın ve bunların kilidini açın.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Üç hücreyi kilitleyin... yani A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Son olarak, sayfayı şimdi koruyun.
sheet.Protect(ProtectionType.All);
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Çözüm

Tebrikler! Artık .NET için Aspose.Cells kütüphanesini kullanarak bir Excel çalışma sayfasındaki belirli hücreleri korumanıza olanak tanıyan C# kaynak kodunuz var. Kodu özel ihtiyaçlarınıza uyacak şekilde özelleştirmekten çekinmeyin.

### SSS (Sık Sorulan Sorular)

#### Bu kod Excel'in son sürümleriyle çalışıyor mu?

Evet, bu kod, Excel 2010 ve üzeri formattaki dosyalar da dahil olmak üzere Excel'in son sürümleriyle çalışır.

#### A1, B1 ve C1 dışında diğer hücreleri de koruyabilir miyim?

Evet, ilgili kod satırlarındaki hücre referanslarını ayarlayarak diğer belirli hücreleri kilitlemek için kodu değiştirebilirsiniz.

#### Kilitli hücrelerin kilidini tekrar nasıl açabilirim?

 Kullanabilirsiniz`SetStyle` ile yöntem`IsLocked` ayarlanır`false` hücrelerin kilidini açmak için.

#### Çalışma kitabına daha fazla çalışma sayfası ekleyebilir miyim?

 Evet, çalışma kitabına başka çalışma sayfalarını kullanarak ekleyebilirsiniz.`Worksheets.Add()`yöntemini kullanın ve her çalışma sayfası için hücre koruma adımlarını tekrarlayın.

#### Excel dosyasının kaydetme biçimini nasıl değiştirebilirim?

 Kaydetme formatını kullanarak değiştirebilirsiniz.`SaveFormat` İstenilen formatta yöntem, örneğin`SaveFormat.Xlsx` Excel 2007 ve sonrası için.