---
title: Izinkan Apostrof Terkemuka
linktitle: Izinkan Apostrof Terkemuka
second_title: Aspose.Cells untuk Referensi .NET API
description: Izinkan tanda kutip utama di buku kerja Excel dengan Aspose.Cells untuk .NET.
type: docs
weight: 60
url: /id/net/excel-workbook/allow-leading-apostrophe/
---
Dalam tutorial langkah demi langkah ini, kami akan menjelaskan kode sumber C# yang disediakan yang memungkinkan Anda mengizinkan penggunaan tanda kutip utama di buku kerja Excel menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk melakukan operasi ini.

## Langkah 1: Tetapkan direktori sumber dan keluaran

```csharp
// direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
// Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
```

Pada langkah pertama ini, kami menentukan direktori sumber dan keluaran untuk file Excel.

## Langkah 2: Buat instance objek WorkbookDesigner

```csharp
// Membuat instance objek WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Kami membuat sebuah instance dari`WorkbookDesigner` kelas dari Aspose.Cells.

## Langkah 3: Muat Buku Kerja Excel

```csharp
// Muat buku kerja Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Kami memuat buku kerja Excel dari file yang ditentukan dan menonaktifkan konversi otomatis apostrof awal ke gaya teks.

## Langkah 4: Tetapkan Sumber Data

```csharp
// Tentukan sumber data untuk buku kerja desainer
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Kami mendefinisikan daftar objek data dan menggunakan`SetDataSource` metode untuk mengatur sumber data untuk buku kerja desainer.

## Langkah 5: Proses penanda cerdas

```csharp
// Proses penanda cerdas
designer. Process();
```

 Kami menggunakan`Process` metode untuk memproses penanda cerdas di buku kerja desainer.

## Langkah 6: Simpan buku kerja Excel yang dimodifikasi

```csharp
// Simpan buku kerja Excel yang dimodifikasi
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Kami menyimpan buku kerja Excel yang dimodifikasi dengan perubahan yang dilakukan.

### Contoh kode sumber untuk Izinkan Apostrof Terkemuka menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Membuat instance objek WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Buka spreadsheet desainer yang berisi penanda cerdas
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Tetapkan sumber data untuk spreadsheet desainer
designer.SetDataSource("sampleData", list);
// Proses penanda pintar
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Kesimpulan

Selamat! Anda mempelajari cara mengizinkan penggunaan tanda kutip di depan dalam buku kerja Excel menggunakan Aspose.Cells untuk .NET. Bereksperimenlah dengan data Anda sendiri untuk mengkustomisasi lebih lanjut buku kerja Excel Anda.

### FAQ

#### T: Apa yang dimaksud dengan izin apostrof di buku kerja Excel?

J: Mengizinkan tanda kutip awal di buku kerja Excel memungkinkan data yang dimulai dengan tanda kutip ditampilkan dengan benar tanpa mengonversinya menjadi gaya teks. Ini berguna bila Anda ingin menyimpan apostrof sebagai bagian dari data.

#### T: Mengapa saya perlu menonaktifkan konversi otomatis apostrof awal?

J: Dengan menonaktifkan konversi otomatis kutipan terkemuka, Anda dapat mempertahankan penggunaannya seperti yang ada di data Anda. Hal ini menghindari modifikasi data yang tidak diinginkan saat membuka atau memanipulasi buku kerja Excel.

#### T: Bagaimana cara mengatur sumber data di buku kerja desainer?

 J: Untuk mengatur sumber data di buku kerja desainer, Anda bisa menggunakan`SetDataSource` metode yang menentukan nama sumber data dan daftar objek data terkait.

#### T: Apakah mengizinkan apostrof di depan memengaruhi data lain di buku kerja Excel?

J: Tidak, mengizinkan apostrof di depan hanya memengaruhi data yang diawali dengan apostrof. Data lain di buku kerja Excel tetap tidak berubah.

#### T: Dapatkah saya menggunakan fitur ini dengan format file Excel lainnya?

A: Ya, Anda dapat menggunakan fitur ini dengan format file Excel lain yang didukung oleh Aspose.Cells, seperti .xls, .xlsm, dll.