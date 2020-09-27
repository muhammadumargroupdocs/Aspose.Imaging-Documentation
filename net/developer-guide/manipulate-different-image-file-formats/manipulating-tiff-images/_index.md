---
title: Manipulating TIFF Images
type: docs
weight: 160
url: /net/manipulating-tiff-images/
---

## **Add Frames with Different Settings**
TIFF is a very flexible format and it allows different frames to be added, with different dimensions, compression and other settings. Aspose.Imaging APIs allow you to add any TIFF frame of any size which helps in creating complex documents. If there is a requirement to adjust the frames during the add process to make them all equal, perform the following steps:

1. Create a new blank frame with the desired options or copy the source frame with the output options specified using the [CreateFrameFrom](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffframe/methods/createframefrom) method.
1. Resize the source frame/image to the desired dimensions using the Resize method.
1. Add the source frame/image pixels to the new frame.
1. Add the new frame to the output TIFF image.
## **Export Multi Page frames to different Image format**
Sometimes you need to export Multi-page TIFF frames to some other image file format. This article will demonstrate how we can perform this task using Aspose.Imaging for .NET API. We will use [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage), [TiffFrame](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffframe), BmpOptions and BmpImage classes to export TIFF frames to BMP image format. First, we will create instance of TIFF image and load images from local disk. Now we will iterate over TIFF frames and copy pixels of active frame using [LoadPixels](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage/methods/loadpixels) method into Colors array and create an instance of BmpOptions for BMP image settings. Set the desired setting for BMP image creation. Create a new BMP image using BmpOptions object and save BMP image using frame pixels, copied in Colors array.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ExtractTIFFFramesToBMPImageFormat-ExtractTIFFFramesToBMPImageFormat.cs" >}}



Please note, the above provided code snippet requires setting the valid license for Aspose.Imaging for .NET API. This is because Aspose.Imaging APIs restrict the usage of core features such as [LoadPixels](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage/methods/loadpixels) & [SavePixels](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage/methods/savepixels) in evaluation mode. Please check the details for [Evaluation Version Limitations_imaging.net]().
## **Adding Multiple images inside Tiff Frames**
` `This article will demonstrate how we can we add multiple images inside single tiff using Aspose.Imaging for .NET API. We will use [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage), [TiffFrame](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffframe),  classes to add multiple images inside tiff frames. Below provided code snippet demonstrates this concept.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-MultipleImagesToTIFF-MultipleImagesToTIFF.cs" >}}
## **Concatenate Multiple TIFF Images**
Sometimes you need to concatenate a TIFF Image into another TIFF image to meet an application need. Aspose.Imaging APIs support the feature of concatenating multiple Tiff images, whereas this article exhibits the TIFF image concatenation feature of Aspose.Imaging for .NET API. We will use [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage) and [TiffFrame](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffframe) classes to concatenate multiple TIFF images. We can use both standard methods, from file and from stream, to concatenate TIFF images.
### **Images Having Single Frame**
{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ConcatTIFFImages-ConcatTIFFImages.cs" >}}


#### **Concatenating Images from Disk**
Firstly, we will create instances of images and load images from the local disk, then we will copy the active frame of source image using [Copyframe](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffframe/methods/copyframe) method of [TiffFrame](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffframe) class and add that copied frame to destination image with the help of [Addframe](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage/methods/addframe) method of [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage) class. Finally we will save image back to local disk.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ConcatTIFFImages-ConcatTIFFImages.cs" >}}


#### **Concatenating Images from Stream**
Sometimes the images that we need to process are stored as a stream. In that case, use the overloaded version of the Load method. Remaining logic would be remained same as described above.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ConcatTIFFImages-ConcatTIFFImages.cs" >}}


### **Images Having Several Frames**
Below provided sample demonstrates the usage of Aspose.Imaging for .NET API to concatenate Tiff images that could have several frames. For demonstration purposes, we will read a list of Tiff images, and create a new Tiff image that will hold the frames from all read Tiff images.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ConcatenateTiffImagesHavingSeveralFrames-ConcatenateTiffImagesHavingSeveralFrames.cs" >}}


## **Data Recovery Options**
Sometimes you may encounter a TIFF image that cannot be rendered properly while using traditional image viewers such as Windows Photo Viewer because the image is damaged or corrupted. When loaded with Aspose.Imaging, such images may throw exceptions and you may not be able to process them further. Aspose.Imaging 2.2.0 and later supports data recovery mode for TIFF files. The data recovery allows you to load a TIFF file that has improper data layout or corrupted data strips. Data recovery replaces the corrupted data with any color specified, and you can retrieve the rest of the data for further processing without experiencing any exception. This mechanism is especially useful for Tiff file format since it stores the data in strips. When a strip is damaged the other strips may still retain the correct information.

Aspose.Imaging provides two recovery modes which provide different results.

1. [ConsistentRecover](http://www.aspose.com/api/net/imaging/aspose.imaging/datarecoverymode): The consistent recovery mode tries to recover all data as long as corruption does not break the file format and allows further processing.
1. [MaximalRecover](http://www.aspose.com/api/net/imaging/aspose.imaging/datarecoverymode): The maximal recovery mode recovers all data even if the file format has a corrupted structure and further processing may yield unexpected effects.

Below is sample code that shows how to use the two data recovery modes.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-TiffDataRecovery-TiffDataRecovery.cs" >}}



When a damaged or corrupted TIFF file is loaded or saved without using data recovery you may get an Aspose.Imaging.Exceptions.Compressors exception.
## **TiffOptions Configuration**
Developers can adjust different properties of [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) class to get desired results. In this document, we will focus on 4 main properties that controls the resultant image attributes.

These properties are listed below.

1. [TiffOptions.Photometric](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions/properties/predictor)

Whenever we initialize an empty [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) structure, each option is set to its default value, for instance compression is set to None, BitsPerSample is set as 1 and Photometric as MinIsWhite. Saving into this format will make the final image black n white and this is expected behavior for such options combination. In order to get the colored results you have to set all the above mentioned properties to values that correspond to desired color space or you can initialize the [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) structure with predefined settings as discussed later in this article. Provided below is a table describing the expected parameter values that you can set in order to achieve desired results. Please note, you should set all 4 columns through [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) in order to save any loaded/created image to TIFF file format.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16 (palette, color mode) single channel only|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (gray-scale mode) single channel only|None|
|Palette|LZW/Uncompressed|8 (palette, color mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (gray-scale mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|RGB|LZW/Uncompressed|[8,8,8] (3 RGB channels)|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 RGB channels and additional alpha channel may be set through TiffOptions.AlphaStorage) Actually any additional channels count is supported but each channel must have 8 bit size like [8,8,8,8,8,8]|None/Horizontal|
All 4 properties should be set through TiffOptions in order to save any image format to Tiff format. When employing different combinations, some viewers (including the Windows Photo Viewer) may refuse to render the resultant image due to the limited support they offer. In such case, please pick different viewer for your testing.
### **Predefined Settings for TiffOptions Class**
In order to facilitate the users and to avoid the miss-configuration of the [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) instance, the Aspose.Imaging for .NET API has exposed another constructor that accepts a parameter of type TiffExpectedFormat. Based on the selected value from the TiffExpectedFormat enumeration, the API auto configures all the mandatory properties for the [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) instance in order to produce the desired results. Before we move towards the sample code, here is the list of the TiffExpectedFormat fields and their details for better understanding of the usage.

1. TiffExpectedFormat.Default: Setting the field to Default acts similar to the default constructor of [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) class with no compression set and BitsPerPixel set to 1 in order to produce a black n white result. It is advised to use this field when other format specific properties are to be set manually according to the desired results.
1. TiffExpectedFormat.TiffCcitRle: Specific to RLE encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffCcittFax3: Specific to CCITT Fax3 encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffCcittFax4: Specific to CCITT Fax4 encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffDeflateBW: Specific to Deflate compression while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffDeflateRGB: Specific to Deflate compression while saving the result in RGB (color) TIFF format.
1. TiffExpectedFormat.TiffJpegRGB: Specific to Jpeg compression while saving the result in RGB (color) TIFF format.
1. TiffExpectedFormat.TiffJpegYCBCR: Specific to Deflate compression while saving the result in YCBCR (color) TIFF format.
1. TiffExpectedFormat.TiffLzwBW: Specific to LZW compression while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffLzwRGB: Specific to LZW compression while saving the result in RGB (color) TIFF format.
1. TiffExpectedFormat.TiffLzwRGBA: Specific to LZW compression while saving the result in RGBA (color with transparency) TIFF format.
1. TiffExpectedFormat.TiffNoCompressionBW: Specific to uncompressed TIFF format while saving the result in 1 BitsPerPixel (black n white).
1. TiffExpectedFormat.TiffNoCompressionRGB: Specific to uncompressed TIFF format while saving the result in RGB (color).
1. TiffExpectedFormat.TiffNoCompressionRGBA: Specific to uncompressed TIFF format while saving the result in RGBA (color with transparency).

The following code snippet elaborates the usage of TiffExpectedFormat fields while creating an instance of [Tiffoptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/tiffoptions) class.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}


## **Support for Deflate and Adobe Deflate Compression**
The TIFF (Tagged Image File Format) file format supports various types of compression whereas the compression type is stored as a tag (an integer value) in the file. One of such compression methods is Adobe Deflate (previously known as Deflate). Since the release of Aspose.Imaging for .NET 2.6.0, the API supports this compression method for loading, converting & creating TIFF images.
### **Loading Image**
Aspose.Imaging for .NET API hides all the ugly details from the user and provides an easy to use mechanism to load images for further processing. In order to load a TIFF image having Adobe Deflate compression, user has to pass the file path location or stream object to the Image.Load method and cast the object to [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage) as per requirement.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-LoadingFile-LoadingFile.cs" >}}
### **Support Tiff deflate Images with Alpha**
Aspose.Imaging for .NET API hides all the ugly details from the user and provides an easy to use mechanism to load images for further processing. In order to load a TIFF image and save that with Deflate compression with Alpha, user has to pass the file path location or stream object to the Image.Load method and cast the object to [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage) as per requirement.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-LoadingFile-LoadingFile.cs" >}}
### **Saving Image**
Converting any raster image to TIFF with Deflate/Adobe Deflate compression is easy as follow.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SavingRasterImageToTIFFWithCompression-SavingRasterImageToTIFFWithCompression.cs" >}}


### **Creating Image**
Below provided sample demonstrates the usage of Aspose.Imaging for .NET API to create an image from scrach using the Adobe Deflate compression method.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-CreatingTIFFImageWithCompression-CreatingTIFFImageWithCompression.cs" >}}


## **Compressing TIFF Images**
Aspose.Imaging for .NET API can be used to convert other raster formats to TIFF image format and even change the compression of existing TIFF image. The API can also be used to store different images as frames in a TIFF image for archiving purposes while compressing the images to lowest data size. The image compression in any case should be performed by reducing the source data size regardless of the compression algorithm used. In order to achieve the best compression ratio we may use indexed color spaces. The below provided code snippet performs the best compression using 16 indexed colors only and LZW compression algorithm however the source colors are slightly dithered.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-CompressingTIFFImagesWithLZWAlgorithm-CompressingTIFFImagesWithLZWAlgorithm.cs" >}}



Another approach which can be used since the release of Aspose.Imaging for .NET v2.6.0 is by using the Adobe Deflate compression as demonstrated below.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-CompressingTIFFImagesWithAdobeDeflateCompression-CompressingTIFFImagesWithAdobeDeflateCompression.cs" >}}


## **Splitting TIFF Frames**
A Tiff image can have multiple frames and a requirement may arise to split these frames into several images. This article demonstrates the use of Aspose.Imaging for .NET API to achieve this requirement in an efficient manner with a few lines of code.
### **Saving Each Frame in TIFF Format**
Splitting the Tiff frames is easy and can be achieved in below simple steps.

1. Firstly, create an instance of [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage) and load a Tiff file from the disk/stream.
1. Iterate over the Tiff frame collection.
1. Save each frame to disc in Tiff format.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SplittingTiffFrames-SplittingTiffFrames.cs" >}}


### **Saving Each Frame in Other Format**
Most of the process is the same as discussed above with a minor change, that is; while saving the frame to disc, you may pass an object of the ImageOptionBase according to the desired raster image format. Below provided code snippet demonstrates this concept by saving each frame in PNG format.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SavingEachFrameInOtherRasterImageFormat-SavingEachFrameInOtherRasterImageFormat.cs" >}}
## **Memory strategy optimization**
Loading of Tiff images can be proceeded using memory strategy optimization - ie limiting memory buffer size for operation.

{{< gist "aspose-com-gists" "7c81f4ab364d8398de3d9d7f5edbc48c" "MemoryStrategyOptimizationTiff.cs" >}}
## **Tiff image export in batch mode**
Aspose.Imaging library supports possibility of batch conversion before saving (exporting) Tiff images. This makes it possible not to keep in memory the resources of all processed pages at the same time, which will certainly give a significant performance boost with a lack of memory. With enough memory, the performance in standard mode and batch mode is the same, but the memory consumption in batch mode is much lower for multi-page tiff images (see illustrations below).

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Tiff-batch-mode-example.cs" >}}
## **Support for extracting paths from TIFF**
#### **Clipping Path**
Clipping path is the Photoshop technique to remove the background from an image. Photoshop allows you to select a part of an image using Clipping Path and save the path within a file. Clipping Paths allow you to hide the part of an image you don't want to appear. Anything inside the clipping path will be visible, but anything outside of it will be transparent.

Other words Photoshop makes it possible to isolate certain parts of an image, without permanently changing the layer. This allows you to tweak the image at any point in the creative process. Clipping Paths are a traditional method of cutting out objects or people in Photoshop that allows you to create image files with transparent backgrounds. This approach works best with objects or people with "hard" edges around the object or person you want to cut out.
#### **Access Clipping Paths in TIFF image**
*PathResources* property allows you to access Clipping Paths in TIFF frame. The following code retrieves paths from TIFF image and displays their names in the console:

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Access-Clipping-Path-In-Tiff-Image.cs" >}}
#### **Modify existing Clipping Paths**
You can easily modify already existing Clipping Paths. For instance, you can keep only one Clipping Path in the image:

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Modify-Clipping-Path-In-Tiff-Image.cs" >}}
#### **Create Clipping Path manually**
You can manually create Clipping Path in TIFF image. In order to do that you need to create an instance of *PathResource* class. The following code demonstrates the way how you can create an empty path in TIFF image:

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Create-Clipping-Path-Manually.cs" >}}

#### **Get existing Clipping Path**
The following code shows how to get existing Clipping Path from TIFF image:
{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-get-existing-clipping-path.cs" >}}

#### **Change Clipping Path**
In case if you have multiple paths in TIFF image you can easily change which of them is Clipping Path:
{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-change-clipping-path.cs" >}}

#### **Create Clipping Path from scratch**
The following source code sample demonstrates how to create paths in TIFF image from scratch:
{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-create-clipping-path-from-scratch.cs" >}}


#### **Clipping Path content**
To create your own Clipping Paths you need to understand their content. Photoshop stores its paths as resources with IDs in the range 2000 through 2997. The name of the resource is the name given to the path when it was saved. If the file contains a resource with an ID of 2999, then this resource contains the name of the clipping path. Each path has a set of records to hold the data.

**Record classes:** 
*LengthRecord* - contains the number of Bezier knot records.
*BezierKnotRecord* - describes the knots of the path.
*ClipboardRecord* - contains four fixed-point numbers for the bounding rectangle.

More details you can find in [Adobe Photoshop File Formats Specification](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/).
