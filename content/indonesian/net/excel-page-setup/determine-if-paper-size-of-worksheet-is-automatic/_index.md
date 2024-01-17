---
title: Tentukan Apakah Ukuran Kertas Lembar Kerja Otomatis
linktitle: Tentukan Apakah Ukuran Kertas Lembar Kerja Otomatis
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara menentukan apakah ukuran kertas spreadsheet otomatis dengan Aspose.Cells untuk .NET.
type: docs
weight: 20
url: /id/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
Pada artikel ini, kami akan membawa Anda langkah demi langkah untuk menjelaskan kode sumber C# berikut: Tentukan apakah ukuran kertas lembar kerja otomatis menggunakan Aspose.Cells untuk .NET. Kami akan menggunakan perpustakaan Aspose.Cells untuk .NET untuk melakukan operasi ini. Ikuti langkah-langkah di bawah ini untuk menentukan apakah ukuran kertas lembar kerja otomatis.

## Langkah 1: Memuat buku kerja
Langkah pertama adalah memuat buku kerja. Kita akan memiliki dua buku kerja: satu dengan ukuran kertas otomatis dinonaktifkan dan yang lainnya dengan ukuran kertas otomatis diaktifkan. Berikut ini kode untuk memuat buku kerja:

```csharp
// direktori sumber
string sourceDir = "YOUR_SOURCE_DIR";
// Direktori keluaran
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Muat buku kerja pertama dengan ukuran kertas otomatis dinonaktifkan
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Muat buku kerja kedua dengan ukuran kertas otomatis diaktifkan
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Langkah 2: Mengakses Spreadsheet
Sekarang kita telah memuat buku kerja, kita perlu mengakses lembar kerja sehingga kita dapat memeriksa ukuran kertas otomatis. Kita akan masuk ke lembar kerja pertama dari dua buku kerja. Berikut kode untuk mengaksesnya:

```csharp
//Masuk ke lembar kerja pertama dari buku kerja pertama
Worksheet ws11 = wb1.Worksheets[0];

// Masuk ke lembar kerja pertama dari buku kerja kedua
Worksheet ws12 = wb2.Worksheets[0];
```

## Langkah 3: Periksa ukuran kertas otomatis
 Pada langkah ini, kita akan memeriksa apakah ukuran kertas lembar kerja sudah otomatis. Kami akan menggunakan`PageSetup.IsAutomaticPaperSize` properti untuk mendapatkan informasi ini. Kami kemudian akan menampilkan hasilnya. Ini kode untuk itu:

```csharp
// Tampilkan properti IsAutomaticPaperSize dari lembar kerja pertama di buku kerja pertama
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Tampilkan properti IsAutomaticPaperSize dari lembar kerja pertama di buku kerja kedua
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Contoh kode sumber untuk Menentukan Apakah Ukuran Kertas Lembar Kerja Otomatis menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Direktori keluaran
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Muat buku kerja pertama yang memiliki ukuran kertas otomatis salah
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Muat buku kerja kedua yang memiliki ukuran kertas otomatis yang benar
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Akses lembar kerja pertama dari kedua buku kerja
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Cetak properti PageSetup.IsAutomaticPaperSize dari kedua lembar kerja
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Kesimpulan
Dalam artikel ini, kita mempelajari cara menentukan apakah ukuran kertas lembar kerja otomatis menggunakan Aspose.Cells untuk .NET. Kami mengikuti langkah-langkah berikut: memuat buku kerja,

akses ke spreadsheet dan pemeriksaan ukuran kertas otomatis. Sekarang Anda dapat menggunakan pengetahuan ini untuk menentukan apakah ukuran kertas spreadsheet Anda otomatis.

### FAQ

#### T: Bagaimana cara memuat buku kerja dengan Aspose.Cells untuk .NET?

J: Anda bisa memuat buku kerja menggunakan kelas Buku Kerja dari perpustakaan Aspose.Cells. Gunakan metode Workbook.Load untuk memuat buku kerja dari file.

#### T: Dapatkah saya memeriksa ukuran kertas otomatis untuk spreadsheet lain?

J: Ya, Anda dapat memeriksa ukuran kertas otomatis untuk lembar kerja mana pun dengan mengakses properti PageSetup.IsAutomaticPaperSize dari objek Lembar Kerja terkait.

#### T: Bagaimana cara mengubah ukuran kertas otomatis pada spreadsheet?

J: Untuk mengubah ukuran kertas otomatis pada lembar kerja, Anda dapat menggunakan properti PageSetup.IsAutomaticPaperSize dan mengaturnya ke nilai yang diinginkan (benar atau salah).

#### T: Fitur lain apa yang ditawarkan Aspose.Cells untuk .NET?

J: Aspose.Cells untuk .NET menawarkan banyak fitur untuk bekerja dengan spreadsheet, seperti membuat, memodifikasi, dan mengonversi buku kerja, serta memanipulasi data, rumus, dan pemformatan.