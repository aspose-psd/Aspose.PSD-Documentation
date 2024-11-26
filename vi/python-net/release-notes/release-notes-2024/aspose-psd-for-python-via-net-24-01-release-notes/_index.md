---
title: Aspose.PSD cho Python via .NET 24.1 - Ghi chú phát hành
type: docs
weight: 10
url: /vi/net/aspose-psd-cho-python-thong-qua-net-24-1-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**     | **Tóm tắt**                                                                                                | **Danh mục**    |
|:--------------|:----------------------------------------------------------------------------------------------------------|:----------------|
|  PSDPYTHON-19 | [Định dạng AI] Thêm xử lý cơ bản cho hình ảnh AI nhiều trang                                             |   Tính năng    |
|  PSDPYTHON-22 | Hiệu ứng Text Warp không áp dụng cho văn bản                                                              |     Lỗi       |
|  PSDPYTHON-23 | Render sai của mặt nạ trong tệp cụ thể                                                                  |     Lỗi       |
|  PSDPYTHON-24 | NullReferenceException tại Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor          |     Lỗi       |
|  PSDPYTHON-25 | [Định dạng AI] Sửa lỗi sử dụng bộ nhớ trong AiExporterUtils                                              |     Lỗi       |



## **Thay đổi API công khai**
# **API Thêm mới:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API đã xóa:**
- Không có


## **Ví dụ sử dụng:**

**PSDPYTHON-19. [Định dạng AI] Thêm xử lý cơ bản cho hình ảnh AI nhiều trang**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Tải hình ảnh AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Theo mặc định, ActivePageIndex là 0.
            # Vì vậy nếu bạn lưu hình ảnh AI mà không thay đổi thuộc tính này, trang đầu tiên sẽ được hiển thị và lưu.
            image.save(firstPageOutputPng, PngOptions())

            # Thay đổi chỉ số trang hoạt động sang trang thứ hai.
            image.active_page_index = 1

            # Lưu trang thứ hai của hình ảnh AI dưới dạng hình ảnh PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Thay đổi chỉ số trang hoạt động sang trang thứ ba.
            image.active_page_index = 2

            # Lưu trang thứ ba của hình ảnh AI dưới dạng hình ảnh PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Hiệu ứng Text Warp không áp dụng cho văn bản**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. Render sai của mặt nạ trong tệp cụ thể**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. NullReferenceException tại Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [Định dạng AI] Sửa lỗi sử dụng bộ nhớ trong AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Việc sử dụng bộ nhớ của C# là 220, nhưng đối với Python, chúng ta không có truy cập trực tiếp đến các hoạt động GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Tải hình ảnh AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Lưu trang đầu tiên của hình ảnh AI dưới dạng hình ảnh PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Thay đổi chỉ số trang hoạt động sang trang thứ hai.
            image.active_page_index = 1

            # Lưu trang thứ hai của hình ảnh AI dưới dạng hình ảnh PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Thay đổi chỉ số trang hoạt động sang trang thứ ba.
            image.active_page_index = 2

            # Lưu trang thứ ba của hình ảnh AI dưới dạng hình ảnh PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Sử dụng bộ nhớ quá lớn. {} thay vì {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}
