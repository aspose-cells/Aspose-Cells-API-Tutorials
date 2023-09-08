---
title: Çalışma Kitabı Yazdırma Önizleme
linktitle: Çalışma Kitabı Yazdırma Önizleme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir çalışma kitabının baskı ön izlemesini nasıl oluşturacağınızı öğrenin.
type: docs
weight: 170
url: /tr/net/excel-workbook/workbook-print-preview/
---
Çalışma Kitabının baskı önizlemesi, Aspose.Cells for .NET ile Excel dosyalarıyla çalışırken önemli bir özelliktir. Aşağıdaki adımları izleyerek kolayca bir baskı önizlemesi oluşturabilirsiniz:

## 1. Adım: Kaynak dizini belirtin

Öncelikle önizlemesini yapmak istediğiniz Excel dosyasının bulunduğu kaynak dizini belirtmeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Adım 2: Çalışma Kitabını Yükleyin

Daha sonra Çalışma Kitabı çalışma kitabını belirtilen Excel dosyasından yüklemeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çalışma Kitabı çalışma kitabını yükleme
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## 3. Adım: Görüntüyü ve yazdırma seçeneklerini yapılandırın

Baskı önizlemeyi oluşturmadan önce görüntüyü ve yazdırma seçeneklerini gerektiği gibi yapılandırabilirsiniz. Bu örnekte varsayılan seçenekleri kullanıyoruz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Resim ve yazdırma seçenekleri
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## 4. Adım: Çalışma kitabının baskı önizlemesini oluşturun

Artık WorkbookPrintingPreview sınıfını kullanarak Workbook çalışma kitabının baskı önizlemesini oluşturabilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çalışma kitabının önizlemesini yazdır
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Adım 5: Çalışma sayfasının baskı önizlemesini oluşturun

Belirli bir çalışma sayfasının baskı önizlemesini oluşturmak istiyorsanız SheetPrintingPreview sınıfını kullanabilirsiniz. İşte bir örnek :

```csharp
// Çalışma sayfasının önizlemesini yazdır
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Aspose.Cells for .NET kullanan Workbook Print Preview için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Çözüm

Bir çalışma kitabının baskı ön izlemesini oluşturmak Aspose.Cells for .NET tarafından sunulan güçlü bir özelliktir. Yukarıda verilen adımları takip ederek Excel çalışma kitabınızı kolayca önizleyebilir ve yazdırılacak sayfa sayısı hakkında bilgi alabilirsiniz.

### SSS

#### S: Çalışma Kitabımı yüklemek için farklı bir kaynak dizini nasıl belirleyebilirim?
    
 C: Kullanabilirsiniz`Set_SourceDirectory` Farklı bir kaynak dizini belirtme yöntemini kullanın. Örneğin:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### S: Baskı önizlemesini oluştururken görüntüyü ve yazdırma seçeneklerini özelleştirebilir miyim?
    
 C: Evet, görselin özelliklerini değiştirerek görsel ve baskı seçeneklerini özelleştirebilirsiniz.`ImageOrPrintOptions` nesne. Örneğin, görüntü çözünürlüğünü, çıktı dosyası formatını vb. ayarlayabilirsiniz.

#### S: Bir Çalışma Kitabındaki birden çok çalışma sayfası için baskı önizlemesi oluşturmak mümkün müdür?
    
C: Evet, Çalışma Kitabındaki farklı çalışma sayfalarını yineleyebilir ve her sayfa için bir baskı ön izlemesi oluşturabilirsiniz.`SheetPrintingPreview` sınıf.

#### S: Baskı önizlemeyi resim veya PDF dosyası olarak nasıl kaydederim?
    
 C: Kullanabilirsiniz`ToImage` veya`ToPdf` yöntemi`WorkbookPrintingPreview` veya`SheetPrintingPreview` Baskı önizlemesini görüntü veya PDF dosyası olarak kaydetmek için nesneyi seçin.

#### S: Baskı ön izleme oluşturulduktan sonra ne yapabilirim?
    
C: Baskı önizlemesini oluşturduktan sonra bunu ekranda görüntüleyebilir, resim veya PDF dosyası olarak kaydedebilir veya e-postayla gönderme veya yazdırma gibi diğer işlemler için kullanabilirsiniz.
	