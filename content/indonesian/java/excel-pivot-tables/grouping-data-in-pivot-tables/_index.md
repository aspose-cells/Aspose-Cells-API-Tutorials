---
title: Mengelompokkan Data dalam Tabel Pivot
linktitle: Mengelompokkan Data dalam Tabel Pivot
second_title: API Pemrosesan Java Excel Aspose.Cells
description: Pelajari cara membuat tabel pivot di Excel menggunakan Aspose.Cells untuk Java. Otomatiskan pengelompokan dan analisis data dengan contoh kode sumber.
type: docs
weight: 14
url: /id/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

Tabel pivot adalah alat yang ampuh untuk menganalisis dan merangkum data dalam spreadsheet. Mereka memungkinkan Anda mengelompokkan dan mengkategorikan data untuk mendapatkan wawasan yang berharga. Dalam artikel ini, kita akan mempelajari cara mengelompokkan data secara efektif dalam tabel pivot menggunakan Aspose.Cells untuk Java, beserta contoh kode sumber.

## Perkenalan

Tabel pivot menyediakan cara yang fleksibel untuk mengatur dan meringkas data dari kumpulan data besar. Mereka memungkinkan Anda membuat tampilan khusus data Anda dengan mengelompokkannya ke dalam kategori atau hierarki. Hal ini dapat membantu Anda mengidentifikasi tren, pola, dan outlier dalam data Anda dengan lebih mudah.

## Langkah 1: Buat Tabel Pivot

Mari kita mulai dengan membuat tabel pivot menggunakan Aspose.Cells untuk Java. Di bawah ini adalah contoh cara membuat tabel pivot dari contoh file Excel.

```java
// Muat file Excel
Workbook workbook = new Workbook("sample.xlsx");

// Akses lembar kerja yang berisi data
Worksheet worksheet = workbook.getWorksheets().get(0);

// Tentukan rentang data
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // Dengan asumsi 20 baris data
sourceData.startColumn = 0;
sourceData.endColumn = 3; // Dengan asumsi 4 kolom data

// Buat tabel pivot berdasarkan rentang data
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Dapatkan tabel pivot berdasarkan indeks
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Tambahkan bidang ke baris dan kolom
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Tambahkan nilai dan terapkan agregasi
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Simpan file Excel yang dimodifikasi
workbook.save("output.xlsx");
```

## Langkah 2: Data Grup

 Di Aspose.Cells untuk Java, Anda dapat mengelompokkan data dalam tabel pivot menggunakan`PivotField` kelas. Berikut ini contoh cara mengelompokkan bidang dalam tabel pivot:

```java
// Akses bidang "Produk" di tabel pivot
PivotField productField = pivotTable.getPivotFields().get("Product");

//Kelompokkan bidang "Produk" berdasarkan kriteria tertentu, misalnya berdasarkan huruf awal
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Simpan file Excel yang dimodifikasi dengan data yang dikelompokkan
workbook.save("output_grouped.xlsx");
```

## Langkah 3: Sesuaikan Pengelompokan

Anda dapat mengkustomisasi lebih lanjut pengaturan pengelompokan, seperti menentukan interval pengelompokan berdasarkan tanggal atau aturan pengelompokan khusus. Berikut ini contoh penyesuaian pengelompokan berdasarkan tanggal:

```java
// Akses bidang "Tanggal" di tabel pivot (dengan asumsi itu adalah bidang tanggal)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Kelompokkan tanggal berdasarkan bulan
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Simpan file Excel yang dimodifikasi dengan pengelompokan tanggal khusus
workbook.save("output_custom_grouping.xlsx");
```

## Kesimpulan

Mengelompokkan data dalam tabel pivot adalah teknik berharga untuk menganalisis dan meringkas data di Excel, dan Aspose.Cells untuk Java memudahkan otomatisasi proses ini. Dengan contoh kode sumber yang diberikan, Anda dapat membuat tabel pivot, menyesuaikan pengelompokan, dan mendapatkan wawasan dari data Anda secara efisien.

## FAQ

### 1. Apa tujuan tabel pivot di Excel?

Tabel pivot di Excel digunakan untuk meringkas dan menganalisis kumpulan data besar. Mereka memungkinkan Anda membuat tampilan khusus data Anda, sehingga lebih mudah untuk mengidentifikasi pola dan tren.

### 2. Bagaimana cara menyesuaikan pengelompokan data dalam tabel pivot?

 Anda dapat menyesuaikan pengelompokan data dalam tabel pivot menggunakan`PivotField` kelas di Aspose.Cells untuk Java. Hal ini memungkinkan Anda menentukan kriteria pengelompokan, seperti interval berbasis tanggal atau aturan khusus.

### 3. Bisakah saya mengotomatiskan pembuatan tabel pivot menggunakan Aspose.Cells untuk Java?

Ya, Anda dapat mengotomatiskan pembuatan tabel pivot di Excel menggunakan Aspose.Cells untuk Java, seperti yang ditunjukkan dalam contoh kode sumber yang disediakan.