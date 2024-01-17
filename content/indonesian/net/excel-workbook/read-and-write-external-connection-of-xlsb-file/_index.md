---
title: Baca Dan Tulis Koneksi Eksternal File XLSB
linktitle: Baca Dan Tulis Koneksi Eksternal File XLSB
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara membaca dan memodifikasi koneksi eksternal file XLSB menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 130
url: /id/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Membaca dan menulis koneksi eksternal ke file XLSB sangat penting untuk memanipulasi data dari sumber eksternal di buku kerja Excel Anda. Dengan Aspose.Cells untuk .NET Anda dapat dengan mudah membaca dan menulis koneksi eksternal menggunakan langkah-langkah berikut:

## Langkah 1: Tentukan direktori sumber dan direktori keluaran

Pertama, Anda harus menentukan direktori sumber tempat file XLSB yang berisi koneksi eksternal berada, serta direktori keluaran tempat Anda ingin menyimpan file yang dimodifikasi. Berikut cara melakukannya menggunakan Aspose.Cells:

```csharp
// direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();

// Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
```

## Langkah 2: Muat file sumber Excel XLSB

Selanjutnya, Anda perlu memuat file Excel XLSB sumber tempat Anda ingin melakukan operasi baca dan tulis koneksi eksternal. Berikut ini contoh kodenya:

```csharp
// Muat file sumber Excel XLSB
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Langkah 3: Baca dan ubah koneksi eksternal

Setelah memuat file, Anda dapat mengakses koneksi eksternal pertama yang sebenarnya adalah koneksi database. Anda dapat membaca dan mengubah berbagai properti koneksi eksternal. Begini caranya:

```csharp
// Baca koneksi eksternal pertama yang merupakan koneksi database
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Menampilkan nama koneksi database, perintah, dan informasi koneksi
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Ubah nama koneksi
dbCon.Name = "NewCustomer";
```

## Langkah 4: Simpan file keluaran Excel XLSB

Setelah Anda membuat perubahan yang diperlukan, Anda dapat menyimpan file Excel XLSB yang dimodifikasi ke direktori keluaran yang ditentukan. Berikut cara melakukannya:

```csharp
// Simpan file keluaran Excel XLSB
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Contoh kode sumber untuk Baca Dan Tulis Koneksi Eksternal File XLSB menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
//Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
//Muat file sumber Excel Xlsb
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Baca koneksi eksternal pertama yang sebenarnya adalah DB-Connection
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Cetak Nama, Perintah dan Info Koneksi DB-Connection
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Ubah Nama Koneksi
dbCon.Name = "NewCust";
//Simpan file Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Kesimpulan

Membaca dan menulis koneksi eksternal ke file XLSB memungkinkan Anda memanipulasi data dari sumber eksternal di buku kerja Excel Anda. Dengan Aspose.Cells untuk .NET, Anda dapat dengan mudah mengakses koneksi eksternal, membaca dan mengubah informasi koneksi, dan menyimpan perubahan. Bereksperimenlah dengan file XLSB Anda sendiri dan manfaatkan kekuatan koneksi eksternal di aplikasi Excel Anda.

### FAQ

#### T: Apa yang dimaksud dengan koneksi eksternal dalam file XLSB?
    
J: Koneksi eksternal dalam file XLSB mengacu pada koneksi yang dibuat dengan sumber data eksternal seperti database. Ini memungkinkan Anda mengimpor data dari sumber eksternal ini ke buku kerja Excel.

#### T: Bisakah saya memiliki beberapa koneksi eksternal dalam satu file XLSB?
     
J: Ya, Anda dapat memiliki beberapa koneksi eksternal dalam file XLSB. Anda dapat mengelolanya satu per satu dengan mengakses setiap objek koneksi.

#### T: Bagaimana cara membaca detail koneksi eksternal dalam file XLSB dengan Aspose.Cells?
     
J: Anda dapat menggunakan fungsionalitas yang disediakan oleh Aspose.Cells untuk mengakses properti koneksi eksternal, seperti nama koneksi, perintah terkait, dan informasi koneksi.

#### T: Apakah mungkin untuk mengubah koneksi eksternal dalam file XLSB dengan Aspose.Cells?
     
J: Ya, Anda dapat mengubah properti koneksi eksternal, seperti nama koneksi, untuk memenuhi kebutuhan spesifik Anda. Aspose.Cells menyediakan metode untuk melakukan perubahan ini.

#### T: Bagaimana cara menyimpan perubahan yang dibuat pada koneksi eksternal ke file XLSB dengan Aspose.Cells?
     
J: Setelah Anda membuat perubahan yang diperlukan pada koneksi eksternal, Anda cukup menyimpan file Excel XLSB yang dimodifikasi menggunakan metode yang sesuai yang disediakan oleh Aspose.Cells.