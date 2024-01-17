---
title: Tetapkan Judul Cetak Excel
linktitle: Tetapkan Judul Cetak Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara memanipulasi file Excel dengan mudah dan menyesuaikan opsi pencetakan menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 170
url: /id/net/excel-page-setup/set-excel-print-title/
---
Dalam panduan ini, kami akan memandu Anda tentang cara mengatur judul cetak di spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk menyelesaikan tugas ini.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menyiapkan lingkungan pengembangan dan menginstal Aspose.Cells untuk .NET. Anda dapat mengunduh perpustakaan versi terbaru dari situs resmi Aspose.

## Langkah 2: Impor namespace yang diperlukan

Dalam proyek C# Anda, impor namespace yang diperlukan untuk bekerja dengan Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Langkah 3: Mengatur jalur ke direktori dokumen

 Nyatakan a`dataDir` variabel untuk menentukan jalur ke direktori tempat Anda ingin menyimpan file Excel yang dihasilkan:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pastikan untuk mengganti`"YOUR_DOCUMENT_DIRECTORY"` dengan jalur yang benar di sistem Anda.

## Langkah 4: Membuat Objek Buku Kerja

Buat instance objek Buku Kerja yang mewakili buku kerja Excel yang ingin Anda buat:

```csharp
Workbook workbook = new Workbook();
```

## Langkah 5: Akses ke lembar kerja pertama

Navigasikan ke lembar kerja pertama di buku kerja Excel menggunakan kode berikut:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Langkah 6: Mendefinisikan Kolom Judul

Tentukan kolom judul menggunakan kode berikut:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Di sini kita telah mendefinisikan kolom A dan B sebagai kolom judul. Anda dapat menyesuaikan nilai ini sesuai dengan kebutuhan Anda.

## Langkah 7: Mendefinisikan Baris Judul

Tentukan baris judul menggunakan kode berikut:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Kami telah mendefinisikan baris 1 dan 2 sebagai baris judul. Anda dapat menyesuaikan nilai-nilai ini sesuai dengan kebutuhan Anda.

## Langkah 8: Menyimpan buku kerja Excel

 Untuk menyimpan buku kerja Excel dengan judul cetak yang ditentukan, gunakan`Save` metode objek Buku Kerja:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Ini akan menyimpan buku kerja Excel dengan nama file "SetPrintTitle_out.xls" di direktori yang ditentukan.

### Contoh kode sumber untuk Menetapkan Judul Cetak Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mendapatkan referensi PageSetup lembar kerja
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Mendefinisikan nomor kolom A & B sebagai kolom judul
pageSetup.PrintTitleColumns = "$A:$B";
// Mendefinisikan baris nomor 1 & 2 sebagai baris judul
pageSetup.PrintTitleRows = "$1:$2";
// Simpan buku kerja.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Kesimpulan

Selamat! Anda telah mempelajari cara mengatur judul cetak di spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Judul cetak memungkinkan Anda menampilkan baris dan kolom tertentu pada setiap halaman yang dicetak, membuat data lebih mudah dibaca dan dijadikan referensi.

### FAQ

#### 1. Bisakah saya mengatur judul cetak untuk kolom tertentu di Excel?

 Ya, dengan Aspose.Cells untuk .NET Anda dapat mengatur kolom tertentu sebagai judul cetak menggunakan`PrintTitleColumns` properti dari`PageSetup` obyek.

#### 2. Apakah mungkin untuk menentukan judul kolom dan baris cetak?

 Ya, Anda dapat mengatur judul kolom dan baris cetak menggunakan`PrintTitleColumns` Dan`PrintTitleRows` properti dari`PageSetup` obyek.

#### 3. Pengaturan tata letak apa lagi yang dapat saya sesuaikan dengan Aspose.Cells untuk .NET?

Dengan Aspose.Cells untuk .NET, Anda dapat menyesuaikan berbagai pengaturan tata letak halaman, seperti margin, orientasi halaman, skala cetak, dan banyak lagi.