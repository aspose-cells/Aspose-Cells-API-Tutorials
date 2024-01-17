---
title: Lindungi Baris Tertentu Di Lembar Kerja Excel
linktitle: Lindungi Baris Tertentu Di Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Lindungi baris tertentu di Excel dengan Aspose.Cells untuk .NET. Panduan langkah demi langkah untuk mengamankan data rahasia Anda.
type: docs
weight: 90
url: /id/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Melindungi data rahasia dalam spreadsheet Excel sangat penting untuk memastikan keamanan informasi. Aspose.Cells untuk .NET menawarkan solusi ampuh untuk melindungi baris tertentu dalam spreadsheet Excel. Panduan ini akan memandu Anda tentang cara memproteksi baris tertentu di lembar kerja Excel menggunakan kode sumber C# yang disediakan. Ikuti langkah-langkah sederhana ini untuk mengatur perlindungan baris di file Excel Anda.

## Langkah 1: Impor perpustakaan yang diperlukan

Untuk memulai, pastikan Anda telah menginstal Aspose.Cells for .NET di sistem Anda. Anda juga perlu menambahkan referensi yang sesuai dalam proyek C# Anda untuk dapat menggunakan fungsionalitas Aspose.Cells. Berikut adalah kode untuk mengimpor perpustakaan yang diperlukan:

```csharp
// Tambahkan referensi yang diperlukan
using Aspose.Cells;
```

## Langkah 2: Membuat buku kerja dan spreadsheet Excel

Setelah mengimpor perpustakaan yang diperlukan, Anda bisa membuat buku kerja Excel baru dan lembar kerja baru. Berikut cara melakukannya:

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Buat direktori jika belum ada.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Buat buku kerja baru.
Workbook wb = new Workbook();

// Buat objek spreadsheet dan dapatkan lembar pertama.
Worksheet sheet = wb.Worksheets[0];
```

## Langkah 3: Mengatur Gaya dan Bendera Gaya

Sekarang kita akan mengatur gaya sel dan bendera gaya untuk membuka kunci semua kolom di lembar kerja. Ini kode yang diperlukan:

```csharp
// Atur objek gaya.
Styling styling;

// Atur objek styleflag.
StyleFlag flag;

// Ulangi semua kolom di lembar kerja dan buka kuncinya.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Langkah 4: Lindungi jalur tertentu

Sekarang kita akan memproteksi baris tertentu di lembar kerja. Kami akan mengunci baris pertama untuk mencegah modifikasi apa pun. Begini caranya:

```csharp
// Dapatkan gaya baris pertama.
style = sheet.Cells.Rows[0].Style;

// Kunci itu.
style. IsLocked = true;

//Buat contoh benderanya.
flag = new StyleFlag();

// Atur parameter kunci.
flag. Locked = true;

// Terapkan gaya ke baris pertama.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Langkah 5: Melindungi lembar kerja

Terakhir, kami akan melindungi seluruh lembar kerja Excel untuk mencegah modifikasi yang tidak sah. Begini caranya:

```csharp
// Lindungi lembar kerja.
sheet.Protect(ProtectionType.All);
```

## Langkah 6: Simpan file Excel yang dilindungi

Setelah Anda selesai memproteksi baris tertentu di lembar kerja Excel, Anda dapat menyimpan file Excel yang diproteksi ke sistem Anda. Begini caranya:

```csharp
// Simpan file Excelnya.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Setelah mengikuti langkah-langkah ini, Anda akan berhasil memproteksi baris tertentu di spreadsheet Excel Anda menggunakan Aspose.Cells untuk .NET.

### Contoh kode sumber untuk Melindungi Baris Tertentu di Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Buat direktori jika belum ada.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Buat buku kerja baru.
Workbook wb = new Workbook();
// Buat objek lembar kerja dan dapatkan lembar pertama.
Worksheet sheet = wb.Worksheets[0];
// Tentukan objek gaya.
Style style;
// Tentukan objek styleflag.
StyleFlag flag;
// Ulangi semua kolom di lembar kerja dan buka kuncinya.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Dapatkan gaya baris pertama.
style = sheet.Cells.Rows[0].Style;
// Kunci itu.
style.IsLocked = true;
//Buat contoh benderanya.
flag = new StyleFlag();
// Atur pengaturan kunci.
flag.Locked = true;
// Terapkan gaya ke baris pertama.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Lindungi lembaran itu.
sheet.Protect(ProtectionType.All);
// Simpan file excelnya.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Kesimpulan

Melindungi data dalam file Excel sangat penting untuk mencegah akses tidak sah atau modifikasi yang tidak diinginkan. Dengan menggunakan pustaka Aspose.Cells untuk .NET, Anda dapat dengan mudah memproteksi baris tertentu dalam spreadsheet Excel menggunakan kode sumber C# yang disediakan. Ikuti panduan langkah demi langkah ini untuk menambahkan lapisan keamanan ekstra ke file Excel Anda.

### FAQ

#### Apakah perlindungan baris tertentu berfungsi di semua versi Excel?

Ya, perlindungan baris tertentu menggunakan Aspose.Cells untuk .NET berfungsi di semua versi Excel yang didukung.

#### Bisakah saya memproteksi beberapa baris tertentu dalam spreadsheet Excel?

Ya, Anda dapat melindungi beberapa baris tertentu menggunakan metode serupa yang dijelaskan dalam panduan ini.

#### Bagaimana cara membuka kunci baris tertentu di spreadsheet Excel?

 Untuk membuka kunci baris tertentu, Anda harus memodifikasi kode sumber menggunakan`IsLocked` metode`Style` obyek.