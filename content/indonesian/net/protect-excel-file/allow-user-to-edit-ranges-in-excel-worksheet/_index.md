---
title: Izinkan Pengguna Untuk Mengedit Rentang Di Lembar Kerja Excel
linktitle: Izinkan Pengguna Untuk Mengedit Rentang Di Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Izinkan pengguna mengedit rentang tertentu dalam spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Panduan langkah demi langkah dengan kode sumber dalam C#.
type: docs
weight: 10
url: /id/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
Dalam panduan ini, kami akan memandu Anda tentang cara menggunakan Aspose.Cells untuk .NET agar pengguna dapat mengedit rentang tertentu dalam spreadsheet Excel. Ikuti langkah-langkah di bawah ini untuk menyelesaikan tugas ini.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menyiapkan lingkungan pengembangan dan menginstal Aspose.Cells untuk .NET. Anda dapat mengunduh perpustakaan versi terbaru dari situs resmi Aspose.

## Langkah 2: Impor namespace yang diperlukan

Dalam proyek C# Anda, impor namespace yang diperlukan untuk bekerja dengan Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Langkah 3: Mengatur jalur ke direktori dokumen

 Nyatakan a`dataDir` variabel untuk menentukan jalur ke direktori tempat Anda ingin menyimpan file Excel yang dihasilkan:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pastikan untuk mengganti`"YOUR_DOCUMENT_DIRECTORY"` dengan jalur yang benar di sistem Anda.

## Langkah 4: Membuat Objek Buku Kerja

Buat instance objek Buku Kerja baru yang mewakili buku kerja Excel yang ingin Anda buat:

```csharp
Workbook book = new Workbook();
```

## Langkah 5: Akses ke lembar kerja pertama

Navigasikan ke lembar kerja pertama di buku kerja Excel menggunakan kode berikut:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Langkah 6: Mengambil rentang modifikasi resmi

 Dapatkan koleksi rentang edit yang diizinkan menggunakan`AllowEditRanges` Properti:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Langkah 7: Tentukan Rentang yang Dilindungi

 Tentukan rentang yang dilindungi menggunakan`Add` metode`AllowEditRanges` koleksi:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Di sini kita telah membuat rentang terlindung "r2" yang membentang dari sel A1 hingga sel C3.

## Langkah 8: Menentukan kata sandi

 Tentukan kata sandi untuk rentang yang dilindungi menggunakan`Password` Properti:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Pastikan untuk mengganti`"YOUR_PASSWORD"` dengan kata sandi yang diinginkan.

## Langkah 9: Melindungi lembar kerja

 Lindungi lembar kerja menggunakan`Protect` metode`Worksheet` obyek:

```csharp
sheet.Protect(ProtectionType.All);
```

Ini akan melindungi spreadsheet dengan mencegah modifikasi apa pun di luar rentang yang diperbolehkan.

## Langkah 10: Mendaftarkan

  berkas Excel

 Simpan file Excel yang dihasilkan menggunakan`Save` metode`Workbook` obyek:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Pastikan untuk menentukan nama file yang diinginkan dan jalur yang benar.

### Contoh kode sumber untuk Izinkan Pengguna Mengedit Rentang di Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
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
proteced_range.Password = "123";
// Lindungi lembaran itu
sheet.Protect(ProtectionType.All);
// Simpan file Excelnya
book.Save(dataDir + "protectedrange.out.xls");
```

## Kesimpulan

Anda sekarang telah mempelajari cara menggunakan Aspose.Cells untuk .NET untuk memungkinkan pengguna mengedit rentang tertentu dalam spreadsheet Excel. Jangan ragu untuk menjelajahi lebih jauh fitur-fitur yang ditawarkan oleh Aspose.Cells untuk memenuhi kebutuhan spesifik Anda.


### FAQ

#### 1. Bagaimana cara mengizinkan pengguna mengedit rentang tertentu di spreadsheet Excel?

 Anda dapat menggunakan`ProtectedRangeCollection` kelas untuk menentukan rentang modifikasi yang diperbolehkan. Menggunakan`Add` metode untuk membuat rentang terlindungi baru dengan sel yang diinginkan.

#### 2. Dapatkah saya menetapkan kata sandi untuk rentang modifikasi resmi?

 Ya, Anda dapat menentukan kata sandi menggunakan`Password` properti dari`ProtectedRange` obyek. Ini akan membatasi akses hanya untuk pengguna yang memiliki kata sandi.

#### 3. Bagaimana cara melindungi spreadsheet setelah rentang yang diizinkan ditetapkan?

 Menggunakan`Protect` metode`Worksheet` objek untuk melindungi lembar kerja. Ini akan mencegah perubahan apa pun di luar rentang yang diizinkan, yang mungkin meminta kata sandi jika Anda menentukannya.