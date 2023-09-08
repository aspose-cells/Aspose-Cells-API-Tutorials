---
title: Çalışma Sayfasının Bölmelerini Dondur
linktitle: Çalışma Sayfasının Bölmelerini Dondur
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel çalışma sayfasının dondurulan bölmelerini kolayca yönetin.
type: docs
weight: 70
url: /tr/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
Bu eğitimde, Aspose.Cells for .NET ile C# kaynak kodunu kullanarak bir Excel çalışma sayfasındaki bölmeleri nasıl kilitleyeceğinizi göstereceğiz. İstediğiniz sonucu elde etmek için aşağıdaki adımları izleyin.

## 1. Adım: Gerekli kitaplıkları içe aktarın

.NET için Aspose.Cells kütüphanesini kurduğunuzdan emin olun ve gerekli kütüphaneleri C# projenize aktarın.

```csharp
using Aspose.Cells;
```

## Adım 2: Dizin yolunu ayarlayın ve Excel dosyasını açın

 Excel dosyanızı içeren dizinin yolunu ayarlayın, ardından bir örnek oluşturarak dosyayı açın.`Workbook` nesne.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 3. Adım: Elektronik tabloya gidin ve bölme kilidi ayarlarını uygulayın

 kullanarak Excel dosyasındaki ilk çalışma sayfasına gidin.`Worksheet` nesne. Daha sonra şunu kullanın:`FreezePanes` bölme kilidi ayarlarını uygulama yöntemi.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Yukarıdaki örnekte bölmeler 3. satır ve 2. sütundaki hücreye kilitlenmiştir.

## 4. Adım: Değişiklikleri Kaydet

 Gerekli değişiklikleri yaptıktan sonra, değiştirilen Excel dosyasını kullanarak kaydedin.`Save` yöntemi`Workbook` nesne.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET kullanan Çalışma Sayfalarının Dondurulması için örnek kaynak kodu 

```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
// Excel dosyasını dosya akışı aracılığıyla açma
Workbook workbook = new Workbook(fstream);
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = workbook.Worksheets[0];
// Bölmeleri dondurma ayarlarını uygulama
worksheet.FreezePanes(3, 2, 3, 2);
// Değiştirilen Excel dosyasını kaydetme
workbook.Save(dataDir + "output.xls");
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Bu adım adım kılavuz, Aspose.Cells for .NET kullanarak bir Excel tablosundaki bölmeleri nasıl kilitleyeceğinizi gösterdi. Sağlanan C# kaynak kodunu kullanarak, Excel dosyalarındaki verilerinizi daha iyi düzenlemek ve görselleştirmek için bölme kilidi ayarlarını kolayca özelleştirebilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını işlemek için güçlü bir kütüphanedir.

#### Aspose.Cells for .NET'i nasıl kurabilirim?

 Aspose.Cells for .NET'i kurmak için ilgili paketi adresinden indirmeniz gerekmektedir.[Sürümleri Aspose](https://releases/aspose.com/cells/net/) ve bunu .NET projenize ekleyin.

#### Aspose.Cells for .NET kullanılarak Excel çalışma sayfasındaki bölmeler nasıl kilitlenir?

 Şunu kullanabilirsiniz:`FreezePanes` yöntemi`Worksheet` Bir çalışma sayfasının bölmelerini kilitlemek için nesne. Satır ve sütun dizinleri sağlayarak kilitlenecek hücreleri belirtin.

#### Aspose.Cells for .NET ile bölme kilidi ayarlarını özelleştirebilir miyim?

 Evet, kullanarak`FreezePanes` yöntemini kullanarak, uygun satır ve sütun dizinlerini sağlayarak, gerektiğinde hangi hücrelerin kilitleneceğini belirleyebilirsiniz.
