---
title: Public API Changes in Aspose.Imaging 3.0.0
type: docs
weight: 130
url: /net/public-api-changes-in-aspose-imaging-3-0-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.9.0 to 3.0.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added APIs](/imaging/net/public-api-changes-in-aspose-imaging-3-0-0-html/) and [removed APIs](/imaging/net/public-api-changes-in-aspose-imaging-3-0-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Support for DjVu Format Added**
Aspose.Imaging for .NET 3.0.0 has introduced a series of new classes, methods, enumerations and properties to correctly process the images of type DjVu. Details of newly added APIs are as follow:

- Class Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent: To be used for the representation of DirmChunk in Djvu file format for Djvu page. It can be accessed from Header Property of DjvuPage class.
- Class Aspose.Imaging.FileFormats.Djvu.DjvuImage: Represents the base DjVu file format class.
- Class Aspose.Imaging.FileFormats.Djvu.DjvuPage: Represents the DjVu file format page with all needed properties.
- Class Aspose.Imaging.FileFormats.Djvu.DjvuRaster: Represents raster operation result for DjVu file format. For example: getting background image or getting foreground image of the page.
- Class Aspose.Imaging.ImageOptions.DjvuMultiPageOptions: Specifies the multipage DjVu export pages options.
- Event Aspose.Imaging.FileFormats.Djvu.DjvuPage.PageExportedAction: Action that will be fired when page has been exported to some format.
- Event Aspose.Imaging.FileFormats.Djvu.DjvuImage(DjvuPage).PropertyChanged: Action that will be fired when some property has changed its value.
- Field-Enum Aspose.Imaging.FileFormat.Djvu: Field representing the DjVu file format.
- Method Aspose.Imaging.FileFormats.Djvu.DjvuImage.LoadDocument(System.IO.Stream): Loads DjVu image from stream.
- Method Aspose.Imaging.FileFormats.Djvu.DjvuPage.ExtractThumbnailImage: Extracts the thumbnail image for DjVu page.
- Method Aspose.Imaging.FileFormats.Djvu.DjvuPage.GetBackgroundImage(System.Int32): Extracts the Background layer for DjvuPage with specified subsample (default value is 1).
- Method Aspose.Imaging.FileFormats.Djvu.DjvuPage.GetForegroundImage(System.Int32): Extracts foreground layer for DjvuPage with specified subsample (default is 1).
- Method Aspose.Imaging.FileFormats.Djvu.DjvuPage.GetTextImage(System.Int32): Extracts the mask layer for DjvuPage with specified subsample (default is 1).
- Method Aspose.Imaging.ImageOptions.DjvuMultiPageOptions.CheckModeAvailability(Aspose.Imaging.ImageOptions.MultiPageMode): Checks if mode is available for using.
- Method Aspose.Imaging.ImageOptions.DjvuMultiPageOptions ctor: Offers a set of constructors to initialize DjvuMultipage export options that can be used with number of page to export, range of pages, range of pages and extract only specified area.
- Method Aspose.Imaging.ImageOptions.MultiPageOptions ctor: Offers a set of constructors to initialize MultiPageOptions export options that can be used with number of page to export, range of pages, range of pages and extract only specified area.
- Property Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent.HasName: Indicates if DjVu header has name.
- Property Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent.HasTitle: Indicates if DjVu header has title.
- Property Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent.ID: The DjVu header ID.
- Property Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent.Name: The DjVu header name.
- Property Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent.Offset: The DjVu header offset from beginning.
- Property Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent.Size: The DjVu header size.
- Property Aspose.Imaging.FileFormats.Djvu.DataChunks.Directory.DirmComponent.Title: The DjVu header title.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.ActivePage: Represents current active page.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.FirstPage: Represents first page in DjVu image.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.Height: Gets the height of current active page.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.Identifier: Gets the DjVu image identifier.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.LastPage: Gets the last page in DjVu image.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.NextPage: Gets the next page in DjVu image.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.Pages: Represents the pages in DjVu image.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuImage.Width: Gets the width of current active page in DjVu image.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.Header: Gets the header of DjVu page.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.Height: Gets the height of page.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.Width: Gets the width of page.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.Image: Gets the raster representation of page image.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.IsColor: Indicates if this page is colored.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.PageNumber: Gets the page number.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.ParentImage: Gets the parent image for this page.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuPage.ThumbnailImage: Gets raster representation for DjvuPage thumbnail image.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuRaster.Height: Gets the height of current instance.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuRaster.Width: Gets the width of current instance.
- Property Aspose.Imaging.FileFormats.Djvu.DjvuRaster.Length: Gets the colors length for current DjVu raster representation.
### **Optimized Performance**
In order to improve the overall performance of core processing, the Aspose.Imaging for .NET 3.0.0 has added new interfaces and methods. Color is represented as 32-bit ARGB integer structure where there are 4 color channels and they are stored in the following order: | A | R | G | B |

New methods have parameters int[] instead Color[] or int instead Color. Also names of the newly exposed methods have the prefix Argb32 whereas the old interfaces (using Colors) remained unchanged.

**Added Interfaces** 
Class Aspose.Imaging.IPartialArgb32PixelLoader
Method Aspose.Imaging.IPartialArgb32PixelLoader.Process(Aspose.Imaging.Rectangle,System.Int32[],Aspose.Imaging.Point,Aspose.Imaging.Point)
Class Aspose.Imaging.IRasterImageArgb32PixelLoader
Method Aspose.Imaging.IRasterImageArgb32PixelLoader.LoadPartialArgb32Pixels(Aspose.Imaging.Rectangle,Aspose.Imaging.IPartialArgb32PixelLoader)

**Added Methods for IColorPalette** 
Method Aspose.Imaging.IColorPalette.GetArgb32Color(System.Int32)
Method Aspose.Imaging.IColorPalette.GetNearestColorIndex(System.Int32)
Property Aspose.Imaging.IColorPalette.Argb32Entries

**Implementation of Palette Classes** 
Method Aspose.Imaging.ColorPalette.#ctor(System.Int32[])
Method Aspose.Imaging.ColorPalette.#ctor(System.Int32[],System.Boolean)
Method Aspose.Imaging.ColorPalette.GetArgb32Color(System.Int32)
Method Aspose.Imaging.ColorPalette.GetNearestColorIndex(System.Int32)
Property Aspose.Imaging.ColorPalette.Argb32Entries
Method Aspose.Imaging.FileFormats.Psd.PsdColorPalette.#ctor(System.Int32[],System.Boolean)
Method Aspose.Imaging.FileFormats.Psd.PsdColorPalette.GetArgb32Color(System.Int32)
Method Aspose.Imaging.FileFormats.Psd.PsdColorPalette.GetNearestColorIndex(System.Int32)
Property Aspose.Imaging.FileFormats.Psd.PsdColorPalette.Argb32Entries

**Color Converters** 
Method Aspose.Imaging.CMYKColor.ToArgb32(Aspose.Imaging.CMYKColor[])
Method Aspose.Imaging.CMYKColor.ToCMYK(System.Int32)
Method Aspose.Imaging.CMYKColor.ToCMYK(System.Int32[])

**Get/Load Argb32 Pixels Methods** 
Method Aspose.Imaging.RasterImage.GetArgb32Pixel(System.Int32,System.Int32)
Method Aspose.Imaging.RasterImage.GetDefaultArgb32Pixels(Aspose.Imaging.Rectangle)
Method Aspose.Imaging.RasterImage.GetDefaultPixels(Aspose.Imaging.Rectangle,Aspose.Imaging.IPartialArgb32PixelLoader)
Method Aspose.Imaging.RasterImage.LoadArgb32Pixels(Aspose.Imaging.Rectangle)
Method Aspose.Imaging.RasterImage.LoadPartialArgb32Pixels(Aspose.Imaging.Rectangle,Aspose.Imaging.IPartialArgb32PixelLoader)
Method Aspose.Imaging.RasterImage.LoadPixelsInternal(Aspose.Imaging.Rectangle,Aspose.Imaging.IPartialArgb32PixelLoader)

**Set/Save Argb32 Pixels Methods** 
Method Aspose.Imaging.RasterImage.SetArgb32Pixel(System.Int32,System.Int32,System.Int32)
Method Aspose.Imaging.RasterImage.SaveArgb32Pixels(Aspose.Imaging.Rectangle,System.Int32[])
Method Aspose.Imaging.RasterImage.SavePixelsInternal(Aspose.Imaging.Rectangle,System.Int32[])
Method Aspose.Imaging.RasterCachedImage.SavePixelsInternal(Aspose.Imaging.Rectangle,System.Int32[])

**Other APIs** 
Method Aspose.Imaging.Image.GetFitRectangle(Aspose.Imaging.Rectangle,System.Int32[])
Method Aspose.Imaging.Image.GetFittingRectangle(Aspose.Imaging.Rectangle,System.Int32[],System.Int32,System.Int32)
Property Aspose.Imaging.FileFormats.Psd.Resources.ThumbnailResource.ThumbnailArgb32Data

Working with new methods is similar as of the methods with Color arguments, for instance following is the code to load pixels with new implementation.

**C#**

{{< highlight csharp >}}

 using (RasterImage image = (RasterImage)Image.Load(fileName))

{

    int[] pixels = image.LoadArgb32Pixels(image.Bounds);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As RasterImage = CType(Image.Load(fileName), RasterImage)

	Dim pixels() As Integer = image.LoadArgb32Pixels(image.Bounds)

End Using

{{< /highlight >}}

Following is the code to save pixels with new implementation.

**C#**

{{< highlight csharp >}}

 int[] pixels;

using (RasterImage image = new BmpImage(width, height))

{

    image.SaveArgb32Pixels(image.Bounds, pixels);

    image.Save(outFileName);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim pixels() As Integer

Using image As RasterImage = New BmpImage(width, height)

	image.SaveArgb32Pixels(image.Bounds, pixels)

	image.Save(outFileName)

End Using

{{< /highlight >}}
### **Improved Tiff Base Types Layout**
The following methods and properties only serve the purpose of proper data layout so that data offset starts at word boundary. The methods does not influence the way you work with ExifData and therefore you may follow the same approach used before. The only addition is usage of 3 properties such as CommonTags, ExifTags and GPSTags.

While setting the properties to another set of tags please keep in mind that all tags set in the ExifTags property will go to exif section only. The tags set in GPSTags property will go to GPS section only. The tags set in the CommonTags will go to common section only. However there are properties that when set, the ExifData class tries to put each tag into corresponding location according to tag ID. For example if you set several tags for properties such as ExifProperties.Copyright, ExifProperties.PixelXDimension, ExifProperties.GPSAreaInformation will end up in each tag being set for each section individually. When you get the Properties value you will receive all tags regardless of section placement.

Aspose.Imaging for .NET 3.0.0 has exposed the class Aspose.Imaging.Exif.TiffDataTypeController which serves as container for EXIF data type manipulation. This release has also made the ExifData class inherit from TiffDataTypeController class and implemented the following helper methods to work with EXIF data types.

- Method Aspose.Imaging.Exif.ExifData.#ctor(Aspose.Imaging.FileFormats.Tiff.TiffDataType[],Aspose.Imaging.FileFormats.Tiff.TiffDataType[],Aspose.Imaging.FileFormats.Tiff.TiffDataType[])
- Method Aspose.Imaging.Exif.ExifData.GetShortOrLong(System.UInt16)
- Method Aspose.Imaging.Exif.ExifData.RemoveTag(System.UInt16)
- Method Aspose.Imaging.Exif.ExifData.SetShortOrLong(System.UInt16,System.UInt32,System.Int32)
- Method Aspose.Imaging.Exif.JpegExifData.#ctor(Aspose.Imaging.FileFormats.Tiff.TiffDataType[])
- Method Aspose.Imaging.Exif.JpegExifData.#ctor(Aspose.Imaging.FileFormats.Tiff.TiffDataType[],Aspose.Imaging.FileFormats.Tiff.TiffDataType[],Aspose.Imaging.FileFormats.Tiff.TiffDataType[])
- Method Aspose.Imaging.Exif.JpegExifData.SerializeExifData
- Method Aspose.Imaging.Exif.TiffDataTypeController.#ctor
- Method Aspose.Imaging.Exif.TiffDataTypeController.Exists(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetSectionTags(System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffByteValue(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffLongTypeValue(System.UInt16,System.UInt32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffRationalArray(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffRationalValue(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffShortArray(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffShortValue(System.UInt16,System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffSRationalValue(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffStringValue(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffType(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.GetTiffUndefinedValue(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.RemoveTagByID(System.UInt16)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetSectionTags(System.Int32,Aspose.Imaging.FileFormats.Tiff.TiffDataType[])
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffByteValue(System.UInt16,System.Byte[],System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffLongTypeValue(System.UInt16,System.UInt32,System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffRational(System.UInt16,Aspose.Imaging.FileFormats.Tiff.TiffRational,System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffRationalArray(System.UInt16,Aspose.Imaging.FileFormats.Tiff.TiffRational[],System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffShortArray(System.UInt16,System.UInt16[],System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffShortValue(System.UInt16,System.UInt16,System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffSRationalValue(System.UInt16,Aspose.Imaging.FileFormats.Tiff.TiffSRational,System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffStringValue(System.UInt16,System.String,System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffType(Aspose.Imaging.FileFormats.Tiff.TiffDataType,System.Int32)
- Method Aspose.Imaging.Exif.TiffDataTypeController.SetTiffUndefinedValue(System.UInt16,System.Byte[],System.Int32)
- Method Aspose.Imaging.ImageOptions.TiffOptions.GetValidTagsCount(Aspose.Imaging.FileFormats.Tiff.TiffDataType[])
- Property Aspose.Imaging.Exif.ExifData.IsBigEndian
- Property Aspose.Imaging.FileFormats.Tiff.TiffDataType.AlignedDataSize
## **Removed Classes and Properties**
### **Method JpegExifData.EstimateExifSize Removed**
The method Aspose.Imaging.Exif.JpegExifData.EstimateExifSize has been removed with Aspose.Imaging for .NET 3.0.0. It is advised to use the newly added method Aspose.Imaging.Exif.JpegExifData.SerializeExifData which gives a serialized data stream and you can query its size afterwards.
### **APIs Removed in Reference to Performance Improvements**
Following APIs have been removed since the release of Aspose.Imaging for .NET 3.0.0.

- Class Aspose.Imaging.IPartialCMYKPixelLoader
- Method Aspose.Imaging.Image.GetFitRectangle(Aspose.Imaging.Rectangle,Aspose.Imaging.Color[])
- Method Aspose.Imaging.Image.GetFittingRectangle(Aspose.Imaging.Rectangle,Aspose.Imaging.Color[],System.Int32,System.Int32)
- Method Aspose.Imaging.IPartialCMYKPixelLoader.Process(Aspose.Imaging.Rectangle,Aspose.Imaging.CMYKColor[],Aspose.Imaging.Point,Aspose.Imaging.Point)
- Method Aspose.Imaging.RasterCachedImage.SavePixelsInternal(Aspose.Imaging.Rectangle,Aspose.Imaging.Color[])
- Method Aspose.Imaging.RasterImage.GetDefaultPixels(Aspose.Imaging.Rectangle)
- Method Aspose.Imaging.RasterImage.GetDefaultPixels(Aspose.Imaging.Rectangle,Aspose.Imaging.IPartialPixelLoader)
- Method Aspose.Imaging.RasterImage.LoadPixelsInternal(Aspose.Imaging.Rectangle,Aspose.Imaging.IPartialPixelLoader)
- Method Aspose.Imaging.RasterImage.SavePixelsInternal(Aspose.Imaging.Rectangle,Aspose.Imaging.Color[])
