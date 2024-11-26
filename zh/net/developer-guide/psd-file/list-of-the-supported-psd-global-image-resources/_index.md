---
title: 支持的PSD全局图像资源列表
type: docs
weight: 30
url: /zh/net/list-of-the-supported-psd-global-image-resources/
---

## **Aspose.PSD支持图像资源的低级编辑。**
完全支持的图像资源列表，您可以在Aspose.PSD .Net [API 参考](https://reference.aspose.com/psd/net)中找到。

根据Adobe® Photoshop®格式规范：图像资源使用几个标准ID编号，如图像资源ID中所示。并非所有文件格式都使用所有ID。一些信息可能存储在文件的其他部分中。

对于自Photoshop 3.0以来已添加的资源ID，条目将指示它们被引入的版本，例如（*Photoshop 6.0)*。

图像资源ID。

|**ID**|**描述**|
| :- | :- |
|**十进制**|||
|1000|*(已弃用 - 仅Photoshop 2.0)* 通道数、行数、列数、深度和模式|
|1001|Macintosh打印管理器打印信息记录|
|1002|Macintosh页面格式信息。 不再被Photoshop读取。 *(已弃用)*|
|1003|*(已弃用 - 仅Photoshop 2.0)* 索引颜色表|
|1005|[ResolutionInfo 结构](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource)。|
|1006|Alpha通道名称，作为一系列Pascal字符串。|
|1007|*(已弃用) 请参阅ID 1077 DisplayInfo* 结构。|
|1008|作为Pascal字符串的标题。|
|1009|[边框信息。](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource) 包含固定数量（2字节实数，2字节分数）的边框宽度，和2字节边框单位（1 = 英寸，2 = 厘米，3 = 点，4 = 磅，5 = 列）。|
|1010|[背景颜色。](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|打印标志。 一系列一字节布尔值：标签、裁剪标记、彩色条、注册标记、底片、翻转、插值、标题、打印标志。|
|1012|灰度和多通道半色调信息|
|1013|[颜色半色调信息](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|双色调半色调信息|
|1015|灰度和多通道传输函数|
|1016|[颜色传输函数](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|双色调传输函数|
|1018|双色调图像信息|
|1019|点范围的有效黑白值的两个字节|
|1020|*(已弃用)*|
|1021|EPS选项|
|1022|[快速蒙版信息](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource)。 快速蒙版通道ID；1字节布尔值，指示蒙版最初是否为空。|
|1023|*(已弃用)*|
|1024|[图层状态信息](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource)。|
|1025|工作路径（未保存）。路径资源格式。|
|1026|[图层组信息](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource)。 每个图层的2字节，包含用于拖动组的组ID。 组中的图层具有相同的组ID。|
|1027|*(已弃用)*|
|1028|IPTC-NAA记录。 包含*文件信息...*信息。|
|1029|原始格式文件的图像模式|
|1030|JPEG质量。 私有。|
|1032|*(Photoshop 4.0) [网格和指南信息。](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0)* 只有[缩略图资源](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[供 Photoshop 4.0使用](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)*|
|1034|*(Photoshop 4.0)* 版权标志。 布尔值，指示图像是否受版权保护。|
|1035|*(Photoshop 4.0)* URL。 一个具有统一资源定位符的文本字符串的句柄。|
|1036|*(Photoshop 5.0)* [缩略图资源](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)*（取代资源1033）。|
|1037|*(Photoshop 5.0)* [全局角度](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*。 包含0到359之间的整数的4字节，是用于效果图层的全局照射角度。如果不存在，假定为30。|
|1038|*(已弃用) 请参阅下面的ID 1073。（Photoshop 5.0）* 色标资源。|
|1039|*(Photoshop 5.0)* [ICC配置文件](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*。 一个ICC（国际色彩协会）格式配置文件的原始字节。|
|1040|*(Photoshop 5.0)* [水印](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*。|
|1041|*(Photoshop 5.0)* [ICC未标记配置文件](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*。 一个字节，用于在打开文件时禁用任何假定的配置文件处理。 1 = 故意未标记。|
|1042|*(Photoshop 5.0)* 显示效果。 1字节全局标志用于显示/隐藏所有效果图层。 仅在它们被隐藏时显示。|
|1043|*(Photoshop 5.0)* 点位半色调。 版本占4个字节，长度占4个字节，以及可变长度数据。|
|1044|*(Photoshop 5.0)* [文档特定ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* 种子号码。 4字节：基值，开始时将生成层ID的值（或者更大的值，如果现有ID已超过它）。 它的目的是避免我们添加图层、平坦化、保存、打开，然后添加更多图层最终将与第一组相同的ID。|
|1045|*(Photoshop 5.0)* [Unicode Alpha名称](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*。|
|1046|*(Photoshop 6.0)* 索引颜色表计数。 2字节用于实际定义颜色数的表中的颜色数|
|1047|*(Photoshop 6.0)* [透明度索引](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource)。|
|1049|*(Photoshop 6.0)* [全局海拔。](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* 切片。|
|1051|*(Photoshop 6.0)* 工作流URL。|
|1052|*(Photoshop 6.0)* 跳转到XPEP。 2字节主要版本，2字节次要版本，4字节计数。接下来是为每个计数重复的内容：4字节块大小，4字节键，如果键 =*'jtDd'* ，则下一个是用于脏标志的布尔值；否则是用于修改日期的4字节条目。|
|1053|*(Photoshop 6.0)* Alpha标识符。|
|1054|*(Photoshop 6.0)* [URL 列表](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*。|
|1057|*(Photoshop 6.0)* [版本信息](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource)。|
|1058|*(Photoshop 7.0)* EXIF数据1。|
|1059|*(Photoshop 7.0)* EXIF数据3。|
|1060|*(Photoshop 7.0)* [XMP元数据](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource)。 文件信息作为XML描述。|
|1061|*(Photoshop 7.0)* [标题摘要](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)。 16字节：RSA数据安全，MD5消息摘要算法|
|1062|*(Photoshop 7.0)* [打印比例](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)。 （0 = 居中，1 = 按比例缩放，2 = 用户定义）。 4字节x位置（浮点）。 4字节y位置（浮点）。 4字节缩放（浮点）。|
|1064|*(Photoshop CS)* [像素宽高比](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource)。|
|1065|*(Photoshop CS)* 图层组。|
|1066|*(Photoshop CS)* 另类双色调颜色。 该资源不被Photoshop读取或使用。|
|1067|*(Photoshop CS)* 另类专色。 该资源不被Photoshop读取或使用。|
|1069|*(Photoshop CS2)* [图层选择ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerselectionidsresource) (s)。 2字节计数，对每个计数重复：4字节图层ID。|
|1070|*(Photoshop CS2)* HDR调色信息。|
|1071|*(Photoshop CS2)* 打印信息。|
|1072|*(Photoshop CS2)* [已启用图层组ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource)。 文档中每个图层的1字节，由资源长度重复。 注意：图层组有开始和结束标记。|
|1073|*(Photoshop CS3)* 色标资源。 也请参阅1038号旧格式。|
|1074|*(Photoshop CS3)* 测量比例。|
|1075|*(Photoshop CS3)* 时间轴信息。|
|1076|*(Photoshop CS3)* 工作表公开。|
|1077|*(Photoshop CS3)* DisplayInfo结构，支持浮点颜色。 也请参阅ID 1007。|
|1078|*(Photoshop CS3)* 葱皮。|
|1080|*(Photoshop CS4)* 计数信息。|
|1082|*(Photoshop CS5)* 打印信息。|
|1083|*(Photoshop CS5)* 打印样式。 打印标记、标签、装饰等。|
|1084|*(Photoshop CS5)* Macintosh NSPrintInfo。 针对Macintosh的变量OS特定信息。|
|1085|*(Photoshop CS5)* Windows DEVMODE。 针对Windows的变量OS特定信息。|
|1086|*(Photoshop CS6)* 自动保存文件路径。|
|1087|*(Photoshop CS6)* 自动保存格式。|
|1088|*(Photoshop CC)* 路径选择状态。|
|2000-2997|路径信息（保存的路径）。|
|2999|裁剪路径的名称。|
|3000|*(Photoshop CC)* 原始路径信息。|
|4000-4999|插件资源。由插件添加的资源。|
|7000|Image Ready变量。 变量定义的XML表示|
|7001|Image Ready数据集|
|7002|Image Ready默认选择状态|
|7003|Image Ready 7鼠标悬停展开状态|
|7004|Image Ready鼠标悬停展开状态|
|7005|Image Ready保存图层设置|
|7006|Image Ready版本|
|8000|*(Photoshop CS3)* Lightroom工作流，如果存在，则文档处于Lightroom工作流的中间。|
|10000|[打印标志信息](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printflagsresource)。|

Aspose.PSD支持其中一些资源。如果资源没有自己的类，则可以使用[UnknownResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unknownresource)从Aspose.PSD API 参考中使用。

PSD全局图像资源可用于各种情况。您可以获取特定的低级数据，在Adobe Photoshop中无法获得。

此外，欢迎报告您需要的图像资源。[Aspose PSD论坛](https://forum.aspose.com/c/psd) 可以提供帮助。