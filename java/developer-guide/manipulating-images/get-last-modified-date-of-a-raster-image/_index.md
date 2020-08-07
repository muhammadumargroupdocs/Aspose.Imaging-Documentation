---
title: Get Last Modified Date of A Raster Image
type: docs
weight: 120
url: /java/get-last-modified-date-of-a-raster-image/
---

{{% alert color="primary" %}} 

This article demonstrates the usage of Aspose.Imaging for Java to get last modified date of an image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal.

{{% /alert %}} 
### **Get Last Modified Date**
Aspose.Imaging for Java has exposed the **getModifyDate** method of **Image** class to get the last modified date of an image from its metadata. **getModifyDate** method needs a Boolean value to get the modified date accordingly.

The steps to get last modified date are as simple as below:

1. Load an image using the factory method Load exposed by Image class.
1. Convert the image into **RasterImage**.
1. Call the RasterImage.getModifyDate method by passing a Boolean true or false value.

The following code example demonstrates how to get last modified date of the image.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-images-GetLastModifiedDateofRasterImage-GetLastModifiedDateofRasterImage.java" >}}
