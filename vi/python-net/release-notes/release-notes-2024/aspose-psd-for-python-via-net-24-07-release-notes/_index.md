---
title: Aspose.PSD cho Python via .NET 24.7 - Ghi chú phát hành
type: docs
weight: 10
url: /vi/python-net/aspose-psd-cho-python-thong-qua-net-24-7-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                                              | **Danh mục** |
|:-------------|:---------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Ngoại lệ "Load hình ảnh thất bại." khi mở tài liệu AI                                             | Lỗi      |
| PSDPYTHON-87 | Văn bản hiển thị không đúng trong tệp PDF đầu ra                                                 | Lỗi      |
| PSDPYTHON-88 | Sửa lỗi ImageSaveException: Xuất hình ảnh thất bại cho tệp cụ thể trên Linux                  | Lỗi      |
| PSDPYTHON-89 | Sửa lỗi tải phông chữ khi sử dụng Aspose.Drawing                                                | Lỗi      |
| PSDPYTHON-90 | 'Phép toán số học dẫn đến tràn số' khi tạo lớp lớp smart object bằng hình JPEG lớn         | Lỗi      |
| PSDPYTHON-91 | Tệp AI không thể được chuyển đổi thành tệp JPG                                                 | Lỗi      |

## **Thay Đổi API Công Khai**
# **API Đã Thêm:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API Đã Xóa:**
- Không có

## **Ví dụ về cách sử dụng:**

**PSDPYTHON-86. Ngoại lệ "Load hình ảnh thất bại." khi mở tài liệu AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Văn bản hiển thị không đúng trong tệp PDF đầu ra**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Sửa lỗi ImageSaveException: Xuất hình ảnh thất bại cho tệp cụ thể trên Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Sửa lỗi tải phông chữ khi sử dụng Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Trước khi cập nhật. Số lượng phông chữ đã cài đặt: " + str(len(installedFonts.families)))
            print("- Làm mới bộ nhớ cache phông chữ bằng cách thử lấy tên phông chữ Adobe cho 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Sau khi cập nhật. Số lượng phông chữ đã cài đặt: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Phép toán số học dẫn đến tràn số' khi tạo lớp smart object bằng hình JPEG lớn**
{{< highlight python >}}
        # Sửa lỗi đã được thực hiện, nhưng vẫn còn vấn đề khác trong Aspose.PSD cho Python hạn chế thử nghiệm này
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Lớp Thử Nghiệm"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. Tệp AI không thể được chuyển đổi thành tệp JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}
