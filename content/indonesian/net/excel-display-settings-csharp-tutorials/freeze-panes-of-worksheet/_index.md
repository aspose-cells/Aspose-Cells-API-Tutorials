---
title: Bekukan Panel Lembar Kerja
linktitle: Bekukan Panel Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Memanipulasi panel beku lembar kerja Excel dengan mudah menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 70
url: /id/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
Dalam tutorial ini, kami akan menunjukkan cara mengunci panel di lembar kerja Excel menggunakan kode sumber C# dengan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk mendapatkan hasil yang diinginkan.

## Langkah 1: Impor perpustakaan yang diperlukan

Pastikan Anda telah menginstal perpustakaan Aspose.Cells untuk .NET dan mengimpor perpustakaan yang diperlukan ke proyek C# Anda.

```csharp
using Aspose.Cells;
```

## Langkah 2: Tetapkan jalur direktori dan buka file Excel

 Tetapkan jalur ke direktori yang berisi file Excel Anda, lalu buka file tersebut dengan membuat instance a`Workbook` obyek.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Langkah 3: Buka spreadsheet dan terapkan pengaturan kunci panel

 Navigasikan ke lembar kerja pertama di file Excel menggunakan`Worksheet` obyek. Kemudian gunakan`FreezePanes` metode untuk menerapkan pengaturan kunci panel.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Pada contoh di atas, panel dikunci pada sel di baris 3 dan kolom 2.

## Langkah 4: Simpan Perubahan

 Setelah Anda membuat perubahan yang diperlukan, simpan file Excel yang dimodifikasi menggunakan`Save` metode`Workbook` obyek.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Contoh kode sumber untuk Freeze Panes Of Worksheet menggunakan Aspose.Cells untuk .NET 

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
// Menerapkan pengaturan panel beku
worksheet.FreezePanes(3, 2, 3, 2);
// Menyimpan file Excel yang dimodifikasi
workbook.Save(dataDir + "output.xls");
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Panduan langkah demi langkah ini menunjukkan kepada Anda cara mengunci panel di spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Dengan menggunakan kode sumber C# yang disediakan, Anda dapat dengan mudah mengkustomisasi pengaturan kunci panel untuk mengatur dan memvisualisasikan data Anda dalam file Excel dengan lebih baik.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan yang kuat untuk memanipulasi file Excel dalam aplikasi .NET.

#### Bagaimana cara menginstal Aspose.Cells untuk .NET?

 Untuk menginstal Aspose.Cells untuk .NET, Anda perlu mengunduh paket yang relevan dari[Asumsikan Rilis](https://releases/aspose.com/cells/net/) dan menambahkannya ke proyek .NET Anda.

#### Bagaimana cara mengunci panel di lembar kerja Excel menggunakan Aspose.Cells untuk .NET?

 Anda dapat menggunakan`FreezePanes` metode`Worksheet` objek untuk mengunci panel lembar kerja. Tentukan sel yang akan dikunci dengan memberikan indeks baris dan kolom.

#### Bisakah saya menyesuaikan pengaturan kunci panel dengan Aspose.Cells untuk .NET?

 Ya, menggunakan`FreezePanes` metode ini, Anda dapat menentukan sel mana yang akan dikunci sesuai kebutuhan, dengan menyediakan indeks baris dan kolom yang sesuai.
