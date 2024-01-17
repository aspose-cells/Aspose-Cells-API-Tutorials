---
title: Akses Informasi Ekstensi Web
linktitle: Akses Informasi Ekstensi Web
second_title: Aspose.Cells untuk Referensi .NET API
description: Akses informasi ekstensi web dengan Aspose.Cells untuk .NET.
type: docs
weight: 10
url: /id/net/excel-workbook/access-web-extension-information/
---
Akses ke informasi ekstensi web merupakan fitur penting ketika mengembangkan aplikasi menggunakan Aspose.Cells untuk .NET. Dalam panduan langkah demi langkah ini, kami akan menjelaskan kode sumber C# yang disediakan yang memungkinkan Anda mengakses informasi ekstensi web menggunakan Aspose.Cells untuk .NET. Kami juga akan memberikan kesimpulan dan jawaban dalam format Markdown agar lebih mudah dipahami. Ikuti langkah-langkah di bawah ini untuk mendapatkan informasi berharga tentang ekstensi web.

## Langkah 1: Tetapkan direktori sumber

```csharp
// direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
```

Pada langkah pertama ini, kita menentukan direktori sumber yang akan digunakan untuk memuat file Excel yang berisi informasi ekstensi web.

## Langkah 2: Muat file Excel

```csharp
// Muat contoh file Excel
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

Di sini kita memuat contoh file Excel yang berisi informasi ekstensi web yang ingin kita ambil.

## Langkah 3: Akses informasi dari jendela tugas ekstensi web

```csharp
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach(WebExtensionTaskPane taskPane in taskPanes)
{
Console.WriteLine("Width: " + taskPane.Width);
Console.WriteLine("Is visible: " + taskPane.IsVisible);
Console.WriteLine("Is locked: " + taskPane.IsLocked);
Console.WriteLine("Docking State: " + taskPane.DockState);
Console.WriteLine("Store Name: " + taskPane.WebExtension.Reference.StoreName);
Console.WriteLine("Store type: " + taskPane.WebExtension.Reference.StoreType);
Console.WriteLine("Web Extension ID: " + taskPane.WebExtension.Id);
}
```

Pada langkah ini, kita mengakses informasi dari setiap jendela tugas ekstensi web yang ada di file Excel. Kami menampilkan properti yang berbeda seperti lebar, visibilitas, status kunci, status asal, nama toko, jenis toko, dan ID ekstensi web.

## Langkah 4: Tampilkan pesan sukses

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

Terakhir, kami menampilkan pesan yang menunjukkan bahwa informasi ekstensi web berhasil diakses.

### Contoh kode sumber untuk Mengakses Informasi Ekstensi Web menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
//Muat contoh file Excel
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach (WebExtensionTaskPane taskPane in taskPanes)
{
	Console.WriteLine("Width: " + taskPane.Width);
	Console.WriteLine("IsVisible: " + taskPane.IsVisible);
	Console.WriteLine("IsLocked: " + taskPane.IsLocked);
	Console.WriteLine("DockState: " + taskPane.DockState);
	Console.WriteLine("StoreName: " + taskPane.WebExtension.Reference.StoreName);
	Console.WriteLine("StoreType: " + taskPane.WebExtension.Reference.StoreType);
	Console.WriteLine("WebExtension.Id: " + taskPane.WebExtension.Id);
}
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara mengakses informasi ekstensi web menggunakan Aspose.Cells untuk .NET. Dengan mengikuti langkah-langkah yang disediakan, Anda akan dapat dengan mudah mengekstrak informasi jendela tugas dari ekstensi web ke dalam file Excel.


### FAQ

#### T: Apa itu Aspose.Cells untuk .NET?

J: Aspose.Cells for .NET adalah perpustakaan kelas canggih yang memungkinkan pengembang .NET membuat, memodifikasi, mengonversi, dan memanipulasi file Excel dengan mudah.

#### T: Apakah Aspose.Cells mendukung bahasa pemrograman lain?

A: Ya, Aspose.Cells mendukung berbagai bahasa pemrograman seperti C#, VB.NET, Java, PHP, Python, dll.

#### T: Dapatkah saya menggunakan Aspose.Cells dalam proyek komersial?

A: Ya, Aspose.Cells adalah perpustakaan komersial dan dapat digunakan dalam proyek komersial sesuai dengan perjanjian lisensi.

#### T: Apakah ada dokumentasi tambahan tentang Aspose.Cells?

J: Ya, Anda dapat melihat dokumentasi lengkap Aspose.Cells di situs web resmi Aspose untuk informasi dan sumber daya lebih lanjut.