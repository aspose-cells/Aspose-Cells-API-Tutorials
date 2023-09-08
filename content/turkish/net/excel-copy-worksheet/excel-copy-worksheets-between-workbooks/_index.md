---
title: Çalışma Kitapları Arasında Excel Çalışma Sayfalarını Kopyalama
linktitle: Çalışma Kitapları Arasında Excel Çalışma Sayfalarını Kopyalama
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak çalışma sayfalarını Excel çalışma kitapları arasında kolayca kopyalayın.
type: docs
weight: 30
url: /tr/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
Bu eğitimde, .NET için Aspose.Cells kütüphanesini kullanarak çalışma sayfalarını Excel çalışma kitapları arasında kopyalama adımlarında size rehberlik edeceğiz. Bu görevi tamamlamak için aşağıdaki talimatları izleyin.

## Adım 1: Hazırlık

Aspose.Cells for .NET'i kurduğunuzdan ve tercih ettiğiniz entegre geliştirme ortamında (IDE) bir C# projesi oluşturduğunuzdan emin olun.

## Adım 2: Belge dizini yolunu ayarlayın

 bir beyan`dataDir` değişkeni oluşturun ve onu belgeler dizininizin yolu ile başlatın. Örneğin :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIRECTORY"` Dizininizin gerçek yolu ile.

## 3. Adım: Giriş dosyası yolunu tanımlayın

 bir beyan`InputPath` değişkeni seçin ve e-tabloyu kopyalamak istediğiniz Excel dosyasının tam yoluyla başlatın. Örneğin :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Excel dosyanızın olduğundan emin olun`book1.xls` belgeler dizininizde veya doğru dosya adını ve konumunu belirtin.

## 4. Adım: İlk Excel çalışma kitabını oluşturun

 Kullan`Workbook` Aspose.Cells sınıfı, ilk Excel çalışma kitabını oluşturmak ve belirtilen dosyayı açmak için:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Adım 5: İkinci bir Excel çalışma kitabı oluşturun

İkinci bir Excel çalışma kitabı oluşturun:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Adım 6: Çalışma sayfasını ilk çalışma kitabından ikinci çalışma kitabına kopyalayın

 Kullan`Copy`İlk çalışma sayfasını birinci çalışma kitabından ikinci çalışma kitabına kopyalama yöntemi:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Adım 7: Excel dosyasını kaydedin

Kopyalanan e-tabloyu içeren Excel dosyasını kaydedin:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Çıktı dosyası için istediğiniz yolu ve dosya adını belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Çalışma Kitapları Arasında Excel Kopyalama Çalışma Sayfaları için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Bir Çalışma Kitabı oluşturun.
// İlk kitaba bir dosya açın.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Başka bir Çalışma Kitabı oluşturun.
Workbook excelWorkbook1 = new Workbook();
// Birinci kitabın ilk sayfasını ikinci kitaba kopyalayın.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Dosya 'yı kaydet.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Çözüm

Tebrikler! Artık Aspose.Cells for .NET kullanarak çalışma sayfalarını Excel çalışma kitapları arasında nasıl kopyalayacağınızı öğrendiniz. Excel dosyalarını verimli bir şekilde değiştirmek için bu yöntemi kendi projelerinizde kullanmaktan çekinmeyin.

### SSS

#### S. Aspose.Cells for .NET'i kullanmak için hangi kütüphanelere ihtiyaç var?

A. Aspose.Cells for .NET'i kullanmak için Aspose.Cells kütüphanesini projenize dahil etmelisiniz. Bu kitaplığa tümleşik geliştirme ortamınızda (IDE) doğru şekilde başvuruda bulunduğunuzdan emin olun.

#### S. Aspose.Cells XLSX gibi diğer Excel dosya formatlarını destekliyor mu?

A. Evet, Aspose.Cells XLSX, XLS, CSV, HTML ve çok daha fazlasını içeren çeşitli Excel dosya formatlarını destekler. Aspose.Cells for .NET'in özelliklerini kullanarak bu dosya formatlarını değiştirebilirsiniz.

#### S. Elektronik tabloyu kopyalarken düzen seçeneklerini özelleştirebilir miyim?

A.  Evet, e-tabloyu kopyalarken sayfa düzeni seçeneklerini, e-tablonun özelliklerini kullanarak özelleştirebilirsiniz.`PageSetup` nesne. Sayfa üstbilgilerini, altbilgilerini, kenar boşluklarını, yönlendirmeleri vb. belirtebilirsiniz.