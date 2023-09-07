---
title: Excel Çalışma Sayfası İçin Gelişmiş Koruma Ayarları
linktitle: Excel Çalışma Sayfası İçin Gelişmiş Koruma Ayarları
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile gelişmiş koruma ayarları yaparak Excel dosyalarınızı koruyun.
type: docs
weight: 10
url: /tr/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
Bu eğitimde, Aspose.Cells library for .NET'i kullanarak bir Excel elektronik tablosu için gelişmiş koruma ayarları yapma adımlarında size yol göstereceğiz. Bu görevi tamamlamak için aşağıdaki talimatları izleyin.

## Adım 1: Hazırlık

Aspose.Cells for .NET'i kurduğunuzdan ve tercih ettiğiniz entegre geliştirme ortamında (IDE) bir C# projesi oluşturduğunuzdan emin olun.

## 2. Adım: Belge dizini yolunu ayarlayın

 ilan etmek`dataDir` değişken ve onu belgeler dizininizin yolu ile başlatın. Örneğin :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIRECTORY"` dizininize giden gerçek yolla.

## 3. Adım: Excel dosyasını açmak için bir dosya akışı oluşturun

 Oluşturmak`FileStream` açılacak Excel dosyasını içeren nesne:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Excel dosyasına sahip olduğunuzdan emin olun`book1.xls` Belgeler dizininizde veya doğru dosya adını ve konumunu belirtin.

## 4. Adım: Bir Çalışma Kitabı nesnesi örneği oluşturun ve Excel dosyasını açın

 Kullan`Workbook`Aspose.Cells'ten bir Workbook nesnesini somutlaştırmak ve belirtilen Excel dosyasını dosya akışı aracılığıyla açmak için sınıf:

```csharp
Workbook excel = new Workbook(fstream);
```

## 5. Adım: İlk çalışma sayfasına erişin

Excel dosyasının ilk çalışma sayfasına gidin:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## 6. Adım: Çalışma Sayfası Koruma Ayarlarını Ayarlayın

Çalışma sayfası koruma ayarlarını gerektiği gibi ayarlamak için Çalışma Sayfası nesne özelliklerini kullanın. Örneğin :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Diğer koruma ayarlarını gerektiği gibi yapın...
```

## 7. Adım: Değiştirilen Excel dosyasını kaydedin

 Değiştirilen Excel dosyasını kullanarak kaydedin.`Save` Çalışma Kitabı nesnesinin yöntemi:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Çıktı dosyası için istenen yolu ve dosya adını belirttiğinizden emin olun.

## 8. Adım: Dosya akışını kapatın

Kaydedildikten sonra, ilgili tüm kaynakları serbest bırakmak için dosya akışını kapatın:

```csharp
fstream.Close();
```
	
### Aspose.Cells for .NET kullanan Excel İçin Gelişmiş Koruma Ayarları Çalışma Sayfası için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
// Excel dosyasını dosya akışı aracılığıyla açma
Workbook excel = new Workbook(fstream);
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = excel.Worksheets[0];
// Kullanıcıların çalışma sayfasının sütunlarını silmelerini kısıtlama
worksheet.Protection.AllowDeletingColumn = false;
// Kullanıcıların çalışma sayfasının satırını silmelerini kısıtlama
worksheet.Protection.AllowDeletingRow = false;
// Kullanıcıların çalışma sayfasının içeriğini düzenlemesini kısıtlama
worksheet.Protection.AllowEditingContent = false;
// Kullanıcıların çalışma sayfasının nesnelerini düzenlemesini kısıtlama
worksheet.Protection.AllowEditingObject = false;
// Kullanıcıların çalışma sayfasının senaryolarını düzenlemesini kısıtlama
worksheet.Protection.AllowEditingScenario = false;
//Kullanıcıları filtrelemek için kısıtlama
worksheet.Protection.AllowFiltering = false;
// Kullanıcıların çalışma sayfasının hücrelerini biçimlendirmesine izin verme
worksheet.Protection.AllowFormattingCell = true;
// Kullanıcıların çalışma sayfasının satırlarını biçimlendirmesine izin verme
worksheet.Protection.AllowFormattingRow = true;
// Kullanıcıların çalışma sayfasına sütun eklemesine izin verme
worksheet.Protection.AllowFormattingColumn = true;
// Kullanıcıların çalışma sayfasına köprüler eklemesine izin verme
worksheet.Protection.AllowInsertingHyperlink = true;
// Kullanıcıların çalışma sayfasına satır eklemesine izin verme
worksheet.Protection.AllowInsertingRow = true;
// Kullanıcıların çalışma sayfasının kilitli hücrelerini seçmesine izin verme
worksheet.Protection.AllowSelectingLockedCell = true;
// Kullanıcıların çalışma sayfasının kilitli olmayan hücrelerini seçmesine izin verme
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Kullanıcıların sıralama yapmasına izin verme
worksheet.Protection.AllowSorting = true;
// Kullanıcıların çalışma sayfasındaki pivot tabloları kullanmasına izin verme
worksheet.Protection.AllowUsingPivotTable = true;
// Değiştirilen Excel dosyasını kaydetme
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak bir Excel elektronik tablosu için gelişmiş koruma ayarlarını nasıl yapacağınızı artık öğrendiniz. Excel dosyalarınızı güvence altına almak ve kullanıcı eylemlerini kısıtlamak için bu bilgiyi kullanın.

### SSS

#### S: IDE'mde nasıl yeni bir C# projesi oluşturabilirim?

Y: Yeni bir C# projesi oluşturma adımları, kullandığınız IDE'ye bağlı olarak değişebilir. Ayrıntılı talimatlar için IDE'nizin belgelerine bakın.

#### S: Eğitimde belirtilenlerin dışında özel koruma ayarları yapmak mümkün mü?

C: Evet, Aspose.Cells, özel ihtiyaçlarınıza göre özelleştirebileceğiniz çok çeşitli koruma ayarları sunar. Daha fazla ayrıntı için Aspose.Cells belgelerine bakın.

#### S: Değiştirilen Excel dosyasını örnek kodda kaydetmek için kullanılan dosya biçimi nedir?

Y: Örnek kodda, değiştirilen Excel dosyası Excel 97-2003 (.xls) biçiminde kaydedilmiştir. Gerekirse Aspose.Cells tarafından desteklenen diğer biçimleri seçebilirsiniz.

#### S: Excel dosyasındaki diğer çalışma sayfalarına nasıl erişebilirim?

 C: Dizin veya sayfa adını kullanarak diğer çalışma sayfalarına erişebilirsiniz, örneğin:`Worksheet worksheet = excel.Worksheets[1];` veya`Worksheet worksheet = excel.Worksheets[" SheetName"];`.