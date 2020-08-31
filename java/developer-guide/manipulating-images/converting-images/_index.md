---
title: Converting Images
type: docs
weight: 30
url: /java/converting-images/
---

## **Converting Images to Black n White and Grayscale**
Sometimes you may require to convert colored images to Black n White or Grayscale for printing or archiving purposes. This article demonstrates the use of Aspose.Imaging for Java API to achieve this using two methods as stated below.

1. Binarization
1. Grayscaling
### **Binarization**
In order to understand the concept of Binarization, it is important to define a Binary Image; that is a digital image that can have only two possible values for each pixel. Normally, the two colors used for a binary image are black and white though any two colors can be used. Binarization is the process of converting an image to bi-level meaning that each pixel is stored as a single bit (0 or 1) where 0 denotes the absence of color and 1 means presence of color. Aspose.Imaging for Java API currently supports two Binarization methods.
#### **Binarization with Fixed Threshold**
The following code snippet shows you how to use fixed threshold binarization can be applied to an image.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-BinarizationwithFixedThreshold-BinarizationwithFixedThreshold.java" >}}


#### **Binarization with Otsu Threshold**
The following code snippet shows you how Otsu threshold binarization can be applied to an image.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-BinarizationwithOtsuThreshold-BinarizationwithOtsuThreshold.java" >}}


### **Grayscaling**
Gray-scaling is the process of converting a continuous-tone image to an image with discontinues gray shades. The following code snippet shows you how to use Grayscaling.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-Grayscaling-Grayscaling.java" >}}
### **Convert Image to grayscale with Setting 16bit**
Gray-scaling is the process of converting a continuous-tone image to an image with discontinues gray shades. The following code snippet shows you how to use Grayscaling with 16bits.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-Grayscaling-Grayscaling.java" >}}
## **Convert GIF Image Layers To TIFF Image**
Sometimes it is needed to extract and convert layers of a GIF Image into another raster image format to meet an application need. Aspose.Imaging API support the feature of extracting and converting layers of a GIF Image into another raster image formats. Firstly, we will create instance of image and load GIF image from the local disk, then we will get the total count of layers in the source image using Length property of [GifFrameBlock](https://apireference.aspose.com/imaging/java/com.aspose.imaging.fileformats.gif.blocks/GifFrameBlock) class and iterate through the array of blocks. Now we will check if the block is **null** then ignore it else convert the block to TIFF image. The following code snippet shows you how to convert GIF image layers to TIFF image.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ConvertGIFImageLayersToTIFF-ConvertGIFImageLayersToTIFF.java" >}}
## **Converting SVG to Raster Format**
See : 

[Convert SVG to Raster image](/imaging/java/convert-svg-to-raster-image/)

[Convert SVG to PNG](/imaging/java/convert-svg-to-png/)

[Convert SVG to Bmp](/imaging/java/convert-svg-to-bmp/)
## **Converting Raster Image to PDF**
See : 

[Convert Raster Image to PDF](/imaging/java/convert-raster-image-to-pdf/)

[Convert BMP to PDF](/imaging/java/convert-bmp-to-pdf/)  

[Converting PNG to PDF](/imaging/java/convert-png-to-pdf/)
## **Converting Raster Image to Svg**
See

[Convert Raster Image to Svg](/imaging/java/convert-raster-image-to-svg/)
## **Converting RGB color system to CMYK for Tiff file Format**
Using Aspose.Imaging for Java, developers can convert RGB color system file to CMYK tiff format. This article shows how to export/convert RGB color system file to CMYK tiff format with Aspose.Imaging. Using Aspose.Imaging for Java you can load image of any format and than you can set various properties using **TiffOptions** class and save the image. The following code snippet shows you how to achieve this feature.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-RGBColorSystem.java" >}}
## **Working with animation**
See

[Convert APNG files](/imaging/java/convert-apng-files/)
## **Converting Open document graphics**
See

[Convert ODG files](/imaging/java/convert-odg-files/)

[Convert OTG files](/imaging/java/convert-otg-files/)


## **Converting Corel Draw images**
See 
[Convert CDR](/imaging/java/convert-cdr/)
## **Converting webp images**
See
[Convert WebP images](/imaging/java/convert-webp-images/)
## **Converting EPS images**
[Convert EPS images](/imaging/java/convert-eps-to-psd/)
## **Converting cmx images**
[Convert cmx images](/imaging/java/convert-cmx-images/)
## **Converting dicom images**
[Convert dicom images](/imaging/java/convert-dicom-images/)
## **Exporting Images**
Along with a rich set of image processing routines, Aspose.Imaging provides specialized classes to convert images to other formats. Using this library, image format conversion is as simple as changing the file extension to desired format in the [Image](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Image) class [save](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Image#save--) method and by specifying the appropriate [ImageOptionsBase ](https://apireference.aspose.com/imaging/java/com.aspose.imaging/ImageOptionsBase)values. Below are some specialized classes for this purpose in [imageoptions](https://apireference.aspose.com/imaging/java/com.aspose.imaging.imageoptions/package-frame) package.

- [BmpOptions]()
- [GifOptions]()
- [JpegOptions]()
- [TiffOptions]()
- [PngOptions]()
- [PsdOptions]()
- [WebPOptions](/pages/createpage.action?spaceKey=imagingjava&title=Aspose.Imaging.ImageOptions.WebPOptions+Class&linkCreation=true&fromPageId=15302658)
- ApngOptions

It is easy to export images with Aspose.Imaging for Java API. All you need is an object of the appropriate class from [imageoptions](https://apireference.aspose.com/imaging/java/com.aspose.imaging.imageoptions/package-frame) package. By using these classes, you can easily export any image created, edited or simply loaded with Aspose.Imaging for Java to any supported format. Below is an example that demonstrates this simple procedure. In the example, a GIF image is loaded by passing the file path as a parameter to the [load](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Image#load-java.lang.String-com.aspose.imaging.LoadOptions-) method. It is then exported to various image formats using the [save](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Image#save-java.lang.String-com.aspose.imaging.ImageOptionsBase-) method. The examples here show how to load a GIF and save it to BMP, JPEG, PNG and finally TIFF using Aspose.Imaging for Java.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-ExportImageToDifferentFormats.java" >}}
## **Convert compressed vector formats**
Aspose.Imaging supports next compressed vector formats: Emz(compressed emf), Wmz(compressed wmf), Svgz(compressed svg). Supported read of these formats and export to other formats.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-Compressed-Vector-Formats.java" >}}
## **Combining Images**
This example uses [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class and shows how to combine two or more images into a single complete image.To demonstrate the operation, the example creates a new [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) canvas in JPEG format and draw images on the canvas surface using [Draw Image ](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Graphics#drawImage-com.aspose.imaging.Image-com.aspose.imaging.Point-)method exposed by [Graphics](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Graphics) class. Using [Graphics](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Graphics) class two or more images can be combine in such a way that the resultant image will look as a complete image with no space between the image parts and no pages. The **canvas** size must be equal to the size of resultant image. Following is the code demonstration that shows how to use [Draw Image ](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Graphics#drawImage-com.aspose.imaging.Image-com.aspose.imaging.Point-)method of the [Graphics](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Graphics) class to combine images in a single image.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-CombineImagesUsingGraphicsClass.java" >}}
## **Expand and Crop Images**
Aspose.Imaging API allows you to expand or crop an image during image conversion process. Developer needs to create a rectangle with X and Y coordinates and specify the width and height of the rectangle box. The X,Y and Width, Height of rectangle will depict the expansion or cropping of the loaded image. If it is required to expand or crop the image during image conversion, perform the following steps:

1. Create an instance of [RasterImage](https://apireference.aspose.com/imaging/java/com.aspose.imaging/RasterImage) class and load the existing image.
1. Create an Instance of [ImageOptionsBase ](https://apireference.aspose.com/imaging/java/com.aspose.imaging/ImageOptionsBase)class.
1. Create an instance of [Rectangle](https://apireference.aspose.com/imaging/java/com.aspose.imaging/Rectangle) class and initialize the X,Y and Width, Height of the rectangle
1. Call Save method of the [RasterImage](https://apireference.aspose.com/imaging/java/com.aspose.imaging/RasterImage) class while passing output file name, image options and the rectangle object as parameters.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-ExpandOrCropAnImage.java" >}}
## **Read and Write XMP Data To Images**
XMP (Extensible Metadata Platform) is an ISO standard. XMP standardizes a data model, a serialization format and core properties for the definition and processing of extensible metadata. It also provides guidelines for embedding XMP information into popular image such as JPEG, without breaking their readability by applications that do not support XMP. Using Aspose.Imaging for Java API developers can read or write XMP metadata to images. This article demonstrates how XMP metadata can be read from image and write XMP metadata to images.
### **Create XMP Metadata, Write It And Read From File**
The release of Aspose.Imaging for Java 3.3.0 contains the **Xmp** namespace. With the help of Xmp namespace developer can create **XMP metadata** object and write it to an image. The following code snippet shows you how to use the **XmpHeaderPi**, **XmpTrailerPi**, **XmpMeta**, **XmpPacketWrapper**, **PhotoshopPackage** and **DublinCorePackage** packages contained in **Xmp** namespace.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ReadandWriteXMPDataToImages-ReadandWriteXMPDataToImages.java" >}}
## **Export Images in Multi Threaded Environment**
Aspose.Imaging for Java now supports converting images in multi threaded environment. Aspose.Imaging for Java ensure the optimized performance of operations during execution of code in multi-threaded environment. All imaging option classes (e.g. BmpOptions, TiffOptions, JpegOptions, etc.) in the Aspose.Imaging for Java now implement Closeable interface. Therefore it is a must that developer properly dispose off the imaging options class object in case **Source** property is set. Following code snippet demonstrates the said functionality.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ExportImagesInMultiThreadedEnvironment-ExportImagesInMultiThreadedEnvironment.java" >}}

Aspose.Imaging now supports **SyncRoot** property while working in multi-threaded environment. Developer can use this property to synchronize access to the source stream. Following code snippet demonstrates how the **SyncRoot** property can be used.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-SyncRootProperty-ExportImagesInMultiThreadedEnvironment.java" >}}




