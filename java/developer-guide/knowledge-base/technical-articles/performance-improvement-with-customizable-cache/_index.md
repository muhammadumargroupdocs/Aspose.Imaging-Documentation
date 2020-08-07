---
title: Performance Improvement with Customizable Cache
type: docs
weight: 20
url: /java/performance-improvement-with-customizable-cache/
---

{{% alert color="primary" %}} 

Aspose.Images uses caching for temporary data storage. The mechanism is simple to use, customizable and transparent. It ensures that there are no performance issues during image processing. This article explains how to customize the cache with Aspose.imaging API for Java.

{{% /alert %}} 
### **Customizing the Cache**
When a process needs temporary data storage, this storage is allocated in the cache. The cache can be some space in memory or on disk and is set by the user. When the temporary data is no longer needed, the space is released. The statistics of the allocated space can be inspected at any time by calling the getAllocatedDiskBytesCount and getAllocatedMemoryBytesCount methods.

How Aspose.Imaging allocates and uses caches can be customized. This section describes the various settings and their defaults and the code snippets below show how they can be used.
#### **Setting where the Cache is allocated**
To customize how cache space is allocated, set the CacheType property. By default, the cache is allocated in memory and when there is no more space available in memory, it is allocated to disk. This behavior is captured by Auto mode. Auto mode is is flexible and maximizes performance.

There are also other modes:

- CacheOnDiskOnly mode: allocation to disk only.
- CacheInMemoryOnly mode: allocation to memory only.

Selecting CacheOnDiskOnly mode may result in poor performance.
#### **Setting the Size of the Cache**
Set the maximum space (in bytes) that can be allocated on disk or memory by setting the setMaxDiskSpaceForCache and setMaxMemoryForCache properties respectively. By default, both values are set to 0, meaning that there's no upper limit.
#### **Controlling Cache Reallocation**
If there isn't enough space available in memory (as specified by the setMaxMemoryForCache property) when a new cache is allocated, the cache is allocated to disk.

{{% alert color="primary" %}} 

If there's not enough space on disk, an exception is thrown. The cache allocation process moves from memory to disk but not vice versa.

{{% /alert %}} 

The property setExactReallocateOnly is used to control memory re-allocation. Re-allocation is most likely to occur for pre-allocated caches. It can happen when system figures out that the allocated space will not be sufficient. If setExactReallocateOnly is set to the default value, False, the space is re-allocated on the same medium. When set to True, re-allocation cannot exceed the maximum specified space. In this case the existing allocated in-memory cache (which requires re-allocation) is freed and extended space is allocated on disk.

Below is an example demonstrating the use of the Cache class. The example source code has been split in several parts to keep it simple and easy to understand.
##### **Programming Sample**
{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Articles-ControllingCacheReallocation-ColorConversionSavingImage.java" >}}

The allocated byte count properties may be used to check whether all Aspose.Imaging objects were properly disposed. In case you forget to dispose of an object the cache values will be different from 0.
