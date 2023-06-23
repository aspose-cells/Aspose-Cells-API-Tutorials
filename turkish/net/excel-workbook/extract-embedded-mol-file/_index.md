---
title: Gömülü Mol Dosyasını Çıkarın
linktitle: Gömülü Mol Dosyasını Çıkarın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak gömülü MOL dosyalarını bir Excel çalışma kitabından kolayca nasıl çıkaracağınızı öğrenin.
type: docs
weight: 90
url: /tr/net/excel-workbook/extract-embedded-mol-file/
---
Bu öğreticide, .NET için Aspose.Cells kitaplığını kullanarak bir Excel çalışma kitabından katıştırılmış bir MOL dosyasını nasıl çıkaracağınızı adım adım anlatacağız. Çalışma kitabı sayfalarına göz atmayı, karşılık gelen OLE nesnelerini çıkarmayı ve çıkarılan MOL dosyalarını kaydetmeyi öğreneceksiniz. Bu görevi başarıyla tamamlamak için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıktı dizinlerini tanımlayın
Öncelikle kodumuzda kaynak ve çıktı dizinlerini tanımlamamız gerekiyor. Bu dizinler, kaynak Excel çalışma kitabının nerede olduğunu ve çıkarılan MOL dosyalarının nereye kaydedileceğini gösterir. İşte ilgili kod:

```csharp
// dizinler
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Gerektiğinde uygun yolları belirttiğinizden emin olun.

## 2. Adım: Excel çalışma kitabını yükleme
Sonraki adım, katıştırılmış OLE nesnelerini ve MOL dosyalarını içeren Excel çalışma kitabını yüklemektir. İşte çalışma kitabını yüklemek için kod:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Kaynak dosya adını kodda doğru şekilde belirttiğinizden emin olun.

## 3. Adım: Sayfaları dolaşın ve MOL dosyalarını çıkarın
Şimdi çalışma kitabındaki her bir sayfayı dolaşacağız ve MOL dosyalarını içeren karşılık gelen OLE nesnelerini çıkaracağız. İşte ilgili kod:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Bu kod, çalışma kitabındaki her sayfada döngü halinde dolaşır, OLE nesnelerini getirir ve ayıklanan MOL dosyalarını çıkış dizinine kaydeder.

### Aspose.Cells for .NET kullanarak Gömülü Mol Dosyasını Çıkarmak için örnek kaynak kodu 
```csharp
//dizinler
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Çözüm
Tebrikler! Aspose.Cells for .NET kullanarak gömülü bir MOL dosyasını bir Excel çalışma kitabından nasıl çıkaracağınızı öğrendiniz. Artık bu bilgiyi MOL dosyalarını kendi Excel çalışma kitaplarınızdan ayıklamak için uygulayabilirsiniz. Aspose.Cells kitaplığını daha fazla keşfetmekten çekinmeyin ve diğer güçlü özellikleri hakkında bilgi edinin.

### SSS

#### S: MOL dosyası nedir?
 
A: Bir MOL dosyası, hesaplamalı kimyada kimyasal yapıları temsil etmek için kullanılan bir dosya formatıdır. Atomlar, bağlar ve diğer moleküler özellikler hakkında bilgi içerir.

#### S: Bu yöntem tüm Excel dosya türleriyle çalışır mı?

C: Evet, bu yöntem Aspose.Cells tarafından desteklenen tüm Excel dosya türleriyle çalışır.

#### S: Aynı anda birden çok MOL dosyasını çıkarabilir miyim?

Y: Evet, çalışma kitabındaki her sayfada OLE nesnelerini yineleyerek birden çok MOL dosyasını aynı anda çıkarabilirsiniz.