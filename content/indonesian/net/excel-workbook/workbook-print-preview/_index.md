---
title: Pratinjau Cetak Buku Kerja
linktitle: Pratinjau Cetak Buku Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara membuat pratinjau cetak buku kerja menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 170
url: /id/net/excel-workbook/workbook-print-preview/
---
Pratinjau cetak Buku Kerja adalah fitur penting saat bekerja dengan file Excel dengan Aspose.Cells untuk .NET. Anda dapat dengan mudah membuat pratinjau cetak dengan mengikuti langkah-langkah berikut:

## Langkah 1: Tentukan direktori sumber

Pertama, Anda perlu menentukan direktori sumber tempat file Excel yang ingin Anda pratinjau berada. Berikut cara melakukannya:

```csharp
// direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Langkah 2: Muat Buku Kerja

Maka Anda perlu memuat buku kerja Buku Kerja dari file Excel yang ditentukan. Berikut cara melakukannya:

```csharp
// Memuat buku kerja Buku Kerja
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Langkah 3: Konfigurasikan opsi gambar dan cetak

Sebelum membuat pratinjau cetak, Anda dapat mengonfigurasi gambar dan opsi pencetakan sesuai kebutuhan. Dalam contoh ini, kami menggunakan opsi default. Berikut cara melakukannya:

```csharp
// Opsi gambar dan cetak
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Langkah 4: Hasilkan pratinjau cetak buku kerja

Sekarang Anda dapat menghasilkan pratinjau cetak buku kerja Buku Kerja dengan menggunakan kelas WorkbookPrintingPreview. Berikut cara melakukannya:

```csharp
// Cetak pratinjau buku kerja
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Langkah 5: Hasilkan pratinjau cetak lembar kerja

Jika Anda ingin membuat pratinjau cetak lembar kerja tertentu, Anda bisa menggunakan kelas SheetPrintingPreview. Berikut ini contohnya:

```csharp
// Cetak pratinjau lembar kerja
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Contoh kode sumber untuk Pratinjau Cetak Buku Kerja menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Kesimpulan

Menghasilkan pratinjau cetak buku kerja adalah fitur canggih yang ditawarkan oleh Aspose.Cells untuk .NET. Dengan mengikuti langkah-langkah yang diberikan di atas, Anda bisa dengan mudah melihat pratinjau buku kerja Excel Anda dan mendapatkan informasi tentang jumlah halaman yang akan dicetak.

### FAQ

#### T: Bagaimana cara menentukan direktori sumber berbeda untuk memuat Buku Kerja saya?
    
 J: Anda dapat menggunakan`Set_SourceDirectory` metode untuk menentukan direktori sumber yang berbeda. Misalnya:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### T: Dapatkah saya menyesuaikan pilihan gambar dan pencetakan saat membuat pratinjau cetak?
    
 J: Ya, Anda dapat menyesuaikan pilihan gambar dan pencetakan dengan mengubah properti`ImageOrPrintOptions` obyek. Misalnya, Anda dapat mengatur resolusi gambar, format file keluaran, dll.

#### T: Apakah mungkin membuat pratinjau cetak untuk beberapa lembar kerja dalam satu Buku Kerja?
    
J: Ya, Anda bisa mengulangi lembar kerja yang berbeda di Buku Kerja dan menghasilkan pratinjau cetak untuk setiap lembar menggunakan`SheetPrintingPreview` kelas.

#### T: Bagaimana cara menyimpan pratinjau cetak sebagai file gambar atau PDF?
    
 J: Anda dapat menggunakan`ToImage` atau`ToPdf` metode dari`WorkbookPrintingPreview` atau`SheetPrintingPreview` objek untuk menyimpan pratinjau cetak sebagai file gambar atau PDF.

#### T: Apa yang dapat saya lakukan dengan pratinjau cetak setelah dibuat?
    
J: Setelah Anda membuat pratinjau cetak, Anda dapat melihatnya di layar, menyimpannya sebagai gambar atau file PDF, atau menggunakannya untuk operasi lain seperti mengirim melalui email atau mencetak.
	