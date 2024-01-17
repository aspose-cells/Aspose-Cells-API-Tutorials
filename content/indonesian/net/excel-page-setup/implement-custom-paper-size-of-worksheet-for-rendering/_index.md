---
title: Terapkan Ukuran Kertas Khusus Lembar Kerja Untuk Rendering
linktitle: Terapkan Ukuran Kertas Khusus Lembar Kerja Untuk Rendering
second_title: Aspose.Cells untuk Referensi .NET API
description: Panduan langkah demi langkah untuk mengimplementasikan ukuran lembar kerja khusus dengan Aspose.Cells untuk .NET. Atur dimensi, tambahkan pesan dan simpan sebagai PDF.
type: docs
weight: 50
url: /id/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Menerapkan ukuran khusus untuk lembar kerja Anda bisa sangat berguna ketika Anda ingin membuat dokumen PDF dengan ukuran tertentu. Dalam tutorial ini, kita akan mempelajari cara menggunakan Aspose.Cells untuk .NET guna mengatur ukuran khusus lembar kerja dan kemudian menyimpan dokumen sebagai PDF.

## Langkah 1: Membuat folder keluaran

Sebelum memulai, Anda perlu membuat folder keluaran tempat file PDF yang dihasilkan akan disimpan. Anda dapat menggunakan jalur apa pun yang Anda inginkan untuk folder keluaran Anda.

```csharp
// Direktori keluaran
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Pastikan Anda menentukan jalur yang benar ke folder keluaran Anda.

## Langkah 2: Membuat objek Buku Kerja

Untuk memulai, Anda perlu membuat objek Buku Kerja menggunakan Aspose.Cells. Objek ini mewakili spreadsheet Anda.

```csharp
// Buat objek Buku Kerja
Workbook wb = new Workbook();
```

## Langkah 3: Akses ke lembar kerja pertama

Setelah membuat objek Buku Kerja, Anda bisa mengakses lembar kerja pertama di dalamnya.

```csharp
// Akses ke lembar kerja pertama
Worksheet ws = wb.Worksheets[0];
```

## Langkah 4: Mengatur ukuran lembar kerja khusus

 Sekarang Anda dapat mengatur ukuran lembar kerja khusus menggunakan`CustomPaperSize(width, height)` metode kelas PageSetup.

```csharp
// Tetapkan ukuran lembar kerja khusus (dalam inci)
ws.PageSetup.CustomPaperSize(6, 4);
```

Dalam contoh ini, kami telah menetapkan ukuran lembar kerja menjadi lebar 6 inci dan tinggi 4 inci.

## Langkah 5: Akses ke sel B4

Setelah itu, kita bisa mengakses sel tertentu di lembar kerja. Dalam hal ini, kita akan mengakses sel B4.

```csharp
// Akses ke sel B4
Cell b4 = ws.Cells["B4"];
```

## Langkah 6: Menambahkan pesan di sel B4

 Sekarang kita dapat menambahkan pesan ke sel B4 menggunakan`PutValue(value)` metode.

```csharp
// Tambahkan pesan di sel B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

Dalam contoh ini, kami telah menambahkan pesan "Ukuran Halaman PDF: 6,00" x 4,00" di sel B4.

## Langkah 7: Menyimpan lembar kerja dalam format PDF

 Terakhir, kita dapat menyimpan lembar kerja dalam format PDF menggunakan`Save(filePath)` metode objek Buku Kerja.

```csharp
// Simpan lembar kerja dalam format PDF
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Tentukan jalur yang diinginkan ke file PDF yang dihasilkan, menggunakan folder keluaran yang dibuat sebelumnya.

### Contoh kode sumber untuk Menerapkan Ukuran Kertas Khusus Lembar Kerja Untuk Rendering menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori keluaran
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Buat objek buku kerja
Workbook wb = new Workbook();
//Akses lembar kerja pertama
Worksheet ws = wb.Worksheets[0];
//Atur ukuran kertas khusus dalam satuan inci
ws.PageSetup.CustomPaperSize(6, 4);
//Akses sel B4
Cell b4 = ws.Cells["B4"];
//Tambahkan pesan di sel B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Simpan buku kerja dalam format pdf
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Kesimpulan

Dalam tutorial ini, Anda mempelajari cara mengimplementasikan ukuran khusus lembar kerja menggunakan Aspose.Cells untuk .NET. Anda dapat menggunakan langkah-langkah ini untuk mengatur dimensi tertentu untuk lembar kerja Anda dan kemudian menyimpan dokumen dalam format PDF. Kami berharap panduan ini bermanfaat dalam memahami proses penerapan ukuran spreadsheet khusus.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Pertanyaan 1: Dapatkah saya menyesuaikan tata letak spreadsheet lebih lanjut?

Ya, Aspose.Cells menawarkan banyak opsi untuk menyesuaikan tata letak lembar kerja Anda. Anda dapat mengatur dimensi khusus, orientasi halaman, margin, header dan footer, dan banyak lagi.

#### Pertanyaan 2: Format keluaran apa lagi yang didukung Aspose.Cells?

Aspose.Cells mendukung banyak format keluaran berbeda, termasuk PDF, XLSX, XLS, CSV, HTML, TXT dan banyak lagi. Anda dapat memilih format output yang diinginkan sesuai kebutuhan Anda.