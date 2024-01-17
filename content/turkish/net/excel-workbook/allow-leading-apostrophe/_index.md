---
title: Baştaki Kesme İşaretine İzin Ver
linktitle: Baştaki Kesme İşaretine İzin Ver
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel çalışma kitaplarında kesme işaretine izin verin.
type: docs
weight: 60
url: /tr/net/excel-workbook/allow-leading-apostrophe/
---
Bu adım adım eğitimde, Aspose.Cells for .NET kullanarak bir Excel çalışma kitabında baştaki kesme işaretinin kullanımına izin vermenizi sağlayacak sağlanan C# kaynak kodunu açıklayacağız. Bu işlemi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıkış dizinlerini ayarlayın

```csharp
// kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda Excel dosyalarının kaynak ve çıktı dizinlerini tanımlıyoruz.

## 2. Adım: WorkbookDesigner nesnesini örnekleyin

```csharp
// WorkbookDesigner nesnesini örneklendirme
WorkbookDesigner designer = new WorkbookDesigner();
```

 Bunun bir örneğini oluşturuyoruz`WorkbookDesigner` Aspose.Cells'ten sınıf.

## Adım 3: Excel Çalışma Kitabını Yükleyin

```csharp
// Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Excel çalışma kitabını belirtilen dosyadan yüklüyoruz ve ilk kesme işaretlerinin otomatik olarak metin stiline dönüştürülmesini devre dışı bırakıyoruz.

## Adım 4: Veri Kaynağını Ayarlayın

```csharp
// Tasarımcı çalışma kitabı için veri kaynağını tanımlama
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

 Veri nesnelerinin bir listesini tanımlarız ve`SetDataSource` Tasarımcı çalışma kitabının veri kaynağını ayarlama yöntemi.

## 5. Adım: Akıllı işaretleyicileri işleyin

```csharp
// Akıllı işaretleyicileri işleyin
designer. Process();
```

 biz kullanıyoruz`Process` Tasarımcı çalışma kitabındaki akıllı işaretçileri işleme yöntemi.

## Adım 6: Değiştirilen Excel çalışma kitabını kaydedin

```csharp
// Değiştirilen Excel çalışma kitabını kaydedin
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Değiştirilen Excel çalışma kitabını yapılan değişikliklerle birlikte kaydediyoruz.

### Aspose.Cells for .NET kullanarak Öndeki Kesme İşaretine İzin Ver için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// WorkbookDesigner nesnesini örneklendirme
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Akıllı işaretleyiciler içeren bir tasarımcı e-tablosu açın
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
// Tasarımcı e-tablosunun veri kaynağını ayarlama
designer.SetDataSource("sampleData", list);
// Akıllı işaretleyicileri işleyin
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET'i kullanarak bir Excel çalışma kitabında baştaki kesme işaretinin kullanımına nasıl izin vereceğinizi öğrendiniz. Excel çalışma kitaplarınızı daha da özelleştirmek için kendi verilerinizle denemeler yapın.

### SSS

#### S: Excel çalışma kitabındaki kesme işareti izni nedir?

C: Excel çalışma kitabındaki ilk kesme işaretine izin vermek, kesme işaretiyle başlayan verilerin metin stiline dönüştürülmeden doğru şekilde görüntülenmesine olanak tanır. Kesme işaretini verilerin bir parçası olarak tutmak istediğinizde bu kullanışlıdır.

#### S: Neden ilk kesme işaretlerinin otomatik dönüştürülmesini kapatmam gerekiyor?

C: Baştaki alıntıların otomatik olarak dönüştürülmesini devre dışı bırakarak, bunların verilerinizdeki kullanımını koruyabilirsiniz. Bu, Excel çalışma kitabını açarken veya değiştirirken verilerde istenmeyen değişiklikler yapılmasını önler.

#### S: Tasarımcı çalışma kitabında veri kaynağı nasıl ayarlanır?

 C: Veri kaynağını tasarımcı çalışma kitabında ayarlamak için`SetDataSource` veri kaynağının adını ve karşılık gelen veri nesnelerinin listesini belirten yöntem.

#### S: Başta kesme işaretine izin verilmesi Excel çalışma kitabındaki diğer verileri etkiler mi?

C: Hayır, baştaki kesme işaretine izin vermek yalnızca kesme işaretiyle başlayan verileri etkiler. Excel çalışma kitabındaki diğer veriler değişmeden kalır.

#### S: Bu özelliği diğer Excel dosya formatlarıyla kullanabilir miyim?

C: Evet, bu özelliği Aspose.Cells tarafından desteklenen .xls, .xlsm vb. gibi diğer Excel dosya formatlarıyla kullanabilirsiniz.