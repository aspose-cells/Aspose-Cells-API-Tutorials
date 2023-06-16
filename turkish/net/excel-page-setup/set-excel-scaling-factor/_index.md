---
title: Excel Ölçeklendirme Faktörünü Ayarla
linktitle: Excel Ölçeklendirme Faktörünü Ayarla
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel dosyalarını kolayca değiştirmeyi ve ölçekleme faktörünü özelleştirmeyi öğrenin.
type: docs
weight: 180
url: /tr/net/excel-page-setup/set-excel-scaling-factor/
---
Bu kılavuzda, Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunda ölçekleme faktörünü nasıl ayarlayacağınız konusunda size yol göstereceğiz. Bu görevi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Ortamı ayarlama

Geliştirme ortamınızı kurduğunuzdan ve Aspose.Cells for .NET'i kurduğunuzdan emin olun. Kütüphanenin en son sürümünü Aspose resmi web sitesinden indirebilirsiniz.

## 2. Adım: Gerekli ad alanlarını içe aktarın

C# projenizde, Aspose.Cells ile çalışmak için gerekli ad alanlarını içe aktarın:

```csharp
using Aspose.Cells;
```

## 3. Adım: Belgeler dizinine giden yolu ayarlama

 ilan etmek`dataDir` oluşturulan Excel dosyasını kaydetmek istediğiniz dizinin yolunu belirtmek için değişken:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 değiştirdiğinizden emin olun`"YOUR_DOCUMENT_DIRECTORY"` sisteminizdeki doğru yol ile.

## 4. Adım: Çalışma Kitabı Nesnesi Oluşturma

Oluşturmak istediğiniz Excel çalışma kitabını temsil eden bir Çalışma Kitabı nesnesi örneği oluşturun:

```csharp
Workbook workbook = new Workbook();
```

## Adım 5: İlk çalışma sayfasına erişim

Aşağıdaki kodu kullanarak Excel çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 6. Adım: Ölçeklendirme Faktörünü Ayarlayın

Aşağıdaki kodu kullanarak ölçeklendirme faktörünü ayarlayın:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Burada ölçekleme faktörünü 100 olarak ayarladık, bu, elektronik tablo yazdırıldığında normal boyutun %100'ünde görüntüleneceği anlamına gelir.

## 7. Adım: Excel çalışma kitabını kaydetme

 Excel çalışma kitabını tanımlanan ölçekleme faktörüyle kaydetmek için,`Save` Çalışma Kitabı nesnesinin yöntemi:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Bu, Excel çalışma kitabını "ScalingFactor_out.xls" dosya adıyla belirtilen dizine kaydedecektir.

### Aspose.Cells for .NET kullanarak Set Excel Scaling Factor için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook workbook = new Workbook();
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = workbook.Worksheets[0];
// Ölçekleme faktörünü 100 olarak ayarlama
worksheet.PageSetup.Zoom = 100;
// Çalışma kitabını kaydedin.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunda ölçeklendirme faktörünün nasıl ayarlanacağını öğrendiniz. Ölçekleme faktörü, en uygun görüntü için yazdırırken hesap tablosunun boyutunu ayarlamanıza olanak tanır.

### SSS

#### 1. Aspose.Cells for .NET ile Excel elektronik tablosunda ölçekleme faktörü nasıl ayarlanır?

 Kullan`Zoom` mülkiyeti`PageSetup`Ölçekleme faktörünü ayarlamak için nesne. Örneğin,`worksheet.PageSetup.Zoom = 100;` ölçeklendirme faktörünü %100 olarak ayarlayacaktır.

#### 2. Ölçeklendirme faktörünü ihtiyaçlarıma göre özelleştirebilir miyim?

 Evet, ölçeklendirme faktörüne atanan değeri değiştirerek ölçekleme faktörünü ayarlayabilirsiniz.`Zoom` mülk. Örneğin,`worksheet.PageSetup.Zoom = 75;` ölçeklendirme faktörünü %75 olarak ayarlayacaktır.

#### 3. Excel çalışma kitabını tanımlanan ölçekleme faktörü ile kaydetmek mümkün müdür?

 Evet, kullanabilirsiniz`Save` yöntemi`Workbook` Excel çalışma kitabını tanımlanan ölçeklendirme faktörüyle kaydetmek için nesne.