---
title: İşleme İçin Çalışma Sayfasının Özel Kağıt Boyutunu Uygulayın
linktitle: İşleme İçin Çalışma Sayfasının Özel Kağıt Boyutunu Uygulayın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile özel çalışma sayfası boyutunu uygulamaya yönelik adım adım kılavuz. Boyutları ayarlayın, bir mesaj ekleyin ve PDF olarak kaydedin.
type: docs
weight: 50
url: /tr/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Çalışma sayfanız için özel bir boyut uygulamak, belirli bir boyutta bir PDF belgesi oluşturmak istediğinizde çok yararlı olabilir. Bu öğreticide, Aspose.Cells for .NET'i kullanarak bir çalışma sayfası için özel bir boyut belirlemeyi ve ardından belgeyi PDF olarak kaydetmeyi öğreneceğiz.

## 1. Adım: Çıktı klasörünü oluşturma

Başlamadan önce, oluşturulan PDF dosyasının kaydedileceği bir çıktı klasörü oluşturmanız gerekir. Çıktı klasörünüz için istediğiniz yolu kullanabilirsiniz.

```csharp
// Çıkış dizinleri
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Çıktı klasörünüze giden doğru yolu belirttiğinizden emin olun.

## Adım 2: Çalışma Kitabı nesnesini oluşturma

Başlamak için Aspose.Cells'i kullanarak bir Çalışma Kitabı nesnesi oluşturmanız gerekir. Bu nesne elektronik tablonuzu temsil eder.

```csharp
// Çalışma Kitabı nesnesini oluşturma
Workbook wb = new Workbook();
```

## 3. Adım: İlk çalışma sayfasına erişim

Çalışma Kitabı nesnesini oluşturduktan sonra, içindeki ilk çalışma sayfasına erişebilirsiniz.

```csharp
// İlk çalışma sayfasına erişim
Worksheet ws = wb.Worksheets[0];
```

## 4. Adım: Özel çalışma sayfası boyutunu ayarlama

 Artık kullanarak özel çalışma sayfası boyutunu ayarlayabilirsiniz.`CustomPaperSize(width, height)` PageSetup sınıfının yöntemi.

```csharp
// Özel çalışma sayfası boyutunu ayarlayın (inç olarak)
ws.PageSetup.CustomPaperSize(6, 4);
```

Bu örnekte, çalışma sayfası boyutunu 6 inç genişliğinde ve 4 inç yüksekliğinde ayarladık.

## 5. Adım: B4 hücresine erişim

Bundan sonra, çalışma sayfasındaki belirli bir hücreye erişebiliriz. Bu durumda, B4 hücresine erişeceğiz.

```csharp
// B4 hücresine erişim
Cell b4 = ws.Cells["B4"];
```

## Adım 6: B4 hücresine mesaj ekleme

 Artık B4 hücresine şunu kullanarak bir mesaj ekleyebiliriz:`PutValue(value)` yöntem.

```csharp
// B4 hücresindeki mesajı ekleyin
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

Bu örnekte, B4 hücresine "PDF Sayfa Boyutu: 6.00" x 4.00" mesajını ekledik.

## 7. Adım: Çalışma sayfasını PDF formatında kaydetme

 Son olarak, çalışma sayfasını kullanarak PDF formatında kaydedebiliriz.`Save(filePath)` Workbook nesnesinin yöntemi.

```csharp
// Çalışma sayfasını PDF formatında kaydedin
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Daha önce oluşturulan çıktı klasörünü kullanarak, oluşturulan PDF dosyasına giden istenen yolu belirtin.

### Aspose.Cells for .NET kullanarak İşleme İçin Özel Kağıt Boyutu Çalışma Sayfası Uygulamak için örnek kaynak kodu 
```csharp
//Çıkış dizini
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//çalışma kitabı nesnesi oluştur
Workbook wb = new Workbook();
//İlk çalışma sayfasına erişin
Worksheet ws = wb.Worksheets[0];
//Özel kağıt boyutunu inç cinsinden ayarlayın
ws.PageSetup.CustomPaperSize(6, 4);
//B4 hücresine erişim
Cell b4 = ws.Cells["B4"];
//B4 hücresindeki mesajı ekleyin
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Çalışma kitabını pdf formatında kaydedin
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Sonuçlar

Bu öğreticide, Aspose.Cells for .NET kullanarak bir çalışma sayfasının özel boyutunu nasıl uygulayacağınızı öğrendiniz. Çalışma sayfalarınız için belirli boyutları ayarlamak ve ardından belgeleri PDF formatında kaydetmek için bu adımları kullanabilirsiniz. Bu kılavuzun, özel bir e-tablo boyutu uygulama sürecini anlamada yardımcı olduğunu umuyoruz.

### Sık Sorulan Sorular (SSS)

#### Soru 1: Elektronik tablo düzenini daha da özelleştirebilir miyim?

Evet, Aspose.Cells, çalışma sayfası düzeninizi kişiselleştirmek için birçok seçenek sunar. Özel boyutları, sayfa yönlendirmesini, kenar boşluklarını, üst bilgileri ve alt bilgileri ve çok daha fazlasını ayarlayabilirsiniz.

#### Soru 2: Aspose.Cells başka hangi çıktı formatlarını destekliyor?

Aspose.Cells, PDF, XLSX, XLS, CSV, HTML, TXT ve çok daha fazlasını içeren birçok farklı çıktı biçimini destekler. İhtiyaçlarınıza göre istediğiniz çıktı formatını seçebilirsiniz.