---
title: İşleme İçin Çalışma Sayfasının Özel Kağıt Boyutunu Uygulama
linktitle: İşleme İçin Çalışma Sayfasının Özel Kağıt Boyutunu Uygulama
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile özel çalışma sayfası boyutunu uygulamaya yönelik adım adım kılavuz. Boyutları ayarlayın, bir mesaj ekleyin ve PDF olarak kaydedin.
type: docs
weight: 50
url: /tr/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Belirli bir boyutta bir PDF belgesi oluşturmak istediğinizde, çalışma sayfanız için özel bir boyut uygulamak çok yararlı olabilir. Bu eğitimde, Aspose.Cells for .NET'i kullanarak bir çalışma sayfası için özel boyut ayarlamayı ve ardından belgeyi PDF olarak kaydetmeyi öğreneceğiz.

## Adım 1: Çıkış klasörünü oluşturma

Başlamadan önce, oluşturulan PDF dosyasının kaydedileceği bir çıktı klasörü oluşturmanız gerekir. Çıktı klasörünüz için istediğiniz yolu kullanabilirsiniz.

```csharp
// Çıkış dizinleri
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Çıkış klasörünüzün doğru yolunu belirttiğinizden emin olun.

## Adım 2: Çalışma Kitabı nesnesini oluşturma

Başlamak için Aspose.Cells'i kullanarak bir Workbook nesnesi oluşturmanız gerekir. Bu nesne e-tablonuzu temsil eder.

```csharp
// Çalışma Kitabı nesnesini oluşturma
Workbook wb = new Workbook();
```

## 3. Adım: İlk çalışma sayfasına erişim

Çalışma Kitabı nesnesini oluşturduktan sonra içindeki ilk çalışma sayfasına erişebilirsiniz.

```csharp
// İlk çalışma sayfasına erişim
Worksheet ws = wb.Worksheets[0];
```

## 4. Adım: Özel çalışma sayfası boyutunu ayarlama

 Artık özel çalışma sayfası boyutunu kullanarak ayarlayabilirsiniz.`CustomPaperSize(width, height)` PageSetup sınıfının yöntemi.

```csharp
// Özel çalışma sayfası boyutunu ayarlayın (inç cinsinden)
ws.PageSetup.CustomPaperSize(6, 4);
```

Bu örnekte çalışma sayfası boyutunu 6 inç genişliğinde ve 4 inç yüksekliğinde olacak şekilde ayarladık.

## Adım 5: B4 hücresine erişim

Bundan sonra çalışma sayfasındaki belirli bir hücreye erişebiliriz. Bu durumda B4 hücresine erişeceğiz.

```csharp
// B4 hücresine erişim
Cell b4 = ws.Cells["B4"];
```

## Adım 6: Mesajı B4 hücresine ekleme

 Artık B4 hücresine aşağıdaki komutu kullanarak bir mesaj ekleyebiliriz:`PutValue(value)` yöntem.

```csharp
// Mesajı B4 hücresine ekleyin
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

Bu örnekte B4 hücresine "PDF Sayfa Boyutu: 6,00" x 4,00" mesajını ekledik.

## Adım 7: Çalışma sayfasını PDF formatında kaydetme

 Son olarak çalışma sayfasını PDF formatında kaydedebiliriz.`Save(filePath)` Çalışma Kitabı nesnesinin yöntemi.

```csharp
// Çalışma sayfasını PDF formatında kaydedin
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Daha önce oluşturulan çıktı klasörünü kullanarak, oluşturulan PDF dosyasının istenen yolunu belirtin.

### Aspose.Cells for .NET Kullanarak İşleme İçin Çalışma Sayfasının Özel Kağıt Boyutunu Uygulamak için örnek kaynak kodu 
```csharp
//Çıkış dizini
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Çalışma kitabı nesnesi oluştur
Workbook wb = new Workbook();
//İlk çalışma sayfasına erişin
Worksheet ws = wb.Worksheets[0];
//Özel kağıt boyutunu inç cinsinden ayarlayın
ws.PageSetup.CustomPaperSize(6, 4);
//B4 hücresine erişim
Cell b4 = ws.Cells["B4"];
//Mesajı B4 hücresine ekleyin
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Çalışma kitabını pdf formatında kaydedin
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Sonuçlar

Bu eğitimde Aspose.Cells for .NET kullanarak özel çalışma sayfası boyutunun nasıl uygulanacağını öğrendiniz. Çalışma sayfalarınız için belirli boyutları ayarlamak ve ardından belgeleri PDF formatında kaydetmek için bu adımları kullanabilirsiniz. Bu kılavuzun, özel bir e-tablo boyutunu uygulama sürecini anlamada yardımcı olduğunu umuyoruz.

### Sık Sorulan Sorular (SSS)

#### Soru 1: Elektronik tablo düzenini daha da özelleştirebilir miyim?

Evet, Aspose.Cells çalışma sayfanızın düzenini kişiselleştirmeniz için birçok seçenek sunuyor. Özel boyutları, sayfa yönünü, kenar boşluklarını, üstbilgileri ve altbilgileri ve çok daha fazlasını ayarlayabilirsiniz.

#### Soru 2: Aspose.Cells başka hangi çıktı formatlarını destekliyor?

Aspose.Cells, PDF, XLSX, XLS, CSV, HTML, TXT ve çok daha fazlası dahil olmak üzere birçok farklı çıktı formatını destekler. İhtiyaçlarınıza göre istediğiniz çıktı formatını seçebilirsiniz.