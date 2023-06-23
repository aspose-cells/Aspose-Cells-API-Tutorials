---
title: Baştaki Kesme İşaretine İzin Ver
linktitle: Baştaki Kesme İşaretine İzin Ver
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel çalışma kitaplarında önde gelen kesme işaretine izin verin.
type: docs
weight: 60
url: /tr/net/excel-workbook/allow-leading-apostrophe/
---
Bu adım adım öğreticide, Aspose.Cells for .NET kullanarak bir Excel çalışma kitabında önde gelen kesme işareti kullanımına izin vermenizi sağlayacak sağlanan C# kaynak kodunu açıklayacağız. Bu işlemi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıkış dizinlerini ayarlayın

```csharp
// kaynak dizin
string sourceDir = RunExamples.Get_SourceDirectory();
// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda, Excel dosyaları için kaynak ve çıktı dizinlerini tanımlıyoruz.

## Adım 2: Bir WorkbookDesigner nesnesi örneği oluşturun

```csharp
// Bir WorkbookDesigner nesnesinin örneğini oluşturun
WorkbookDesigner designer = new WorkbookDesigner();
```

 örneğini oluşturuyoruz`WorkbookDesigner` Aspose.Cells'ten sınıf.

## 3. Adım: Excel Çalışma Kitabını Yükleyin

```csharp
//Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Excel çalışma kitabını belirtilen dosyadan yüklüyoruz ve ilk kesme işaretlerinin otomatik olarak metin stiline dönüştürülmesini devre dışı bırakıyoruz.

## 4. Adım: Veri Kaynağını Ayarlayın

```csharp
// Tasarımcı çalışma kitabı için veri kaynağını tanımlayın
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Bir veri nesneleri listesi tanımlarız ve`SetDataSource` tasarımcı çalışma kitabı için veri kaynağını ayarlama yöntemi.

## 5. Adım: Akıllı işaretleyicileri işleyin

```csharp
// Akıllı işaretleyicileri işle
designer. Process();
```

 biz kullanıyoruz`Process` tasarımcı çalışma kitabındaki akıllı işaretçileri işleme yöntemi.

## 6. Adım: Değiştirilen Excel çalışma kitabını kaydedin

```csharp
// Değiştirilen Excel çalışma kitabını kaydedin
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Değiştirilen Excel çalışma kitabını yapılan değişikliklerle kaydediyoruz.

### Aspose.Cells for .NET kullanarak Önde Kesme İşaretine İzin Ver için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Bir WorkbookDesigner nesnesinin örneğini oluşturma
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Akıllı işaretçiler içeren bir tasarımcı e-tablosu açın
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Tasarımcı e-tablosu için veri kaynağını ayarlayın
designer.SetDataSource("sampleData", list);
// Akıllı işaretleyicileri işleyin
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak bir Excel çalışma kitabında baştaki kesme işareti kullanımına nasıl izin vereceğinizi öğrendiniz. Excel çalışma kitaplarınızı daha da özelleştirmek için kendi verilerinizle denemeler yapın.

### SSS

#### S: Bir Excel çalışma kitabında önde gelen kesme işareti izni nedir?

Y: Bir Excel çalışma kitabında ilk kesme işaretine izin verilmesi, kesme işaretiyle başlayan verilerin bir metin stiline dönüştürülmeden doğru şekilde görüntülenmesini sağlar. Kesme işaretini verilerin bir parçası olarak tutmak istediğinizde bu kullanışlıdır.

#### S: İlk kesme işaretlerinin otomatik olarak dönüştürülmesini neden kapatmam gerekiyor?

C: Baştaki alıntıların otomatik olarak dönüştürülmesini devre dışı bırakarak, kullanımlarını verilerinizde olduğu gibi koruyabilirsiniz. Bu, Excel çalışma kitabını açarken veya değiştirirken verilerin istenmeyen şekilde değiştirilmesini önler.

#### S: Tasarımcı çalışma kitabında veri kaynağı nasıl ayarlanır?

 C: Veri kaynağını tasarımcı çalışma kitabında ayarlamak için`SetDataSource` veri kaynağının adını ve karşılık gelen veri nesnelerinin bir listesini belirten yöntem.

#### S: Baştaki kesme işaretine izin verilmesi, Excel çalışma kitabındaki diğer verileri etkiler mi?

C: Hayır, baştaki kesme işaretine izin verilmesi yalnızca kesme işaretiyle başlayan verileri etkiler. Excel çalışma kitabındaki diğer veriler değişmeden kalır.

#### S: Bu özelliği diğer Excel dosya biçimleriyle kullanabilir miyim?

C: Evet, bu özelliği Aspose.Cells tarafından desteklenen .xls, .xlsm vb. gibi diğer Excel dosya biçimleriyle kullanabilirsiniz.