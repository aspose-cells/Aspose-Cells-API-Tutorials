---
title: E-tablo Sekmesini Görüntüle
linktitle: E-tablo Sekmesini Görüntüle
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak bir Excel elektronik tablosu sekmesi görüntüleyin.
type: docs
weight: 60
url: /tr/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
Bu öğreticide, Aspose.Cells for .NET ile C# kaynak kodunu kullanarak bir Excel çalışma sayfasının sekmesini nasıl görüntüleyeceğinizi göstereceğiz. İstediğiniz sonucu elde etmek için aşağıdaki adımları izleyin.

## 1. Adım: Gerekli kitaplıkları içe aktarın

.NET için Aspose.Cells kitaplığını kurduğunuzdan ve gerekli kitaplıkları C# projenize aktardığınızdan emin olun.

```csharp
using Aspose.Cells;
```

## 2. Adım: Dizin yolunu ayarlayın ve Excel dosyasını açın

 Excel dosyanızı içeren dizinin yolunu ayarlayın, ardından bir örnek oluşturarak dosyayı açın.`Workbook` nesne.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## 3. Adım: Çalışma sayfası sekmesini gösterin

 Kullan`ShowTabs` mülkiyeti`Workbook.Settings` Excel çalışma sayfası sekmesini göstermek için nesne.

```csharp
workbook.Settings.ShowTabs = true;
```

## 4. Adım: Değişiklikleri Kaydet

 Gerekli değişiklikleri yaptıktan sonra, değiştirilen Excel dosyasını kullanarak kaydedin.`Save` yöntemi`Workbook` nesne.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET kullanan Elektronik Tablo Sekmesini Görüntülemek için örnek kaynak kodu 

```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
// Excel dosyasını açma
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Excel dosyasının sekmelerini gizleme
workbook.Settings.ShowTabs = true;
// Değiştirilen Excel dosyasını kaydetme
workbook.Save(dataDir + "output.xls");
```

### Çözüm

Bu adım adım kılavuz, Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunun sekmesini nasıl göstereceğinizi gösterdi. Sağlanan C# kaynak kodunu kullanarak, Excel dosyalarınızdaki sekmelerin görünümünü kolayca özelleştirebilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını işlemek için güçlü bir kitaplıktır.

#### Aspose.Cells for .NET'i nasıl kurabilirim?

 Aspose.Cells for .NET'i kurmak için ilgili paketi adresinden indirmeniz gerekir.[Bültenler](https://releases/aspose.com/cells/net/) ve .NET projenize ekleyin.

#### Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunun sekmesi nasıl görüntülenir?

 kullanabilirsiniz`ShowTabs` mülkiyeti`Workbook.Settings` nesne ve onu ayarla`true` çalışma sayfası sekmesini göstermek için

#### Aspose.Cells for .NET başka hangi Excel dosya formatlarını destekliyor?

Aspose.Cells for .NET, XLS, XLSX, CSV, HTML, PDF vb. gibi çeşitli Excel dosya formatlarını destekler.
