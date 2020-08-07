---
title: Saving Image to BufferedImage
type: docs
weight: 60
url: /java/saving-image-to-bufferedimage/
---

### **Saving Image to BufferedImage**
This article demonstrates the usage of Aspose.Imaging for Java API to convert an image to an instance of java.awt.image.BufferedImage. Aspose.Imaging for Java API has exposed two variations of the ImageExtensions.toJava method to achieve this goal.

Aspose.Imaging for Java has exposed the ImageExtensions.toJava method to convert an instance of Image to an instance of BufferedImage on the fly. There are two overloads of the toJava method to suit the application needs.
#### **Simple Conversion**
The following code example demonstrates how to convert an image to an instance of BufferedImage.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Articles-BufferedImageSimpleConversion-BufferedImageSimpleConversion.java" >}}
#### **Converting Part of An Image to BufferedImage**
The other overloaded version of ImageExtensions.toJava method accepts an instance of Rectangle as second parameter to export a specific portion of image to BufferedImage.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Articles-ConvertPartofImagetoBufferedImage-ConvertPartofImagetoBufferedImage.java" >}}
