---
title: Kontrol Faktor Zoom Lembar Kerja
linktitle: Kontrol Faktor Zoom Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Kontrol faktor zoom lembar kerja Excel dengan Aspose.Cells untuk .NET.
type: docs
weight: 20
url: /id/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
Mengontrol faktor zoom lembar kerja merupakan fitur penting saat bekerja dengan file Excel menggunakan perpustakaan Aspose.Cells untuk .NET. Dalam panduan ini, kami akan menunjukkan cara menggunakan Aspose.Cells untuk mengontrol faktor zoom lembar kerja menggunakan kode sumber C# langkah demi langkah.

## Langkah 1: Impor perpustakaan yang diperlukan

Sebelum memulai, pastikan Anda telah menginstal pustaka Aspose.Cells untuk .NET dan mengimpor pustaka yang diperlukan ke proyek C# Anda.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## Langkah 2: Tetapkan Jalur Direktori dan Buka File Excel

 Untuk memulai, atur jalur ke direktori yang berisi file Excel Anda, lalu buka menggunakan a`FileStream` objek dan membuat instance a`Workbook` objek untuk mewakili buku kerja Excel.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Langkah 3: Akses spreadsheet dan ubah faktor zoom

Pada langkah ini, kita mengakses lembar kerja pertama dari buku kerja Excel menggunakan indeks`0` dan atur faktor zoom lembar kerja ke`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## Langkah 4: Simpan perubahan dan tutup file

 Setelah kami mengubah faktor zoom lembar kerja, kami menyimpan perubahan tersebut ke file Excel menggunakan`Save` metode`Workbook` obyek. Kemudian kami menutup aliran file untuk melepaskan semua sumber daya yang digunakan.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### Contoh kode sumber untuk Mengontrol Faktor Zoom Lembar Kerja menggunakan Aspose.Cells untuk .NET 

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
// Mengatur faktor zoom lembar kerja menjadi 75
worksheet.Zoom = 75;
// Menyimpan file Excel yang dimodifikasi
workbook.Save(dataDir + "output.xls");
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Panduan langkah demi langkah ini menunjukkan kepada Anda cara mengontrol faktor zoom lembar kerja menggunakan Aspose.Cells untuk .NET. Dengan menggunakan kode sumber C# yang disediakan, Anda dapat dengan mudah menyesuaikan faktor zoom lembar kerja di aplikasi .NET Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan pengarsipan yang kaya fitur untuk memanipulasi file Excel dalam aplikasi .NET.

#### Bagaimana cara menginstal Aspose.Cells untuk .NET?

 Untuk menginstal Aspose.Cells untuk .NET, Anda perlu mengunduh paket NuGet yang sesuai dari[Asumsikan Rilis](https://releases/aspose.com/cells/net/) dan menambahkannya ke proyek .NET Anda.

#### Fitur apa yang ditawarkan Aspose.Cells untuk .NET?

Aspose.Cells untuk .NET menawarkan fitur seperti membuat, mengedit, mengonversi, dan manipulasi lanjutan file Excel.

#### Format file apa yang didukung oleh Aspose.Cells untuk .NET?

Aspose.Cells untuk .NET mendukung berbagai format file termasuk XLSX, XLSM, CSV, HTML, PDF, dan banyak lagi.
