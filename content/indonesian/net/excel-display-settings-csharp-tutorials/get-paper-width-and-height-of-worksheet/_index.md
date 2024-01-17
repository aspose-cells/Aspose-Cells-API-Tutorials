---
title: Dapatkan Lebar Kertas Dan Tinggi Lembar Kerja
linktitle: Dapatkan Lebar Kertas Dan Tinggi Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Buat panduan langkah demi langkah untuk menjelaskan kode sumber C# berikut untuk mendapatkan lebar dan tinggi kertas spreadsheet menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 80
url: /id/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
Dalam tutorial ini, kami akan membawa Anda langkah demi langkah menjelaskan kode sumber C# berikut untuk mendapatkan lebar dan tinggi kertas lembar kerja menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini:

## Langkah 1: Buat buku kerja
 Mulailah dengan membuat buku kerja baru menggunakan`Workbook` kelas:

```csharp
Workbook wb = new Workbook();
```

## Langkah 2: Akses lembar kerja pertama
 Selanjutnya, navigasikan ke lembar kerja pertama di buku kerja menggunakan`Worksheet` kelas:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Langkah 3: Atur ukuran kertas menjadi A2 dan tunjukkan lebar dan tinggi kertas dalam inci
 Menggunakan`PaperSize` properti dari`PageSetup` objek untuk mengatur ukuran kertas menjadi A2, lalu gunakan`PaperWidth` Dan`PaperHeight` properti untuk mendapatkan lebar dan tinggi kertas masing-masing. Tampilkan nilai-nilai ini menggunakan`Console.WriteLine` metode:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Langkah 4: Ulangi langkah untuk ukuran kertas lainnya
Ulangi langkah sebelumnya, ubah ukuran kertas menjadi A3, A4, dan Letter, lalu tampilkan nilai lebar dan tinggi kertas untuk setiap ukuran:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Contoh kode sumber untuk Mendapatkan Lebar dan Tinggi Kertas Lembar Kerja menggunakan Aspose.Cells untuk .NET 

```csharp
//Buat buku kerja
Workbook wb = new Workbook();
//Akses lembar kerja pertama
Worksheet ws = wb.Worksheets[0];
//Atur ukuran kertas ke A2 dan cetak lebar dan tinggi kertas dalam inci
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Atur ukuran kertas ke A3 dan cetak lebar dan tinggi kertas dalam inci
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Atur ukuran kertas ke A4 dan cetak lebar dan tinggi kertas dalam inci
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Atur ukuran kertas ke Letter dan cetak lebar dan tinggi kertas dalam inci
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Kesimpulan

Anda mempelajari cara menggunakan Aspose.Cells untuk .NET untuk mendapatkan lebar dan tinggi kertas spreadsheet. Fitur ini dapat berguna untuk konfigurasi dan tata letak dokumen Excel Anda secara presisi.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan yang kuat untuk memanipulasi dan memproses file Excel dalam aplikasi .NET. Ia menawarkan banyak fitur untuk membuat, memodifikasi, mengkonversi dan menganalisis file Excel.

#### Bagaimana saya bisa mendapatkan ukuran kertas spreadsheet dengan Aspose.Cells untuk .NET?

 Anda dapat menggunakan`PageSetup` kelas tersebut`Worksheet` objek untuk mengakses ukuran kertas. Menggunakan`PaperSize` properti untuk mengatur ukuran kertas dan`PaperWidth` Dan`PaperHeight` properti untuk mendapatkan lebar dan tinggi kertas masing-masing.

#### Berapa ukuran kertas yang didukung Aspose.Cells untuk .NET?

Aspose.Cells untuk .NET mendukung berbagai ukuran kertas yang umum digunakan, seperti A2, A3, A4, dan Letter, serta banyak ukuran khusus lainnya.

#### Bisakah saya menyesuaikan ukuran kertas spreadsheet dengan Aspose.Cells untuk .NET?

 Ya, Anda dapat mengatur ukuran kertas khusus dengan menentukan dimensi lebar dan tinggi yang tepat menggunakan`PaperWidth` Dan`PaperHeight` properti dari`PageSetup` kelas.