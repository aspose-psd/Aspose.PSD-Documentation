---
title: Raw Data Processing
type: docs
weight: 50
url: /net/raw-data-processing/
---

## **Raw Data Processing**
To improve the Aspose.PSD API's performance we introduced a method for raw data processing with version 2.4.0. The raw data processing is now used internally and has an external API so it can be used from outside the library to improve the overall performance. Sometimes the processing gets a little tricky and needs some explanation. Raw data processing is currently available for BMP format only.

To help developers get the best performance, the Aspose.PSD API provides a raw data processing system which has an external API for customization. Developers call the LoadRawData and SaveRawData method family to use raw data processing. These methods also require the desired raw data format to be set using the RawDataSettings class. The RawDataSettings class allows developers to specify any raw data format. However, to achieve the best performance you need to use the raw data format the data is stored in. The RawDataSettings defined in the RasterImage class helps determine the image's raw data format. When passing the RawDataSettings instance into the LoadRawData method the data is returned as it is, without any conversion applied, and may improve performance. On the opposite side, you need to take care of all possible raw data formats layout which may be sometimes a bit complicated.

To simplify the handling process, at cost of some performance penalty, you may specify the desired RawDataSettings by instantiating and initializing the class with the desired raw data settings. There are cases when it is not possible to return the raw data in the specified format (for example conversion from CMYK color space to RGB is not available in version 2.4.0). Moreover, there could be scenarios when raw data processing is not available at all for an image format. In order to determine if you can use the LoadRawData and SaveRawData methods family you need to query the IsRawDataAvailable property.
### **Insight**
For RGB pixel data format there are indexed (palette-based) and RGB based raw data formats available. Indexed raw data formats contain palette entry indexes in the 0..(2^bis count – 1) range. The indexed raw data formats are 1, 2, 4 and 8 bits per pixel. The rest are RGB based raw data formats. When loading raw data, take care that there are enough bytes available to load the data, otherwise an appropriate exception will be thrown. You may simply estimate the byte array size by multiplying the line size by the lines required. The line size may vary and depends on the raw data storage format.

To achieve the best performance always use a raw data line size equal to the RasterImage.RawLineSize property value. However, sometimes you may need to add additional padding to the raw data rows, or reduce it, and when this is the case a different line size may be used. If a subset of an image bounding rectangle is required, then take into account the bit shifts which may occur for indexed RGB pixel formats. For example, let's consider an image with the dimensions 100x100 pixels and 1 bit per pixel raw data format. You want to load a raw data rectangle with the location (7,0) and (2,1) dimensions, or in the other words, you requires 2 pixels starting from x=7 and y=0. In this case, you should receive the following data layout:



![todo:image_alt_text](raw-data-processing_1.png)

This means that you receive 2 bytes where the first byte contains 7 undesired pixels, then 1 desired pixel, and the second byte contains 1 desired pixel and then 7 undesired ones. You may ask why we haven't performed data shift and put those 2 pixels into single byte? The answer is simple: to keep performance high. All internal processing is typically performed with all data starting from the first pixel and ending with the last available pixel. There are rare situations when a pixel subset is required. Besides, we have no idea how those pixels will be processed afterwards so shift will lower performance and make the code unnecessarily complex. Always estimate the right bit (no need to determine the right byte since the data always comes with the first byte filled) where the demanded pixels will start. To calculate the right bit a simple formula may be used: (rect.Left * bitsCount) % 8.
### **Indexed RGB Color Conversion**
To get the highest performance possible, always use the same source and destination raw data settings, pixel formats and line sizes. However, sometimes you may need to perform data conversion. For example you may load a 1 bit per pixel RGB image and save it with 2 bits per pixel, or load a 4 bit RGB image and downgrade its color range to 2 bits per pixel. In either case, a color conversion should be applied. Converting an indexed RGB images can be sometimes tricky and cannot be performed without some settings applied. We need to determine how the source color range is mapped to the target color space. To accomplish this task we have dofferent modes:

- Palette mapping (DitheringMethods.PaletteConversion)
- Raw data mapping (DitheringMethods.PaletteIgnore)
- Custom conversion (DitheringMethods.CustomConverter)

When palette conversion is used, the source color space tries to match the target color space as close as possible. For example let's assume we have a 4 bit image with the following colors:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

The source image looks like the following:



![todo:image_alt_text](raw-data-processing_2.png)

And we convert the 4 bit image to the 1 bit image with the following palette colors defined:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

In palette conversion mode the converter reads the source color and determines the target index using the target palette's GetNearestColorIndex method. The RasterImage.RawFallbackIndex property value is used in case the palette's GetNearestColorIndex method gives an out of range index. This converts the source colors to the closest target colors in terms of intensity values. The target image matches the source image as close as possible. You can see the following result:



![todo:image_alt_text](raw-data-processing_3.png)

In raw data mapping mode a different scenario is used. The source and target color palettes are simply ignored and the source indexes are mapped onto destination indexes. When a value is found which cannot be mapped into target range (when lowering bits count) then the RasterImage.RawFallbackIndex property value is used. The value is 0 by default and will be mapped to the first color in the destination palette. If this property value lies outside the destination range, an appropriate exception is thrown. This leads to less predictable results which can be shown on the following image:



![todo:image_alt_text](raw-data-processing_4.png)

The palette conversion mode is a more correct solution for the color mapping issue but it also takes a little more time to complete since calculations need to be performed to estimate the correct palettes mapping. (Typically there is a very small performance difference between the two methods.) On the other hand, raw mapping mode performs a little faster and may be used for more rough color conversion when exact color mapping is not so important. For example, there are cases when the source color palette is trimmed and may be safely converted to lesser bit counts since the extra bits have not been used anyway.

To use any of the these approaches, use the RasterImage class' RawDitheringMethod property. By default, it is set to the palette conversion method to achieve the best looking results. You can change this property before any conversion takes place (when saving image to stream for example). Please note that the palette ignore and palette conversion dithering methods will not take place if you have loaded an image and rewritten some of the original pixel data since the new data goes into cache and the cache stores the data in the maximal available format 32ARGB (as of 2.4.0, subject to change). This format is used to overcome issues with possible different color ranges for loaded and saved images. Furthermore the palette ignore and palette conversion dithering methods will be ignored when an image is loaded in RGB mode and converted to indexed mode or vice versa.
### **Custom Color Converters**
Sometimes it is not sufficient to use the standard approach for color conversion. You may want to use a custom algorithm to get complete freedom when using color conversion routines. When the source and target images pixel formats are both indexed RGB formats a simpler interface, IIndexedColorConverter, may be used. You need to set the RasterImage.RawIndexedColorConverter property to an instance of the IIndexedColorConverter interface and use the DitheringMethods.CustomConverter for the RawDitheringMethod property value. When this combination is implied then any indexed color conversion goes through that specified IIndexedColorConverter instance. The custom indexed color converter has the following method defined:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



The FillIndexedtoIndexedMap method is called when conversion is required from indexed RGB image to indexed RGB image format (when any of the 1,2,4 or 8 bits count are converted to each other). The map array has the length of all possible source format entries count. You need to fill that array to mapping from source color palette entry to destination palette entry. Take care that the destination index value is in the 0..(bits count - 1) range, or an appropriate exception is thrown.

If the requirement is to perform a more custom color conversion scenario then the RasterImage.RawCustomColorConverter property should be set to an instance of the IColorConverter interface. The RawCustomColorConverter property always overrides the RawIndexedColorConverter property if both of them are set and an indexed color converter will not be used in such a case. The IColorConverter has a single method:



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}



The Convert method is called each time color conversion is required. The method receives the source raw data in the source format and has an output buffer to receive the color format converted to the destination. The destination buffer should be sufficient to receive the converted data (if the interface call is made internally by the Aspose.PSD library) and should contain the converted raw data upon the method return. The Convert method may be called several times until the whole source data is covered.
