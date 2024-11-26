---
title: 通过可自定义缓存提高Aspose.PSD的性能
type: docs
weight: 30
url: /zh/java/aspose-psd-performance-improvement-using-customizable-cache/
---

## **使用可自定义缓存提高性能**
Aspose.PSD使用缓存进行临时数据存储。该机制简单易用、可定制且透明。它确保在图像处理过程中没有性能问题。本文介绍了如何使用Aspose.PSD API为Java自定义缓存。
### **自定义缓存**
当进程需要临时数据存储时，这些数据存储在缓存中。缓存可以是内存中的空间或磁盘上分配的空间，并由用户设置。当临时数据不再需要时，空间将被释放。随时可以检查已分配空间的统计信息。Aspose.PSD如何分配和使用缓存可以进行自定义。本节描述了各种设置及其默认值，下面的代码片段展示了它们的使用方法。
### **设置缓存分配位置**
要自定义缓存空间的分配方式，请设置CacheType属性。默认情况下，缓存分配在内存中，当内存中没有更多空间可用时，会分配到磁盘上。此行为由自动模式捕获。自动模式灵活且可最大化性能。还有其他模式：

- 仅分配到磁盘的CacheOnDiskOnly模式。
- 仅分配到内存的CacheInMemoryOnly模式。

选择CacheOnDiskOnly模式可能导致性能不佳。
### **设置缓存大小**
通过设置MaxDiskSpaceForCache和MaxMemoryForCache属性（以字节为单位），可以设置可以在磁盘或内存中分配的最大空间。默认情况下，这两个值均设置为0，表示没有上限。
### **控制缓存重新分配**
如果内存中没有足够的空间（由MaxMemoryForCache属性指定）来分配新的缓存，缓存将被分配到磁盘。如果磁盘上没有足够的空间，则会引发异常。缓存分配过程会从内存移动到磁盘，但反之则不会。ExactReallocateOnly属性用于控制内存重新分配。重新分配最有可能发生在预分配的缓存上。当系统确定分配的空间不足时，它可能会发生。如果ExactReallocateOnly设置为默认值False，则空间会重新分配到同一介质。当设置为True时，重新分配不能超过指定的最大空间。在这种情况下，已分配的内存缓存（需要重新分配的）会被释放，并在磁盘上分配扩展空间。
### **程序示例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}

