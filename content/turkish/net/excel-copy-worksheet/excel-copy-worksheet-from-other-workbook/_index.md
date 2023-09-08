---
title: Excel Çalışma Sayfasını Diğer Çalışma Kitabından Kopyala
linktitle: Excel Çalışma Sayfasını Diğer Çalışma Kitabından Kopyala
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak bir Excel çalışma sayfasını bir çalışma kitabından diğerine kolayca kopyalayın.
type: docs
weight: 10
url: /tr/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
Bu eğitimde, .NET için Aspose.Cells kütüphanesini kullanarak bir Excel çalışma sayfasını başka bir çalışma kitabından kopyalama adımlarında size yol göstereceğiz. Bu görevi tamamlamak için aşağıdaki talimatları izleyin.

## Adım 1: Hazırlık

Başlamadan önce Aspose.Cells for .NET'i kurduğunuzdan ve tercih ettiğiniz entegre geliştirme ortamında (IDE) bir C# projesi oluşturduğunuzdan emin olun.

## Adım 2: Belge dizini yolunu ayarlayın

 bir beyan`dataDir` değişkeni oluşturun ve onu belgeler dizininizin yolu ile başlatın. Örneğin :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIRECTORY"` Dizininizin gerçek yolu ile.

## 3. Adım: Yeni bir Excel çalışma kitabı oluşturun

 Kullan`Workbook` Yeni bir Excel çalışma kitabı oluşturmak için Aspose.Cells'ten sınıf:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Adım 4: Çalışma kitabındaki ilk çalışma sayfasını alın

Dizin 0'ı kullanarak çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## 5. Adım: Başlık satırlarına veri ekleyin (A1:A4)

 Kullanın`for` başlık satırlarına veri eklemek için döngü (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## 6. Adım: Ayrıntılı verileri ekleyin (A5:A999)

 Başka birini kullan`for` ayrıntılı veri eklemek için döngü (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## 7. Adım: Düzen seçeneklerini ayarlayın

 Çalışma sayfasının sayfa yapısı seçeneklerini kullanarak ayarlayın.`PageSetup` nesne:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## 8. Adım: Başka bir Excel çalışma kitabı oluşturun

Başka bir Excel çalışma kitabı oluşturun:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Adım 9: İkinci çalışma kitabından ilk çalışma sayfasını alın

İkinci çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Adım 10: Çalışma sayfasına bir ad verin

ateşe isim ver

hesaplama adası:

```csharp
ws1.Name = "MySheet";
```

## Adım 11: İlk çalışma kitabının ilk çalışma sayfasındaki verileri ikinci çalışma kitabının ilk çalışma sayfasına kopyalayın

İlk çalışma kitabının ilk çalışma sayfasındaki verileri ikinci çalışma kitabının ilk çalışma sayfasına kopyalayın:

```csharp
ws1.Copy(ws0);
```

## Adım 12: Excel dosyasını kaydedin

Excel dosyasını kaydedin:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Çıktı dosyası için istediğiniz yolu ve dosya adını belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Excel Çalışma Sayfasını Diğer Çalışma Kitabından Kopyalama için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Yeni bir Çalışma Kitabı oluşturun.
Workbook excelWorkbook0 = new Workbook();
// Kitaptaki ilk çalışma sayfasını alın.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Başlık satırlarına bazı veriler koyun (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Bazı ayrıntılı verileri koyun (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// İlk çalışma sayfasını temel alan bir sayfa düzeni nesnesi tanımlayın.
PageSetup pagesetup = ws0.PageSetup;
// İlk beş satır her sayfada tekrarlanıyor...
// Baskı ön izlemesinde görülebilir.
pagesetup.PrintTitleRows = "$1:$5";
// Başka bir Çalışma Kitabı oluşturun.
Workbook excelWorkbook1 = new Workbook();
// Kitaptaki ilk çalışma sayfasını alın.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Çalışma sayfasına bir ad verin.
ws1.Name = "MySheet";
// İlk çalışma kitabının ilk çalışma sayfasındaki verileri kopyalayın.
// ikinci çalışma kitabının ilk çalışma sayfası.
ws1.Copy(ws0);
// Excel dosyasını kaydedin.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Çözüm

Tebrikler! Artık Aspose.Cells for .NET kullanarak bir Excel çalışma sayfasını başka bir çalışma kitabından nasıl kopyalayacağınızı öğrendiniz. Excel dosyalarını verimli bir şekilde değiştirmek için bu yöntemi kendi projelerinizde kullanmaktan çekinmeyin.

### SSS

#### S. Aspose.Cells for .NET'i kullanmak için hangi kütüphanelere ihtiyaç var?

A. Aspose.Cells for .NET'i kullanmak için Aspose.Cells kütüphanesini projenize dahil etmelisiniz. Bu kitaplığa tümleşik geliştirme ortamınızda (IDE) doğru şekilde başvuruda bulunduğunuzdan emin olun.

#### S. Aspose.Cells XLSX gibi diğer Excel dosya formatlarını destekliyor mu?

A. Evet, Aspose.Cells XLSX, XLS, CSV, HTML ve çok daha fazlasını içeren çeşitli Excel dosya formatlarını destekler. Aspose.Cells for .NET'in özelliklerini kullanarak bu dosya formatlarını değiştirebilirsiniz.

#### S. Çalışma sayfasını kopyalarken düzen seçeneklerini özelleştirebilir miyim?

A.  Evet, çalışma sayfasını kopyalarken sayfa düzeni seçeneklerini, çalışma sayfasının özelliklerini kullanarak özelleştirebilirsiniz.`PageSetup` nesne. Sayfa üstbilgilerini, altbilgilerini, kenar boşluklarını, yönlendirmeleri vb. belirtebilirsiniz.