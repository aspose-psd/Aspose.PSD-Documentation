---
title: 使用可定制缓存改进Aspose.PSD性能
type: docs
weight: 20
url: /zh/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **使用可定制缓存改进性能**
[Aspose.PSD](https://products.aspose.com/psd/family) 使用缓存进行临时数据存储。该机制简单易用，可定制且透明。它确保在图像处理过程中没有性能问题。本文解释了如何使用Aspose.PSD API为.NET定制缓存。
### **自定义缓存**
当一个过程需要临时数据存储时，该存储空间分配在缓存中。缓存可以是内存中的空间或者磁盘上的空间，由用户设置。当临时数据不再需要时，该空间被释放。可以随时检查分配的空间的统计信息。如何分配和使用缓存可以进行定制。本节描述了各种设置及其默认值，并下面的代码片段展示了如何使用它们。
### **设置缓存分配位置**
要自定义如何分配缓存空间，请设置[CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype)属性。默认情况下，缓存分配在内存中，当内存中没有更多空间可用时，将分配到磁盘。这种行为由“Auto”模式捕获。Auto模式灵活且能最大化性能。还有其他模式:

- CacheOnDiskOnly模式：仅分配到磁盘。
- CacheInMemoryOnly模式：仅分配到内存。

选择CacheOnDiskOnly模式可能导致性能不佳。
### **设置缓存的大小**
通过设置[MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache)和[MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache)属性，设置可以分配在磁盘上或内存中的最大空间（以字节为单位）。默认情况下，这两个值均设置为0，表示没有上限。
### **控制缓存重新分配**
如果在分配新缓存时内存中没有足够的空间（由MaxMemoryForCache属性指定），则将缓存分配到磁盘。如果磁盘上没有足够的空间，将引发异常。缓存分配过程从内存移动到磁盘，但反之则不然。属性[ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly)用于控制内存重新分配。重新分配最可能发生在预分配的缓存中。当系统确定分配的空间不足时，它可能会发生。如果ExactReallocateOnly设置为默认值False，则空间会重新分配到同一介质。当设置为True时，重新分配不会超过指定的最大空间。在这种情况下，将释放已分配在内存中的缓存（需要重新分配）并在磁盘上分配扩展空间。
### **程序示例**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}

