---
title: Lindungi Kata Sandi Atau Buka Proteksi Buku Kerja Bersama
linktitle: Lindungi Kata Sandi Atau Buka Proteksi Buku Kerja Bersama
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara memproteksi atau membuka proteksi buku kerja bersama dengan kata sandi menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 120
url: /id/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Melindungi buku kerja bersama dengan kata sandi penting untuk memastikan privasi data. Dengan Aspose.Cells untuk .NET, Anda dapat dengan mudah memproteksi atau membuka proteksi buku kerja bersama menggunakan kata sandi. Ikuti langkah-langkah di bawah ini untuk mendapatkan hasil yang diinginkan:

## Langkah 1: Tentukan direktori keluaran

Pertama, Anda perlu menentukan direktori keluaran tempat file Excel yang dilindungi akan disimpan. Berikut cara melakukannya menggunakan Aspose.Cells:

```csharp
// Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
```

## Langkah 2: Buat file Excel kosong

Kemudian Anda dapat membuat file Excel kosong yang ingin Anda terapkan proteksi atau tidak proteksi. Berikut ini contoh kodenya:

```csharp
// Buat buku kerja Excel kosong
Workbook wb = new Workbook();
```

## Langkah 3: Proteksi atau buka proteksi buku kerja bersama

Setelah membuat buku kerja, Anda bisa memproteksi atau membuka proteksi buku kerja bersama dengan menentukan kata sandi yang sesuai. Begini caranya:

```csharp
// Lindungi buku kerja bersama dengan kata sandi
wb.ProtectSharedWorkbook("1234");

// Batalkan komentar pada baris ini untuk membuka proteksi buku kerja bersama
// wb.UnprotectSharedWorkbook("1234");
```

## Langkah 4: Simpan file Excel keluaran

Setelah Anda menerapkan proteksi atau pembatalan proteksi, Anda dapat menyimpan file Excel yang dilindungi ke direktori keluaran yang ditentukan. Berikut cara melakukannya:

```csharp
// Simpan file keluaran Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Contoh kode sumber untuk Buku Kerja Bersama yang Dilindungi atau Dilindungi Kata Sandi menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
//Buat file Excel kosong
Workbook wb = new Workbook();
//Lindungi Buku Kerja Bersama dengan Kata Sandi
wb.ProtectSharedWorkbook("1234");
//Batalkan komentar pada baris ini untuk Membuka Proteksi Buku Kerja Bersama
//wb.UnprotectSharedWorkbook("1234");
//Simpan file keluaran Excel
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Kesimpulan

Memproteksi atau membuka proteksi buku kerja bersama dengan kata sandi sangat penting untuk memastikan keamanan data. Dengan Aspose.Cells untuk .NET Anda dapat dengan mudah menambahkan fungsi ini ke file Excel Anda. Dengan mengikuti langkah-langkah dalam panduan ini, Anda bisa secara efektif memproteksi atau membuka proteksi buku kerja bersama menggunakan kata sandi. Bereksperimenlah dengan file Excel Anda sendiri dan pastikan untuk menjaga keamanan data sensitif Anda.

### FAQ

#### T: Jenis perlindungan apa yang bisa saya terapkan pada buku kerja yang dibagikan dengan Aspose.Cells?
    
J: Dengan Aspose.Cells, Anda bisa melindungi buku kerja bersama dengan menentukan kata sandi untuk mencegah akses tidak sah, modifikasi, atau penghapusan data.

#### T: Bisakah saya memproteksi buku kerja bersama tanpa menentukan kata sandi?
    
J: Ya, Anda bisa memproteksi buku kerja bersama tanpa menentukan kata sandi. Namun, disarankan untuk menggunakan kata sandi yang kuat untuk keamanan yang lebih baik.

#### T: Bagaimana cara membuka proteksi buku kerja yang dibagikan dengan Aspose.Cells?
    
J: Untuk membuka proteksi buku kerja bersama, Anda harus menentukan kata sandi yang sama yang digunakan saat memproteksi buku kerja. Hal ini memungkinkan perlindungan dihapus dan data dapat diakses secara bebas.

#### T: Apakah memproteksi buku kerja bersama memengaruhi fitur dan rumus dalam buku kerja?
    
J: Saat Anda memproteksi buku kerja bersama, pengguna masih bisa mengakses fitur dan rumus yang ada di buku kerja. Perlindungan hanya mempengaruhi perubahan struktural pada buku kerja.