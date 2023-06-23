---
title: Paylaşılan Çalışma Kitabını Parolayla Koruma veya Korumayı Kaldırma
linktitle: Paylaşılan Çalışma Kitabını Parolayla Koruma veya Korumayı Kaldırma
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak paylaşılan bir çalışma kitabını nasıl parola ile koruyacağınızı veya korumasını kaldıracağınızı öğrenin.
type: docs
weight: 120
url: /tr/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Paylaşılan bir çalışma kitabını parolayla korumak, veri gizliliğini sağlamak için önemlidir. Aspose.Cells for .NET ile paylaşılan bir çalışma kitabını parola kullanarak kolayca koruyabilir veya korumasını kaldırabilirsiniz. İstenen sonuçları elde etmek için aşağıdaki adımları izleyin:

## 1. Adım: Çıkış dizinini belirtin

Öncelikle, korumalı Excel dosyasının kaydedileceği çıktı dizinini belirtmeniz gerekir. Aspose.Cells kullanarak bunu şu şekilde yapabilirsiniz:

```csharp
// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. Adım: Boş bir Excel dosyası oluşturun

Ardından, koruma veya koruma kaldırma uygulamak istediğiniz boş bir Excel dosyası oluşturabilirsiniz. İşte örnek bir kod:

```csharp
// Boş bir Excel çalışma kitabı oluşturun
Workbook wb = new Workbook();
```

## 3. Adım: Paylaşılan çalışma kitabını koruyun veya korumasını kaldırın

Çalışma kitabını oluşturduktan sonra, uygun parolayı belirterek paylaşılan çalışma kitabını koruyabilir veya korumasını kaldırabilirsiniz. İşte nasıl:

```csharp
// Paylaşılan çalışma kitabını bir parolayla koruyun
wb.ProtectSharedWorkbook("1234");

// Paylaşılan çalışma kitabının korumasını kaldırmak için bu satırın açıklamasını kaldırın
// wb.UnprotectSharedWorkbook("1234");
```

## 4. Adım: Çıktı Excel dosyasını kaydedin

Korumayı veya korumayı kaldırmayı uyguladığınızda, korumalı Excel dosyasını belirtilen çıkış dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel dosyasını kaydedin
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak Parola Koruma veya Korumayı Kaldırma Paylaşımlı Çalışma Kitabı için örnek kaynak kodu 
```csharp
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Boş Excel dosyası oluştur
Workbook wb = new Workbook();
//Paylaşılan Çalışma Kitabını Parola ile Koruyun
wb.ProtectSharedWorkbook("1234");
//Paylaşılan Çalışma Kitabının Korumasını Kaldırmak için bu satırın açıklamasını kaldırın
//wb.UnprotectSharedWorkbook("1234");
//Çıktı Excel dosyasını kaydedin
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Çözüm

Veri güvenliğini sağlamak için paylaşılan bir çalışma kitabını bir parolayla korumak veya korumasını kaldırmak çok önemlidir. Aspose.Cells for .NET ile bu işlevselliği Excel dosyalarınıza kolayca ekleyebilirsiniz. Bu kılavuzdaki adımları izleyerek, paylaşılan çalışma kitaplarınızı parola kullanarak etkili bir şekilde koruyabilir veya korumasını kaldırabilirsiniz. Kendi Excel dosyalarınızla denemeler yapın ve hassas verilerinizin güvenliğini sağladığınızdan emin olun.

### SSS

#### S: Aspose.Cells ile paylaşılan bir çalışma kitabına ne tür koruma uygulayabilirim?
    
Y: Aspose.Cells ile paylaşılan bir çalışma kitabını, verilere yetkisiz erişimi, verilerin değiştirilmesini veya silinmesini önlemek için bir parola belirleyerek koruyabilirsiniz.

#### S: Paylaşılan bir çalışma kitabını parola belirtmeden koruyabilir miyim?
    
Y: Evet, paylaşılan bir çalışma kitabını parola belirlemeden koruyabilirsiniz. Ancak, daha iyi güvenlik için güçlü bir parola kullanılması önerilir.

#### S: Aspose.Cells ile paylaşılan bir çalışma kitabının korumasını nasıl kaldırabilirim?
    
Y: Paylaşılan bir çalışma kitabının korumasını kaldırmak için, çalışma kitabını korurken kullanılan parolanın aynısını belirtmeniz gerekir. Bu, korumanın kaldırılmasına ve verilere serbestçe erişilmesine izin verir.

#### S: Paylaşılan bir çalışma kitabını korumak, çalışma kitabındaki özellikleri ve formülleri etkiler mi?
    
C: Paylaşılan bir çalışma kitabını koruduğunuzda, kullanıcılar çalışma kitabında bulunan özelliklere ve formüllere erişmeye devam edebilir. Koruma yalnızca çalışma kitabındaki yapısal değişiklikleri etkiler.