---
title: Atur Header dan Footer Excel
linktitle: Atur Header dan Footer Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mengatur header dan footer di Excel menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 100
url: /id/net/excel-page-setup/set-excel-headers-and-footers/
---

Dalam tutorial ini, kami akan menunjukkan kepada Anda langkah demi langkah cara mengatur header dan footer di Excel menggunakan Aspose.Cells untuk .NET. Kami akan menggunakan kode sumber C# untuk mengilustrasikan prosesnya.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET di mesin Anda. Buat juga proyek baru di lingkungan pengembangan pilihan Anda.

## Langkah 2: Impor perpustakaan yang diperlukan

Dalam file kode Anda, impor pustaka yang diperlukan untuk bekerja dengan Aspose.Cells. Ini kode yang sesuai:

```csharp
using Aspose.Cells;
```

## Langkah 3: Tetapkan Direktori Data

Tetapkan direktori data tempat Anda ingin menyimpan file Excel yang dimodifikasi. Gunakan kode berikut:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Pastikan untuk menentukan jalur direktori lengkap.

## Langkah 4: Membuat buku kerja dan lembar kerja

Buat objek Buku Kerja baru dan navigasikan ke lembar kerja pertama di buku kerja menggunakan kode berikut:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Ini akan membuat buku kerja kosong dengan lembar kerja dan memberikan akses ke objek PageSetup lembar kerja tersebut.

## Langkah 5: Mengatur Header

 Atur header spreadsheet menggunakan`SetHeader` metode objek PageSetup. Berikut ini contoh kodenya:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Ini akan mengatur nama lembar kerja, tanggal dan waktu saat ini, dan nama file di header masing-masing.

## Langkah 6: Mendefinisikan footer

 Atur footer spreadsheet menggunakan`SetFooter` metode objek PageSetup. Berikut ini contoh kodenya:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Ini masing-masing akan menetapkan string teks, nomor halaman saat ini dan jumlah total halaman di footer.

## Langkah 7: Menyimpan Buku Kerja yang Dimodifikasi

Simpan buku kerja yang dimodifikasi menggunakan kode berikut:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Ini akan menyimpan buku kerja yang dimodifikasi ke direktori data yang ditentukan.

### Contoh kode sumber untuk Mengatur Header dan Footer Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook excel = new Workbook();
// Mendapatkan referensi PageSetup lembar kerja
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Mengatur nama lembar kerja di bagian kiri header
pageSetup.SetHeader(0, "&A");
//Menetapkan tanggal saat ini dan waktu saat ini di bagian tengah header
// dan mengubah font header
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Menetapkan nama file saat ini di bagian kanan header dan mengubah
// font tajuk
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Menetapkan string di bagian kiri footer dan mengubah font
// dari bagian string ini ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Menetapkan nomor halaman saat ini di bagian tengah footer
pageSetup.SetFooter(1, "&P");
// Mengatur jumlah halaman di bagian kanan footer
pageSetup.SetFooter(2, "&N");
// Simpan Buku Kerja.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Kesimpulan

Anda sekarang telah mempelajari cara mengatur header dan footer di Excel menggunakan Aspose.Cells untuk .NET. Tutorial ini memandu Anda melalui setiap langkah proses, mulai dari menyiapkan lingkungan hingga menyimpan buku kerja yang dimodifikasi. Jangan ragu untuk menjelajahi lebih jauh fitur Aspose.Cells untuk melakukan manipulasi lebih lanjut pada file Excel Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### 1. Bagaimana cara menginstal Aspose.Cells untuk .NET di sistem saya?
Untuk menginstal Aspose.Cells untuk .NET, Anda perlu mengunduh paket instalasi dari situs resmi Aspose dan ikuti instruksi yang diberikan dalam dokumentasi.

#### 2. Apakah metode ini berfungsi pada semua versi Excel?
Ya, metode pengaturan header dan footer dengan Aspose.Cells untuk .NET berfungsi dengan semua versi Excel yang didukung.

#### 3. Bisakah saya menyesuaikan header dan footer lebih lanjut?
Ya, Aspose.Cells menawarkan beragam fitur untuk menyesuaikan header dan footer, termasuk penempatan teks, warna, font, nomor halaman, dan banyak lagi.

#### 4. Bagaimana cara menambahkan informasi dinamis ke header dan footer?
Anda dapat menggunakan variabel khusus dan kode pemformatan untuk menambahkan informasi dinamis seperti tanggal sekarang, waktu, nama file, nomor halaman, dll., ke header dan footer.

#### 5. Bisakah saya menghapus header dan footer setelah mengaturnya?
 Ya, Anda dapat menghapus header dan footer menggunakan`ClearHeaderFooter` metode`PageSetup` obyek. Ini akan mengembalikan header dan footer default.