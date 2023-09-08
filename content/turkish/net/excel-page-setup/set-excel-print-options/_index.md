---
title: Excel Yazdırma Seçeneklerini Ayarlama
linktitle: Excel Yazdırma Seçeneklerini Ayarlama
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak Excel dosyalarını yönetmeyi ve yazdırma seçeneklerini kolaylıkla özelleştirmeyi öğrenin.
type: docs
weight: 150
url: /tr/net/excel-page-setup/set-excel-print-options/
---
Bu kılavuzda, Aspose.Cells for .NET kullanarak bir Excel çalışma kitabının yazdırma seçeneklerini nasıl ayarlayacağınız konusunda size yol göstereceğiz. Bu görevi gerçekleştirmek için size sağlanan C# kaynak kodunu adım adım anlatacağız.

## 1. Adım: Ortamı ayarlama

Başlamadan önce geliştirme ortamınızı kurduğunuzdan ve Aspose.Cells for .NET'i kurduğunuzdan emin olun. Kütüphanenin son sürümünü Aspose resmi web sitesinden indirebilirsiniz.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells ile çalışmak için C# projenize gerekli ad alanlarını içe aktarın:

```csharp
using Aspose.Cells;
```

## 3. Adım: Belgeler dizininin yolunu ayarlama

 bir beyan`dataDir` Oluşturulan Excel dosyasını kaydetmek istediğiniz dizinin yolunu belirtmek için değişken:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Değiştirdiğinizden emin olun`"YOUR_DOCUMENT_DIRECTORY"` sisteminizde doğru yolla.

## Adım 4: Çalışma Kitabı Nesnesi Oluşturma

Oluşturmak istediğiniz Excel çalışma kitabını temsil eden bir Çalışma Kitabı nesnesinin örneğini oluşturun:

```csharp
Workbook workbook = new Workbook();
```

## Adım 5: Çalışma sayfasının PageSetup referansını alma

Yazdırma seçeneklerini ayarlamak için öncelikle çalışma sayfasından PageSetup referansını almamız gerekiyor. Referansı almak için aşağıdaki kodu kullanın:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Adım 6: Kılavuz Çizgilerini Yazdırmayı Etkinleştirin

Kılavuz çizgilerinin yazdırılmasını etkinleştirmek için aşağıdaki kodu kullanın:

```csharp
pageSetup. PrintGridlines = true;
```

## Adım 7: Satır/Sütun Başlığı Yazdırmayı Etkinleştirin

Satır ve sütun başlıklarının yazdırılmasını etkinleştirmek için aşağıdaki kodu kullanın:

```csharp
pageSetup.PrintHeadings = true;
```

## Adım 8: Siyah Beyaz Yazdırma Modunu Etkinleştirme

Çalışma sayfasının siyah beyaz modda yazdırılmasını etkinleştirmek için aşağıdaki kodu kullanın:

```csharp
pageSetup.BlackAndWhite = true;
```

## Adım 9: Geri Bildirimli Yazdırmayı Etkinleştirme

Yorumların e-tabloda göründükleri şekilde yazdırılmasına izin vermek için aşağıdaki kodu kullanın:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Adım 10: Taslak Modunda Yazdırmayı Etkinleştirin

Elektronik tablonun taslak modunda yazdırılmasını etkinleştirmek için aşağıdaki kodu kullanın:

```csharp
pageSetup.PrintDraft = true;
```

## Adım 11: Hücre Hatalarını Yok Olarak Yazdırmayı Etkinleştirin

Hücre hatalarının şu şekilde yazdırılmasına izin vermek için:

  Yok'tan ziyade aşağıdaki kodu kullanın:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Adım 12: Excel çalışma kitabını kaydetme

 Excel çalışma kitabını yazdırma seçenekleri ayarlı olarak kaydetmek için`Save` Çalışma Kitabı nesnesinin yöntemi:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Bu, Excel çalışma kitabını "OtherPrintOptions_out.xls" dosya adıyla belirtilen dizine kaydedecektir.

### Aspose.Cells for .NET kullanarak Excel Yazdırma Seçeneklerini Ayarlama için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook workbook = new Workbook();
// Çalışma sayfasının PageSetup referansının alınması
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Kılavuz çizgilerini yazdırmaya izin verme
pageSetup.PrintGridlines = true;
// Satır/sütun başlıklarının yazdırılmasına izin verilmesi
pageSetup.PrintHeadings = true;
// Çalışma sayfasının siyah beyaz modda yazdırılmasına izin verilmesi
pageSetup.BlackAndWhite = true;
// Yorumların çalışma sayfasında görüntülendiği şekilde yazdırılmasına izin verilmesi
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Taslak kalitesinde çalışma sayfasının yazdırılmasına izin verilmesi
pageSetup.PrintDraft = true;
// Hücre hatalarının Yok olarak yazdırılmasına izin veriliyor
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Çalışma kitabını kaydedin.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Çözüm

Artık Aspose.Cells for .NET kullanarak bir Excel çalışma kitabının yazdırma seçeneklerini nasıl ayarlayacağınızı öğrendiniz. Bu güçlü ve kullanıcı dostu kitaplık, Excel çalışma kitaplarınızın yazdırma ayarlarını kolay ve verimli bir şekilde özelleştirmenize olanak tanır.

### SSS


#### 1. Kenar boşlukları veya sayfa yönü gibi yazdırma seçeneklerini daha da özelleştirebilir miyim?

Evet, Aspose.Cells for .NET kenar boşlukları, sayfa yönü, ölçek vb. gibi çok çeşitli özelleştirilebilir yazdırma seçenekleri sunar.

#### 2. Aspose.Cells for .NET diğer Excel dosya formatlarını destekliyor mu?

Evet, Aspose.Cells for .NET, XLSX, XLS, CSV, HTML, PDF vb. gibi çeşitli Excel dosya formatlarını destekler.

#### 3. Aspose.Cells for .NET, .NET Framework'ün tüm sürümleriyle uyumlu mu?

Aspose.Cells for .NET, 3.5, 4.0, 4.5, 4.6 vb. sürümler de dahil olmak üzere .NET Framework 2.0 veya sonraki sürümleriyle uyumludur.