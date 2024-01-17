---
title: Dapatkan Dimensi Halaman
linktitle: Dapatkan Dimensi Halaman
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mengambil dimensi halaman di Excel menggunakan Aspose.Cells untuk .NET. Panduan langkah demi langkah dengan kode sumber dalam C#.
type: docs
weight: 40
url: /id/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan file Microsoft Excel secara terprogram. Ia menawarkan berbagai fitur untuk memanipulasi dokumen Excel, termasuk kemampuan untuk mendapatkan dimensi halaman. Dalam tutorial ini, kami akan memandu Anda melalui langkah-langkah untuk mengambil dimensi halaman menggunakan Aspose.Cells untuk .NET.

## Langkah 1: Buat instance kelas Buku Kerja

Untuk memulai, kita perlu membuat sebuah instance dari kelas Workbook, yang mewakili buku kerja Excel. Hal ini dapat dicapai dengan menggunakan kode berikut:

```csharp
Workbook book = new Workbook();
```

## Langkah 2: Mengakses spreadsheet

Selanjutnya, kita perlu menavigasi ke lembar kerja di buku kerja tempat kita ingin mengatur dimensi halaman. Dalam contoh ini, misalkan kita ingin mengerjakan lembar kerja pertama. Kita dapat mengaksesnya menggunakan kode berikut:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Langkah 3: Atur ukuran kertas ke A2 dan lebar dan tinggi cetak dalam inci

Sekarang kita akan mengatur ukuran kertas menjadi A2 dan mencetak lebar dan tinggi halaman dalam inci. Hal ini dapat dicapai dengan menggunakan kode berikut:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Langkah 4: Atur ukuran kertas ke A3 dan lebar dan tinggi cetak dalam inci

Selanjutnya, kita akan mengatur ukuran kertas menjadi A3 dan mencetak lebar dan tinggi halaman dalam inci. Ini kode yang sesuai:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Langkah 5: Atur ukuran kertas ke A4 dan lebar dan tinggi cetak dalam inci

Kami sekarang akan mengatur ukuran kertas menjadi A4 dan mencetak lebar dan tinggi halaman dalam inci. Ini kodenya:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Langkah 6: Atur ukuran kertas menjadi Letter dan cetak lebar dan tinggi dalam inci

Terakhir, kita akan mengatur ukuran kertas menjadi Letter dan mencetak lebar dan tinggi halaman dalam inci. Ini kodenya:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Contoh kode sumber untuk Mendapatkan Dimensi Halaman menggunakan Aspose.Cells untuk .NET 
```csharp
// Buat instance kelas Buku Kerja
Workbook book = new Workbook();
// Akses lembar kerja pertama
Worksheet sheet = book.Worksheets[0];
// Atur ukuran kertas ke A2 dan cetak lebar dan tinggi kertas dalam inci
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Atur ukuran kertas ke A3 dan cetak lebar dan tinggi kertas dalam inci
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Atur ukuran kertas ke A4 dan cetak lebar dan tinggi kertas dalam inci
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Atur ukuran kertas ke Letter dan cetak lebar dan tinggi kertas dalam inci
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Kesimpulan

Selamat! Anda mempelajari cara mengambil dimensi halaman menggunakan Aspose.Cells untuk .NET. Fitur ini dapat berguna ketika Anda perlu melakukan operasi tertentu berdasarkan dimensi halaman di file Excel Anda.

Jangan lupa untuk menjelajahi lebih jauh dokumentasi Aspose.Cells untuk menemukan semua fitur canggih yang ditawarkannya.

### FAQ

#### 1. Berapa ukuran kertas lain yang didukung Aspose.Cells untuk .NET?

Aspose.Cells for .NET mendukung berbagai ukuran kertas termasuk A1, A5, B4, B5, Executive, Legal, Letter dan masih banyak lagi. Anda dapat memeriksa dokumentasi untuk mengetahui daftar lengkap ukuran kertas yang didukung.

#### 2. Bisakah saya mengatur dimensi halaman khusus dengan Aspose.Cells untuk .NET?

Ya, Anda dapat mengatur dimensi halaman khusus dengan menentukan lebar dan tinggi yang diinginkan. Aspose.Cells menawarkan fleksibilitas penuh untuk menyesuaikan dimensi halaman dengan kebutuhan Anda.

#### 3. Bisakah saya mendapatkan dimensi halaman dalam satuan selain inci?

Ya, Aspose.Cells untuk .NET memungkinkan Anda mendapatkan dimensi halaman dalam satuan berbeda, termasuk inci, sentimeter, milimeter, dan titik.

#### 4. Apakah Aspose.Cells untuk .NET mendukung fitur pengeditan pengaturan halaman lainnya?

Ya, Aspose.Cells menawarkan berbagai fitur untuk mengedit pengaturan halaman, termasuk mengatur margin, orientasi, header dan footer, dll.