---
title: Manipulating WMF Files
type: docs
weight: 260
url: /java/manipulating-wmf-files/
---

## **Crop WMF Image**
Image cropping usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used for to cut out some portion of an image to increase the focus on a particular area. The **WmfImage** class provides **Crop** method that accepts an instance of the **Rectangle** class. You can cut out any portion of an image by providing the desired boundaries to the **Rectangle** object.

The code snippet below demonstrates how to Crop any image by Rectangle.

.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-wmf-CropWMFFile-CropWMFFile.java" >}}
