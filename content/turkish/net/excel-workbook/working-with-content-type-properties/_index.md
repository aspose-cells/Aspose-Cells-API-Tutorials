---
title: İçerik Türü Özellikleriyle Çalışma
linktitle: İçerik Türü Özellikleriyle Çalışma
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak içerik türü özellikleriyle nasıl çalışacağınızı öğrenin.
type: docs
weight: 180
url: /tr/net/excel-workbook/working-with-content-type-properties/
---
İçerik türü özellikleri, .NET için Aspose.Cells kitaplığı kullanılarak Excel dosyalarının yönetilmesinde ve işlenmesinde hayati bir rol oynar. Bu özellikler, Excel dosyaları için ek meta veriler tanımlamanıza olanak tanıyarak verileri düzenlemeyi ve bulmayı kolaylaştırır. Bu öğreticide, örnek C# kodunu kullanarak içerik türü özelliklerini anlamanız ve bunlarla çalışmanız için adım adım yol göstereceğiz.

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

- Aspose.Cells for .NET geliştirme makinenizde yüklü.
- Visual Studio gibi C# ile uyumlu tümleşik bir geliştirme ortamı (IDE).

## 1. Adım: Ortamı ayarlama

İçerik türü özellikleriyle çalışmaya başlamadan önce, geliştirme ortamınızı Aspose.Cells for .NET ile kurduğunuzdan emin olun. Referansı projenizdeki Aspose.Cells kitaplığına ekleyebilir ve gerekli ad alanını sınıfınıza aktarabilirsiniz.

```csharp
using Aspose.Cells;
```

## 2. Adım: Yeni bir Excel çalışma kitabı oluşturma

 İlk olarak, kullanarak yeni bir Excel çalışma kitabı oluşturacağız.`Workbook`Aspose.Cells tarafından sağlanan sınıf. Aşağıdaki kod, yeni bir Excel çalışma kitabının nasıl oluşturulacağını ve belirli bir çıktı dizininde nasıl saklanacağını gösterir.

```csharp
// Hedef dizini
string outputDir = RunExamples.Get_OutputDirectory();

// Yeni bir Excel çalışma kitabı oluşturma
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## 3. Adım: İçerik Türü Özelliklerini Ekleme

 Artık Excel çalışma kitabımıza sahip olduğumuza göre, içerik türü özelliklerini kullanarak ekleyebiliriz.`Add` yöntemi`ContentTypeProperties` koleksiyonu`Workbook` sınıf. Her özellik bir ad ve değerle temsil edilir. SEN

  Özelliğin veri türünü de belirleyebilirsiniz.

```csharp
// İlk içerik türü özelliğini ekleyin
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// İkinci içerik türü özelliğini ekleyin
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## 4. Adım: Excel çalışma kitabını kaydetme

 İçerik türü özelliklerini ekledikten sonra, Excel çalışma kitabını değişikliklerle kaydedebiliriz. Kullan`Save` yöntemi`Workbook` çıktı dizini ve dosya adını belirtmek için sınıf.

```csharp
// Excel çalışma kitabını kaydetme
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### Aspose.Cells for .NET kullanarak İçerik Türü Özellikleriyle Çalışmak için örnek kaynak kodu 
```csharp
//kaynak dizin
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak içerik türü özellikleriyle nasıl çalışacağınızı öğrendiniz. Artık Excel dosyalarınıza özel meta veriler ekleyebilir ve bunları daha verimli bir şekilde yönetebilirsiniz.

### SSS

#### S: İçerik türü özellikleri Excel'in tüm sürümleriyle uyumlu mu?

Y: Evet, içerik türü özellikleri, Excel'in tüm sürümlerinde oluşturulan Excel dosyalarıyla uyumludur.

#### S: İçerik türü özelliklerini Excel çalışma kitabına ekledikten sonra düzenleyebilir miyim?

 C: Evet, içerik türü özelliklerini istediğiniz zaman şu adrese giderek değiştirebilirsiniz:`ContentTypeProperties` koleksiyonu`Workbook` sınıf ve ve p yöntemlerine uygun özellikleri kullanma.

#### S: PDF'ye kaydederken içerik türü özellikleri destekleniyor mu?

C: Hayır, PDF'ye kaydederken içerik türü özellikleri desteklenmez. Excel dosyalarına özgüdürler.