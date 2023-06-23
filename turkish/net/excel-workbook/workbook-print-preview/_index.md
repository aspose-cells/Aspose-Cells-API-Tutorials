---
title: Çalışma Kitabı Baskı Önizleme
linktitle: Çalışma Kitabı Baskı Önizleme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir çalışma kitabının baskı önizlemesini nasıl oluşturacağınızı öğrenin.
type: docs
weight: 170
url: /tr/net/excel-workbook/workbook-print-preview/
---
Bir Çalışma Kitabının baskı önizlemesi, Aspose.Cells for .NET ile Excel dosyalarıyla çalışırken önemli bir özelliktir. Aşağıdaki adımları izleyerek kolayca bir baskı ön izleme oluşturabilirsiniz:

## 1. Adım: Kaynak dizini belirtin

Öncelikle, önizlemesini yapmak istediğiniz Excel dosyasının bulunduğu kaynak dizini belirtmeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// kaynak dizin
string sourceDir = RunExamples.Get_SourceDirectory();
```

## 2. Adım: Çalışma Kitabını Yükleyin

Ardından, Çalışma Kitabı çalışma kitabını belirtilen Excel dosyasından yüklemeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çalışma Kitabı çalışma kitabını yükleyin
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## 3. Adım: Görüntü ve yazdırma seçeneklerini yapılandırın

Baskı ön izlemeyi oluşturmadan önce, görüntüyü ve baskı seçeneklerini gerektiği gibi yapılandırabilirsiniz. Bu örnekte, varsayılan seçenekleri kullanıyoruz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Resim ve baskı seçenekleri
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## 4. Adım: Çalışma kitabının baskı ön izlemesini oluşturun

Artık WorkbookPrintingPreview sınıfını kullanarak Workbook çalışma kitabının baskı ön izlemesini oluşturabilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çalışma kitabının baskı önizlemesi
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Adım 5: Çalışma sayfasının baskı ön izlemesini oluşturun

Belirli bir çalışma sayfasının baskı önizlemesini oluşturmak istiyorsanız SheetPrintingPreview sınıfını kullanabilirsiniz. İşte bir örnek :

```csharp
// Çalışma sayfasının baskı önizlemesi
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

Bir çalışma kitabının baskı önizlemesini oluşturmak, Aspose.Cells for .NET tarafından sunulan güçlü bir özelliktir. Yukarıda verilen adımları takip ederek, Excel çalışma kitabınızı kolayca önizleyebilir ve yazdırılacak sayfa sayısı hakkında bilgi alabilirsiniz.

### SSS

#### S: Çalışma Kitabımı yüklemek için farklı bir kaynak dizini nasıl belirleyebilirim?
    
 C: Şunu kullanabilirsiniz:`Set_SourceDirectory` farklı bir kaynak dizini belirtme yöntemi. Örneğin:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### S: Baskı ön izleme oluştururken görüntü ve baskı seçeneklerini özelleştirebilir miyim?
    
 C: Evet, görüntü ve yazdırma seçeneklerini, özellikleri değiştirerek özelleştirebilirsiniz.`ImageOrPrintOptions` nesne. Örneğin, görüntü çözünürlüğünü, çıktı dosyası biçimini vb. ayarlayabilirsiniz.

#### S: Bir Çalışma Kitabında birden çok çalışma sayfası için baskı ön izleme oluşturmak mümkün müdür?
    
C: Evet, Çalışma Kitabındaki farklı çalışma sayfalarını yineleyebilir ve her sayfa için bir baskı ön izleme oluşturabilirsiniz.`SheetPrintingPreview` sınıf.

#### S: Baskı ön izlemeyi resim veya PDF dosyası olarak nasıl kaydedebilirim?
    
 A: kullanabilirsiniz`ToImage` veya`ToPdf` yöntemi`WorkbookPrintingPreview` veya`SheetPrintingPreview` baskı ön izlemeyi görüntü veya PDF dosyası olarak kaydetmek için nesne.

#### S: Oluşturulduktan sonra baskı ön izleme ile ne yapabilirim?
    
C: Baskı ön izlemeyi oluşturduktan sonra ekranda görüntüleyebilir, resim veya PDF dosyası olarak kaydedebilir veya e-postayla gönderme veya yazdırma gibi diğer işlemler için kullanabilirsiniz.
	