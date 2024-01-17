---
title: Sembunyikan Dan Perlihatkan Lembar Kerja
linktitle: Sembunyikan Dan Perlihatkan Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Pustaka yang kuat untuk bekerja dengan file Excel, termasuk membuat, memodifikasi, dan memanipulasi data.
type: docs
weight: 90
url: /id/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
Dalam tutorial ini, kami akan membawa Anda langkah demi langkah untuk menjelaskan kode sumber C# berikut yang digunakan untuk menyembunyikan dan menampilkan lembar kerja menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini:

## Langkah 1: Mempersiapkan lingkungan

Sebelum memulai, pastikan Anda telah menginstal Aspose.Cells for .NET di sistem Anda. Jika Anda belum menginstalnya, Anda dapat mendownloadnya dari situs resmi Aspose. Setelah terinstal, Anda dapat membuat proyek baru di lingkungan pengembangan terintegrasi (IDE) pilihan Anda.

## Langkah 2: Impor namespace yang diperlukan

Di file sumber C# Anda, tambahkan namespace yang diperlukan untuk menggunakan fitur Aspose.Cells. Tambahkan baris berikut ke awal file Anda:

```csharp
using Aspose.Cells;
using System.IO;
```

## Langkah 3: Muat file Excel

Sebelum menyembunyikan atau memperlihatkan lembar kerja, Anda harus memuat file Excel ke dalam aplikasi Anda. Pastikan Anda memiliki file Excel yang ingin Anda gunakan di direktori yang sama dengan proyek Anda. Gunakan kode berikut untuk memuat file Excel:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Pastikan untuk mengganti "PATH TO YOUR DOCUMENTS DIRECTORY" dengan jalur sebenarnya ke direktori yang berisi file Excel Anda.

## Langkah 4: Akses spreadsheet

Setelah file Excel dimuat, Anda dapat menavigasi ke lembar kerja yang ingin Anda sembunyikan atau tampilkan. Gunakan kode berikut untuk mengakses lembar kerja pertama dalam file:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Langkah 5: Sembunyikan lembar kerja

 Sekarang Anda telah mengakses lembar kerja, Anda bisa menyembunyikannya menggunakan`IsVisible` Properti. Gunakan kode berikut untuk menyembunyikan lembar kerja pertama dalam file:

```csharp
worksheet. IsVisible = false;
```

## Langkah 6: Tampilkan kembali lembar kerja

Jika Anda ingin menampilkan kembali lembar kerja yang sebelumnya tersembunyi, Anda dapat menggunakan kode yang sama dengan mengubah nilai`IsVisible` Properti. Gunakan kode berikut untuk menampilkan kembali lembar kerja pertama:

```csharp
worksheet. IsVisible = true;
```

## Langkah 7: Simpan Perubahan

Sekali kamu

  telah menyembunyikan atau memperlihatkan lembar kerja sesuai kebutuhan, Anda harus menyimpan perubahannya ke file Excel. Gunakan kode berikut untuk menyimpan perubahan:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Pastikan untuk menentukan jalur keluaran yang benar untuk menyimpan file Excel yang dimodifikasi.

### Contoh kode sumber untuk Sembunyikan dan Perlihatkan Lembar Kerja menggunakan Aspose.Cells untuk .NET 

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat aliran file yang berisi file Excel yang akan dibuka
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Membuat instance objek Buku Kerja dengan membuka file Excel melalui aliran file
Workbook workbook = new Workbook(fstream);
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Menyembunyikan lembar kerja pertama dari file Excel
worksheet.IsVisible = false;
// Menampilkan lembar kerja pertama dari file Excel
//Lembar Kerja.IsVisible = true;
// Menyimpan file Excel yang dimodifikasi dalam format default (yaitu Excel 2003).
workbook.Save(dataDir + "output.out.xls");
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Selamat! Anda telah mempelajari cara menyembunyikan dan menampilkan spreadsheet menggunakan Aspose.Cells untuk .NET. Anda sekarang dapat menggunakan fitur ini untuk mengontrol visibilitas spreadsheet di file Excel Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Bagaimana cara menginstal Aspose.Cells untuk .NET?

 Anda dapat menginstal Aspose.Cells untuk .NET dengan mengunduh paket NuGet yang relevan dari[Asumsikan Rilis](https://releases/aspose.com/cells/net/) dan menambahkannya ke proyek Visual Studio Anda.

#### Berapa versi minimum .NET Framework yang diperlukan untuk menggunakan Aspose.Cells untuk .NET?

Aspose.Cells untuk .NET mendukung .NET Framework 2.0 dan yang lebih baru.

#### Bisakah saya membuka dan mengedit file Excel yang ada dengan Aspose.Cells untuk .NET?

Ya, Anda dapat membuka dan mengedit file Excel yang ada menggunakan Aspose.Cells untuk .NET. Anda dapat mengakses lembar kerja, sel, rumus, dan elemen lain dari file Excel.

#### Apakah Aspose.Cells for .NET mendukung pelaporan dan ekspor ke format file lain?

Ya, Aspose.Cells untuk .NET mendukung pembuatan laporan dan ekspor ke format seperti PDF, HTML, CSV, TXT, dll.

#### Apakah modifikasi file Excel bersifat permanen?

Ya, pengeditan file Excel bersifat permanen setelah Anda menyimpannya. Pastikan untuk menyimpan salinan cadangan sebelum membuat perubahan apa pun pada file asli.