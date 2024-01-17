---
title: Lindungi Sel Di Lembar Kerja Excel
linktitle: Lindungi Sel Di Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara melindungi sel tertentu di Excel dengan Aspose.Cells untuk .NET. Tutorial langkah demi langkah di C#.
type: docs
weight: 30
url: /id/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel adalah alat yang banyak digunakan untuk membuat dan mengelola spreadsheet. Salah satu fitur inti Excel adalah kemampuan untuk melindungi sel tertentu untuk menjaga integritas data. Dalam tutorial ini, kami akan memandu Anda langkah demi langkah untuk melindungi sel tertentu di spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Aspose.Cells for .NET adalah pustaka pemrograman canggih yang memudahkan manipulasi file Excel dengan fleksibilitas tinggi dan fitur-fitur canggih. Ikuti langkah-langkah yang diberikan untuk mempelajari cara melindungi sel penting Anda dan menjaga keamanan data Anda.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells for .NET di lingkungan pengembangan Anda. Unduh perpustakaan dari situs resmi Aspose dan periksa dokumentasi untuk petunjuk instalasi.

## Langkah 2: Inisialisasi Buku Kerja dan Lembar Kerja

Untuk memulai, kita perlu membuat buku kerja baru dan mendapatkan referensi ke lembar kerja tempat kita ingin melindungi selnya. Gunakan kode berikut:

```csharp
// Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Buat direktori jika belum ada.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Buat buku kerja baru
Workbook workbook = new Workbook();

// Dapatkan lembar kerja pertama
Worksheet sheet = workbook.Worksheets[0];
```

 Pada cuplikan kode ini, pertama-tama kita tentukan path ke direktori tempat file Excel akan disimpan. Selanjutnya, kita membuat instance baru dari`Workbook` kelas dan dapatkan referensi ke lembar kerja pertama menggunakan`Worksheets` Properti.

## Langkah 3: Tentukan Gaya Sel

Sekarang kita perlu menentukan gaya sel yang ingin kita lindungi. Gunakan kode berikut:

```csharp
// Tentukan objek gaya
Styling styling;

// Ulangi semua kolom di lembar kerja dan buka kuncinya
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 Dalam kode ini, kita menggunakan loop untuk mengulang semua kolom di lembar kerja dan membuka kunci selnya dengan mengatur gayanya.`IsLocked` properti ke`false` . Kami kemudian menggunakan`ApplyStyle` metode untuk menerapkan gaya ke kolom dengan`StyleFlag` bendera untuk mengunci sel.

## Langkah 4: Lindungi Sel Tertentu

Sekarang kita akan melindungi sel tertentu yang ingin kita kunci. Gunakan kode berikut:

```csharp
// Kunci tiga sel: A1, B1, C1
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

 Dalam kode ini, kita mendapatkan gaya setiap sel tertentu menggunakan`GetStyle` metode, dan kemudian kami mengatur`IsLocked` properti gaya ke`true`untuk mengunci sel. Terakhir, kami menerapkan gaya yang diperbarui ke setiap sel menggunakan`SetStyle` metode.

## Langkah 5: Melindungi lembar kerja

Sekarang kita telah mendefinisikan sel yang akan dilindungi, kita dapat memproteksi lembar kerja itu sendiri. Gunakan kode berikut:

```csharp
// Lindungi lembar kerja
leaf.Protect(ProtectionType.All);
```

 Kode ini menggunakan`Protect` metode untuk melindungi lembar kerja dengan jenis perlindungan yang ditentukan, dalam hal ini`ProtectionType.All` yang melindungi semua item di lembar kerja.

## Langkah 6: Simpan file Excel

Terakhir, kami menyimpan file Excel dengan perubahan yang dilakukan. Gunakan kode berikut:

```csharp
// Simpan file Excelnya
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 Dalam kode ini, kami menggunakan`Save` metode untuk menyimpan buku kerja di direktori yang ditentukan dengan`Excel97To2003` format.

### Contoh kode sumber untuk Melindungi Sel di Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
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
// Tentukan objek styleflag
StyleFlag styleflag;
// Ulangi semua kolom di lembar kerja dan buka kuncinya.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Kunci ketiga sel...yaitu A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Terakhir, Lindungi lembar itu sekarang.
sheet.Protect(ProtectionType.All);
// Simpan file excelnya.
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Kesimpulan

Selamat! Anda telah mempelajari cara melindungi sel tertentu dalam spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Anda sekarang dapat menerapkan teknik ini dalam proyek Anda sendiri dan meningkatkan keamanan file Excel Anda.


### FAQ

#### T: Mengapa saya harus menggunakan Aspose.Cells untuk .NET untuk melindungi sel dalam lembar bentang Excel?

J: Aspose.Cells for .NET adalah perpustakaan canggih yang memudahkan bekerja dengan file Excel. Ia menawarkan fitur-fitur canggih untuk melindungi sel, membuka kunci rentang, dll.

#### T: Apakah mungkin untuk melindungi rentang sel, bukan sel individual?

 A: Ya, Anda dapat menentukan rentang sel tertentu yang akan dilindungi menggunakan`ApplyStyle` metode dengan yang sesuai`StyleFlag`.

#### T: Bagaimana cara membuka file Excel yang dilindungi setelah menyimpannya?

J: Saat Anda membuka file Excel yang diproteksi, Anda harus memberikan kata sandi yang ditentukan saat memproteksi lembar kerja.

#### T: Apakah ada jenis perlindungan lain yang bisa saya terapkan pada lembar bentang Excel?

J: Ya, Aspose.Cells untuk .NET mendukung berbagai jenis perlindungan, seperti perlindungan struktur, perlindungan jendela, dll. Anda dapat memilih jenis perlindungan yang sesuai dengan kebutuhan Anda.