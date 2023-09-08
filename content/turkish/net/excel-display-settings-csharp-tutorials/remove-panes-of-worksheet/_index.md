---
title: Çalışma Sayfasının Bölmelerini Kaldır
linktitle: Çalışma Sayfasının Bölmelerini Kaldır
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasındaki bölmeleri kaldırmak için adım adım kılavuz.
type: docs
weight: 120
url: /tr/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
Bu eğitimde Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasındaki bölmelerin nasıl kaldırılacağını açıklayacağız. İstenilen sonucu elde etmek için şu adımları izleyin:

## 1. Adım: Ortamı ayarlama

Aspose.Cells for .NET'i kurduğunuzdan ve geliştirme ortamınızı kurduğunuzdan emin olun. Ayrıca bölmeleri kaldırmak istediğiniz Excel dosyasının bir kopyasına sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli bağımlılıkları içe aktarın

Aspose.Cells'teki sınıfları kullanmak için gerekli yönergeleri ekleyin:

```csharp
using Aspose.Cells;
```

## 3. Adım: Kodun başlatılması

Excel belgelerinizi içeren dizinin yolunu başlatarak başlayın:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Adım 4: Excel dosyasını açma

 Yeni bir örnek oluştur`Workbook` nesneyi kullanın ve Excel dosyasını kullanarak açın.`Open` yöntem:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Adım 5: Etkin hücreyi tanımlayın

 Çalışma sayfasının etkin hücresini kullanarak ayarlayın.`ActiveCell` mülk:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Adım 6: Bölmeleri silme

 kullanarak çalışma sayfası penceresinden bölmeleri kaldırın.`RemoveSplit` yöntem:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Adım 7: Değişiklikleri Kaydetme

Excel dosyasına yapılan değişiklikleri kaydedin:

```csharp
book.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET kullanarak Çalışma Sayfasının Bölmelerini Kaldırmak için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Yeni bir çalışma kitabı oluşturun ve bir şablon dosyası açın
Workbook book = new Workbook(dataDir + "Book1.xls");
// Aktif hücreyi ayarla
book.Worksheets[0].ActiveCell = "A20";
// Çalışma sayfası penceresini bölme
book.Worksheets[0].RemoveSplit();
// Excel dosyasını kaydedin
book.Save(dataDir + "output.xls");
```

## Çözüm

Bu eğitimde Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasındaki bölmeleri nasıl kaldıracağınızı öğrendiniz. Açıklanan adımları izleyerek Excel dosyalarınızın görünümünü ve davranışını kolayca özelleştirebilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını işlemek için kullanılan popüler bir yazılım kütüphanesidir.

#### Aspose.Cells'te bir çalışma sayfasının aktif hücresini nasıl ayarlayabilirim?

 Etkin hücreyi kullanarak ayarlayabilirsiniz.`ActiveCell`Çalışma Sayfası nesnesinin özelliği.

#### Çalışma sayfası penceresinden yalnızca yatay veya dikey bölmeleri kaldırabilir miyim?

 Evet, Aspose.Cells'i kullanarak aşağıdaki gibi uygun yöntemleri kullanarak yalnızca yatay veya dikey bölmeleri kaldırabilirsiniz.`RemoveHorizontalSplit` veya`RemoveVerticalSplit`.

#### Aspose.Cells yalnızca .xls formatındaki Excel dosyalarıyla mı çalışır?

Hayır, Aspose.Cells .xls ve .xlsx dahil olmak üzere çeşitli Excel dosya formatlarını destekler.
	