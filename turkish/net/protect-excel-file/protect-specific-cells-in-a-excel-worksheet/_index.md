---
title: Bir Excel Çalışma Sayfasında Belirli Hücreleri Koruyun
linktitle: Bir Excel Çalışma Sayfasında Belirli Hücreleri Koruyun
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel'de belirli hücreleri nasıl koruyacağınızı öğrenin. C# ile adım adım öğretici.
type: docs
weight: 70
url: /tr/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
Bu eğitimde, bir Excel elektronik tablosundaki belirli hücreleri korumak için Aspose.Cells kitaplığını kullanan C# kaynak koduna bakacağız. Kodun her adımını inceleyeceğiz ve nasıl çalıştığını açıklayacağız. İstenen sonuçları elde etmek için talimatları dikkatlice izleyin.

## 1. Adım: Önkoşullar

Başlamadan önce, .NET için Aspose.Cells kitaplığını kurduğunuzdan emin olun. Aspose resmi sitesinden temin edebilirsiniz. Ayrıca, Visual Studio'nun veya başka herhangi bir C# geliştirme ortamının yeni bir sürümüne sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells kütüphanesini kullanmak için gerekli namespace'leri kodumuza import etmemiz gerekiyor. C# kaynak dosyanızın en üstüne aşağıdaki satırları ekleyin:

```csharp
using Aspose.Cells;
```

## 3. Adım: Excel çalışma kitabı oluşturma

Bu adımda, yeni bir Excel çalışma kitabı oluşturacağız. Bir Excel çalışma kitabı oluşturmak için aşağıdaki kodu kullanın:

```csharp
// Belgeler dizinine giden yol.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Yeni bir çalışma kitabı oluşturun.
Workbook wb = new Workbook();
```

 değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIR"` belgeler dizininize uygun yolla.

## 4. Adım: Bir e-tablo oluşturma

Artık Excel çalışma kitabını oluşturduğumuza göre, bir çalışma sayfası oluşturalım ve ilk sayfayı alalım. Aşağıdaki kodu kullanın:

```csharp
// Bir elektronik tablo nesnesi oluşturun ve ilk sayfayı alın.
Worksheet sheet = wb.Worksheets[0];
```

## Adım 5: Stili Tanımlama

Bu adımda, belirli hücrelere uygulanacak stili tanımlayacağız. Aşağıdaki kodu kullanın:

```csharp
// Stil nesnesinin tanımı.
Styling styling;
```

## 6. Adım: Tüm sütunların kilidini açmak için döngü yapın

Şimdi çalışma sayfasındaki tüm sütunları dolaşıp kilidini açacağız. Aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasındaki tüm sütunlarda dolaşın ve bunların kilidini açın.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## 7. Adım: Belirli Hücreleri Kilitleme

Bu adımda, belirli hücreleri kilitleyeceğiz. Aşağıdaki kodu kullanın:

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

## 8. Adım: Çalışma sayfasını koruma

Son olarak, belirli hücrelerin değiştirilmesini önlemek için çalışma sayfasını koruyacağız. Aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasını koruyun.
sheet.Protect(ProtectionType.All);
```

## 9. Adım: Excel dosyasını kaydetme

Şimdi değiştirilmiş Excel dosyasını kaydedeceğiz. Aşağıdaki kodu kullanın:

```csharp
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Değiştirilen Excel dosyasını kaydetmek için doğru yolu belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Bir Excel Çalışma Sayfasında Belirli Hücreleri Koru için örnek kaynak kodu 
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
// styleflag nesnesini tanımlayın
StyleFlag styleflag;
// Çalışma sayfasındaki tüm sütunlarda dolaşın ve bunların kilidini açın.
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
//Son olarak, sayfayı şimdi koruyun.
sheet.Protect(ProtectionType.All);
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Çözüm

Tebrikler! Artık, Aspose.Cells for .NET kitaplığını kullanarak bir Excel çalışma sayfasındaki belirli hücreleri korumanıza izin veren C# kaynak koduna sahipsiniz. Kodu özel ihtiyaçlarınıza uyacak şekilde özelleştirmekten çekinmeyin.

### SSS (Sıkça Sorulan Sorular)

#### Bu kod, Excel'in son sürümleriyle çalışır mı?

Evet, bu kod, Excel 2010 ve üzeri formattaki dosyalar dahil olmak üzere Excel'in son sürümleriyle çalışır.

#### A1, B1 ve C1 dışındaki hücreleri koruyabilir miyim?

Evet, karşılık gelen kod satırlarındaki hücre referanslarını ayarlayarak diğer belirli hücreleri kilitlemek için kodu değiştirebilirsiniz.

#### Kilitli hücrelerin kilidini tekrar nasıl açabilirim?

 Kullanabilirsiniz`SetStyle` ile yöntem`IsLocked` ayarlanır`false` hücrelerin kilidini açmak için.

#### Çalışma kitabına daha fazla çalışma sayfası ekleyebilir miyim?

 Evet, çalışma kitabına başka çalışma sayfaları ekleyebilirsiniz.`Worksheets.Add()`yöntemini seçin ve her çalışma sayfası için hücre koruma adımlarını tekrarlayın.

#### Excel dosyasının kaydetme biçimini nasıl değiştirebilirim?

 kullanarak kaydetme biçimini değiştirebilirsiniz.`SaveFormat` İstenilen formatta yöntem, örneğin`SaveFormat.Xlsx` Excel 2007 ve sonrası için.