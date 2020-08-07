---
title: Manipulating DjVu Formats
type: docs
weight: 40
url: /net/manipulating-djvu-formats/
---

## **Converting DjVu to TIFF Format**
Aspose.Imaging APIs are capable of loading DjVu files for possible conversion to raster image formats. This example demonstrates the usage of Aspose.Imaging for .NET API to convert a DjVu file having multiple pages to a multipage TIFF image. You can convert a DjVu file having multiple pages to TIFF image as elaborated below.

1. Load the DjVu file into an instance of [DjvuImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.djvu/djvuimage).
1. Create an instance of TiffOptions while using any of the TiffExpectedFormat enumeration fields.
1. Create an instance of [DjvuMultiPageOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/djvumultipageoptions) and set it as MultiPageOptions property of the TiffOptions created in previous step.
1. Call Image.Save by passing the file path (or an object of MemoryStream) as well as the instance of TiffOptions.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Djvu-ConvertDjVuToTIFF-ConvertDjVuToTIFF.cs" >}}


## **Converting Range of DjVu Pages**
A DjVu image may have more than one pages like a multipage TIFF or multiframe GIF. If such DjVu image has to be converted to any raster format that could have more than one page or frame then be default, all pages of DjVu are exported. Aspose.Imaging APIs also provides the facility to convert only specific range of DjVu pages to multipage TIFF or multiframe GIF. You can convert a specific range of DjVu pages to multiframe GIF or TIFF using the simple steps as elaborated below.

1. Load the DjVu file into an instance of [DjvuImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.djvu/djvuimage).
1. Create an instance of TiffOptions or GifOptions.
1. Create an instance of IntRange and initialize it with range of pages to be exported.
1. Create an instance of [DjvuMultiPageOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/djvumultipageoptions) with instance of IntRange as parameter and set it as MultiPageOptions property of the ImageOptionsBase created in step 2.
1. Call Image.Save by passing the file path (or an object of MemoryStream) as well as the instance of ImageOptionsBase.

Here is the source code to convert first 2 pages of DjVu to TIFF format.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Djvu-ConvertRangeOfDjVuPages-ConvertRangeOfDjVuPages.cs" >}}



Following code snippet converts the first 2 pages of DjVu to GIF format.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Djvu-DjVuToGIF-DjVuToGIF.cs" >}}


## **Converting Range of DjVu Pages to Separate Images**
It is possible to [convert only a specific range of DjVu pages to multipage TIFF or multiframe GIF]() where the resultant image will contain multiple pages/frames. Aspose.Imaging APIs also provide the means to convert the specific range of DjVu pages to raster image formats that do not support layering such as BMP, PNG & JPEG. In this case each DjVu page will be converted to a separate image. You can convert a specific range of DjVu pages to separate images using the simple steps as elaborated below.

1. Load the DjVu file into an instance of [DjvuImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.djvu/djvuimage).
1. Create an instance of ImageOptionsBase.
1. Create an instance of IntRange and initialize it with range of pages to be exported.
1. Create an instance of [DjvuMultiPageOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/djvumultipageoptions) while passing the indices of DjVu pages as parameter and set it as MultiPageOptions property of the ImageOptionsBase created in step 2.
1. Call Image.Save by passing the file path (or an object of MemoryStream) as well as the instance of ImageOptionsBase.

Here is the source code to convert first 2 pages of DjVu to BMP format.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Djvu-ConvertSpecificPortionOfDjVuPage-ConvertSpecificPortionOfDjVuPage.cs" >}}


## **Converting Specific Portion of DjVu Page**
Aspose.Imaging APIs provides an easy to use mechanism to export only a specific portion of DjVu page to raster image formats. Aspose.Imaging for .NET API has exposed an overload version of [DjvuMultiPageOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/djvumultipageoptions) constructor that can accept an integer parameter for DjVu page index and an instance of Rectangle to specify the desired area to be exported. You can convert a specific portion of DjVu page to image using the simple steps as elaborated below.

1. Load the DjVu file into an instance of [DjvuImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.djvu/djvuimage).
1. Create an instance of ImageOptionsBase.
1. Create an instance of [DjvuMultiPageOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/djvumultipageoptions) while passing the index of DjVu page along with an instance of Rectangle as parameter, and set it as MultiPageOptions property of the ImageOptionsBase created in step 2.
1. Call Image.Save by passing the file path (or an object of MemoryStream) as well as the instance of ImageOptionsBase.

Here is the source code to convert a portion of 1st page of DjVu to PNG format.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Djvu-ConvertSpecificPortionOfDjVuPage-ConvertSpecificPortionOfDjVuPage.cs" >}}


## **Converting DjVu to PDF Format**
Aspose.Imaging APIs provides the functionality to export the DjVu files to raster images as well as PDF format. This article demonstrates the usage of Aspose.Imaging for .NET API to export the DjVu pages to PDF format. You can convert a specific range of DjVu pages to PDF format using the simple steps as elaborated below.

1. Load the DjVu file into an instance of [DjvuImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.djvu/djvuimage).
1. Create an instance of PdfOptions.
1. Create an instance of IntRange and initialize it with range of pages to be exported.
1. Create an instance of [DjvuMultiPageOptions](http://www.aspose.com/api/net/imaging/aspose.imaging.imageoptions/djvumultipageoptions) while passing the indices of DjVu pages as parameter and set it as MultiPageOptions property of the PdfOptions created in step 2.
1. Call Image.Save by passing the file path (or an object of MemoryStream) as well as the instance of PdfOptions.

Here is the source code to convert first 5 pages of DjVu to PDF format.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-Djvu-ConvertDjVuToPDF-ConvertDjVuToPDF.cs" >}}
## **Image Processing using Multithreading**
Aspose.Imaging is multithread safe as long as only one thread works on a Document at a time. It is a typical scenario to have one thread working on one document.This article demonstrates how Aspose.Imaging for .NET supports parallel DJVU images processing using multithreading.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-CSharp-ModifyingAndConvertingImages-DjVu-ParallelDJVUImagesProcessingUsingMultithreading-ParallelDJVUImagesProcessingUsingMultithreading.cs" >}}
## **Memory Strategy optimization**
Loading of Djvu images can be proceeded using memory strategy optimization - ie limiting memory buffer size for operation.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "MemoryStrategyOptimizationDJVU.cs" >}}






