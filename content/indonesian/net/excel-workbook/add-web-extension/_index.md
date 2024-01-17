---
title: Tambahkan Ekstensi Web
linktitle: Tambahkan Ekstensi Web
second_title: Aspose.Cells untuk Referensi .NET API
description: Tambahkan ekstensi web dengan mudah ke buku kerja Excel Anda dengan Aspose.Cells untuk .NET.
type: docs
weight: 40
url: /id/net/excel-workbook/add-web-extension/
---
Dalam tutorial langkah demi langkah ini, kami akan menjelaskan kode sumber C# yang disediakan yang memungkinkan Anda menambahkan ekstensi web menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk menambahkan ekstensi web ke buku kerja Excel Anda.

## Langkah 1: Tetapkan direktori keluaran

```csharp
// Direktori keluaran
string outDir = RunExamples.Get_OutputDirectory();
```

Pada langkah pertama ini, kita menentukan direktori keluaran tempat buku kerja Excel yang dimodifikasi akan disimpan.

## Langkah 2: Buat buku kerja baru

```csharp
// Buat buku kerja baru
Workbook workbook = new Workbook();
```

Di sini kita membuat buku kerja Excel baru menggunakan`Workbook` kelas dari Aspose.Cells.

## Langkah 3: Akses Koleksi Ekstensi Web

```csharp
// Akses koleksi ekstensi web
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Kami mengakses koleksi ekstensi web buku kerja Excel menggunakan`WebExtensions` properti dari`Worksheets` obyek.

## Langkah 4: Tambahkan ekstensi web baru

```csharp
// Tambahkan ekstensi web baru
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Kami menambahkan ekstensi web baru ke koleksi ekstensi. Kami menentukan ID referensi, nama toko, dan jenis toko ekstensi.

## Langkah 5: Akses Koleksi Panel Tugas Ekstensi Web

```csharp
// Akses kumpulan panel tugas ekstensi web
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Kami mengakses koleksi panel tugas Ekstensi Web Buku Kerja Excel menggunakan`WebExtensionTaskPanes` properti dari`Worksheets` obyek.

## Langkah 6: Tambahkan panel tugas baru

```csharp
// Tambahkan panel tugas baru
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Kami menambahkan panel tugas baru ke koleksi panel tugas. Kami mengatur visibilitas panel, status dockingnya, dan ekstensi web terkait.

## Langkah 7: Simpan dan tutup buku kerja

```csharp
// Simpan dan tutup buku kerja
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Kami menyimpan buku kerja yang dimodifikasi ke direktori keluaran yang ditentukan dan kemudian menutupnya.

### Contoh kode sumber untuk Menambahkan Ekstensi Web menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
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

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara menambahkan ekstensi web menggunakan Aspose.Cells untuk .NET. Bereksperimenlah dengan kode dan jelajahi fitur tambahan Aspose.Cells untuk memaksimalkan manipulasi ekstensi web di buku kerja Excel Anda.

## FAQ

#### T: Apa yang dimaksud dengan ekstensi web di buku kerja Excel?

J: Ekstensi web di buku kerja Excel adalah komponen yang memungkinkan Anda menambahkan fungsionalitas tambahan ke Excel dengan mengintegrasikan aplikasi web. Itu dapat menawarkan fitur interaktif, dasbor khusus, integrasi eksternal, dan banyak lagi.

#### T: Bagaimana cara menambahkan ekstensi web ke buku kerja Excel dengan Aspose.Cells?

 J: Untuk menambahkan ekstensi web ke buku kerja Excel dengan Aspose.Cells, Anda dapat mengikuti langkah-langkah yang disediakan dalam panduan langkah demi langkah kami. Menggunakan`WebExtensionCollection` Dan`WebExtensionTaskPaneCollection` kelas untuk menambah dan mengonfigurasi ekstensi web dan panel tugas terkait.

#### T: Informasi apa yang diperlukan untuk menambahkan ekstensi web?

J: Saat menambahkan ekstensi web, Anda harus memberikan ID SKU ekstensi, nama toko, dan jenis toko. Informasi ini membantu mengidentifikasi dan memuat ekstensi dengan benar.

#### T: Dapatkah saya menambahkan beberapa ekstensi web ke satu buku kerja Excel?

 J: Ya, Anda bisa menambahkan beberapa Ekstensi Web ke satu buku kerja Excel. Menggunakan`Add` metode kumpulan ekstensi web untuk menambahkan setiap ekstensi, lalu mengaitkannya dengan panel tugas yang sesuai.