---
title: Edit Rentang Di Lembar Kerja Excel
linktitle: Edit Rentang Di Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mengedit rentang tertentu dalam spreadsheet Excel dengan Aspose.Cells untuk .NET. Tutorial langkah demi langkah di C#.
type: docs
weight: 20
url: /id/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel adalah alat yang ampuh untuk membuat dan mengelola spreadsheet, menawarkan banyak fitur untuk mengontrol dan mengamankan data. Salah satu fitur tersebut adalah memungkinkan pengguna mengedit rentang tertentu di lembar kerja sambil melindungi bagian lainnya. Dalam tutorial ini, kami akan memandu Anda langkah demi langkah untuk mengimplementasikan fungsi ini menggunakan Aspose.Cells untuk .NET, perpustakaan populer untuk bekerja dengan file Excel secara terprogram.

Menggunakan Aspose.Cells untuk .NET akan memungkinkan Anda memanipulasi rentang dalam spreadsheet Excel dengan mudah, menyediakan antarmuka yang ramah pengguna dan fitur-fitur canggih. Ikuti langkah-langkah di bawah ini untuk memungkinkan pengguna mengedit rentang tertentu dalam spreadsheet Excel menggunakan Aspose.Cells untuk .NET.
## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells for .NET di lingkungan pengembangan Anda. Unduh perpustakaan dari situs resmi Aspose dan periksa dokumentasi untuk petunjuk instalasi.

## Langkah 2: Inisialisasi Buku Kerja dan Lembar Kerja

Untuk memulai, kita perlu membuat buku kerja baru dan mendapatkan referensi ke lembar kerja yang rentangnya ingin kita ubah. Gunakan kode berikut untuk mencapai hal ini:

```csharp
// Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Buat direktori jika belum ada.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Buat instance buku kerja baru
Workbook workbook = new Workbook();

// Dapatkan lembar kerja pertama (default)
Worksheet sheet = workbook.Worksheets[0];
```

 Pada cuplikan kode ini, pertama-tama kita tentukan path ke direktori tempat file Excel akan disimpan. Selanjutnya, kita membuat instance baru dari`Workbook` kelas dan dapatkan referensi ke lembar kerja pertama menggunakan`Worksheets` Properti.

## Langkah 3: Dapatkan Rentang yang Dapat Diedit

Sekarang kita perlu mengambil rentang yang ingin kita izinkan modifikasinya. Gunakan kode berikut:

```csharp
// Dapatkan rentang yang dapat dimodifikasi
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Langkah 4: Tetapkan Rentang Terlindungi

Sebelum mengizinkan rentang untuk dimodifikasi, kita perlu menentukan rentang yang dilindungi. Begini caranya:

```csharp
// Tentukan rentang yang dilindungi
ProtectedRange ProtectedRange;

// Buat rentangnya
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 Dalam kode ini, kami membuat instance baru dari`ProtectedRange` kelas dan gunakan`Add` metode untuk menentukan rentang yang akan dilindungi.

## Langkah 5: Tentukan Kata Sandi

Untuk meningkatkan keamanan, Anda dapat menentukan kata sandi untuk rentang yang dilindungi. Begini caranya:

```csharp
// Tentukan kata sandi
protectedBeach.Password = "YOUR_PASSWORD";
```

## Langkah 6: Lindungi lembar kerja

Sekarang kita telah menetapkan rentang yang dilindungi, kita dapat melindungi lembar kerja untuk mencegah modifikasi yang tidak sah. Gunakan kode berikut:

```csharp
// Lindungi lembar kerja
leaf.Protect(ProtectionType.All);
```

## Langkah 7: Simpan File Excel

Terakhir, kami menyimpan file Excel dengan perubahan yang dilakukan. Ini kode yang diperlukan:

```csharp
// Simpan file Excelnya
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Contoh kode sumber untuk Edit Rentang Di Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Buat direktori jika belum ada.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Buat instance Buku Kerja baru
Workbook book = new Workbook();

// Dapatkan lembar kerja pertama (default).
Worksheet sheet = book.Worksheets[0];

// Dapatkan Izinkan Edit Rentang
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Tentukan Rentang Terproteksi
ProtectedRange proteced_range;

// Buat rentangnya
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Tentukan kata sandi
proteced_range.Password = "YOUR_PASSWORD";

// Lindungi lembaran itu
sheet.Protect(ProtectionType.All);

// Simpan file Excelnya
book.Save(dataDir + "protectedrange.out.xls");
```

## Kesimpulan

Selamat! Anda mempelajari cara mengizinkan pengguna mengedit rentang tertentu dalam spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Anda sekarang dapat menerapkan teknik ini dalam proyek Anda sendiri dan meningkatkan keamanan file Excel Anda.


#### FAQ

#### T: Mengapa saya harus menggunakan Aspose.Cells untuk .NET untuk mengedit rentang dalam lembar bentang Excel?

J: Aspose.Cells for .NET menawarkan API yang kuat dan mudah digunakan untuk bekerja dengan file Excel. Ini menyediakan fitur-fitur canggih, seperti manipulasi rentang, perlindungan lembar kerja, dll.

#### T: Dapatkah saya mengatur beberapa rentang yang dapat diedit dalam satu lembar kerja?

 J: Ya, Anda dapat menentukan beberapa rentang yang dapat diedit menggunakan`Add` metode`ProtectedRangeCollection` koleksi. Setiap rentang dapat memiliki pengaturan perlindungannya sendiri.

####  T: Apakah mungkin untuk menghapus rentang yang dapat diedit setelah menentukannya?

 A: Ya, Anda dapat menggunakan`RemoveAt` metode`ProtectedRangeCollection` koleksi untuk menghapus rentang tertentu yang dapat diedit dengan menentukan indeksnya.

#### T: Bagaimana cara membuka file Excel yang dilindungi setelah menyimpannya?

J: Anda harus memberikan kata sandi yang ditentukan saat membuat rentang terproteksi untuk membuka file Excel yang diproteksi. Pastikan untuk menyimpan kata sandi di tempat yang aman untuk mencegah hilangnya akses ke data.