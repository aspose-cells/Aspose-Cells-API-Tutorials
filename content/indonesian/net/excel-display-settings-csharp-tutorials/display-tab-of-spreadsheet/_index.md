---
title: Tampilkan Tab Spreadsheet
linktitle: Tampilkan Tab Spreadsheet
second_title: Aspose.Cells untuk Referensi .NET API
description: Tampilkan tab spreadsheet Excel menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 60
url: /id/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
Dalam tutorial ini, kami akan menunjukkan cara menampilkan tab lembar kerja Excel menggunakan kode sumber C# dengan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk mendapatkan hasil yang diinginkan.

## Langkah 1: Impor perpustakaan yang diperlukan

Pastikan Anda telah menginstal perpustakaan Aspose.Cells untuk .NET dan mengimpor perpustakaan yang diperlukan ke proyek C# Anda.

```csharp
using Aspose.Cells;
```

## Langkah 2: Tetapkan jalur direktori dan buka file Excel

 Tetapkan jalur ke direktori yang berisi file Excel Anda, lalu buka file tersebut dengan membuat instance a`Workbook` obyek.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Langkah 3: Tampilkan tab lembar kerja

 Menggunakan`ShowTabs` properti dari`Workbook.Settings` objek untuk memperlihatkan tab lembar kerja Excel.

```csharp
workbook.Settings.ShowTabs = true;
```

## Langkah 4: Simpan Perubahan

 Setelah Anda membuat perubahan yang diperlukan, simpan file Excel yang dimodifikasi menggunakan`Save` metode`Workbook` obyek.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Contoh kode sumber untuk Menampilkan Tab Spreadsheet menggunakan Aspose.Cells untuk .NET 

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
// Membuka file Excelnya
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Menyembunyikan tab file Excel
workbook.Settings.ShowTabs = true;
// Menyimpan file Excel yang dimodifikasi
workbook.Save(dataDir + "output.xls");
```

### Kesimpulan

Panduan langkah demi langkah ini menunjukkan kepada Anda cara memperlihatkan tab spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Dengan menggunakan kode sumber C# yang disediakan, Anda dapat dengan mudah menyesuaikan tampilan tab di file Excel Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan yang kuat untuk memanipulasi file Excel dalam aplikasi .NET.

#### Bagaimana cara menginstal Aspose.Cells untuk .NET?

 Untuk menginstal Aspose.Cells untuk .NET, Anda perlu mengunduh paket yang relevan dari[Asumsikan Rilis](https://releases/aspose.com/cells/net/) dan menambahkannya ke proyek .NET Anda.

#### Bagaimana cara menampilkan tab spreadsheet Excel menggunakan Aspose.Cells untuk .NET?

 Anda dapat menggunakan`ShowTabs` properti dari`Workbook.Settings` objek dan atur ke`true` untuk memperlihatkan tab lembar kerja.

#### Format file Excel apa lagi yang didukung oleh Aspose.Cells untuk .NET?

Aspose.Cells untuk .NET mendukung berbagai format file Excel, seperti XLS, XLSX, CSV, HTML, PDF, dll.
