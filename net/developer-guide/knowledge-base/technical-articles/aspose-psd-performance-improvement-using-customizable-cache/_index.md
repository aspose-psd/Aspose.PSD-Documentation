---
title: Aspose.PSD Performance Improvement using Customizable Cache
type: docs
weight: 20
url: /net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Improves Performance with Customizable Cache**
Aspose.Images uses caching for temporary data storage. The mechanism is simple to use, customizable and transparent. It ensures that there are no performance issues during image processing. This article explains how to customize the cache with Aspose.PSD API for .NET.
### **Customizing the Cache**
When a process needs temporary data storage, this storage is allocated in the cache. The cache can be space in memory or on disk and is set by the user. When the temporary data is no longer needed, the space is released. The statistics of the allocated space can be inspected at any time. How Aspose.PSD allocates and uses caches can be customized. This section describes the various settings and their defaults and the code snippets below show how they can be used.
### **Setting where the Cache is Allocated**
To customize how cache space is allocated, set the CacheType property. By default, the cache is allocated in memory and when there is no more space available in memory, it is allocated to disk. This behavior is captured by Auto mode. Auto mode is is flexible and maximizes performance. There are also other modes:

- CacheOnDiskOnly mode: allocation to disk only.
- CacheInMemoryOnly mode: allocation to memory only.

Selecting CacheOnDiskOnly mode may result in poor performance.
### **Setting the Size of the Cache**
Set the maximum space (in bytes) that can be allocated on disk or memory by setting the MaxDiskSpaceForCache and MaxMemoryForCache properties respectively. By default, both values are set to 0, meaning that there's no upper limit.
### **Controlling Cache Reallocation**
If there isn't enough space available in memory (as specified by the MaxMemoryForCache property) when a new cache is allocated, the cache is allocated to disk. If there's not enough space on disk, an exception is thrown. The cache allocation process moves from memory to disk but not vice versa. The property ExactReallocateOnly is used to control memory re-allocation. Re-allocation is most likely to occur for pre-allocated caches. It can happen when the system figures out that the allocated space will not be sufficient. If ExactReallocateOnly is set to the default value, False, the space is re-allocated to the same medium. When set to True, re-allocation cannot exceed the maximum specified space. In this case the existing allocated in-memory cache (which requires re-allocation) is freed and extended space is allocated on disk.
### **Program Samples**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}
