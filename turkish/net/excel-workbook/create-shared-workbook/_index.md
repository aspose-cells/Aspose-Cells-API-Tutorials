---
title: Paylaşılan Çalışma Kitabı Oluştur
linktitle: Paylaşılan Çalışma Kitabı Oluştur
second_title: Aspose.Cells for .NET API Referansı
description: Eşzamanlı veri işbirliğini etkinleştirmek için Aspose.Cells for .NET ile bir Excel paylaşımlı çalışma kitabı oluşturun.
type: docs
weight: 70
url: /tr/net/excel-workbook/create-shared-workbook/
---
Bu öğreticide, Aspose.Cells for .NET kullanarak paylaşılan bir çalışma kitabı oluşturmanıza olanak sağlayacak olan sağlanan C# kaynak kodunda size yol göstereceğiz. Bu işlemi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Çıkış dizinini ayarlayın

```csharp
// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda, paylaşılan çalışma kitabının kaydedileceği çıktı dizinini tanımlıyoruz.

## 2. Adım: Bir Çalışma Kitabı Nesnesi Oluşturun

```csharp
// Çalışma Kitabı nesnesi oluşturma
Workbook wb = new Workbook();
```

Excel çalışma kitabımızı temsil edecek yeni bir Workbook nesnesi yaratıyoruz.

## 3. Adım: Çalışma Kitabı Paylaşımını Etkinleştirin

```csharp
// Çalışma kitabını paylaşın
wb.Settings.Shared = true;
```

 ayarlayarak çalışma kitabının paylaşım özelliğini etkinleştiriyoruz.`Shared` Workbook nesnesinin özelliği`true`.

## 4. Adım: Paylaşılan çalışma kitabını kaydedin

```csharp
// Paylaşılan çalışma kitabını kaydet
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Çıktı dosyasının yolunu ve adını belirterek paylaşılan çalışma kitabını kaydediyoruz.

### Aspose.Cells for .NET kullanarak Create Shared Workbook için örnek kaynak kodu 
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

Tebrikler! Aspose.Cells for .NET kullanarak paylaşılan bir çalışma kitabı oluşturmayı öğrendiniz. Paylaşılan çalışma kitabı, veriler üzerinde işbirliği yapmak için aynı anda birden çok kullanıcı tarafından kullanılabilir. Güçlü ve kişiselleştirilmiş Excel çalışma kitapları oluşturmak için kendi verilerinizle deneyler yapın ve Aspose.Cells'in özelliklerini keşfedin.

### SSS

#### S: Paylaşılan çalışma kitabı nedir?

Y: Paylaşılan çalışma kitabı, veriler üzerinde işbirliği yapmak için birden çok kullanıcı tarafından aynı anda kullanılabilen bir Excel çalışma kitabıdır. Her kullanıcı çalışma kitabında değişiklik yapabilir ve diğer kullanıcılar güncellemeleri gerçek zamanlı olarak görür.

#### S: Aspose.Cells for .NET'te bir çalışma kitabının paylaşılması nasıl etkinleştirilir?

 Y: Aspose.Cells for .NET'te bir çalışma kitabının paylaşımını etkinleştirmek için`Shared` Workbook nesnesinin özelliği`true`. Bu, kullanıcıların çalışma kitabı üzerinde aynı anda çalışmasına olanak tanır.

#### S: Paylaşılan bir çalışma kitabında kullanıcı izinlerini kısıtlayabilir miyim?

Y: Evet, Excel'in güvenlik özelliklerini kullanarak paylaşılan bir çalışma kitabında kullanıcı izinlerini kısıtlayabilirsiniz. Her kullanıcı için düzenleme, salt okunur gibi belirli izinler ayarlayabilirsiniz.

#### S: Çalışma kitabını diğer kullanıcılarla nasıl paylaşabilirim?

Y: Paylaşılan çalışma kitabını oluşturduktan sonra, Excel dosyasını göndererek diğer kullanıcılarla paylaşabilirsiniz. Diğer kullanıcılar dosyayı açabilecek ve aynı anda üzerinde çalışabilecektir.

#### S: Paylaşılan bir çalışma kitabında tüm Excel özellikleri destekleniyor mu?

C: Çoğu Excel özelliği, paylaşılan bir çalışma kitabında desteklenir. Ancak, makrolar ve eklentiler gibi bazı gelişmiş özelliklerin, paylaşılan bir çalışma kitabında kullanıldığında sınırlamaları veya kısıtlamaları olabilir.