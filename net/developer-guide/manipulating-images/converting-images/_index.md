---
title: Converting Images
type: docs
weight: 30
url: /net/converting-images/
---

## **Converting Images to Black n White and Grayscale**
Sometimes you may require to convert colored images to Black n White or Grayscale for printing or archiving purposes. This article demonstrates the use of Aspose.Imaging for .NET API to achieve this using two methods as stated below.

1. Binarization
1. Grayscaling
### **Binarization**
In order to understand the concept of Binarization, it is important to define a Binary Image; that is a digital image that can have only two possible values for each pixel. Normally, the two colors used for a binary image are black and white though any two colors can be used. Binarization is the process of converting an image to bi-level meaning that each pixel is stored as a single bit (0 or 1) where 0 denotes the absence of color and 1 means presence of color. Aspose.Imaging for .NET API currently supports two Binarization methods.
#### **Binarization with Fixed Threshold**
The following code snippet shows you how to use fixed threshold binarization can be applied to an image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarization with Otsu Threshold**
The following code snippet shows you how Otsu threshold binarization can be applied to an image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Grayscaling**
Gray-scaling is the process of converting a continuous-tone image to an image with discontinues gray shades. The following code snippet shows you how to use Grayscaling.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Grayscaling-Grayscaling.cs" >}}
### **Convert Image to grayscale with Setting 16bit**
Gray-scaling is the process of converting a continuous-tone image to an image with discontinues gray shades. The following code snippet shows you how to use Grayscaling with 16bits.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Grayscaling-Grayscaling.cs" >}}
## **Convert GIF Image Layers To TIFF Image**
Sometimes it is needed to extract and convert layers of a GIF Image into another raster image format to meet an application need. Aspose.Imaging API support the feature of extracting and converting layers of a GIF Image into another raster image formats. Firstly, we will create instance of image and load GIF image from the local disk, then we will get the total count of layers in the source image using Length property of GifFrameBlock class and iterate through the array of blocks. Now we will check if the block is NULL then ignore it else convert the block to TIFF image. The following code snippet shows you how to convert GIF image layers to TIFF image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ConvertGIFImageLayersToTIFF-ConvertGIFImageLayersToTIFF.cs" >}}
## **Converting SVG to Raster Format**
See : 

[Convert SVG to Raster image](/imaging/net/convert-svg-to-raster-image-html/)

[Convert SVG to PNG](/imaging/net/convert-svg-to-png-html/)

[Convert SVG to Bmp](/imaging/net/convert-svg-to-bmp-html/)
## **Converting Raster Image to PDF**
See : 

[Convert Raster Image to PDF](/imaging/net/convert-raster-image-to-pdf-html/)

[Convert BMP to PDF](/imaging/net/convert-bmp-to-pdf-html/)  

[Converting PNG to PDF](/imaging/net/convert-png-to-pdf-html/)
## **Converting Raster Image to Svg**
See

[Convert Raster Image to Svg](/imaging/net/convert-raster-image-to-svg-html/)
## **Converting RGB color system to CMYK for Tiff file Format**
Using Aspose.Imaging for .NET, developers can convert RGB color system file to CMYK tiff format. This article shows how to export/convert RGB color system file to CMYK tiff format with Aspose.Imaging. Using Aspose.Imaging for .NET you can load image of any format and than you can set various properties using **TiffOptions** class and save the image. The following code snippet shows you how to achieve this feature.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-RGBColorSytem-RGBColorSytem.cs" >}}
## **Working with animation**
See

` `[Convert APNG files](/imaging/net/convert-apng-files-html/)
## **Converting Open document graphics**
See

[Convert ODG files](/imaging/net/convert-odg-files-html/)

[Convert OTG files](/imaging/net/convert-otg-files-html/)


## **Converting Corel Draw images**
See 
[Convert CDR](/imaging/net/convert-cdr/)
## **Converting webp images**
See
[Convert webp images](/imaging/net/convert-webp-images/)
## **Converting eps images**
[Convert eps images](/imaging/net/convert-eps-images/)
## **Converting cmx images**
[Convert cmx images](/imaging/net/convert-cmx-images/)
## **Converting dicom images**
[Convert dicom images](/imaging/net/convert-dicom-images/)
## **Exporting Images**
Along with a rich set of image processing routines, Aspose.Imaging provides specialized classes to convert images to other formats. Using this library, image format conversion is as simple as changing the file extension to desired format in the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class [Save](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/save/index) method and by specifying the appropriate [ImageOptions](/pages/createpage.action?spaceKey=imagingnet&title=Aspose.Imaging.ImageOptions+namespace&linkCreation=true&fromPageId=14823896) values. Below are some specialized classes for this purpose in [ImageOptions](/pages/createpage.action?spaceKey=imagingnet&title=Aspose.Imaging.ImageOptions+namespace&linkCreation=true&fromPageId=14823896) namespace.

- [BmpOptions]()
- [GifOptions]()
- [JpegOptions]()
- [TiffOptions]()
- [PngOptions]()
- [PsdOptions]()
- [WebPOptions](/pages/createpage.action?spaceKey=imagingnet&title=Aspose.Imaging.ImageOptions.WebPOptions+Class&linkCreation=true&fromPageId=14823896)
- ApngOptions

It is easy to export images with Aspose.Imaging for .NET API. All you need is an object of the appropriate class from [ImageOptions](/pages/createpage.action?spaceKey=imagingnet&title=Aspose.Imaging.ImageOptions+namespace&linkCreation=true&fromPageId=14823896) namespace. By using these classes, you can easily export any image created, edited or simply loaded with Aspose.Imaging for .NET to any supported format. Below is an example that demonstrates this simple procedure. In the example, a GIF image is loaded by passing the file path as a parameter to the [Load](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/load) method. It is then exported to various image formats using the [Save](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/save/index) method. The examples here show how to load a GIF and save it to BMP, JPEG, PNG and finally TIFF using Aspose.Imaging for .NET with C# and Visual Basic.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ExportImageToDifferentFormats-ExportImageToDifferentFormats.cs" >}}
## **Convert compressed vector formats**
Aspose.Imaging supports next compressed vector formats: Emz(compressed emf), Wmz(compressed wmf), Svgz(compressed svg). Supported read of these formats and export to other formats.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Compressed-Vector-Formats.cs" >}}
## **Combining Images**
This example uses [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class and shows how to combine two or more images into a single complete image.To demonstrate the operation, the example creates a new [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) canvas in JPEG format and draw images on the canvas surface using [Draw Image ](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/drawimage/index)method exposed by [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class. Using [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class two or more images can be combine in such a way that the resultant image will look as a complete image with no space between the image parts and no pages. The **canvas** size must be equal to the size of resultant image. Following is the code demonstration that shows how to use [Draw Image ](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/drawimage/index)method of the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class to combine images in a single image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-CombineImages-CombineImages.cs" >}}
## **Expand and Crop Images**
Aspose.Imaging API allows you to expand or crop an image during image conversion process. Developer needs to create a rectangle with X and Y coordinates and specify the width and height of the rectangle box. The X,Y and Width, Height of rectangle will depict the expansion or cropping of the loaded image. If it is required to expand or crop the image during image conversion, perform the following steps:

1. Create an instance of [RasterImage](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage) class and load the existing image.
1. Create an Instance of ImageOption class.
1. Create an instance of [Rectangle](http://www.aspose.com/api/net/imaging/aspose.imaging/rectangle) class and initialize the X,Y and Width, Height of the rectangle
1. Call Save method of the [RasterImage](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage) class while passing output file name, image options and the rectangle object as parameters.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ExpandOrCropAnImage-ExpandOrCropAnImage.cs" >}}
## **Read and Write XMP Data To Images**
XMP (Extensible Metadata Platform) is an ISO standard. XMP standardizes a data model, a serialization format and core properties for the definition and processing of extensible metadata. It also provides guidelines for embedding XMP information into popular image such as JPEG, without breaking their readability by applications that do not support XMP. Using Aspose.Imaging for .NET API developers can read or write XMP metadata to images. This article demonstrates how XMP metadata can be read from image and write XMP metadata to images.
### **Create XMP Metadata, Write It And Read From File**
The release of Aspose.Imaging for .NET 3.3.0 contains the **Xmp** namespace. With the help of Xmp namespace developer can create **XMP metadata** object and write it to an image. The following code snippet shows you how to use the **XmpHeaderPi**, **XmpTrailerPi**, **XmpMeta**, **XmpPacketWrapper**, **PhotoshopPackage** and **DublinCorePackage** packages contained in **Xmp** namespace.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ReadAndWriteXMPDataToImages-ReadAndWriteXMPDataToImages.cs" >}}
## **Export Images in Multi Threaded Environment**
Aspose.Imaging for .NET now supports converting images in multi threaded environment. Aspose.Imaging for .NET ensure the optimized performance of operations during execution of code in multi-threaded environment. All imaging option classes (e.g. BmpOptions, TiffOptions, JpegOptions, etc.) in the Aspose.Imaging for .NET now implement **IDisposable** interface. Therefore it is a must that developer properly dispose off the imaging options class object in case **Source** property is set. Following code snippet demonstrates the said functionality.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ExportImagesInMultiThreadedEnvironment-ExportImagesInMultiThreadedEnvironment.cs" >}}

Aspose.Imaging now supports **SyncRoot** property while working in multi-threaded environment. Developer can use this property to synchronize access to the source stream. Following code snippet demonstrates how the **SyncRoot** property can be used.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SyncRootProperty-SyncRootProperty.cs" >}}




