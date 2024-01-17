---
title: Salin Pengaturan Pengaturan Halaman Dari Lembar Kerja Lain
linktitle: Salin Pengaturan Pengaturan Halaman Dari Lembar Kerja Lain
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara menyalin pengaturan konfigurasi halaman dari satu spreadsheet ke spreadsheet lainnya menggunakan Aspose.Cells untuk .NET. Panduan langkah demi langkah untuk mengoptimalkan penggunaan perpustakaan ini.
type: docs
weight: 10
url: /id/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Pada artikel ini, kami akan membawa Anda langkah demi langkah untuk menjelaskan kode sumber C# berikut: Salin pengaturan konfigurasi halaman dari spreadsheet lain menggunakan Aspose.Cells untuk .NET. Kami akan menggunakan perpustakaan Aspose.Cells untuk .NET untuk melakukan operasi ini. Jika Anda ingin menyalin pengaturan pengaturan halaman dari satu lembar kerja ke lembar kerja lainnya, ikuti langkah-langkah di bawah ini.

## Langkah 1: Membuat Buku Kerja
Langkah pertama adalah membuat buku kerja. Dalam kasus kita, kita akan menggunakan kelas Workbook yang disediakan oleh perpustakaan Aspose.Cells. Berikut ini kode untuk membuat buku kerja:

```csharp
Workbook wb = new Workbook();
```

## Langkah 2: Menambahkan Lembar Kerja Tes
Setelah membuat buku kerja, kita perlu menambahkan lembar kerja pengujian. Dalam contoh ini, kita akan menambahkan dua lembar kerja. Berikut kode untuk menambahkan dua lembar kerja:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Langkah 3: Mengakses Lembar Kerja
Sekarang kita telah menambahkan lembar kerja, kita perlu mengaksesnya agar dapat mengubah pengaturannya. Kami akan mengakses lembar kerja "TestSheet1" dan "TestSheet2" menggunakan namanya. Berikut kode untuk mengaksesnya:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Langkah 4: Mengatur Ukuran Kertas
 Pada langkah ini, kita akan mengatur ukuran kertas lembar kerja "TestSheet1". Kami akan menggunakan`PageSetup.PaperSize` properti untuk mengatur ukuran kertas. Misalnya, kita akan mengatur ukuran kertas menjadi "PaperA3ExtraTransverse". Ini kode untuk itu:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Langkah 5: Menyalin Pengaturan Pengaturan Halaman
Sekarang kita akan menyalin pengaturan konfigurasi halaman dari lembar kerja "TestSheet1" ke "TestSheet2". Kami akan menggunakan`PageSetup.Copy` metode untuk melakukan operasi ini. Ini kode untuk itu:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Langkah 6: Mencetak Ukuran Kertas
 Setelah menyalin pengaturan pengaturan halaman, kami akan mencetak ukuran kertas kedua lembar kerja. Kami akan menggunakan`Console.WriteLine` untuk menampilkan ukuran kertas. Ini kode untuk itu:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Contoh kode sumber untuk Salin Pengaturan Pengaturan Halaman Dari Lembar Kerja Lain menggunakan Aspose.Cells untuk .NET 
```csharp
//Buat buku kerja
Workbook wb = new Workbook();
//Tambahkan dua lembar kerja tes
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Akses kedua lembar kerja sebagai TestSheet1 dan TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Atur Ukuran Kertas TestSheet1 ke PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Cetak Ukuran Kertas kedua lembar kerja
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Salin PageSetup dari TestSheet1 ke TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Cetak Ukuran Kertas kedua lembar kerja
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Kesimpulan
Dalam artikel ini, kita mempelajari cara menyalin pengaturan konfigurasi halaman dari satu lembar kerja ke lembar kerja lainnya menggunakan Aspose.Cells untuk .NET. Kami melalui langkah-langkah berikut: membuat buku kerja, menambahkan lembar kerja pengujian, mengakses lembar kerja, mengatur ukuran kertas, menyalin pengaturan pengaturan halaman, dan mencetak ukuran kertas. Sekarang Anda dapat menggunakan pengetahuan ini untuk menyalin pengaturan konfigurasi halaman ke proyek Anda sendiri.

### FAQ

#### T: Dapatkah saya menyalin pengaturan konfigurasi halaman di antara instans buku kerja yang berbeda?

 J: Ya, Anda bisa menyalin pengaturan pengaturan halaman antara contoh buku kerja yang berbeda menggunakan`PageSetup.Copy` metode perpustakaan Aspose.Cells.

#### T: Dapatkah saya menyalin pengaturan pengaturan halaman lainnya, seperti orientasi atau margin?

 J: Ya, Anda dapat menyalin pengaturan pengaturan halaman lainnya menggunakan`PageSetup.Copy` metode dengan pilihan yang sesuai. Misalnya, Anda dapat menyalin orientasi menggunakan`CopyOptions.Orientation` dan margin menggunakan`CopyOptions.Margins`.

#### T: Bagaimana saya mengetahui opsi apa saja yang tersedia untuk ukuran kertas?

J: Anda dapat memeriksa Referensi API perpustakaan Aspose.Cells untuk opsi ukuran kertas yang tersedia. Ada enum yang disebut`PaperSizeType` yang mencantumkan berbagai ukuran kertas yang didukung.

#### T: Bagaimana cara mengunduh perpustakaan Aspose.Cells untuk .NET?

 A: Anda dapat mengunduh perpustakaan Aspose.Cells untuk .NET dari[Asumsikan Rilis](https://releases.aspose.com/cells/net). Tersedia versi uji coba gratis, serta lisensi berbayar untuk penggunaan komersial.

#### T: Apakah perpustakaan Aspose.Cells mendukung bahasa pemrograman lain?

J: Ya, perpustakaan Aspose.Cells mendukung beberapa bahasa pemrograman termasuk C#, Java, Python, dan banyak lagi.