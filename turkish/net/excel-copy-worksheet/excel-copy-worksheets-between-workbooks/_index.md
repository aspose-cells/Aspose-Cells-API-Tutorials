---
title: Çalışma Kitapları Arasında Excel Kopyalama Çalışma Sayfaları
linktitle: Çalışma Kitapları Arasında Excel Kopyalama Çalışma Sayfaları
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak çalışma sayfalarını Excel çalışma kitapları arasında kolayca kopyalayın.
type: docs
weight: 30
url: /tr/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
Bu eğitimde, Aspose.Cells for .NET kütüphanesini kullanarak çalışma sayfalarını Excel çalışma kitapları arasında kopyalama adımlarında size rehberlik edeceğiz. Bu görevi tamamlamak için aşağıdaki talimatları izleyin.

## Adım 1: Hazırlık

Aspose.Cells for .NET'i kurduğunuzdan ve tercih ettiğiniz entegre geliştirme ortamında (IDE) bir C# projesi oluşturduğunuzdan emin olun.

## 2. Adım: Belge dizini yolunu ayarlayın

 ilan etmek`dataDir` değişken ve onu belgeler dizininizin yolu ile başlatın. Örneğin :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIRECTORY"` dizininize giden gerçek yolla.

## 3. Adım: Giriş dosyası yolunu tanımlayın

 ilan etmek`InputPath` değişkenini seçin ve elektronik tabloyu kopyalamak istediğiniz Excel dosyasının tam yolu ile başlatın. Örneğin :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Excel dosyasına sahip olduğunuzdan emin olun`book1.xls` Belgeler dizininizde veya doğru dosya adını ve konumunu belirtin.

## 4. Adım: İlk Excel çalışma kitabını oluşturun

 Kullan`Workbook` İlk Excel çalışma kitabını oluşturmak ve belirtilen dosyayı açmak için Aspose.Cells sınıfı:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## 5. Adım: İkinci bir Excel çalışma kitabı oluşturun

İkinci bir Excel çalışma kitabı oluşturun:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Adım 6: Çalışma sayfasını birinci çalışma kitabından ikinci çalışma kitabına kopyalayın

 Kullan`Copy`ilk çalışma kitabındaki ilk çalışma sayfasını ikinci çalışma kitabına kopyalama yöntemi:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## 7. Adım: Excel dosyasını kaydedin

Kopyalanan e-tabloyu içeren Excel dosyasını kaydedin:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Çıktı dosyası için istenen yolu ve dosya adını belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfalarını Çalışma Kitapları Arasında Kopyalamak için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Bir Çalışma Kitabı oluşturun.
// İlk kitapta bir dosya açın.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Başka bir Çalışma Kitabı oluşturun.
Workbook excelWorkbook1 = new Workbook();
// Birinci kitabın ilk sayfasını ikinci kitaba kopyalayın.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Dosya 'yı kaydet.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Çözüm

Tebrikler! Artık Aspose.Cells for .NET kullanarak çalışma sayfalarını Excel çalışma kitapları arasında nasıl kopyalayacağınızı öğrendiniz. Excel dosyalarını verimli bir şekilde işlemek için bu yöntemi kendi projelerinizde kullanmaktan çekinmeyin.

### SSS

#### S. Aspose.Cells for .NET'i kullanmak için hangi kütüphanelere ihtiyaç var?

A. Aspose.Cells for .NET'i kullanmak için Aspose.Cells kütüphanesini projenize dahil etmelisiniz. Tümleşik geliştirme ortamınızda (IDE) bu kitaplığa doğru şekilde başvurduğunuzdan emin olun.

#### S. Aspose.Cells, XLSX gibi diğer Excel dosya formatlarını destekliyor mu?

A. Evet, Aspose.Cells, XLSX, XLS, CSV, HTML ve çok daha fazlasını içeren çeşitli Excel dosya formatlarını destekler. Aspose.Cells for .NET'in özelliklerini kullanarak bu dosya formatlarını değiştirebilirsiniz.

#### S. Elektronik tabloyu kopyalarken düzen seçeneklerini özelleştirebilir miyim?

A.  Evet, elektronik tabloyu kopyalarken sayfa düzeni seçeneklerini özelleştirebilirsiniz.`PageSetup` nesne. Sayfa üst bilgilerini, alt bilgilerini, kenar boşluklarını, yönlendirmeleri vb. belirtebilirsiniz.