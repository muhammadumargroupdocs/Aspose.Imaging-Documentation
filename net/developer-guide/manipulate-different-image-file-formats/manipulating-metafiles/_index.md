---
title: Manipulating Metafiles
type: docs
weight: 120
url: /net/manipulating-metafiles/
---

## **Converting EMF To PDF**
Using Aspose.Imaging for .NET, developers can convert EMF metafile to PDF format. This topic explains the approach to load existing metafiles and convert it to PDF. Aspose.Imaging for .NET provides the **EmfImage** class to load EMF files and same can be used to save the image to PDF format. Below provided sample code demonstrate how to convert EMF to PDF.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MetaFiles-ConvertEMFToPDF-ConvertEMFToPDF.cs" >}}


## **Cropping EMF Image**
**Image cropping** usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used to cut out some portion of an image to increase the focus on a particular area. Aspose.Imaging for .NET API supports two different approaches for cropping image: by [shifts](http://www.aspose.com/docs/display/imagingnet/Manipulating+Metafiles#ManipulatingMetafiles-UsingShifts) and by [rectangle](http://www.aspose.com/docs/display/imagingnet/Manipulating+Metafiles#ManipulatingMetafiles-UsingRectangle).
#### **Using Shifts**
The EmfImage class provides an overloaded version of the [Crop](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage/methods/crop/index) method that accepts 4 integer values denoting Left, Right, Top & Bottom. Based on these four values, the Crop method moves the image boundaries toward the center of the image while discarding the outer portion.

The code snippet below demonstrates how to crop an EMF image by shifts.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MetaFiles-CroppingEMFImage-CroppingEMFImage.cs" >}}


#### **Using Rectangle**
The EmfImage class provides another overloaded version of the Crop method that accepts an instance of the Rectangle class. You can cut out any portion of an image by providing the desired boundaries to the Rectangle object. The code snippet below demonstrates how.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MetaFiles-CroppingEMFImage-CroppingEMFImage.cs" >}}


## **Export MetaFile To Raster Formats**
Using Aspose.Imaging for .NET, developers can convert metafile (Emf/Emf+) to raster formats. This article shows how to export/convert metafile file to raster image formats with Aspose.Imaging. Aspose.Imaging for .NET provides the **EmfImage** class to load EMF files and same can be used to convert the Emf to raster formats. Below provided sample code demonstrate how to convert Emf/Emf+ to raster images.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MetaFiles-ExportMetaFileToRasterFormats-ExportMetaFileToRasterFormats.cs" >}}


## **Specifying Font Folder While Converting**
Using Aspose.Imaging for .NET, developers can specify the font folder path used while converting WMF file. This topic explains the approach to specify the font folder that should be used. The following code snippet demonstrates the usage of Aspose.Imaging for .NET API to change the font while converting EMF to raster image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MetaFiles-SpecifyFontFolder-SpecifyFontFolder.cs" >}}
## **Support For Replacing Missing Fonts**
Using Aspose.Imaging for .NET, developers can replace missing fonts when saving ODG, SVG and MetaFile images. This topic explains the approach to replace the fonts that should be used. The following code snippet demonstrates the usage of Aspose.Imaging for .NET API to replace the font while saving ODG images.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MetaFiles-SpecifyFontFolder-SpecifyFontFolder.cs" >}}
## **Managing resources while saving Metafile as SVG**
Using Aspose.Imaging for .NET, developers can manage resources (fonts and internal images) when saving Metafile images (emf and wmf) into SVG file stream. This topic explains that there should be a setting that will let us specify whether to save contained image as a separate file and provide a stream for saving it, or to embed image as base64 string inside of SVG. The following code snippet demonstrates the usage of Aspose.Imaging for .NET API to manage resources.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MetaFiles-MetaFilesAsSVG-SvgImageTester.cs" >}}
