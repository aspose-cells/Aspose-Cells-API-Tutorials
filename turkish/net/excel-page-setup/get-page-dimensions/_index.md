---
title: Sayfa Boyutlarını Alın
linktitle: Sayfa Boyutlarını Alın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel'de sayfa boyutlarını nasıl alacağınızı öğrenin. C# dilinde kaynak koduyla adım adım kılavuz.
type: docs
weight: 40
url: /tr/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET, geliştiricilerin Microsoft Excel dosyalarıyla programlı olarak çalışmasına olanak tanıyan güçlü bir kitaplıktır. Sayfa boyutlarını alma yeteneği de dahil olmak üzere Excel belgelerini işlemek için çok çeşitli özellikler sunar. Bu öğreticide, Aspose.Cells for .NET kullanarak sayfa boyutlarını alma adımlarında size yol göstereceğiz.

## 1. Adım: Workbook sınıfının bir örneğini oluşturun

Başlamak için, Excel çalışma kitabını temsil eden Workbook sınıfının bir örneğini oluşturmamız gerekiyor. Bu, aşağıdaki kod kullanılarak elde edilebilir:

```csharp
Workbook book = new Workbook();
```

## 2. Adım: Elektronik tabloya erişme

Ardından, çalışma kitabında sayfa boyutlarını ayarlamak istediğimiz çalışma sayfasına gitmemiz gerekiyor. Bu örnekte, ilk çalışma sayfasıyla çalışmak istediğimizi varsayalım. Aşağıdaki kodu kullanarak ona erişebiliriz:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 3. Adım: Kağıt boyutunu A2 olarak ayarlayın ve genişliği ve yüksekliği inç olarak yazdırın

Şimdi kağıt boyutunu A2 olarak ayarlayıp sayfa genişliğini ve yüksekliğini inç cinsinden yazdıracağız. Bu, aşağıdaki kod kullanılarak elde edilebilir:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 4. Adım: Kağıt boyutunu A3 olarak ayarlayın ve genişliği ve yüksekliği inç cinsinden yazdırın

Ardından, kağıt boyutunu A3 olarak ayarlayacağız ve sayfa genişliğini ve yüksekliğini inç cinsinden yazdıracağız. İşte ilgili kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Adım 5: Kağıt boyutunu A4 olarak ayarlayın ve genişliği ve yüksekliği inç olarak yazdırın

Şimdi kağıt boyutunu A4 olarak ayarlayıp sayfa genişliğini ve yüksekliğini inç cinsinden yazdıracağız. İşte kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Adım 6: Kağıt boyutunu Letter olarak ayarlayın ve genişliği ve yüksekliği inç olarak yazdırın

Son olarak, kağıt boyutunu Letter olarak ayarlayacağız ve sayfa genişliğini ve yüksekliğini inç cinsinden yazdıracağız. İşte kod:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Aspose.Cells for .NET kullanarak Get Page Dimensions için örnek kaynak kodu 
```csharp
// Workbook sınıfının bir örneğini oluşturun
Workbook book = new Workbook();
// İlk çalışma sayfasına erişin
Worksheet sheet = book.Worksheets[0];
// Kağıt boyutunu A2 olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç olarak yazdırın
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Kağıt boyutunu A3 olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç cinsinden yazdırın
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Kağıt boyutunu A4 olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç olarak yazdırın
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Kağıt boyutunu Letter olarak ayarlayın ve kağıt genişliğini ve yüksekliğini inç olarak yazdırın
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak sayfa boyutlarını nasıl alacağınızı öğrendiniz. Bu özellik, Excel dosyalarınızda sayfa boyutlarına dayalı olarak belirli işlemler gerçekleştirmeniz gerektiğinde yararlı olabilir.

Aspose.Cells'in sunduğu tüm güçlü özellikleri keşfetmek için belgelerini incelemeyi unutmayın.

### SSS

#### 1. Aspose.Cells for .NET başka hangi kağıt boyutlarını destekliyor?

Aspose.Cells for .NET, A1, A5, B4, B5, Executive, Legal, Letter ve çok daha fazlasını içeren çeşitli kağıt boyutlarını destekler. Desteklenen kağıt boyutlarının tam listesi için belgelere bakabilirsiniz.

#### 2. Aspose.Cells for .NET ile özel sayfa boyutları belirleyebilir miyim?

Evet, istediğiniz genişlik ve yüksekliği belirterek özel sayfa boyutları belirleyebilirsiniz. Aspose.Cells, sayfa boyutlarını ihtiyaçlarınıza göre özelleştirmek için tam esneklik sunar.

#### 3. İnç dışındaki birimlerde sayfa boyutları alabilir miyim?

Evet, Aspose.Cells for .NET sayfa boyutlarını inç, santimetre, milimetre ve punto gibi farklı birimlerde almanızı sağlar.

#### 4. Aspose.Cells for .NET diğer sayfa ayarları düzenleme özelliklerini destekliyor mu?

Evet, Aspose.Cells sayfa ayarlarını düzenlemek için kenar boşlukları, yönlendirme, üstbilgiler ve altbilgiler vb. dahil olmak üzere çok çeşitli özellikler sunar.