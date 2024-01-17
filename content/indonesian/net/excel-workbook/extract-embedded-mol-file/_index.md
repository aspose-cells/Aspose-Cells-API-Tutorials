---
title: Ekstrak File Mol Tertanam
linktitle: Ekstrak File Mol Tertanam
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mengekstrak file MOL yang disematkan dengan mudah dari buku kerja Excel menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 90
url: /id/net/excel-workbook/extract-embedded-mol-file/
---
Dalam tutorial ini, kami akan memandu Anda melalui langkah demi langkah cara mengekstrak file MOL yang disematkan dari buku kerja Excel menggunakan pustaka Aspose.Cells untuk .NET. Anda akan mempelajari cara menelusuri lembar buku kerja, mengekstrak objek OLE yang sesuai, dan menyimpan file MOL yang diekstrak. Ikuti langkah-langkah di bawah ini untuk menyelesaikan tugas ini dengan sukses.

## Langkah 1: Tentukan direktori sumber dan keluaran
Pertama, kita perlu mendefinisikan direktori sumber dan keluaran dalam kode kita. Direktori ini menunjukkan di mana buku kerja Excel sumber berada dan di mana file MOL yang diekstraksi akan disimpan. Ini kode yang sesuai:

```csharp
// Direktori
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Pastikan untuk menentukan jalur yang sesuai sesuai kebutuhan.

## Langkah 2: Memuat buku kerja Excel
Langkah selanjutnya adalah memuat buku kerja Excel yang berisi objek OLE dan file MOL yang disematkan. Berikut ini kode untuk memuat buku kerja:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Pastikan untuk menentukan nama file sumber dengan benar dalam kode.

## Langkah 3: Telusuri lembaran dan ekstrak file MOL
Sekarang kita akan mengulang setiap lembar di buku kerja dan mengekstrak objek OLE yang sesuai, yang berisi file MOL. Ini kode yang sesuai:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Kode ini mengulang setiap lembar di buku kerja, mengambil objek OLE, dan menyimpan file MOL yang diekstraksi ke direktori keluaran.

### Contoh kode sumber untuk Ekstrak File Mol Tertanam menggunakan Aspose.Cells untuk .NET 
```csharp
//direktori
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Kesimpulan
Selamat! Anda telah mempelajari cara mengekstrak file MOL yang disematkan dari buku kerja Excel menggunakan Aspose.Cells untuk .NET. Anda sekarang dapat menerapkan pengetahuan ini untuk mengekstrak file MOL dari buku kerja Excel Anda sendiri. Jangan ragu untuk menjelajahi perpustakaan Aspose.Cells lebih jauh dan mempelajari fitur-fitur canggih lainnya.

### FAQ

#### T: Apa itu file MOL?
 
J: File MOL adalah format file yang digunakan untuk mewakili struktur kimia dalam kimia komputasi. Ini berisi informasi tentang atom, ikatan dan sifat molekul lainnya.

#### T: Apakah metode ini berfungsi pada semua jenis file Excel?

J: Ya, metode ini berfungsi dengan semua jenis file Excel yang didukung oleh Aspose.Cells.

#### T: Bisakah saya mengekstrak beberapa file MOL sekaligus?

J: Ya, Anda bisa mengekstrak beberapa file MOL sekaligus dengan melakukan iterasi melalui objek OLE pada setiap lembar di buku kerja.