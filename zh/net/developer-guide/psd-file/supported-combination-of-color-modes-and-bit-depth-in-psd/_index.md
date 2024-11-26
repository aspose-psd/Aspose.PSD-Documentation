---
title: 在PSD中支持的色彩模式和位深度组合
type: docs
weight: 80
url: /zh/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **描述**
Aspose.PSD支持在Adobe Photoshop PSD文件中以任何色彩模式和位深度的组合打开PSD文件。您可以打开这些文件并使用低级API来修改文件的内容。但是对于一些不太流行的组合可能会存在特定问题，其中一些与色彩模式限制有关。

## **PSD中受支持的色彩模式和位深度的可导出组合（只读模式）**

| | 位图 | 灰度 | 索引 | RGB | CMYK | 多通道 | 双色调 | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| 深度1 | 是[](https://issue.kharkov.dynabic.com/issues/PSDNET-283) | - | - | - | - | - | - | - |
| 深度8 | - | 是 | 是 | 是 | 是 | 无 Q3-Q4 | 无 Q3-Q4 | 是[](https://issue.kharkov.dynabic.com/issues/PSDNET-290) |
| 深度16 | - | 是 | - | 是 | 是 | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-287) | - | 不支持（Q3-Q4） |
| 深度32 | - | 是*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125) | - | 是* | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-285) | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-288) | - | - |
\* 在某些情况下存在轻微问题

## **PSD中受支持的色彩模式和位深度的可导出组合（可编辑模式）**

| | 位图 | 灰度 | 索引 | RGB | CMYK | 多通道 | 双色调 | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| 深度1 | 是 | - | - | - | - | - | - | - |
| 深度8 | - | 是 | 不支持 | 是 | 是 | 无 Q3-Q4 | 无 Q3-Q4 | 是* |
| 深度16 | - | 是 | - | 是 | 是* | - | - | 不支持（Q3-Q4） |
| 深度32 | - | 不支持（Q3-Q4） | - | 不支持（Q3-Q4） | - | - | - | - |
\* 在某些情况下存在轻微问题

如果您需要特定色彩模式/位深度组合的支持，可以在[Aspose论坛](https://forum.aspose.com/c/psd)上发布。
