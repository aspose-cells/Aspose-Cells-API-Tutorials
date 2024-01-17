---
title: Paylaşılan Çalışma Kitabı Oluştur
linktitle: Paylaşılan Çalışma Kitabı Oluştur
second_title: Aspose.Cells for .NET API Referansı
description: Eş zamanlı veri işbirliğini etkinleştirmek için Aspose.Cells for .NET ile bir Excel paylaşımlı çalışma kitabı oluşturun.
type: docs
weight: 70
url: /tr/net/excel-workbook/create-shared-workbook/
---
Bu eğitimde, Aspose.Cells for .NET'i kullanarak paylaşılan bir çalışma kitabı oluşturmanıza olanak tanıyan sağlanan C# kaynak kodunu size anlatacağız. Bu işlemi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Çıkış dizinini ayarlayın

```csharp
// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda paylaşılan çalışma kitabının kaydedileceği çıktı dizinini tanımlıyoruz.

## Adım 2: Çalışma Kitabı Nesnesi Oluşturun

```csharp
// Çalışma Kitabı nesnesi oluşturma
Workbook wb = new Workbook();
```

Excel çalışma kitabımızı temsil edecek yeni bir Çalışma Kitabı nesnesi oluşturuyoruz.

## 3. Adım: Çalışma Kitabı Paylaşımını Etkinleştirin

```csharp
// Çalışma kitabını paylaşın
wb.Settings.Shared = true;
```

 Çalışma kitabının paylaşım özelliğini ayarlayarak etkinleştiriyoruz.`Shared` Çalışma Kitabı nesnesinin özelliği`true`.

## 4. Adım: Paylaşılan çalışma kitabını kaydedin

```csharp
// Paylaşılan çalışma kitabını kaydet
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Çıktı dosyasının yolunu ve adını belirterek paylaşılan çalışma kitabını kaydediyoruz.

### Aspose.Cells for .NET kullanarak Paylaşılan Çalışma Kitabı Oluşturmak için örnek kaynak kodu 
```csharp
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Çalışma Kitabı nesnesi oluştur
Workbook wb = new Workbook();
//Çalışma Kitabını Paylaşın
wb.Settings.Shared = true;
//Paylaşılan Çalışma Kitabını Kaydet
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET'i kullanarak paylaşılan bir çalışma kitabının nasıl oluşturulacağını öğrendiniz. Paylaşılan çalışma kitabı, veriler üzerinde işbirliği yapmak için birden fazla kullanıcı tarafından aynı anda kullanılabilir. Güçlü ve kişiselleştirilmiş Excel çalışma kitapları oluşturmak için kendi verilerinizle denemeler yapın ve Aspose.Cells'in özelliklerini daha fazla keşfedin.

### SSS

#### S: Paylaşılan çalışma kitabı nedir?

C: Paylaşılan çalışma kitabı, birden çok kullanıcı tarafından veriler üzerinde işbirliği yapmak için aynı anda kullanılabilen bir Excel çalışma kitabıdır. Her kullanıcı çalışma kitabında değişiklik yapabilir ve diğer kullanıcılar güncellemeleri gerçek zamanlı olarak görebilir.

#### S: Aspose.Cells for .NET'te çalışma kitabı paylaşımı nasıl etkinleştirilir?

 C: Aspose.Cells for .NET'te bir çalışma kitabının paylaşımını etkinleştirmek için`Shared` Çalışma Kitabı nesnesinin özelliği`true`. Bu, kullanıcıların çalışma kitabı üzerinde aynı anda çalışmasına olanak tanır.

#### S: Paylaşılan bir çalışma kitabındaki kullanıcı izinlerini kısıtlayabilir miyim?

C: Evet, paylaşılan bir çalışma kitabındaki kullanıcı izinlerini Excel'in güvenlik özelliklerini kullanarak kısıtlayabilirsiniz. Her kullanıcı için düzenleme, salt okuma vb. gibi belirli izinler ayarlayabilirsiniz.

#### S: Çalışma kitabını diğer kullanıcılarla nasıl paylaşabilirim?

C: Paylaşılan çalışma kitabını oluşturduktan sonra, onu diğer kullanıcılara Excel dosyasını göndererek paylaşabilirsiniz. Diğer kullanıcılar dosyayı aynı anda açıp üzerinde çalışabilecek.

#### S: Paylaşılan bir çalışma kitabında tüm Excel özellikleri destekleniyor mu?

C: Çoğu Excel özelliği, paylaşılan bir çalışma kitabında desteklenir. Ancak makrolar ve eklentiler gibi bazı gelişmiş özellikler, paylaşılan bir çalışma kitabında kullanıldığında sınırlamalara veya kısıtlamalara sahip olabilir.