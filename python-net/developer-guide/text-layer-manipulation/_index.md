---
title: Working with Text Layers in Aspose.PSD for Python
weight: 100
type: docs
description: Examples of how to work with Text Layers in PSD File
keywords: [text layer, update text, editing text portions, text style, text paragraph, psd api, python, code sample]
url: python-net/text-layer-manipulation/
---

## **Overview**

**Overview**

Aspose.PSD for Python is a powerful library that allows you to work with PSD (Photoshop Document) files in Python. One of the key features of this library is the ability to edit text layers within PSD files. In this article, we will explore two different methods of editing text in PSD files using Aspose.PSD for Python - the simple way and the more powerful way using text portions.

** Simple Way to Update Text Layer **
To update a text layer in a PSD file using Aspose.PSD for Python, you can use the update_text method of the TextLayer class. This method allows you to easily update the text content of a text layer. Here is an example code snippet that demonstrates the simple way of updating a text layer

	{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-psd-text-layer-manipulation-simple.py" >}}

** Editing using Text Portion **

More Powerful Way to Update Text Layer Using Text Portions: The simple way of updating text layers in PSD files is suitable for basic text editing. However, if you need more control over the styling and formatting of the text, you can use the more powerful method of using text portions. Text portions allow you to specify different styles and paragraphs within the text layer. Here is an example code snippet that demonstrates this method:

	{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-psd-text-layer-manipulation-text-portion.py" >}}

In the above code, we first access the text layer that we want to update (image.layers[1]). We then retrieve the text_data object from the text layer, which allows us to work with the text portions. We create a default_style and default_paragraph object, which will be used as the default style and paragraph for the text portions.

Next, we define the text portions that we want to add to the text layer. Each portion represents a segment of text with its own style and formatting. In this example, we have five text portions - "E=mc", "2\r", "Bold", "Italic\r", and "Lowercasetext". We also update the styles of these portions as per our requirements.

We then iterate over the new portions and add them to the text_data object using the add_portion method. Finally, we call the update_layer_data method of the text_data object to update the text layer with the new text portions.

**Conclusion**
Aspose.PSD for Python provides powerful capabilities for editing text in PSD files. Whether you need to update the text content of a text layer or apply more advanced styling and formatting, Aspose.PSD for Python has you covered. By using the simple way or the more powerful way using text portions, you can easily manipulate text layers in your PSD files.

Please check full example.

## **Example**
	{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-psd-text-layer-manipulation-full.py" >}}