---
title: Convert AI to PNG using Java
weight: 100
type: docs
description: Check how Aspose.PSD for Java can convert AI File to PNG.
keywords: [ai to png, ai format, illustrator files, convert illustrator, png, psd api, java, code sample]
url: java/convert/ai-to-png
---

## **Overview**
To convert AI files to PNG format using Aspose.PSD for Java, you can follow these steps:

- Install Aspose.PSD for Java: Begin by downloading and installing the Aspose.PSD library for Java. You can include it as a dependency in your project by adding it to your Maven or Gradle configuration or by manually including the JAR file.

- Import the necessary modules: Once you have added the Aspose.PSD library to your project, import the necessary classes in your Java code. These classes include those required for loading and manipulating AI files, as well as exporting them to PNG format.

- Load and Manipulate AI Files: Utilize the classes provided by Aspose.PSD to load your AI files into your Java application. You can use the Image class to load the AI file and manipulate its contents as needed.

- Export AI to PNG: After loading the AI file, create an instance of the PsdOptions class to specify the settings for the PNG export. This includes parameters such as image quality, compression level, and more. Configure these options according to your requirements.

- Save and Use the PNG: Once you have configured the export options, use the Image.Save method to save the AI file as a PNG. Specify the desired file path where you want to save the resulting PNG file.

- Use the PNG File: After saving the PNG file, you can use it for various purposes, such as sharing, displaying on a webpage, or further processing. The resulting PNG file will contain all the content from the original AI file, converted into the PNG format.

## **Summary**
In summary, using Aspose.PSD for Java, you can seamlessly convert AI files to the PNG format, enabling compatibility with various applications and devices that support PNG. The conversion process entails loading the AI file, configuring export options utilizing the [PngOptions](https://reference.aspose.com/psd/java/com.aspose.psd.imageoptions/pngoptions/), and saving the output as a PNG file using the PsdImage.save method. With Aspose.PSD for Java, you can achieve precise and dependable AI to PNG conversions effortlessly.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-Convert-Ai-To-Png.java" >}}