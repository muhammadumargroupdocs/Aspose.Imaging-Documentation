---
title: Manipulating WMF Files
type: docs
weight: 180
url: /net/manipulating-wmf-files/
---

## **Create WMF MetaFile Image**
Using Aspose.Imaging for .NET, developers can create WMF metafile image. This topic explains in detail that how WMF metafile image can be created. Aspose.Imaging for .NET provides the **WmfRecorderGraphics2D** class to create WMF metafile. The following code snippet shows you how to create WMF Metafile Image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-CreateWMFMetaFileImage-CreateWMFMetaFileImage.cs" >}}


## **Create EMF MetaFile Image**
Using Aspose.Imaging for .NET, developers can create EMF metafile image. This topic explains in detail that how EMF metafile image can be created. This topic also covers the test to convert the newly generated EMF metafile image to PDF format. Aspose.Imaging for .NET provides the **EmfRecorderGraphics2D** class to create EMF metafile. Below is the code demonstration of the said functionality.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-CreateEMFMetaFileImage-CreateEMFMetaFileImage.cs" >}}


## **Resize WMF file while converting to PNG**
Using Aspose.Imaging for .NET, developers can resize the WMF metafile while converting it to raster format. This topic explains the approach to load existing metafiles, resize it and convert it to raster format. Aspose.Imaging for .NET provides the **Image** class to load WMF files and same can be used to resize and save the image to PNG format. The following code snippet shows you how to resize the WMF file while converting it to PNG.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ResizeWMFFile-ResizeWMFFile.cs" >}}


## **Converting EMF to WMF**
Using Aspose.Imaging for .NET, developers can convert EMF to WMF metafile format. This topic explains the approach to load existing EMF metafiles and convert it to WMF format. Aspose.Imaging for .NET provides the **Image** class to load EMF files and same can be used to save the image to WMF format. The following code snippet shows you how to convert EMF to WMF.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ConvertEMFToWMF-ConvertEMFToWMF.cs" >}}


## **Exporting Text as Shape While Converting EMF MetaFile**
Using Aspose.Imaging for .NET, developers can get text as shapes while converting EMF to SVG format. This topic explains in detail how to convert text into shape while converting EMF to SVG format. Aspose.Imaging for .NET provides the **TextAsShapes** property to get text as shape while converting EMF metafile. Below is the code demonstration of the said functionality.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ExportTextAsShape-ExportTextAsShape.cs" >}}


## **Get Last Modified Date of A Raster Image**
This article demonstrates the usage of Aspose.Imaging for .NET to get last modified date of an image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal.
### **Get Last Modified Date**
Aspose.Imaging for .NET has exposed the **GetModifyDate** method of **Image** class to get the last modified date of an image from its metadata. **GetModifyDate** method needs a Boolean value to get the modified date accordingly. The steps to get last modified date are as simple as below:

1. Load an image using the factory method Load exposed by Image class.
1. Convert the image into **RasterImage**.
1. Call the RasterImage.GetModifyDate method by passing a Boolean true or false value.

The following code snippet shows you how to get last modified date of the image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GetLastModifiedDate-GetLastModifiedDate.cs" >}}
## **Crop WMF Image**
Image cropping usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used for to cut out some portion of an image to increase the focus on a particular area. The **WmfImage** class provides **Crop** method that accepts an instance of the **Rectangle** class. You can cut out any portion of an image by providing the desired boundaries to the **Rectangle** object.

The code snippet below demonstrates how to Crop any image by Rectangle.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-CSharp-ModifyingAndConvertingImages-CropWMFFile-CropWMFFile.cs" >}}




