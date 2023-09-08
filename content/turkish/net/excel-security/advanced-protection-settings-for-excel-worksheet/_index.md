---
title: Excel Çalışma Sayfası İçin Gelişmiş Koruma Ayarları
linktitle: Excel Çalışma Sayfası İçin Gelişmiş Koruma Ayarları
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile gelişmiş koruma ayarlarını yaparak Excel dosyalarınızı koruyun.
type: docs
weight: 10
url: /tr/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
Bu eğitimde, .NET için Aspose.Cells kütüphanesini kullanarak bir Excel elektronik tablosu için gelişmiş koruma ayarlarını belirleme adımlarında size yol göstereceğiz. Bu görevi tamamlamak için aşağıdaki talimatları izleyin.

## Adım 1: Hazırlık

Aspose.Cells for .NET'i kurduğunuzdan ve tercih ettiğiniz entegre geliştirme ortamında (IDE) bir C# projesi oluşturduğunuzdan emin olun.

## Adım 2: Belge dizini yolunu ayarlayın

 bir beyan`dataDir` değişkeni oluşturun ve onu belgeler dizininizin yolu ile başlatın. Örneğin :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Değiştirdiğinizden emin olun`"YOUR_DOCUMENTS_DIRECTORY"` Dizininizin gerçek yolu ile.

## 3. Adım: Excel dosyasını açmak için bir dosya akışı oluşturun

 Oluşturmak`FileStream` Açılacak Excel dosyasını içeren nesne:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Excel dosyanızın olduğundan emin olun`book1.xls` belgeler dizininizde veya doğru dosya adını ve konumunu belirtin.

## Adım 4: Bir Çalışma Kitabı nesnesinin örneğini oluşturun ve Excel dosyasını açın

 Kullan`Workbook`Aspose.Cells'ten bir Workbook nesnesi örneği oluşturmak ve belirtilen Excel dosyasını dosya akışı yoluyla açmak için class'ı kullanın:

```csharp
Workbook excel = new Workbook(fstream);
```

## 5. Adım: İlk çalışma sayfasına erişin

Excel dosyasının ilk çalışma sayfasına gidin:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Adım 6: Çalışma Sayfası Koruma Ayarlarını Ayarlayın

Çalışma sayfası koruma ayarlarını gerektiği gibi ayarlamak için Çalışma Sayfası nesne özelliklerini kullanın. Örneğin :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Gerektiğinde diğer koruma ayarlarını yapın...
```

## Adım 7: Değiştirilen Excel dosyasını kaydedin

 Değiştirilen Excel dosyasını kullanarak kaydedin.`Save` Çalışma Kitabı nesnesinin yöntemi:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Çıktı dosyası için istediğiniz yolu ve dosya adını belirttiğinizden emin olun.

## 8. Adım: Dosya akışını kapatın

Kaydedildikten sonra, ilgili tüm kaynakların serbest bırakılması için dosya akışını kapatın:

```csharp
fstream.Close();
```
	
### Aspose.Cells for .NET kullanan Excel Çalışma Sayfası İçin Gelişmiş Koruma Ayarları için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
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
// Kullanıcıların çalışma sayfasının satırını silmeleri kısıtlanıyor
worksheet.Protection.AllowDeletingRow = false;
// Kullanıcıların çalışma sayfasının içeriğini düzenlemesini kısıtlama
worksheet.Protection.AllowEditingContent = false;
// Kullanıcıların çalışma sayfasının nesnelerini düzenlemesini kısıtlama
worksheet.Protection.AllowEditingObject = false;
// Kullanıcıların çalışma sayfasının senaryolarını düzenlemesini kısıtlama
worksheet.Protection.AllowEditingScenario = false;
//Kullanıcıların filtrelemesini kısıtlama
worksheet.Protection.AllowFiltering = false;
// Kullanıcıların çalışma sayfasının hücrelerini biçimlendirmesine izin verme
worksheet.Protection.AllowFormattingCell = true;
// Kullanıcıların çalışma sayfasının satırlarını biçimlendirmesine izin verme
worksheet.Protection.AllowFormattingRow = true;
// Kullanıcıların çalışma sayfasına sütun eklemesine izin verme
worksheet.Protection.AllowFormattingColumn = true;
// Kullanıcıların çalışma sayfasına köprü eklemesine izin verme
worksheet.Protection.AllowInsertingHyperlink = true;
// Kullanıcıların çalışma sayfasına satır eklemesine izin verme
worksheet.Protection.AllowInsertingRow = true;
// Kullanıcıların çalışma sayfasının kilitli hücrelerini seçmesine izin verme
worksheet.Protection.AllowSelectingLockedCell = true;
// Kullanıcıların çalışma sayfasının kilidi açılmış hücrelerini seçmesine izin verme
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Kullanıcıların sıralama yapmasına izin verme
worksheet.Protection.AllowSorting = true;
// Kullanıcıların çalışma sayfasında pivot tabloları kullanmasına izin verme
worksheet.Protection.AllowUsingPivotTable = true;
// Değiştirilen Excel dosyasını kaydetme
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Tebrikler! Artık Aspose.Cells for .NET'i kullanarak bir Excel tablosu için gelişmiş koruma ayarlarını nasıl ayarlayacağınızı öğrendiniz. Excel dosyalarınızın güvenliğini sağlamak ve kullanıcı eylemlerini kısıtlamak için bu bilgiyi kullanın.

### SSS

#### S: IDE'mde nasıl yeni bir C# projesi oluşturabilirim?

C: Yeni bir C# projesi oluşturma adımları, kullandığınız IDE'ye bağlı olarak değişebilir. Ayrıntılı talimatlar için IDE'nizin belgelerine bakın.

#### S: Eğitimde belirtilenlerin dışında özel koruma ayarları belirlemek mümkün mü?

C: Evet, Aspose.Cells özel ihtiyaçlarınıza göre kişiselleştirebileceğiniz çok çeşitli koruma ayarları sunar. Daha fazla ayrıntı için Aspose.Cells belgelerine bakın.

#### S: Değiştirilen Excel dosyasını örnek koda kaydetmek için kullanılan dosya biçimi nedir?

C: Örnek kodda, değiştirilen Excel dosyası Excel 97-2003 (.xls) biçiminde kaydedilmiştir. Gerekirse Aspose.Cells tarafından desteklenen diğer formatları da seçebilirsiniz.

#### S: Excel dosyasındaki diğer çalışma sayfalarına nasıl erişebilirim?

 C: Dizin veya sayfa adını kullanarak diğer çalışma sayfalarına erişebilirsiniz, örneğin:`Worksheet worksheet = excel.Worksheets[1];` veya`Worksheet worksheet = excel.Worksheets[" SheetName"];`.