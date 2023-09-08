---
title: Gömülü Mol Dosyasını Çıkart
linktitle: Gömülü Mol Dosyasını Çıkart
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak gömülü MOL dosyalarını bir Excel çalışma kitabından nasıl kolayca çıkaracağınızı öğrenin.
type: docs
weight: 90
url: /tr/net/excel-workbook/extract-embedded-mol-file/
---
Bu eğitimde, .NET için Aspose.Cells kütüphanesini kullanarak gömülü bir MOL dosyasını bir Excel çalışma kitabından nasıl çıkaracağınızı adım adım anlatacağız. Çalışma kitabı sayfalarına nasıl göz atacağınızı, karşılık gelen OLE nesnelerini nasıl çıkaracağınızı ve çıkarılan MOL dosyalarını nasıl kaydedeceğinizi öğreneceksiniz. Bu görevi başarıyla tamamlamak için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıktı dizinlerini tanımlayın
Öncelikle kodumuzda kaynak ve çıktı dizinlerini tanımlamamız gerekiyor. Bu dizinler, kaynak Excel çalışma kitabının nerede bulunduğunu ve çıkarılan MOL dosyalarının nereye kaydedileceğini gösterir. İşte ilgili kod:

```csharp
// Dizinler
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Gerektiğinde uygun yolları belirttiğinizden emin olun.

## Adım 2: Excel çalışma kitabını yükleme
Bir sonraki adım, katıştırılmış OLE nesnelerini ve MOL dosyalarını içeren Excel çalışma kitabını yüklemektir. Çalışma kitabını yüklemek için gereken kod:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Kodda kaynak dosya adını doğru belirttiğinizden emin olun.

## Adım 3: Sayfaları dolaşın ve MOL dosyalarını çıkarın
Şimdi çalışma kitabındaki her sayfada döngü yapacağız ve MOL dosyalarını içeren ilgili OLE nesnelerini çıkaracağız. İşte ilgili kod:

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

Bu kod, çalışma kitabındaki her sayfada döngü yapar, OLE nesnelerini getirir ve çıkarılan MOL dosyalarını çıkış dizinine kaydeder.

### Aspose.Cells for .NET kullanarak Gömülü Mol Dosyasını Çıkarma için örnek kaynak kodu 
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
Tebrikler! Aspose.Cells for .NET'i kullanarak bir Excel çalışma kitabından gömülü bir MOL dosyasını nasıl çıkaracağınızı öğrendiniz. Artık bu bilgiyi kendi Excel çalışma kitaplarınızdan MOL dosyalarını ayıklamak için uygulayabilirsiniz. Aspose.Cells kütüphanesini daha fazla keşfetmekten ve diğer güçlü özellikleri hakkında bilgi edinmekten çekinmeyin.

### SSS

#### S: MOL dosyası nedir?
 
C: MOL dosyası, hesaplamalı kimyadaki kimyasal yapıları temsil etmek için kullanılan bir dosya formatıdır. Atomlar, bağlar ve diğer moleküler özellikler hakkında bilgi içerir.

#### S: Bu yöntem tüm Excel dosya türleriyle çalışır mı?

C: Evet, bu yöntem Aspose.Cells tarafından desteklenen tüm Excel dosya türleriyle çalışır.

#### S: Aynı anda birden fazla MOL dosyasını çıkarabilir miyim?

C: Evet, çalışma kitabındaki her sayfada OLE nesneleri arasında yineleme yaparak birden fazla MOL dosyasını aynı anda çıkarabilirsiniz.