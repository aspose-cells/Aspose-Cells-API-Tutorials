---
title: Diğer Çalışma Sayfasından Sayfa Yapısı Ayarlarını Kopyala
linktitle: Diğer Çalışma Sayfasından Sayfa Yapısı Ayarlarını Kopyala
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak sayfa yapılandırma ayarlarını bir elektronik tablodan diğerine nasıl kopyalayacağınızı öğrenin. Bu kitaplığın kullanımını optimize etmek için adım adım kılavuz.
type: docs
weight: 10
url: /tr/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Bu makalede, aşağıdaki C# kaynak kodunu açıklamak için size adım adım yol göstereceğiz: Aspose.Cells for .NET kullanarak sayfa yapılandırma ayarlarını başka bir elektronik tablodan kopyalayın. Bu işlemi gerçekleştirmek için .NET için Aspose.Cells kütüphanesini kullanacağız. Sayfa yapısı ayarlarını bir çalışma sayfasından diğerine kopyalamak istiyorsanız, aşağıdaki adımları izleyin.

## 1. Adım: Çalışma Kitabını Oluşturma
İlk adım bir çalışma kitabı oluşturmaktır. Bizim durumumuzda Aspose.Cells kütüphanesi tarafından sağlanan Workbook sınıfını kullanacağız. İşte bir çalışma kitabı oluşturmak için kod:

```csharp
Workbook wb = new Workbook();
```

## 2. Adım: Test Çalışma Sayfaları Ekleme
Çalışma kitabını oluşturduktan sonra test çalışma sayfalarını eklememiz gerekiyor. Bu örnekte, iki çalışma sayfası ekleyeceğiz. İşte iki çalışma sayfası eklemek için kod:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## 3. Adım: Çalışma Sayfalarına Erişim
Artık çalışma sayfalarını eklediğimize göre, ayarlarını değiştirebilmek için onlara erişmemiz gerekiyor. "TestSheet1" ve "TestSheet2" çalışma sayfalarına isimlerini kullanarak ulaşacağız. İşte ona erişmek için kod:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## 4. Adım: Kağıt Boyutunu Ayarlama
 Bu adımda "TestSheet1" çalışma sayfasının kağıt boyutunu ayarlayacağız. biz kullanacağız`PageSetup.PaperSize` kağıt boyutunu ayarlama özelliği. Örneğin, kağıt boyutunu "PaperA3ExtraTransverse" olarak ayarlayacağız. İşte bunun için kod:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Adım 5: Sayfa Yapısı Ayarlarını Kopyalama
 Şimdi sayfa yapılandırma ayarlarını "TestSheet1" çalışma sayfasından "TestSheet2"ye kopyalayacağız. biz kullanacağız`PageSetup.Copy` Bu işlemi gerçekleştirmek için yöntem. İşte bunun için kod:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Adım 6: Kağıt Boyutlarını Yazdırma
 Sayfa kurulum ayarlarını kopyaladıktan sonra iki çalışma sayfasının kağıt boyutlarını yazdıracağız. Kullanacağız`Console.WriteLine` Kağıt boyutlarını görüntülemek için İşte bunun için kod:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Aspose.Cells for .NET kullanarak Diğer Çalışma Sayfasından Sayfa Kurulum Ayarlarını Kopyalamak için örnek kaynak kodu 
```csharp
//çalışma kitabı oluştur
Workbook wb = new Workbook();
//İki test çalışma sayfası ekleyin
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Her iki çalışma sayfasına da TestSheet1 ve TestSheet2 olarak erişin
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//TestSheet1'in Kağıt Boyutunu PaperA3ExtraTransverse olarak ayarlayın
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Her iki çalışma sayfasının Kağıt Boyutunu yazdırın
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//PageSetup'ı TestSheet1'den TestSheet2'ye kopyalayın
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Her iki çalışma sayfasının Kağıt Boyutunu yazdırın
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Çözüm
Bu makalede, Aspose.Cells for .NET kullanarak sayfa yapılandırma ayarlarının bir çalışma sayfasından diğerine nasıl kopyalanacağını öğrendik. Çalışma kitabının oluşturulması, test çalışma sayfalarının eklenmesi, çalışma sayfalarına erişim, kağıt boyutunun ayarlanması, sayfa düzeni ayarlarının kopyalanması ve kağıt boyutlarının yazdırılması adımlarından geçtik. Artık bu bilgiyi, sayfa yapılandırma ayarlarını kendi projelerinize kopyalamak için kullanabilirsiniz.

### SSS

S: Farklı çalışma kitabı örnekleri arasında sayfa yapılandırma ayarlarını kopyalayabilir miyim?

 Y: Evet, farklı çalışma kitabı örnekleri arasında sayfa yapısı ayarlarını kopyalayabilirsiniz.`PageSetup.Copy` Aspose.Cells kitaplığının yöntemi.

S: Yön veya kenar boşlukları gibi diğer sayfa düzeni ayarlarını kopyalayabilir miyim?

 A: Evet, diğer sayfa kurulum ayarlarını kullanarak kopyalayabilirsiniz.`PageSetup.Copy` Uygun seçeneklerle yöntem. Örneğin, yönlendirmeyi kullanarak kopyalayabilirsiniz.`CopyOptions.Orientation` ve kenar boşluklarını kullanarak`CopyOptions.Margins`.

S: Kağıt boyutu için hangi seçeneklerin mevcut olduğunu nasıl bilebilirim?

 C: Mevcut kağıt boyutu seçenekleri için Aspose.Cells library API Reference'a bakabilirsiniz. diye bir numara var`PaperSizeType` desteklenen farklı kağıt boyutlarını listeler.

S: .NET için Aspose.Cells kitaplığını nasıl indirebilirim?

 C: .NET için Aspose.Cells kitaplığını adresinden indirebilirsiniz.[Bültenler](https://releases.aspose.com/cells/net). Ücretsiz deneme sürümlerinin yanı sıra ticari kullanım için ücretli lisanslar da mevcuttur.

S: Aspose.Cells kütüphanesi diğer programlama dillerini destekliyor mu?

C: Evet, Aspose.Cells kitaplığı C#, Java, Python ve daha birçok programlama dilini destekler.