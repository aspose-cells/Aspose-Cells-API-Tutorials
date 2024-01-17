---
title: Pengaturan Perlindungan Tingkat Lanjut Untuk Lembar Kerja Excel
linktitle: Pengaturan Perlindungan Tingkat Lanjut Untuk Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Lindungi file Excel Anda dengan mengatur pengaturan perlindungan tingkat lanjut dengan Aspose.Cells untuk .NET.
type: docs
weight: 10
url: /id/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
Dalam tutorial ini, kami akan memandu Anda melalui langkah-langkah untuk mengatur pengaturan perlindungan tingkat lanjut untuk spreadsheet Excel menggunakan perpustakaan Aspose.Cells untuk .NET. Ikuti petunjuk di bawah ini untuk menyelesaikan tugas ini.

## Langkah 1: Persiapan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET dan membuat proyek C# di lingkungan pengembangan terintegrasi (IDE) pilihan Anda.

## Langkah 2: Tetapkan jalur direktori dokumen

 Nyatakan a`dataDir` variabel dan inisialisasi dengan jalur ke direktori dokumen Anda. Misalnya :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pastikan untuk mengganti`"YOUR_DOCUMENTS_DIRECTORY"` dengan jalur sebenarnya ke direktori Anda.

## Langkah 3: Buat aliran file untuk membuka file Excel

 Membuat`FileStream` objek yang berisi file Excel untuk dibuka:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Pastikan Anda memiliki file Excelnya`book1.xls` di direktori dokumen Anda atau tentukan nama file dan lokasi yang benar.

## Langkah 4: Buat instance objek Buku Kerja dan buka file Excel

 Menggunakan`Workbook`kelas dari Aspose.Cells untuk membuat instance objek Buku Kerja dan membuka file Excel yang ditentukan melalui aliran file:

```csharp
Workbook excel = new Workbook(fstream);
```

## Langkah 5: Akses lembar kerja pertama

Arahkan ke lembar kerja pertama dari file Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Langkah 6: Tetapkan Pengaturan Perlindungan Lembar Kerja

Gunakan properti objek Lembar Kerja untuk mengatur pengaturan perlindungan lembar kerja sesuai kebutuhan. Misalnya :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Tetapkan pengaturan perlindungan lainnya sesuai kebutuhan...
```

## Langkah 7: Simpan file Excel yang dimodifikasi

 Simpan file Excel yang dimodifikasi menggunakan`Save` metode objek Buku Kerja:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Pastikan untuk menentukan jalur dan nama file yang diinginkan untuk file keluaran.

## Langkah 8: Tutup aliran file

Setelah disimpan, tutup aliran file untuk melepaskan semua sumber daya terkait:

```csharp
fstream.Close();
```
	
### Contoh kode sumber untuk Pengaturan Perlindungan Tingkat Lanjut Untuk Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat aliran file yang berisi file Excel yang akan dibuka
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Membuat instance objek Buku Kerja
// Membuka file Excel melalui aliran file
Workbook excel = new Workbook(fstream);
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = excel.Worksheets[0];
// Membatasi pengguna untuk menghapus kolom lembar kerja
worksheet.Protection.AllowDeletingColumn = false;
// Membatasi pengguna untuk menghapus baris lembar kerja
worksheet.Protection.AllowDeletingRow = false;
// Membatasi pengguna untuk mengedit isi lembar kerja
worksheet.Protection.AllowEditingContent = false;
// Membatasi pengguna untuk mengedit objek lembar kerja
worksheet.Protection.AllowEditingObject = false;
// Membatasi pengguna untuk mengedit skenario lembar kerja
worksheet.Protection.AllowEditingScenario = false;
//Membatasi pengguna untuk memfilter
worksheet.Protection.AllowFiltering = false;
// Mengizinkan pengguna memformat sel lembar kerja
worksheet.Protection.AllowFormattingCell = true;
// Mengizinkan pengguna memformat baris lembar kerja
worksheet.Protection.AllowFormattingRow = true;
// Mengizinkan pengguna menyisipkan kolom di lembar kerja
worksheet.Protection.AllowFormattingColumn = true;
// Mengizinkan pengguna menyisipkan hyperlink di lembar kerja
worksheet.Protection.AllowInsertingHyperlink = true;
// Mengizinkan pengguna menyisipkan baris di lembar kerja
worksheet.Protection.AllowInsertingRow = true;
// Mengizinkan pengguna memilih sel terkunci pada lembar kerja
worksheet.Protection.AllowSelectingLockedCell = true;
// Mengizinkan pengguna memilih sel lembar kerja yang tidak terkunci
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Mengizinkan pengguna untuk mengurutkan
worksheet.Protection.AllowSorting = true;
// Mengizinkan pengguna menggunakan tabel pivot di lembar kerja
worksheet.Protection.AllowUsingPivotTable = true;
// Menyimpan file Excel yang dimodifikasi
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara mengatur pengaturan perlindungan tingkat lanjut untuk spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Gunakan pengetahuan ini untuk mengamankan file Excel Anda dan membatasi tindakan pengguna.

### FAQ

#### T: Bagaimana cara membuat proyek C# baru di IDE saya?

J: Langkah-langkah untuk membuat proyek C# baru mungkin berbeda-beda tergantung IDE yang Anda gunakan. Konsultasikan dokumentasi IDE Anda untuk instruksi rinci.

#### T: Apakah mungkin untuk menetapkan pengaturan perlindungan khusus selain yang disebutkan dalam tutorial?

J: Ya, Aspose.Cells menawarkan berbagai pengaturan perlindungan yang dapat Anda sesuaikan dengan kebutuhan spesifik Anda. Lihat dokumentasi Aspose.Cells untuk detail selengkapnya.

#### T: Apa format file yang digunakan untuk menyimpan file Excel yang dimodifikasi dalam kode contoh?

A: Dalam kode contoh, file Excel yang dimodifikasi disimpan dalam format Excel 97-2003 (.xls). Anda dapat memilih format lain yang didukung oleh Aspose.Cells jika diperlukan.

#### T: Bagaimana cara mengakses lembar kerja lain di file Excel?

 A: Anda dapat mengakses lembar kerja lain menggunakan indeks atau nama lembar, misalnya:`Worksheet worksheet = excel.Worksheets[1];` atau`Worksheet worksheet = excel.Worksheets[" SheetName"];`.