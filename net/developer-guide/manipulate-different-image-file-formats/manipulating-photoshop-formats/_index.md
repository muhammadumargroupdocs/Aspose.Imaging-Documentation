---
title: Manipulating Photoshop Formats
type: docs
weight: 130
url: /net/manipulating-photoshop-formats/
---

## **Exporting Image to PSD**
PSD, PhotoShop document, is the default file format used by Adobe PhotoShop for working with images. Aspose.Imaging lets you save files to PSD so that they can be opened and edited in PhotoShop. This article shows how to save a file to PSD with Aspose.Imaging, and it also discusses some of the settings that can be used when saving to this format. [PsdOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/psdoptions) is a specialized class in the [ImageOptions](/pages/createpage.action?spaceKey=imagingnet&title=Aspose.Imaging.ImageOptions+namespace&linkCreation=true&fromPageId=14784475) namespace used to export images to PSD. To export to PSD, create an instance of the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class, either loaded from an existing image file or created from scratch. This article explains how. In the examples below, an existing image is loaded by passing the file path to the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class static Load method. Once it is loaded, save the image using the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class [Save](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/save/index) method, and supply a [PsdOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/psdoptions) object as the second argument. Several of the [PsdOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/psdoptions) class properties can be set for advanced conversion. Some of the properties are ColorMode, [CompressionMethod](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.psd/compressionmethod) and Version. Aspose.Imaging for .NET supports the following compression methods through the [CompressionMethod](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.psd/compressionmethod) enumeration:

- [CompressionMethod.Raw](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.psd/compressionmethod)
- [CompressionMethod.RLE](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.psd/compressionmethod)
- [CompressionMethod.ZipWithoutProtection](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.psd/compressionmethod)
- [CompressionMethod.ZipWithProtection](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.psd/compressionmethod)

The following color modes are supported through the [ColorModes]() enumeration:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

Additional resources can be added, such as thumbnail resources for PSD v4.0, v5.0 and higher, or grid and guide resources for PSD v4.0 and higher. The code below opens a BMP file from disk and saves it to PSD with RLE compression and grayscale color mode, the following code snippet shows you how to export Image to PSD.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **Creating Indexed PSD Files**
Aspose.Imaging for .NET API can create Indexed PSD files from scratch. This article demonstrates the use of PsdOptions and PsdImage classes to create an Indexed PSD while drawing some shapes over the newly created canvas. The following simple steps are required to create an Indexed PSD file.

1. Create an instance of PsdOptions and set it's source.
1. Set ColorMode property of the PsdOptions to ColorModes.Indexed.
1. Create a new palette of colors from RGB space and set it as Palette property of PsdOptions.
1. Set [CompressionMethod](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.psd/compressionmethod) property to required compression algorithm.
1. Create a new PSD image by calling the PsdImage.Create method.
1. Draw graphics or perform other operations as per requirement.
1. Call PsdImage.Save method to commit all changes.

The following code snippet shows you how to create indexed PSD files.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **Support for EPS Format**
This article shows how to  option parsing and rendering for PSD text layer. The following code snippet shows you how to support SmallCap.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SupportForEPSFormat-SupportForEPSFormat.cs" >}}
