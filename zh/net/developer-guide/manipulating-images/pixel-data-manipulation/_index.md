---
title: 使用 Aspose.PSD 在 C# 中进行像素数据操作
weight: 100
type: docs
description: 通过 PSD C# API 直接快速更新原始像素数据的示例
keywords: [编辑像素, 编辑 PSD, 编辑图层, 原始数据操作, 编辑 PSD 数据, psd api, C#, csharp, 代码示例]
url: /zh/pixel-data-manipulation/
---

## 简介

Aspose.PSD 是一个强大的库，允许您在 C# 中处理 Adobe Photoshop 文件（PSD）。在本文中，我们将探讨如何使用 Aspose.PSD for C# 操作 PSD 文件中的像素数据。

## 概述

提供的代码演示了如何创建一个 PSD 文件，添加一个新图层，直接操作像素数据，并保存修改后的图像。

### 操作像素数据的步骤

1. **导入所需模块**：
   导入必要的模块。您需要从 Aspose.PSD 库中导入 `PsdImage` 和 `Layer` 类。

2. **定义输入和输出文件路径**：
   指定输入和输出文件路径。

3. **打开输入文件流**：
   使用 `FileStream` 类以只读模式打开输入文件流。通过加载流创建一个 `PsdImage` 对象。

4. **创建新的 PSD 图像**：
   使用 `PsdImage` 构造函数创建一个新的 PSD 图像，并提供图层的宽度和高度作为参数。

5. **将图层分配给 PSD 图像**：
   将图层分配给 PSD 图像的 `Layers` 属性。

6. **操作像素数据**：
   使用 `LoadArgb32Pixels` 方法从图层加载 ARGB32 像素。根据像素数组的长度定义索引范围，并根据需要修改像素值。

7. **保存修改后的像素数据**：
   使用 `SaveArgb32Pixels` 方法将修改后的像素数据保存回图层。

8. **保存 PSD 图像**：
   使用 `Save` 方法将 PSD 图像保存到输出文件。

### 示例

以下是一个演示如何使用 Aspose.PSD for C# 操作像素数据的代码示例：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### 总结

Aspose.PSD for C# 提供了一组强大的功能，可用于操作 PSD 文件中的像素数据。无论您需要根据特定条件修改像素还是创建复杂的图案，Aspose.PSD 都可以使这些任务变得简单高效。

有关更详细信息和示例，请访问[Aspose.PSD for C# 文档](https://docs.aspose.com/psd/net/)。
