---
title: Thêm tiện ích mở rộng web
linktitle: Thêm tiện ích mở rộng web
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng thêm tiện ích mở rộng web vào sổ làm việc Excel của bạn với Aspose.Cells for .NET.
type: docs
weight: 40
url: /vi/net/excel-workbook/add-web-extension/
---
Trong hướng dẫn từng bước này, chúng tôi sẽ giải thích mã nguồn C# được cung cấp để cho phép bạn thêm tiện ích mở rộng web bằng Aspose.Cells cho .NET. Hãy làm theo các bước bên dưới để thêm tiện ích mở rộng web vào sổ làm việc Excel của bạn.

## Bước 1: Đặt thư mục đầu ra

```csharp
// Thư mục đầu ra
string outDir = RunExamples.Get_OutputDirectory();
```

Trong bước đầu tiên này, chúng tôi xác định thư mục đầu ra nơi sổ làm việc Excel đã sửa đổi sẽ được lưu.

## Bước 2: Tạo một bảng tính mới

```csharp
// Tạo một sổ làm việc mới
Workbook workbook = new Workbook();
```

Ở đây chúng ta đang tạo một sổ làm việc Excel mới bằng cách sử dụng`Workbook` lớp từ Aspose.Cells.

## Bước 3: Truy cập Bộ sưu tập tiện ích mở rộng web

```csharp
// Truy cập bộ sưu tập tiện ích mở rộng web
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Chúng tôi truy cập bộ sưu tập tiện ích mở rộng web của sổ làm việc Excel bằng cách sử dụng`WebExtensions` tài sản của`Worksheets` sự vật.

## Bước 4: Thêm tiện ích mở rộng web mới

```csharp
// Thêm tiện ích mở rộng web mới
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Chúng tôi đang thêm tiện ích mở rộng web mới vào bộ sưu tập tiện ích mở rộng. Chúng tôi xác định ID tham chiếu, tên cửa hàng và loại cửa hàng của tiện ích mở rộng.

## Bước 5: Truy cập Bộ sưu tập ngăn tác vụ mở rộng web

```csharp
// Truy cập bộ sưu tập ngăn tác vụ của tiện ích mở rộng web
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Chúng tôi truy cập vào bộ sưu tập các ngăn tác vụ của Excel Workbook Web Extension bằng cách sử dụng`WebExtensionTaskPanes` tài sản của`Worksheets` sự vật.

## Bước 6: Thêm ngăn tác vụ mới

```csharp
// Thêm một ngăn tác vụ mới
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Chúng tôi đang thêm một ngăn tác vụ mới vào bộ sưu tập ngăn tác vụ. Chúng tôi đặt chế độ hiển thị của ngăn, trạng thái gắn đế của ngăn và tiện ích mở rộng web được liên kết.

## Bước 7: Lưu và đóng sổ làm việc

```csharp
// Lưu và đóng sổ làm việc
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Chúng tôi lưu sổ làm việc đã sửa đổi vào thư mục đầu ra đã chỉ định rồi đóng nó lại.

### Mã nguồn mẫu cho Thêm tiện ích mở rộng web bằng Aspose.Cells cho .NET 
```csharp
//Thư mục nguồn
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách thêm tiện ích mở rộng web bằng Aspose.Cells cho .NET. Thử nghiệm mã và khám phá các tính năng bổ sung của Aspose.Cells để tận dụng tối đa thao tác tiện ích mở rộng web trong sổ làm việc Excel của bạn.

## Câu hỏi thường gặp

#### Hỏi: Tiện ích mở rộng web trong sổ làm việc Excel là gì?

Đáp: Phần mở rộng web trong sổ làm việc Excel là một thành phần cho phép bạn thêm chức năng bổ sung vào Excel bằng cách tích hợp các ứng dụng web. Nó có thể cung cấp các tính năng tương tác, bảng điều khiển tùy chỉnh, tích hợp bên ngoài, v.v.

#### Hỏi: Làm cách nào để thêm tiện ích mở rộng web vào sổ làm việc Excel bằng Aspose.Cells?

 Trả lời: Để thêm tiện ích mở rộng web vào sổ làm việc Excel bằng Aspose.Cells, bạn có thể làm theo các bước được cung cấp trong hướng dẫn từng bước của chúng tôi. Sử dụng`WebExtensionCollection` Và`WebExtensionTaskPaneCollection` các lớp để thêm và định cấu hình tiện ích mở rộng web cũng như ngăn tác vụ liên quan.

#### Hỏi: Cần có thông tin gì để thêm tiện ích mở rộng web?

Trả lời: Khi thêm tiện ích mở rộng web, bạn phải cung cấp ID SKU tiện ích mở rộng, tên cửa hàng và loại cửa hàng. Thông tin này giúp xác định và tải tiện ích mở rộng một cách chính xác.

#### Hỏi: Tôi có thể thêm nhiều tiện ích mở rộng web vào một sổ làm việc Excel không?

 Đáp: Có, bạn có thể thêm nhiều Tiện ích mở rộng Web vào một sổ làm việc Excel. Sử dụng`Add` của bộ sưu tập tiện ích mở rộng web để thêm từng tiện ích mở rộng, sau đó liên kết chúng với các ngăn tác vụ tương ứng.