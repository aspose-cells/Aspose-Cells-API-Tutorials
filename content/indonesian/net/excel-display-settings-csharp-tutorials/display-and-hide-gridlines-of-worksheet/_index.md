---
title: Tampilkan Dan Sembunyikan Garis Kisi Lembar Kerja
linktitle: Tampilkan Dan Sembunyikan Garis Kisi Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Kontrol tampilan garis kisi di lembar kerja Excel dengan Aspose.Cells untuk .NET.
type: docs
weight: 30
url: /id/net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
Dalam tutorial ini, kami akan menunjukkan cara menampilkan dan menyembunyikan garis kisi di lembar kerja Excel menggunakan kode sumber C# dengan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk mendapatkan hasil yang diinginkan.

## Langkah 1: Impor perpustakaan yang diperlukan

Pastikan Anda telah menginstal perpustakaan Aspose.Cells untuk .NET dan mengimpor perpustakaan yang diperlukan ke proyek C# Anda.

```csharp
using Aspose.Cells;
using System.IO;
```

## Langkah 2: Tetapkan jalur direktori dan buka file Excel

 Tetapkan jalur ke direktori yang berisi file Excel Anda, lalu buka file tersebut dengan membuat aliran file dan membuat instance a`Workbook` obyek.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Langkah 3: Buka lembar kerja pertama dan sembunyikan garis kisi

 Akses lembar kerja pertama di file Excel menggunakan`Worksheets` properti dari`Workbook` obyek. Kemudian gunakan`IsGridlinesVisible` properti dari`Worksheet` objek untuk menyembunyikan garis kisi.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## Langkah 4: Simpan Perubahan

 Setelah Anda membuat perubahan yang diperlukan, simpan file Excel yang dimodifikasi menggunakan`Save` metode`Workbook` obyek.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Contoh kode sumber untuk Menampilkan dan Menyembunyikan Garis Kisi Lembar Kerja menggunakan Aspose.Cells untuk .NET 

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat aliran file yang berisi file Excel yang akan dibuka
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Membuat instance objek Buku Kerja
// Membuka file Excel melalui aliran file
Workbook workbook = new Workbook(fstream);
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Menyembunyikan garis grid pada lembar kerja pertama file Excel
worksheet.IsGridlinesVisible = false;
// Menyimpan file Excel yang dimodifikasi
workbook.Save(dataDir + "output.xls");
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Panduan langkah demi langkah ini menunjukkan kepada Anda cara menampilkan dan menyembunyikan garis kisi di spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Dengan menggunakan kode sumber C# yang disediakan, Anda dapat dengan mudah menyesuaikan tampilan garis kisi di file Excel Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan yang kuat untuk memanipulasi file Excel dalam aplikasi .NET.

#### Bagaimana cara menginstal Aspose.Cells untuk .NET?

 Untuk menginstal Aspose.Cells untuk .NET, Anda perlu mengunduh paket yang relevan dari[Asumsikan Rilis](https://releases/aspose.com/cells/net/) dan menambahkannya ke proyek .NET Anda.

#### Bagaimana cara menampilkan atau menyembunyikan garis kisi di lembar bentang Excel dengan Aspose.Cells untuk .NET?

 Anda dapat menggunakan`IsGridlinesVisible` properti dari`Worksheet` objek untuk menampilkan atau menyembunyikan garis kisi. Setel ke`true` untuk menunjukkan kepada mereka dan untuk`false` untuk menyembunyikannya.

#### Format file Excel apa lagi yang didukung oleh Aspose.Cells untuk .NET?

Aspose.Cells for .NET mendukung berbagai format file Excel, seperti XLS, XLSX, CSV, HTML, PDF, dan masih banyak lagi.

