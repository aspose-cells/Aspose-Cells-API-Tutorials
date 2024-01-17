---
title: Buat Buku Kerja Bersama
linktitle: Buat Buku Kerja Bersama
second_title: Aspose.Cells untuk Referensi .NET API
description: Buat buku kerja bersama Excel dengan Aspose.Cells untuk .NET untuk mengaktifkan kolaborasi data secara bersamaan.
type: docs
weight: 70
url: /id/net/excel-workbook/create-shared-workbook/
---
Dalam tutorial ini, kami akan memandu Anda melalui kode sumber C# yang disediakan yang memungkinkan Anda membuat buku kerja bersama menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk melakukan operasi ini.

## Langkah 1: Tetapkan direktori keluaran

```csharp
// Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
```

Pada langkah pertama ini, kita menentukan direktori keluaran tempat buku kerja bersama akan disimpan.

## Langkah 2: Buat Objek Buku Kerja

```csharp
// Buat objek Buku Kerja
Workbook wb = new Workbook();
```

Kami membuat objek Buku Kerja baru yang akan mewakili buku kerja Excel kami.

## Langkah 3: Aktifkan Berbagi Buku Kerja

```csharp
// Bagikan buku kerja
wb.Settings.Shared = true;
```

 Kami mengaktifkan fitur berbagi buku kerja dengan mengatur`Shared` milik objek Buku Kerja`true`.

## Langkah 4: Simpan buku kerja bersama

```csharp
// Simpan buku kerja bersama
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Kami menyimpan buku kerja bersama dengan menentukan jalur dan nama file keluaran.

### Contoh kode sumber untuk Membuat Buku Kerja Bersama menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
//Buat objek Buku Kerja
Workbook wb = new Workbook();
//Bagikan Buku Kerja
wb.Settings.Shared = true;
//Simpan Buku Kerja Bersama
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Kesimpulan

Selamat! Anda mempelajari cara membuat buku kerja bersama menggunakan Aspose.Cells untuk .NET. Buku kerja bersama bisa digunakan oleh beberapa pengguna secara bersamaan untuk berkolaborasi pada data. Bereksperimenlah dengan data Anda sendiri dan jelajahi lebih jauh fitur Aspose.Cells untuk membuat buku kerja Excel yang canggih dan dipersonalisasi.

### FAQ

#### T: Apa yang dimaksud dengan buku kerja bersama?

J: Buku kerja bersama adalah buku kerja Excel yang bisa digunakan secara bersamaan oleh beberapa pengguna untuk berkolaborasi pada data. Setiap pengguna bisa membuat perubahan pada buku kerja dan pengguna lain akan melihat pembaruan secara real time.

#### T: Bagaimana cara mengaktifkan berbagi buku kerja di Aspose.Cells untuk .NET?

 J: Untuk mengaktifkan berbagi buku kerja di Aspose.Cells untuk .NET, Anda harus mengatur`Shared` milik objek Buku Kerja`true`. Ini akan memungkinkan pengguna untuk mengerjakan buku kerja secara bersamaan.

#### T: Bisakah saya membatasi izin pengguna di buku kerja bersama?

J: Ya, Anda bisa membatasi izin pengguna di buku kerja bersama menggunakan fitur keamanan Excel. Anda dapat mengatur izin khusus untuk setiap pengguna, seperti kemampuan untuk mengedit, hanya membaca, dll.

#### T: Bagaimana cara berbagi buku kerja dengan pengguna lain?

J: Setelah Anda membuat buku kerja bersama, Anda bisa membaginya dengan pengguna lain dengan mengirimkan file Excel kepada mereka. Pengguna lain akan dapat membuka file dan mengerjakannya secara bersamaan.

#### T: Apakah semua fitur Excel didukung di buku kerja bersama?

J: Sebagian besar fitur Excel didukung di buku kerja bersama. Namun, beberapa fitur tingkat lanjut, seperti makro dan add-in, mungkin memiliki batasan atau pembatasan saat digunakan dalam buku kerja bersama.