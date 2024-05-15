---
title: Aspose.PSD for Python via .NET 24.3 - Release Notes
type: docs
weight: 10
url: /net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**      | **Summary**                                                          | **Category**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI Format] Reduce loading time of large multipage AI images         | Enhancement |
| PSDPYTHON-45 | PSD File after the converting from 8 bit to 16 bit became unreadable |     Bug     |
| PSDPYTHON-46 | PSD File after the converting from 8 bit to 32 bit became unreadable |     Bug     |
| PSDPYTHON-47 | [AI Format] Fix the Short Curve rendering at AI file                 |     Bug     |



## **Public API Changes**
# **Added APIs:**
- None

# **Removed APIs:**
- None


## **Usage examples:**

**PSDPYTHON-42. [AI Format] Reduce loading time of large multipage AI images**

{{< highlight python >}}
   # No sample
{{< /highlight >}}

**PSDPYTHON-45. PSD File after the converting from 8 bit to 16 bit became unreadable**

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
                raise Exception("Wrong global resource, the first resource should be Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. PSD File after the converting from 8 bit to 32 bit became unreadable**


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
                raise Exception("Wrong global resource, the first resource should be Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [AI Format] Fix the Short Curve rendering at AI file**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}