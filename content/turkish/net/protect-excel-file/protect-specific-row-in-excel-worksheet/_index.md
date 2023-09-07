---
title: Excel Çalışma Sayfasında Belirli Satırı Koru
linktitle: Excel Çalışma Sayfasında Belirli Satırı Koru
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel'de belirli bir satırı koruyun. Gizli verilerinizin güvenliğini sağlamak için adım adım kılavuz.
type: docs
weight: 90
url: /tr/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Bilgi güvenliğini sağlamak için bir Excel elektronik tablosundaki gizli verileri korumak çok önemlidir. Aspose.Cells for .NET, bir Excel elektronik tablosundaki belirli satırları korumak için güçlü bir çözüm sunar. Bu kılavuz, sağlanan C# kaynak kodunu kullanarak bir Excel çalışma sayfasındaki belirli bir satırı nasıl koruyacağınız konusunda size yol gösterecektir. Excel dosyalarınızda satır korumasını ayarlamak için bu basit adımları izleyin.

## 1. Adım: Gerekli kitaplıkları içe aktarın

Başlamak için sisteminizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Aspose.Cells'in işlevselliğini kullanabilmek için C# projenize uygun referansları da eklemeniz gerekir. İşte gerekli kitaplıkları içe aktarmak için kod:

```csharp
// Gerekli referansları ekleyin
using Aspose.Cells;
```

## 2. Adım: Bir Excel çalışma kitabı ve elektronik tablosu oluşturma

Gerekli kitaplıkları içe aktardıktan sonra, yeni bir Excel çalışma kitabı ve yeni bir çalışma sayfası oluşturabilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Halihazırda yoksa bir dizin oluşturun.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Yeni bir çalışma kitabı oluşturun.
Workbook wb = new Workbook();

// Bir elektronik tablo nesnesi oluşturun ve ilk sayfayı alın.
Worksheet sheet = wb.Worksheets[0];
```

## 3. Adım: Stili ve Stil Bayrağını Ayarlama

Şimdi, çalışma sayfasındaki tüm sütunların kilidini açmak için hücre stilini ve stil bayrağını ayarlayacağız. İşte gerekli kod:

```csharp
// Stil nesnesini ayarlayın.
Styling styling;

// styleflag nesnesini ayarlayın.
StyleFlag flag;

// Çalışma sayfasındaki tüm sütunlarda dolaşın ve bunların kilidini açın.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## 4. Adım: Belirli hattı koruyun

Şimdi çalışma sayfasındaki belirli satırı koruyacağız. Herhangi bir değişikliği önlemek için ilk satırı kilitleyeceğiz. İşte nasıl:

```csharp
// İlk satırın stilini alın.
style = sheet.Cells.Rows[0].Style;

// Kilitle.
style. IsLocked = true;

//Bayrağı somutlaştırın.
flag = new StyleFlag();

// Kilit parametresini ayarlayın.
flag. Locked = true;

// Stili ilk satıra uygulayın.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## 5. Adım: Çalışma sayfasını koruma

Son olarak, izinsiz değişiklik yapılmasını önlemek için Excel çalışma sayfasının tamamını koruyacağız. İşte nasıl:

```csharp
// Çalışma sayfasını koruyun.
sheet.Protect(ProtectionType.All);
```

## 6. Adım: Korumalı Excel dosyasını kaydedin

Excel çalışma sayfasındaki belirli satırı korumayı bitirdiğinizde, korunan Excel dosyasını sisteminize kaydedebilirsiniz. İşte nasıl:

```csharp
// Excel dosyasını kaydedin.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Bu adımları izledikten sonra, Aspose.Cells for .NET'i kullanarak Excel çalışma tablonuzdaki belirli bir satırı başarıyla korumuş olacaksınız.

### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfasında Belirli Satırı Koru için örnek kaynak kodu 
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

Excel dosyalarındaki verileri korumak, yetkisiz erişimi veya istenmeyen değişiklikleri önlemek için çok önemlidir. Aspose.Cells library for .NET'i kullanarak, sağlanan C# kaynak kodunu kullanarak bir Excel elektronik tablosundaki belirli satırları kolayca koruyabilirsiniz. Excel dosyalarınıza fazladan bir güvenlik katmanı eklemek için bu adım adım kılavuzu izleyin.

### SSS

#### Belirli satır koruması Excel'in tüm sürümlerinde çalışır mı?

Evet, Aspose.Cells for .NET kullanan belirli satır koruması, Excel'in desteklenen tüm sürümlerinde çalışır.

#### Bir Excel elektronik tablosundaki birden çok belirli satırı koruyabilir miyim?

Evet, bu kılavuzda açıklanan benzer yöntemleri kullanarak birden çok belirli satırı koruyabilirsiniz.

#### Bir Excel elektronik tablosundaki belirli bir satırın kilidini nasıl açabilirim?

 Belirli bir satırın kilidini açmak için kaynak kodunu kullanarak uygun şekilde değiştirmelisiniz.`IsLocked` yöntemi`Style` nesne.