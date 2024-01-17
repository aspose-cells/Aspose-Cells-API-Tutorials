---
title: Perbarui Item Rumus Power Query
linktitle: Perbarui Item Rumus Power Query
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara memperbarui elemen rumus Power Query dalam file Excel menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 160
url: /id/net/excel-workbook/update-power-query-formula-item/
---
Memperbarui item rumus Power Query adalah operasi umum saat bekerja dengan data dalam file Excel. Dengan Aspose.Cells untuk .NET, Anda dapat dengan mudah memperbarui item rumus Power Query dengan mengikuti langkah-langkah berikut:

## Langkah 1: Tentukan direktori sumber dan keluaran

Pertama, Anda perlu menentukan direktori sumber tempat file Excel yang berisi rumus Power Query yang akan diperbarui berada, serta direktori keluaran tempat Anda ingin menyimpan file yang dimodifikasi. Berikut cara melakukannya menggunakan Aspose.Cells:

```csharp
// direktori sumber
string SourceDir = RunExamples.Get_SourceDirectory();

// Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
```

## Langkah 2: Muat buku kerja Excel sumber

Selanjutnya, Anda perlu memuat buku kerja Excel sumber tempat Anda ingin memperbarui item rumus Power Query. Berikut cara melakukannya:

```csharp
// Muat buku kerja Excel sumber
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Langkah 3: Telusuri dan Perbarui Item Rumus Power Query

Setelah memuat buku kerja, Anda bisa menavigasi ke kumpulan rumus Power Query dan menelusuri setiap rumus dan elemennya. Dalam contoh ini, kita mencari item rumus dengan nama "Sumber" dan memperbarui nilainya. Berikut ini contoh kode untuk memperbarui item rumus Power Query:

```csharp
// Akses kumpulan rumus Power Query
DataMashup mashupData = workbook.DataMashup;

// Ulangi rumus Power Query dan elemennya
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Langkah 4: Simpan buku kerja Excel keluaran

Setelah Anda memperbarui item rumus Power Query, Anda bisa menyimpan buku kerja Excel yang dimodifikasi ke direktori output yang ditentukan. Berikut cara melakukannya:

```csharp
// Simpan buku kerja Excel keluaran
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Contoh kode sumber untuk Memperbarui Item Rumus Power Query menggunakan Aspose.Cells untuk .NET 
```csharp
// Direktori kerja
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Simpan buku kerja keluaran.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Kesimpulan

Memperbarui elemen rumus Power Query merupakan operasi penting saat menggunakan Aspose.Cells untuk memanipulasi dan memproses data dalam file Excel. Dengan mengikuti langkah-langkah yang diberikan di atas, Anda dapat dengan mudah memperbarui elemen rumus

### FAQ

#### T: Apa itu Power Query di Excel?
     
J: Power Query adalah fitur di Excel yang membantu mengumpulkan, mengubah, dan memuat data dari berbagai sumber. Ia menawarkan alat canggih untuk membersihkan, menggabungkan, dan membentuk ulang data sebelum mengimpornya ke Excel.

#### T: Bagaimana cara mengetahui apakah item rumus Power Query berhasil diperbarui?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### T: Bisakah saya memperbarui beberapa item rumus Power Query sekaligus?
    
J: Ya, Anda bisa mengulang kumpulan item rumus Power Query dan memperbarui beberapa item dalam satu putaran, bergantung pada kebutuhan spesifik Anda.

#### T: Apakah ada operasi lain yang bisa saya lakukan pada rumus Power Query dengan Aspose.Cells?
    
J: Ya, Aspose.Cells menawarkan serangkaian fitur lengkap untuk bekerja dengan rumus Power Query, termasuk membuat, menghapus, menyalin, dan mencari rumus di buku kerja Excel.