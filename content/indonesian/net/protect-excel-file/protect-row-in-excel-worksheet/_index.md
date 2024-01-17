---
title: Lindungi Baris Di Lembar Kerja Excel
linktitle: Lindungi Baris Di Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Temukan dalam tutorial ini cara melindungi baris spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Tutorial langkah demi langkah di C#.
type: docs
weight: 60
url: /id/net/protect-excel-file/protect-row-in-excel-worksheet/
---
Dalam tutorial ini, kita akan melihat beberapa kode sumber C# yang menggunakan perpustakaan Aspose.Cells untuk melindungi baris dalam spreadsheet Excel. Kami akan memandu setiap langkah kode dan menjelaskan cara kerjanya. Ikuti instruksi dengan seksama untuk mendapatkan hasil yang diinginkan.

## Langkah 1: Prasyarat

Sebelum memulai, pastikan Anda telah menginstal perpustakaan Aspose.Cells untuk .NET. Anda bisa mendapatkannya dari situs resmi Aspose. Pastikan juga Anda memiliki versi terbaru Visual Studio atau lingkungan pengembangan C# lainnya.

## Langkah 2: Impor namespace yang diperlukan

Untuk menggunakan perpustakaan Aspose.Cells, kita perlu mengimpor namespace yang diperlukan ke dalam kode kita. Tambahkan baris berikut ke bagian atas file sumber C# Anda:

```csharp
using Aspose.Cells;
```

## Langkah 3: Membuat buku kerja Excel

Pada langkah ini, kita akan membuat buku kerja Excel baru. Gunakan kode berikut untuk membuat buku kerja Excel:

```csharp
// Jalur ke direktori dokumen.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Buat buku kerja baru.
Workbook wb = new Workbook();
```

 Pastikan untuk mengganti`"YOUR_DOCUMENTS_DIR"` dengan jalur yang sesuai ke direktori dokumen Anda.

## Langkah 4: Membuat spreadsheet

Sekarang kita telah membuat buku kerja Excel, mari buat lembar kerja dan dapatkan lembar pertama. Gunakan kode berikut:

```csharp
// Buat objek spreadsheet dan dapatkan lembar pertama.
Worksheet sheet = wb.Worksheets[0];
```

## Langkah 5: Mendefinisikan Gaya

Pada langkah ini, kita akan menentukan gaya yang akan diterapkan pada baris spreadsheet. Gunakan kode berikut:

```csharp
// Definisi objek gaya.
Styling styling;
```

## Langkah 6: Ulangi untuk membuka kunci semua kolom

Sekarang kita akan menelusuri semua kolom di lembar kerja dan membuka kuncinya. Gunakan kode berikut:

```csharp
// Ulangi semua kolom di lembar kerja dan buka kuncinya.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Langkah 7: Mengunci baris pertama

Pada langkah ini, kita akan mengunci baris pertama lembar kerja. Gunakan kode berikut:

```csharp
// Dapatkan gaya baris pertama.
style = sheet.Cells.Rows[0].Style;
// Kunci gayanya.
style. IsLocked = true;
// Terapkan gaya ke baris pertama.
sheet.Cells.ApplyRowStyle(0, style);
```

## Langkah 8: Melindungi lembar kerja

Sekarang kita telah mengatur gaya dan mengunci baris, mari lindungi spreadsheet. Gunakan kode berikut:

```csharp
// Lindungi lembar kerja.
sheet.Protect(ProtectionType.All);
```

## Langkah 9: Menyimpan file Excel

Terakhir, kami akan menyimpan file Excel yang dimodifikasi. Gunakan kode berikut:

```csharp
// Simpan file Excelnya.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Pastikan untuk menentukan jalur yang benar untuk menyimpan file Excel yang dimodifikasi.

### Contoh kode sumber untuk Melindungi Baris Di Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
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

Selamat! Anda sekarang memiliki kode sumber C# yang memungkinkan Anda melindungi baris dalam spreadsheet Excel menggunakan pustaka Aspose.Cells untuk .NET. Pastikan untuk mengikuti langkah-langkahnya dengan cermat dan sesuaikan kode dengan kebutuhan spesifik Anda.

### FAQ (Pertanyaan yang Sering Diajukan)

#### Apakah kode ini berfungsi dengan versi terbaru Excel?

Ya, kode ini berfungsi dengan versi terbaru Excel, termasuk file dalam format Excel 2010 dan yang lebih baru.

#### Bisakah saya memproteksi hanya baris tertentu dan bukan semua baris di lembar kerja?

Ya, Anda dapat mengubah kode untuk menentukan baris tertentu yang ingin Anda lindungi. Anda perlu menyesuaikan loop dan indeksnya.

#### Bagaimana cara membuka kembali saluran yang terkunci?

 Anda dapat menggunakan`IsLocked` metode`Style` objek untuk menetapkan nilainya`false` dan membuka kunci baris.

#### Apakah mungkin untuk memproteksi beberapa lembar kerja dalam buku kerja Excel yang sama?

Ya, Anda bisa mengulangi langkah-langkah membuat lembar kerja, mengatur gaya dan memproteksi setiap lembar kerja di buku kerja.

#### Bagaimana cara mengubah kata sandi perlindungan spreadsheet?

 Anda dapat mengubah kata sandi menggunakan`Protect` metode dan menentukan kata sandi baru sebagai argumen.