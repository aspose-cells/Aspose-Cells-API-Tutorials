---
title: Excel Çalışma Sayfasında Satırı Koru
linktitle: Excel Çalışma Sayfasında Satırı Koru
second_title: Aspose.Cells for .NET API Referansı
description: Bu eğitimde Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunun satırlarını nasıl koruyacağınızı keşfedin. C# ile adım adım öğretici.
type: docs
weight: 60
url: /tr/net/protect-excel-file/protect-row-in-excel-worksheet/
---
Bu öğreticide, bir Excel elektronik tablosundaki satırları korumak için Aspose.Cells kitaplığını kullanan bazı C# kaynak kodlarına bakacağız. Kodun her adımını inceleyeceğiz ve nasıl çalıştığını açıklayacağız. İstenen sonuçları elde etmek için talimatları dikkatlice izleyin.

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

Bu adımda, elektronik tablonun satırlarına uygulanacak stili tanımlayacağız. Aşağıdaki kodu kullanın:

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

## Adım 7: İlk satırı kilitleme

Bu adımda, çalışma sayfasının ilk satırını kilitleyeceğiz. Aşağıdaki kodu kullanın:

```csharp
// İlk satırın stilini alın.
style = sheet.Cells.Rows[0].Style;
// Stili kilitle.
style. IsLocked = true;
// Stili ilk satıra uygulayın.
sheet.Cells.ApplyRowStyle(0, style);
```

## 8. Adım: Çalışma sayfasını koruma

Stilleri ayarlayıp satırları kilitlediğimize göre, e-tabloyu korumaya geçelim. Aşağıdaki kodu kullanın:

```csharp
// Çalışma sayfasını koruyun.
sheet.Protect(ProtectionType.All);
```

## 9. Adım: Excel dosyasını kaydetme

Son olarak, değiştirilen Excel dosyasını kaydedeceğiz. Aşağıdaki kodu kullanın:

```csharp
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Değiştirilen Excel dosyasını kaydetmek için doğru yolu belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanan Excel Çalışma Sayfasında Satırı Koru için örnek kaynak kodu 
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
// styleflag nesnesini tanımlayın.
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

Tebrikler! Artık Aspose.Cells library for .NET'i kullanarak bir Excel elektronik tablosundaki satırları korumanıza izin veren C# kaynak koduna sahipsiniz. Adımları dikkatli bir şekilde uyguladığınızdan ve kodu özel ihtiyaçlarınıza göre özelleştirdiğinizden emin olun.

### SSS (Sıkça Sorulan Sorular)

#### Bu kod, Excel'in son sürümleriyle çalışır mı?

Evet, bu kod, Excel 2010 ve üzeri formattaki dosyalar dahil olmak üzere Excel'in son sürümleriyle çalışır.

#### Çalışma sayfasındaki tüm satırlar yerine yalnızca belirli satırları koruyabilir miyim?

Evet, korumak istediğiniz belirli satırları belirtmek için kodu değiştirebilirsiniz. Döngüyü ve indeksleri buna göre ayarlamanız gerekecektir.

#### Kilitli hatları tekrar nasıl açabilirim?

 kullanabilirsiniz`IsLocked` yöntemi`Style` değeri ayarlamak için nesne`false` ve satırların kilidini açın.

#### Aynı Excel çalışma kitabında birden çok çalışma sayfasını korumak mümkün müdür?

Evet, çalışma kitabı oluşturma, stil belirleme ve koruma adımlarını çalışma kitabındaki her çalışma sayfası için tekrarlayabilirsiniz.

#### Elektronik tablo koruma parolasını nasıl değiştirebilirim?

 kullanarak parolayı değiştirebilirsiniz.`Protect` yöntem ve bağımsız değişken olarak yeni bir parola belirtmek.