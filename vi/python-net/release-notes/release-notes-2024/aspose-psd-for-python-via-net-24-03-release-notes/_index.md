---
title: Aspose.PSD cho Python via .NET 24.3 - Ghi chú Phát hành
type: docs
weight: 10
url: /vi/net/aspose-psd-cho-python-thong-qua-net-24-3-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Khóa**      | **Tóm tắt**                                                          | **Danh mục**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [Định dạng AI] Giảm thời gian tải của hình ảnh AI nhiều trang lớn   | Cải tiến |
| PSDPYTHON-45 | Tệp PSD sau khi chuyển từ 8 bit thành 16 bit trở nên không đọc được |     Lỗi     |
| PSDPYTHON-46 | Tệp PSD sau khi chuyển từ 8 bit thành 32 bit trở nên không đọc được |     Lỗi     |
| PSDPYTHON-47 | [Định dạng AI] Sửa lỗi hiển thị Đường cong ngắn trong tệp AI       |     Lỗi     |



## **Thay đổi Công khai API**
# **API Thêm vào:**
- Không có

# **API Loại bỏ:**
- Không có


## **Ví dụ sử dụng:**

**PSDPYTHON-42. [Định dạng AI] Giảm thời gian tải của hình ảnh AI nhiều trang lớn**

{{< highlight python >}}
   # Không có mẫu
{{< /highlight >}}

**PSDPYTHON-45. Tệp PSD sau khi chuyển từ 8 bit thành 16 bit trở nên không đọc được**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # is ok
                pass
            else:
                raise Exception("Thông số tài nguyên toàn cầu không đúng, tài nguyên đầu tiên phải là Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Tệp PSD sau khi chuyển từ 8 bit thành 32 bit trở nên không đọc được**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # is ok
                pass
            else:
                raise Exception("Thông số tài nguyên toàn cầu không đúng, tài nguyên đầu tiên phải là Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Định dạng AI] Sửa lỗi hiển thị Đường cong ngắn trong tệp AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
