---
title: Lindungi Sel Tertentu di Lembar Kerja Excel
linktitle: Lindungi Sel Tertentu di Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara melindungi sel tertentu di Excel dengan Aspose.Cells untuk .NET. Tutorial langkah demi langkah di C#.
type: docs
weight: 70
url: /id/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
Dalam tutorial ini, kita akan melihat kode sumber C# yang menggunakan perpustakaan Aspose.Cells untuk melindungi sel tertentu dalam spreadsheet Excel. Kami akan memandu setiap langkah kode dan menjelaskan cara kerjanya. Ikuti instruksi dengan seksama untuk mendapatkan hasil yang diinginkan.

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

Pada langkah ini, kita akan menentukan gaya yang akan diterapkan ke sel tertentu. Gunakan kode berikut:

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

## Langkah 7: Mengunci Sel Tertentu

Pada langkah ini, kita akan mengunci sel tertentu. Gunakan kode berikut:

```csharp
//Mengunci ketiga sel... yaitu A1, B1, C1.
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

## Langkah 8: Melindungi lembar kerja

Terakhir, kami akan melindungi lembar kerja untuk mencegah sel tertentu diubah. Gunakan kode berikut:

```csharp
// Lindungi lembar kerja.
sheet.Protect(ProtectionType.All);
```

## Langkah 9: Menyimpan file Excel

Kami sekarang akan menyimpan file Excel yang dimodifikasi. Gunakan kode berikut:

```csharp
// Simpan file Excelnya.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Pastikan untuk menentukan jalur yang benar untuk menyimpan file Excel yang dimodifikasi.

### Contoh kode sumber untuk Melindungi Sel Tertentu di Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
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
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Kesimpulan

Selamat! Anda sekarang memiliki kode sumber C# yang memungkinkan Anda melindungi sel tertentu di lembar kerja Excel menggunakan pustaka Aspose.Cells untuk .NET. Jangan ragu untuk menyesuaikan kode agar sesuai dengan kebutuhan spesifik Anda.

### FAQ (Pertanyaan yang Sering Diajukan)

#### Apakah kode ini berfungsi dengan versi terbaru Excel?

Ya, kode ini berfungsi dengan versi terbaru Excel, termasuk file dalam format Excel 2010 dan yang lebih baru.

#### Bisakah saya melindungi sel lain selain A1, B1 dan C1?

Ya, Anda dapat mengubah kode untuk mengunci sel spesifik lainnya dengan menyesuaikan referensi sel di baris kode yang sesuai.

#### Bagaimana cara membuka kembali sel yang terkunci?

 Anda dapat gunakan`SetStyle` metode dengan`IsLocked` mulai`false` untuk membuka kunci sel.

#### Bisakah saya menambahkan lebih banyak lembar kerja ke buku kerja?

 Ya, Anda bisa menambahkan lembar kerja lain ke buku kerja menggunakan`Worksheets.Add()`metode dan ulangi langkah-langkah perlindungan sel untuk setiap lembar kerja.

#### Bagaimana cara mengubah format penyimpanan file Excel?

 Anda dapat mengubah format penyimpanan menggunakan`SaveFormat` metode dengan format yang diinginkan, misalnya`SaveFormat.Xlsx` untuk Excel 2007 dan yang lebih baru.