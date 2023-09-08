---
title: Web Uzantısı Ekle
linktitle: Web Uzantısı Ekle
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel çalışma kitaplarınıza kolayca web uzantısı ekleyin.
type: docs
weight: 40
url: /tr/net/excel-workbook/add-web-extension/
---
Bu adım adım eğitimde, Aspose.Cells for .NET kullanarak bir web uzantısı eklemenizi sağlayacak C# kaynak kodunu açıklayacağız. Excel çalışma kitabınıza web uzantısı eklemek için aşağıdaki adımları izleyin.

## 1. Adım: Çıkış dizinini ayarlayın

```csharp
// Çıkış dizini
string outDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda değiştirilen Excel çalışma kitabının kaydedileceği çıktı dizinini tanımlıyoruz.

## Adım 2: Yeni bir çalışma kitabı oluşturun

```csharp
// Yeni bir çalışma kitabı oluştur
Workbook workbook = new Workbook();
```

Burada aşağıdakileri kullanarak yeni bir Excel çalışma kitabı oluşturuyoruz:`Workbook` Aspose.Cells'ten sınıf.

## 3. Adım: Web Uzantıları Koleksiyonuna Erişin

```csharp
// Web uzantıları koleksiyonuna erişin
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Excel çalışma kitabının web uzantıları koleksiyonuna şunu kullanarak erişiyoruz:`WebExtensions` mülkiyeti`Worksheets` nesne.

## 4. Adım: Yeni bir web uzantısı ekleyin

```csharp
// Yeni bir web uzantısı ekleyin
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Uzantı koleksiyonuna yeni bir web uzantısı ekliyoruz. Uzantının referans kimliğini, mağaza adını ve mağaza tipini tanımlıyoruz.

## Adım 5: Web Uzantısı Görev Bölmesi Koleksiyonuna Erişin

```csharp
// Web uzantısının görev bölmesi koleksiyonuna erişin
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Excel Çalışma Kitabı Web Uzantısı görev bölmeleri koleksiyonuna şunu kullanarak erişiyoruz:`WebExtensionTaskPanes` mülkiyeti`Worksheets` nesne.

## 6. Adım: Yeni bir görev bölmesi ekleyin

```csharp
// Yeni bir görev bölmesi ekleme
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Görev bölmesi koleksiyonuna yeni bir görev bölmesi ekliyoruz. Bölmenin görünürlüğünü, kenetlenme durumunu ve ilgili web uzantısını ayarlıyoruz.

## Adım 7: Çalışma kitabını kaydedin ve kapatın

```csharp
// Çalışma kitabını kaydedin ve kapatın
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Değiştirilen çalışma kitabını belirtilen çıktı dizinine kaydedip sonra kapatıyoruz.

### Aspose.Cells for .NET kullanarak Web Uzantısı Ekleme için örnek kaynak kodu 
```csharp
//Kaynak dizini
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Çözüm

Tebrikler! Artık Aspose.Cells for .NET kullanarak bir web uzantısının nasıl ekleneceğini öğrendiniz. Kodlarla denemeler yapın ve Aspose.Cells'in ek özelliklerini keşfederek Excel çalışma kitaplarınızda web uzantılarını düzenlemeden en iyi şekilde yararlanın.

## SSS

#### S: Excel çalışma kitabındaki web uzantısı nedir?

C: Excel çalışma kitabındaki web uzantısı, web uygulamalarını entegre ederek Excel'e ek işlevler eklemenizi sağlayan bir bileşendir. Etkileşimli özellikler, özel kontrol panelleri, harici entegrasyonlar ve daha fazlasını sunabilir.

#### S: Aspose.Cells ile Excel çalışma kitabına web uzantısı nasıl eklenir?

 C: Aspose.Cells ile bir Excel çalışma kitabına web uzantısı eklemek için adım adım kılavuzumuzda verilen adımları takip edebilirsiniz. Kullan`WebExtensionCollection` Ve`WebExtensionTaskPaneCollection` web uzantısını ve ilgili görev bölmesini eklemek ve yapılandırmak için sınıflar.

#### S: Bir web uzantısı eklemek için hangi bilgiler gereklidir?

C: Bir web uzantısı eklerken uzantı SKU kimliğini, mağaza adını ve mağaza türünü sağlamanız gerekir. Bu bilgi, uzantının doğru şekilde tanımlanmasına ve yüklenmesine yardımcı olur.

#### S: Tek bir Excel çalışma kitabına birden fazla web uzantısı ekleyebilir miyim?

 C: Evet, tek bir Excel çalışma kitabına birden çok Web Uzantısı ekleyebilirsiniz. Kullan`Add` Her bir uzantıyı eklemek ve ardından bunları ilgili görev bölmeleriyle ilişkilendirmek için web uzantıları koleksiyonunun yöntemini kullanın.