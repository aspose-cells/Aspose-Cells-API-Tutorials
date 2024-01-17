---
title: Sesuaikan Tingkat Kompresi
linktitle: Sesuaikan Tingkat Kompresi
second_title: Aspose.Cells untuk Referensi .NET API
description: Kurangi ukuran buku kerja Excel Anda dengan menyesuaikan tingkat kompresi dengan Aspose.Cells untuk .NET.
type: docs
weight: 50
url: /id/net/excel-workbook/adjust-compression-level/
---
Dalam tutorial langkah demi langkah ini, kami akan menjelaskan kode sumber C# yang disediakan yang memungkinkan Anda menyesuaikan tingkat kompresi menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk menyesuaikan tingkat kompresi di buku kerja Excel Anda.

## Langkah 1: Tetapkan direktori sumber dan keluaran

```csharp
// direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
// Direktori keluaran
string outDir = RunExamples.Get_OutputDirectory();
```

Pada langkah pertama ini, kami menentukan direktori sumber dan keluaran untuk file Excel.

## Langkah 2: Muat Buku Kerja Excel

```csharp
// Muat buku kerja Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Kami memuat buku kerja Excel dari file yang ditentukan menggunakan`Workbook` kelas dari Aspose.Cells.

## Langkah 3: Tetapkan opsi cadangan

```csharp
// Tentukan opsi cadangan
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Kami membuat sebuah instance dari`XlsbSaveOptions` kelas untuk mengatur opsi penyimpanan.

## Langkah 4: Sesuaikan tingkat kompresi (Level 1)

```csharp
// Sesuaikan tingkat kompresi (Level 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Kami menyesuaikan tingkat kompresi dengan mengatur`CompressionType` ke`Level1`. Kemudian kami menyimpan buku kerja Excel dengan opsi kompresi yang ditentukan.

## Langkah 5: Sesuaikan tingkat kompresi (Level 6)

```csharp
// Sesuaikan tingkat kompresi (Level 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Kami ulangi proses untuk menyesuaikan tingkat kompresi`Level6` dan simpan buku kerja Excel dengan opsi ini.

## Langkah 6: Sesuaikan tingkat kompresi (Level 9)

```csharp
// Sesuaikan tingkat kompresi (Level 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Kami mengulangi proses ini untuk terakhir kalinya untuk menyesuaikan tingkat kompresi`Level9` dan simpan buku kerja Excel dengan opsi ini.

### Contoh kode sumber untuk Menyesuaikan Tingkat Kompresi menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Kesimpulan

Selamat! Anda mempelajari cara menyesuaikan tingkat kompresi di buku kerja Excel menggunakan Aspose.Cells untuk .NET. Bereksperimenlah dengan berbagai tingkat kompresi untuk menemukan yang paling sesuai dengan kebutuhan Anda.

### FAQ

#### T: Apa yang dimaksud dengan kompresi dalam buku kerja Excel?

A: Kompresi dalam buku kerja Excel adalah proses pengurangan ukuran file dengan menggunakan algoritma kompresi. Hal ini mengurangi ruang penyimpanan yang diperlukan dan meningkatkan kinerja saat memuat dan memanipulasi file.

#### T: Tingkat kompresi apa yang tersedia dengan Aspose.Cells?

A: Dengan Aspose.Cells, Anda dapat mengatur tingkat kompresi dari 1 hingga 9. Semakin tinggi tingkat kompresi, ukuran file akan semakin kecil, namun juga dapat menambah waktu pemrosesan.

#### T: Bagaimana cara memilih tingkat kompresi yang tepat untuk buku kerja Excel saya?

J: Pilihan tingkat kompresi bergantung pada kebutuhan spesifik Anda. Jika Anda ingin kompresi maksimum dan waktu pemrosesan tidak menjadi masalah, Anda dapat menggunakan level 9. Jika Anda lebih suka kompromi antara ukuran file dan waktu pemrosesan, Anda dapat memilih level perantara.

#### T: Apakah kompresi mempengaruhi kualitas data di buku kerja Excel?

J: Tidak, kompresi tidak mempengaruhi kualitas data di buku kerja Excel. Ini hanya mengurangi ukuran file menggunakan teknik kompresi tanpa mengubah data itu sendiri.

#### T: Dapatkah saya menyesuaikan tingkat kompresi setelah menyimpan file Excel?

A: Tidak, setelah Anda menyimpan file Excel dengan tingkat kompresi tertentu, Anda tidak dapat menyesuaikan tingkat kompresinya nanti. Anda perlu menyimpan file lagi dengan tingkat kompresi baru jika Anda ingin memodifikasinya.