---
title: Sayfa Yapısı Ayarlarını Diğer Çalışma Sayfasından Kopyala
linktitle: Sayfa Yapısı Ayarlarını Diğer Çalışma Sayfasından Kopyala
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak sayfa yapılandırma ayarlarını bir e-tablodan diğerine nasıl kopyalayacağınızı öğrenin. Bu kitaplığın kullanımını optimize etmeye yönelik adım adım kılavuz.
type: docs
weight: 10
url: /tr/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Bu makalede, sizi adım adım aşağıdaki C# kaynak kodunu açıklamaya yönlendireceğiz: Aspose.Cells for .NET kullanarak sayfa yapılandırma ayarlarını başka bir elektronik tablodan kopyalayın. Bu işlemi gerçekleştirmek için .NET için Aspose.Cells kütüphanesini kullanacağız. Sayfa yapısı ayarlarını bir çalışma sayfasından diğerine kopyalamak istiyorsanız aşağıdaki adımları izleyin.

## Adım 1: Çalışma Kitabını Oluşturma
İlk adım bir çalışma kitabı oluşturmaktır. Bizim durumumuzda Aspose.Cells kütüphanesinin sağladığı Workbook sınıfını kullanacağız. İşte çalışma kitabı oluşturma kodu:

```csharp
Workbook wb = new Workbook();
```

## Adım 2: Test Çalışma Sayfalarını Ekleme
Çalışma kitabını oluşturduktan sonra test çalışma sayfalarını eklememiz gerekiyor. Bu örnekte iki çalışma sayfası ekleyeceğiz. İki çalışma sayfası ekleme kodu:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## 3. Adım: Çalışma Sayfalarına Erişim
Artık çalışma sayfalarını eklediğimize göre, ayarlarını değiştirebilmek için onlara erişmemiz gerekiyor. "TestSheet1" ve "TestSheet2" çalışma sayfalarına adlarını kullanarak erişeceğiz. İşte ona erişmenizi sağlayacak kod:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Adım 4: Kağıt Boyutunu Ayarlama
 Bu adımda "TestSheet1" çalışma sayfasının kağıt boyutunu ayarlayacağız. kullanacağız`PageSetup.PaperSize` Kağıt boyutunu ayarlama özelliği. Örneğin kağıt boyutunu "PaperA3ExtraTransverse" olarak ayarlayacağız. İşte bunun için kod:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Adım 5: Sayfa Yapısı Ayarlarını Kopyalama
Şimdi "TestSheet1" çalışma sayfasından sayfa yapılandırma ayarlarını "TestSheet2"ye kopyalayacağız. kullanacağız`PageSetup.Copy` Bu işlemi gerçekleştirmek için yöntem. İşte bunun için kod:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Adım 6: Kağıt Boyutlarını Yazdırma
 Sayfa düzeni ayarlarını kopyaladıktan sonra iki çalışma sayfasının kağıt boyutlarını yazdıracağız. Kullanacağız`Console.WriteLine` Kağıt boyutlarını görüntülemek için. İşte bunun için kod:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Aspose.Cells for .NET kullanarak Sayfa Yapısı Ayarlarını Diğer Çalışma Sayfalarından Kopyalamak için örnek kaynak kodu 
```csharp
//Çalışma kitabı oluştur
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
Bu makalede Aspose.Cells for .NET kullanarak sayfa yapılandırma ayarlarını bir çalışma sayfasından diğerine nasıl kopyalayacağımızı öğrendik. Şu adımları izledik: çalışma kitabını oluşturmak, test çalışma sayfalarını eklemek, çalışma sayfalarına erişmek, kağıt boyutunu ayarlamak, sayfa düzeni ayarlarını kopyalamak ve kağıt boyutlarını yazdırmak. Artık bu bilgiyi sayfa yapılandırma ayarlarını kendi projelerinize kopyalamak için kullanabilirsiniz.

### SSS

#### S: Sayfa yapılandırma ayarlarını farklı çalışma kitabı örnekleri arasında kopyalayabilir miyim?

 C: Evet, sayfa yapısı ayarlarını farklı çalışma kitabı örnekleri arasında kopyalayabilirsiniz.`PageSetup.Copy` Aspose.Cells kütüphanesinin yöntemi.

#### S: Yön veya kenar boşlukları gibi diğer sayfa düzeni ayarlarını kopyalayabilir miyim?

 C: Evet, diğer sayfa düzeni ayarlarını kullanarak kopyalayabilirsiniz.`PageSetup.Copy` Uygun seçeneklerle yöntem. Örneğin, yönlendirmeyi kullanarak kopyalayabilirsiniz.`CopyOptions.Orientation` ve kenar boşlukları kullanılarak`CopyOptions.Margins`.

#### S: Kağıt boyutu için hangi seçeneklerin mevcut olduğunu nasıl bilebilirim?

C: Mevcut kağıt boyutu seçenekleri için Aspose.Cells kütüphanesi API Referansını kontrol edebilirsiniz. adında bir numaralandırma var`PaperSizeType` desteklenen farklı kağıt boyutlarını listeler.

#### S: .NET için Aspose.Cells kütüphanesini nasıl indirebilirim?

 C: .NET için Aspose.Cells kütüphanesini şu adresten indirebilirsiniz:[Sürümleri Aspose](https://releases.aspose.com/cells/net). Ücretsiz deneme sürümlerinin yanı sıra ticari kullanım için ücretli lisanslar da mevcuttur.

#### S: Aspose.Cells kütüphanesi diğer programlama dillerini destekliyor mu?

C: Evet, Aspose.Cells kütüphanesi C#, Java, Python ve daha pek çok programlama dilini destekler.