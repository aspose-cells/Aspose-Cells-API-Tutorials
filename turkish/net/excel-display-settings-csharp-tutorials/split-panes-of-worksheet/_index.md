---
title: Çalışma Sayfasının Bölme Bölmeleri
linktitle: Çalışma Sayfasının Bölme Bölmeleri
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasında bölmeleri bölmek için adım adım kılavuz.
type: docs
weight: 130
url: /tr/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
Bu eğitimde, Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasında bölmelerin nasıl bölüneceğini açıklayacağız. İstediğiniz sonucu elde etmek için şu adımları izleyin:

## 1. Adım: Ortamı ayarlama

Aspose.Cells for .NET'i kurduğunuzdan ve geliştirme ortamınızı kurduğunuzdan emin olun. Ayrıca bölmeleri bölmek istediğiniz Excel dosyasının bir kopyasına sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli bağımlılıkları içe aktarın

Aspose.Cells'ten sınıfları kullanmak için gerekli direktifleri ekleyin:

```csharp
using Aspose.Cells;
```

## 3. Adım: Kod başlatma

Excel belgelerinizi içeren dizinin yolunu başlatarak başlayın:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Adım 4: Excel dosyasını açma

 Yeni bir örnek oluştur`Workbook` nesnesini seçin ve Excel dosyasını kullanarak açın.`Open` yöntem:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Adım 5: Etkin hücreyi tanımlayın

 Çalışma sayfasının aktif hücresini kullanarak ayarlayın.`ActiveCell` mülk:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Adım 6: Kanatların bölünmesi

 Çalışma sayfası penceresini kullanarak bölme`Split` yöntem:

```csharp
book.Worksheets[0].Split();
```

## 7. Adım: Değişiklikleri Kaydetme

Excel dosyasında yapılan değişiklikleri kaydedin:

```csharp
book.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET kullanan Çalışma Sayfasının Bölünmüş Bölmeleri için örnek kaynak kodu 

```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Yeni bir çalışma kitabı oluşturun ve bir şablon dosyası açın
Workbook book = new Workbook(dataDir + "Book1.xls");
// Etkin hücreyi ayarla
book.Worksheets[0].ActiveCell = "A20";
// Çalışma sayfası penceresini bölme
book.Worksheets[0].Split();
// Excel dosyasını kaydedin
book.Save(dataDir + "output.xls");
```

## Çözüm

Bu öğreticide, Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasında bölmeleri nasıl ayıracağınızı öğrendiniz. Açıklanan adımları izleyerek, Excel dosyalarınızın görünümünü ve davranışını kolayca özelleştirebilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını işlemek için popüler bir yazılım kitaplığıdır.

#### Aspose.Cells'te bir çalışma sayfasının aktif hücresini nasıl ayarlayabilirim?

 Aktif hücreyi kullanarak ayarlayabilirsiniz.`ActiveCell`Çalışma Sayfası nesnesinin özelliği.

#### Çalışma sayfası penceresinin yalnızca yatay veya dikey bölmelerini bölebilir miyim?

 Evet, Aspose.Cells kullanarak yalnızca yatay veya dikey bölmeleri aşağıdaki gibi uygun yöntemlerle ayırabilirsiniz.`SplitColumn` veya`SplitRow`.

#### Aspose.Cells sadece .xls formatındaki Excel dosyalarıyla mı çalışır?

Hayır, Aspose.Cells, .xls ve .xlsx dahil olmak üzere çeşitli Excel dosya formatlarını destekler.