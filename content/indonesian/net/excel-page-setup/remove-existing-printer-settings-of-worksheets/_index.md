---
title: Hapus Pengaturan Printer yang Ada Pada Lembar Kerja
linktitle: Hapus Pengaturan Printer yang Ada Pada Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara menghapus pengaturan printer yang ada dari spreadsheet Excel dengan Aspose.Cells untuk .NET.
type: docs
weight: 80
url: /id/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
Dalam tutorial ini, kami akan memandu Anda langkah demi langkah cara menghapus pengaturan printer yang ada dari lembar kerja di Excel menggunakan Aspose.Cells untuk .NET. Kami akan menggunakan kode sumber C# untuk mengilustrasikan prosesnya.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET di mesin Anda. Buat juga proyek baru di lingkungan pengembangan pilihan Anda.

## Langkah 2: Impor perpustakaan yang diperlukan

Dalam file kode Anda, impor pustaka yang diperlukan untuk bekerja dengan Aspose.Cells. Ini kode yang sesuai:

```csharp
using Aspose.Cells;
```

## Langkah 3: Tetapkan direktori sumber dan keluaran

Tetapkan direktori sumber dan keluaran tempat file Excel asli berada dan tempat Anda ingin menyimpan file yang dimodifikasi. Gunakan kode berikut:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Pastikan untuk menentukan jalur direktori lengkap.

## Langkah 4: Memuat File Sumber Excel

Muat file Excel sumber menggunakan kode berikut:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Ini akan memuat file Excel yang ditentukan ke dalam objek Buku Kerja.

## Langkah 5: Navigasikan lembar kerja

Iterasi seluruh lembar kerja di buku kerja menggunakan loop. Gunakan kode berikut:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Kode lainnya akan ditambahkan pada langkah berikutnya.
}
```

## Langkah 6: Hapus Pengaturan Printer yang Ada

Periksa apakah pengaturan printer ada untuk setiap lembar kerja dan hapus jika perlu. Gunakan kode berikut:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Langkah 7: Menyimpan Buku Kerja yang Dimodifikasi

Simpan buku kerja yang dimodifikasi menggunakan kode berikut:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Ini akan menyimpan buku kerja yang dimodifikasi ke direktori keluaran yang ditentukan.

### Contoh kode sumber untuk Menghapus Pengaturan Printer yang Ada Pada Lembar Kerja menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
//Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
//Muat file Excel sumber
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Dapatkan jumlah lembar buku kerja
int sheetCount = wb.Worksheets.Count;
//Ulangi semua lembar
for (int i = 0; i < sheetCount; i++)
{
    //Akses lembar kerja ke-i
    Worksheet ws = wb.Worksheets[i];
    //Akses pengaturan halaman lembar kerja
    PageSetup ps = ws.PageSetup;
    //Periksa apakah pengaturan printer untuk lembar kerja ini ada
    if (ps.PrinterSettings != null)
    {
        //Cetak pesan berikut
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Nama lembar cetak dan ukuran kertasnya
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Hapus pengaturan printer dengan menyetelnya ke nol
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//jika
}//untuk
//Simpan buku kerja
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Kesimpulan

Anda sekarang telah mempelajari cara menghapus pengaturan printer yang ada dari lembar kerja di Excel menggunakan Aspose.Cells untuk .NET. Tutorial ini memandu Anda melalui setiap langkah proses, mulai dari menyiapkan lingkungan hingga menavigasi spreadsheet dan menghapus pengaturan printer. Anda sekarang dapat menggunakan pengetahuan ini untuk mengelola pengaturan printer di file Excel Anda.

### FAQ

#### Q1: Bagaimana saya tahu jika spreadsheet sudah memiliki pengaturan printer?

 A1: Anda dapat memeriksa apakah pengaturan printer ada untuk lembar kerja dengan mengakses`PrinterSettings` properti dari`PageSetup` obyek. Jika nilainya bukan null berarti sudah ada pengaturan printer.

#### Q2: Bisakah saya menghapus pengaturan printer hanya untuk spreadsheet tertentu?

 A2: Ya, Anda dapat menggunakan pendekatan yang sama untuk menghapus pengaturan printer untuk lembar kerja tertentu dengan mengakses`PageSetup` obyek.

#### Q3: Apakah metode ini juga menghapus pengaturan tata letak lainnya?

A3: Tidak, cara ini hanya menghapus pengaturan printer. Pengaturan tata letak lainnya, seperti margin, orientasi kertas, dll., tetap tidak berubah.

#### Q4: Apakah metode ini berfungsi untuk semua format file Excel, seperti .xls dan .xlsx?

A4: Ya, metode ini berfungsi untuk semua format file Excel yang didukung oleh Aspose.Cells, termasuk .xls dan .xlsx.

#### Q5: Apakah perubahan yang dilakukan pada pengaturan printer bersifat permanen pada file Excel yang diedit?

A5: Ya, perubahan pengaturan printer disimpan secara permanen di file Excel yang diedit.