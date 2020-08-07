---
title: Public API Changes in Aspose.Imaging 3.0.1
type: docs
weight: 130
url: /java/public-api-changes-in-aspose-imaging-3-0-1/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.9.1 to 3.0.1 that may be of interest to module/application developers. It includes not only new and updated public methods, [added APIs](/imaging/java/public-api-changes-in-aspose-imaging-3-0-1-html/) and [removed APIs](/imaging/java/public-api-changes-in-aspose-imaging-3-0-1-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Support for DjVu Format Added**
Aspose.Imaging for Java 3.0.1 has introduced a series of new classes, methods, enumerations and properties to correctly process the images of type DjVu. Details of newly added APIs are as follow:

- Class com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent: To be used for the representation of DirmChunk in Djvu file format for Djvu page. It can be accessed from Header Property of DjvuPage class.
- Class com.aspose.imaging.fileformats.djvu.DjvuImage: Represents the base DjVu file format class.
- Class com.aspose.imaging.fileformats.djvu.DjvuPage: Represents the DjVu file format page with all needed properties.
- Class com.aspose.imaging.fileformats.djvu.DjvuRaster: Represents raster operation result for DjVu file format. For example: getting background image or getting foreground image of the page.
- Class com.aspose.imaging.imageoptions.DjvuMultiPageOptions: Specifies the multipage DjVu export pages options.
- Event com.aspose.imaging.fileformats.djvu.DjvuPage.PageExportedAction: Action that will be fired when page has been exported to some format.
- Event com.aspose.imaging.fileformats.djvu.DjvuImage(DjvuPage).PropertyChanged: Action that will be fired when some property has changed its value.
- Field-Enum com.aspose.imaging.fileFormat.Djvu: Field representing the DjVu file format.
- Method com.aspose.imaging.fileformats.djvu.DjvuImage.LoadDocument(InputStream): Loads DjVu image from stream.
- Method com.aspose.imaging.fileformats.djvu.DjvuPage.ExtractThumbnailImage: Extracts the thumbnail image for DjVu page.
- Method com.aspose.imaging.fileformats.djvu.DjvuPage.GetBackgroundImage(int): Extracts the Background layer for DjvuPage with specified subsample (default value is 1).
- Method com.aspose.imaging.fileformats.djvu.DjvuPage.GetForegroundImage(int): Extracts foreground layer for DjvuPage with specified subsample (default is 1).
- Method com.aspose.imaging.fileformats.djvu.DjvuPage.GetTextImage(int): Extracts the mask layer for DjvuPage with specified subsample (default is 1).
- Method com.aspose.imaging.imageoptions.DjvuMultiPageOptions.CheckModeAvailability(com.aspose.imaging.imageoptions.MultiPageMode): Checks if mode is available for using.
- Method com.aspose.imaging.imageoptions.DjvuMultiPageOptions ctor: Offers a set of constructors to initialize DjvuMultipage export options that can be used with number of page to export, range of pages, range of pages and extract only specified area.
- Method com.aspose.imaging.imageoptions.MultiPageOptions ctor: Offers a set of constructors to initialize MultiPageOptions export options that can be used with number of page to export, range of pages, range of pages and extract only specified area.
- Property com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent.HasName: Indicates if DjVu header has name.
- Property com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent.HasTitle: Indicates if DjVu header has title.
- Property com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent.ID: The DjVu header ID.
- Property com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent.Name: The DjVu header name.
- Property com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent.Offset: The DjVu header offset from beginning.
- Property com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent.Size: The DjVu header size.
- Property com.aspose.imaging.fileformats.djvu.datachunks.directory.DirmComponent.Title: The DjVu header title.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.ActivePage: Represents current active page.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.FirstPage: Represents first page in DjVu image.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.Height: Gets the height of current active page.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.Identifier: Gets the DjVu image identifier.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.LastPage: Gets the last page in DjVu image.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.NextPage: Gets the next page in DjVu image.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.Pages: Represents the pages in DjVu image.
- Property com.aspose.imaging.fileformats.djvu.DjvuImage.Width: Gets the width of current active page in DjVu image.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.Header: Gets the header of DjVu page.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.Height: Gets the height of page.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.Width: Gets the width of page.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.Image: Gets the raster representation of page image.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.IsColor: Indicates if this page is colored.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.PageNumber: Gets the page number.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.ParentImage: Gets the parent image for this page.
- Property com.aspose.imaging.fileformats.djvu.DjvuPage.ThumbnailImage: Gets raster representation for DjvuPage thumbnail image.
- Property com.aspose.imaging.fileformats.djvu.DjvuRaster.Height: Gets the height of current instance.
- Property com.aspose.imaging.fileformats.djvu.DjvuRaster.Width: Gets the width of current instance.
- Property com.aspose.imaging.fileformats.djvu.DjvuRaster.Length: Gets the colors length for current DjVu raster representation.
### **Improved Tiff Base Types Layout**
The following methods and properties only serve the purpose of proper data layout so that data offset starts at word boundary. The methods does not influence the way you work with ExifData and therefore you may follow the same approach used before. The only addition is usage of 3 properties such as CommonTags, ExifTags and GPSTags.

While setting the properties to another set of tags please keep in mind that all tags set in the ExifTags property will go to exif section only. The tags set in GPSTags property will go to GPS section only. The tags set in the CommonTags will go to common section only. However there are properties that when set, the ExifData class tries to put each tag into corresponding location according to tag ID. For example if you set several tags for properties such as ExifProperties.Copyright, ExifProperties.PixelXDimension, ExifProperties.GPSAreaInformation will end up in each tag being set for each section individually. When you get the Properties value you will receive all tags regardless of section placement.

Aspose.Imaging for Java 3.0.1 has exposed the class com.aspose.imaging.exif.TiffDataTypeController which serves as container for EXIF data type manipulation. This release has also made the ExifData class inherit from TiffDataTypeController class and implemented the following helper methods to work with EXIF data types.

- Method com.aspose.imaging.exif.ExifData.#ctor(com.aspose.imaging.fileformats.tiff.TiffDataType[],com.aspose.imaging.fileformats.tiff.TiffDataType[],com.aspose.imaging.fileformats.tiff.TiffDataType[])
- Method com.aspose.imaging.exif.ExifData.GetShortOrLong(int)
- Method com.aspose.imaging.exif.ExifData.RemoveTag(int)
- Method com.aspose.imaging.exif.ExifData.SetShortOrLong(int,int,int)
- Method com.aspose.imaging.exif.JpegExifData.#ctor(com.aspose.imaging.fileformats.tiff.TiffDataType[])
- Method com.aspose.imaging.exif.JpegExifData.#ctor(com.aspose.imaging.fileformats.tiff.TiffDataType[],com.aspose.imaging.fileformats.tiff.TiffDataType[],com.aspose.imaging.fileformats.tiff.TiffDataType[])
- Method com.aspose.imaging.exif.JpegExifData.SerializeExifData
- Method com.aspose.imaging.exif.TiffDataTypeController.#ctor
- Method com.aspose.imaging.exif.TiffDataTypeController.Exists(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetSectionTags(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffByteValue(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffLongTypeValue(int,int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffRationalArray(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffRationalValue(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffShortArray(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffShortValue(int,int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffSRationalValue(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffStringValue(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffType(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.GetTiffUndefinedValue(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.RemoveTagByID(int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetSectionTags(int, com.aspose.imaging.fileformats.tiff.TiffDataType[])
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffByteValue(int, Byte[],int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffLongTypeValue(int, int, int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffRational(int, com.aspose.imaging.fileformats.tiff.TiffRational, int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffRationalArray(int, com.aspose.imaging.fileformats.tiff.TiffRational[],int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffShortArray(int, int[], int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffShortValue(int, int, int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffSRationalValue(int, com.aspose.imaging.fileformats.tiff.TiffSRational, int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffStringValue(int, String, int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffType(com.aspose.imaging.fileformats.tiff.TiffDataType, int)
- Method com.aspose.imaging.exif.TiffDataTypeController.SetTiffUndefinedValue(int, Byte[],int)
- Method com.aspose.imaging.imageoptions.TiffOptions.GetValidTagsCount(com.aspose.imaging.fileformats.tiff.TiffDataType[])
- Property com.aspose.imaging.exif.ExifData.IsBigEndian
- Property com.aspose.imaging.fileformats.tiff.TiffDataType.AlignedDataSize
## **Removed Classes and Properties**
### **Method JpegExifData.estimateExifSize Removed**
The method com.aspose.imaging.exif.JpegExifData.estimateExifSize has been removed with Aspose.Imaging for Java 3.0.1. It is advised to use the newly added method com.aspose.imaging.exif.JpegExifData.serializeExifData which gives a serialized data stream and you can query its size afterwards.
