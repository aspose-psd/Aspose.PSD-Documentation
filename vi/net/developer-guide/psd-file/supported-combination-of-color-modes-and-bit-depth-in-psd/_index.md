---
title: Các Kết Hợp Được Hỗ Trợ của Chế Độ Màu và Độ Sâu Bit trong PSD
type: docs
weight: 80
url: /vi/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Mô tả**
Aspose.PSD hỗ trợ mở các tệp PSD với bất kỳ kết hợp nào của Chế Độ Màu và Độ Sâu Bit trong các tệp Adobe Photoshop PSD. Bạn có thể mở các tệp như vậy và sử dụng API Cấp Thấp để sửa đổi nội dung của tệp. Nhưng đối với một số kết hợp ít phổ biến có thể xuất hiện các vấn đề cụ thể, một số trong số chúng liên quan đến Giới Hạn Chế Độ Màu.

## **Kết hợp xuất được hỗ trợ của Chế Độ Màu và Độ Sâu Bit trong PSD ở chế độ chỉ đọc**

| |Hình ảnh đa bản|Trắng đen|Chỉ mục|RGB|CMYK|Nhiều kênh|Đôi tông|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Độ sâu 1|Có[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Độ sâu 8|-|Có|Có|Có|Có|Không Q3-Q4|Không Q3-Q4|Có[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Độ sâu 16|-|Có|-|Có|Có|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Không (Q3-Q4)|
|Độ sâu 32|-|Có*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Có*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Vấn đề nhỏ trong một số trường hợp

## **Kết hợp xuất được hỗ trợ của Chế Độ Màu và Độ Sâu Bit trong PSD ở chế độ có thể chỉnh sửa**

| |Hình ảnh đa bản|Trắng đen|Chỉ mục|RGB|CMYK|Nhiều kênh|Đôi tông|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Độ sâu 1|Có|-|-|-|-|-|-|-|
|Độ sâu 8|-|Có|Không|Có|Có|Không Q3-Q4|Không Q3-Q4|Có*|
|Độ sâu 16|-|Có|-|Có|Có*|-|-|Không (Q3-Q4)|
|Độ sâu 32|-|Không (Q3-Q4)|-|Không (Q3-Q4)|-|-|-|-|
\* Vấn đề nhỏ trong một số trường hợp

Nếu bạn cần hỗ trợ về Kết Hợp Chế Độ Màu/Độ Sâu Bit cụ thể, bạn có thể đăng bài trên [Diễn Đàn Aspose](https://forum.aspose.com/c/psd)
