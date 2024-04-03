---
title: Aspose.PSD Adapters for .NET Full Manual
type: docs
weight: 10
url: /net/adapters/full-manual
keywords: Adapters Full Manual PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP quick start quide
description: Aspose.PSD Adapters Full Manual.
---

## Overview

This is a full manual of how to work with Aspose.PSD adapters to widen Aspose.PSD Capabilities.
Adapters are the special Nuget Packages that enable seamless integration of Aspose.PSD with other Aspose products, empowering you to export your files to various unsupported formats effortlessly, without additional integration code writing .

## Applying of licenses

Please check Full [article about applying licenses](/psd/net/adapters/license) for adapters.

{{% alert color="primary" %}} 
Please note, to use Adapters you both Aspose.PSD and adaptees Licenses. 
{{% /alert %}} 

License can be applied using this sample:
{{< gist "dimsa" "dc26f93541d2b7c3872d4873d7da72af" "Aspose-PSD-Adapters-CSharp-License.cs" >}}

It's better to apply license once in the initializing module of your Project

## Reference Aspose.PSD Adapters

Firstly you need to reference Aspose.PSD.Adapters.Imaging from [Nuget](https://www.nuget.org/aspose.psd.adapters.imaging) or download them from [Aspose Release Page](https://releases.aspose.com/psd/net/)(Adapters are included in the main release artifact at this moment as the separate binary) to your project.

![Necessary references](references.png)

It's possible that you also will be needed to reference other additional packages


## Enabling Loaders and Exportes of adaptees

### Enabling of adapters
When you need to use adapters just use the following code:
{{< gist "dimsa" "dc26f93541d2b7c3872d4873d7da72af" "Adapters-CSharp-Enable-Adapters.cs" >}}
 
 
### Disabling of adapters
 In the process of developement you can face situation when Adapters should be disabled. This common case if you need in one code part to use Aspose.PSD loaders and use Adaptees' Loaders in other one. In this case just use the following code:
{{< gist "dimsa" "dc26f93541d2b7c3872d4873d7da72af" "Adapters-CSharp-Disable-Adapters.cs " >}}

## Loading of Images using Adapters

Using adapters you can [load popular non-supported by Aspose.PSD formats]((/net/adapters/load-unsupported-formats)) like SVG or WebP.

### Simple using
Just use the following code for loading:
{{< gist "dimsa" "dc26f93541d2b7c3872d4873d7da72af" "Adapters-CSharp-Add-Imaging-Adapters-Loading-Unsupported-Formats.cs" >}}

### Intermediate usage for the complex Image Processing
If you need to specify additional options that are provided by Adaptee, please check the following example:
{{< gist "dimsa" "dc26f93541d2b7c3872d4873d7da72af" "Aspose-PSD-Adapters-CSharp-Full-Manual-Complex-Loading.cs" >}}

You can work with SVG image using all Imaging features, and then export it with one method call.

## Exporting of Images using Adapters

There are many situations when you need not to [open unsupported format](/net/adapters/load-unsupported-formats), but [export to it](/net/adapters/export-to-unsupported-formats). In this cases you should enable exporters and use the following code:
{{< gist "dimsa" "dc26f93541d2b7c3872d4873d7da72af" "Adapters-CSharp-Add-Imaging-Adapters-Exporting-to-Unsupported-Formats.cs" >}}

## Conclusion

Using Aspose.PSD Adapters for loading and exporting files is a game-changer for developers. These powerful Nuget Packages allow for seamless integration of Aspose.PSD with other Aspose products, making it easier than ever to open and work with unsupported file formats without writing of additional integration code. With Aspose.PSD Adapters, you can save time and effort by eliminating the need for extra code and manual conversion processes. Whether you are loading or exporting files, Aspose.PSD Adapters provide a convenient and efficient solution that opens up new possibilities for your projects. Experience the power of Aspose.PSD Adapters and take your development process to the next level.