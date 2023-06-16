---
title: Çalışma Sayfasının Kağıt Genişliğini ve Yüksekliğini Alın
linktitle: Çalışma Sayfasının Kağıt Genişliğini ve Yüksekliğini Alın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir elektronik tablonun kağıt genişliğini ve yüksekliğini elde etmek için aşağıdaki C# kaynak kodunu açıklayan bir adım adım kılavuz oluşturun.
type: docs
weight: 80
url: /tr/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
Bu eğitimde, Aspose.Cells for .NET kullanarak bir çalışma sayfasının kağıt genişliğini ve yüksekliğini elde etmek için aşağıdaki C# kaynak kodunu adım adım açıklayacağız. Aşağıdaki adımları takip et:

## 1. Adım: Çalışma kitabını oluşturun
 kullanarak yeni bir çalışma kitabı oluşturarak başlayın.`Workbook` sınıf:

```csharp
Workbook wb = new Workbook();
```

## 2. Adım: İlk çalışma sayfasına erişin
 Ardından, çalışma kitabındaki ilk çalışma sayfasına gidin.`Worksheet` sınıf:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## 3. Adım: Kağıt boyutunu A2 olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç cinsinden gösterin
 Kullan`PaperSize` mülkiyeti`PageSetup` Kağıt boyutunu A2 olarak ayarlamak için nesneyi kullanın, ardından`PaperWidth` Ve`PaperHeight` Sırasıyla kağıt genişliğini ve yüksekliğini elde etmek için özellikler. kullanarak bu değerleri görüntüleyin.`Console.WriteLine` yöntem:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## 4. Adım: Diğer kağıt boyutları için adımları tekrarlayın
Kağıt boyutunu A3, A4 ve Letter olarak değiştirerek ve ardından her boyut için kağıt genişliği ve yükseklik değerlerini görüntüleyerek önceki adımları tekrarlayın:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Aspose.Cells for .NET kullanarak Çalışma Sayfasının Kağıt Genişliğini ve Yüksekliğini Al için örnek kaynak kodu 

```csharp
//çalışma kitabı oluştur
Workbook wb = new Workbook();
//İlk çalışma sayfasına erişin
Worksheet ws = wb.Worksheets[0];
//Kağıt boyutunu A2 olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç olarak yazdırın
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Kağıt boyutunu A3 olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç cinsinden yazdırın
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Kağıt boyutunu A4 olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç olarak yazdırın
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Kağıt boyutunu Letter olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç cinsinden yazdırın
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Çözüm

Bir elektronik tablonun kağıt genişliğini ve yüksekliğini elde etmek için Aspose.Cells for .NET'i nasıl kullanacağınızı öğrendiniz. Bu özellik, Excel belgelerinizin yapılandırması ve kesin düzeni için yararlı olabilir.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını manipüle etmek ve işlemek için güçlü bir kitaplıktır. Excel dosyalarını oluşturmak, değiştirmek, dönüştürmek ve analiz etmek için birçok özellik sunar.

#### Aspose.Cells for .NET ile bir elektronik tablonun kağıt boyutunu nasıl alabilirim?

 kullanabilirsiniz`PageSetup` sınıfı`Worksheet` Kağıt boyutuna erişmek için nesne. Kullan`PaperSize` özelliği, kağıt boyutunu ve`PaperWidth` Ve`PaperHeight` Sırasıyla kağıt genişliğini ve yüksekliğini elde etmek için özellikler.

#### Aspose.Cells for .NET hangi kağıt boyutlarını destekliyor?

Aspose.Cells for .NET, A2, A3, A4 ve Letter gibi çok çeşitli yaygın olarak kullanılan kağıt boyutlarının yanı sıra diğer birçok özel boyutu da destekler.

#### Aspose.Cells for .NET ile bir elektronik tablonun kağıt boyutunu özelleştirebilir miyim?

Evet, kullanarak tam genişlik ve yükseklik boyutlarını belirterek özel bir kağıt boyutu ayarlayabilirsiniz.`PaperWidth` Ve`PaperHeight` özellikleri`PageSetup` sınıf.