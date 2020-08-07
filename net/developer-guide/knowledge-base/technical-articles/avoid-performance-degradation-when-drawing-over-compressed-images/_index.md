---
title: Avoid Performance Degradation when Drawing over Compressed Images
type: docs
weight: 20
url: /net/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **Avoid Performance Degradation when Drawing over Compressed Images**
There are times when you want to perform extremely extensive graphic operations on a compressed image. When Aspose.Imaging has to compress and decompress images on the fly, performance degradation may occur. [Drawing]() over compressed images may also carry a performance penalty.
### **Solution**
To avoid performance degradation, we recommend that you convert the image to an uncompressed, or raw, format before performing graphic operations.
### **Using File Path**
In the example that follows, a Png image is converted to another Png and saved to disk. The image is then loaded back before graphic operations are performed on it. The same technique applies for BMP and GIF files.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-CSharp-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **Using a Stream Object**
The following code snippet shows you how to Png image is converted to another Png image and saved to disk using MemoryStream.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-CSharp-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
