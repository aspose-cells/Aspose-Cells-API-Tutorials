---
title: Excel Kopyalama Çalışma Sayfası
linktitle: Excel Kopyalama Çalışma Sayfası
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile bir Excel çalışma sayfasını diğerine kopyalayın.
type: docs
weight: 20
url: /tr/net/excel-copy-worksheet/excel-copy-worksheet/
---

Bu kılavuzda, .NET için Aspose.Cells kütüphanesini kullanarak bir Excel çalışma sayfasının nasıl kopyalanacağını açıklayacağız. Size C# kaynak kodunu sağlayacağız ve bu görevi tamamlamak için gereken adımlarda size yol göstereceğiz. Sonunda size beklenen sonucu göstereceğiz. Başlamak için aşağıdaki talimatları izleyin.

## Adım 1: Hazırlık

Başlamadan önce Aspose.Cells for .NET'i kurduğunuzdan ve tercih ettiğiniz entegre geliştirme ortamında (IDE) bir C# projesi oluşturduğunuzdan emin olun. Ayrıca, işlemek istediğiniz Excel dosyasının bir kopyasına sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

 C# kaynak dosyanızda, gerekli kütüphaneleri Aspose.Cells'den içe aktarın.`using` direktif:

```csharp
using Aspose.Cells;
```

## 3. Adım: Dosya yolunu ayarlayın

 bir beyan`dataDir` değişkeni seçin ve onu Excel dosyanızı içeren dizinle başlatın. Örneğin :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Değiştirdiğinizden emin olun`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` Dizininizin gerçek yolu ile.

## 4. Adım: Mevcut Excel dosyasını yükleyin

 Kullan`Workbook` Mevcut Excel dosyasını açmak için Aspose.Cells'den sınıfa gidin. Kullan`InputPath` dosya yolunu belirtmek için değişken:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Değiştirdiğinizden emin olun`"book1.xls"` Excel dosyanızın gerçek adıyla.

## 5. Adım: Çalışma sayfasını kopyalayın

 Şimdi mevcut çalışma sayfasını yeni bir çalışma sayfasına kopyalayacağız. Kullan`Worksheets` mülkiyeti`Workbook` çalışma sayfaları koleksiyonuna erişmek için nesne:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Daha sonra şunu kullanın:`AddCopy` Belirtilen çalışma sayfasını kopyalama yöntemi. Örneğin, "Sayfa1"i kopyalamak için:

```csharp
sheets.AddCopy("Sheet1");
```

## Adım 6: Excel dosyasını kaydedin

 Kullan`Save` yöntemi`Workbook` Değişiklikleri yeni bir dosyaya kaydetmek için nesne:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Çıktı dosyası için istediğiniz yolu ve dosya adını belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanan Excel Kopyalama Çalışma Sayfası için örnek kaynak kodu 

```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Mevcut bir Excel dosyasını açın.
Workbook wb = new Workbook(InputPath);
// Referansla bir Çalışma Sayfaları nesnesi oluşturun
// Çalışma Kitabının sayfaları.
WorksheetCollection sheets = wb.Worksheets;
// Verileri mevcut bir sayfadan yeni bir sayfaya kopyalayın
// Çalışma Kitabı'ndaki sayfa.
sheets.AddCopy("Sheet1");
// Excel dosyasını kaydedin.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Çözüm

Tebrikler! Artık Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasını nasıl kopyalayacağınızı öğrendiniz. Bu adım adım kılavuz, gerekli kitaplıkların nasıl içe aktarılacağını, mevcut bir Excel dosyasının nasıl yükleneceğini, çalışma sayfasının nasıl kopyalanacağını ve değiştirilen dosyanın nasıl kaydedileceğini gösterdi. Excel dosyalarını verimli bir şekilde değiştirmek için bu yöntemi kendi projelerinizde kullanmaktan çekinmeyin.

### SSS

#### S. Aspose.Cells diğer programlama dilleriyle uyumlu mudur?

A. Evet, Aspose.Cells, C#, Java, Python ve daha pek çok programlama dilini destekler.

#### S. Bir çalışma sayfasını başka bir Excel çalışma kitabına kopyalayabilir miyim?

A.  Evet, kullanabilirsiniz`AddCopy` Bir çalışma sayfasını başka bir Excel çalışma kitabına kopyalama yöntemi.

#### S. Aspose.Cells çalışma sayfasını kopyalarken formülleri ve formatı koruyor mu?

A. Evet, Aspose.Cells bir çalışma sayfasını kopyalarken formülleri, formatı ve diğer özellikleri korur.

#### S. Aspose.Cells ticari kullanım için lisans gerektiriyor mu?

A. Evet, Aspose.Cells ticari bir üründür ve ticari kullanım için lisans satın alınması gerekir. Aspose'un resmi web sitesinde daha fazla lisans bilgisi bulabilirsiniz.