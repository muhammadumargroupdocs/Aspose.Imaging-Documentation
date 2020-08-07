---
title: Public API Changes in Aspose.Imaging 2.4.0
type: docs
weight: 180
url: /java/public-api-changes-in-aspose-imaging-2-4-0/
---

{{% alert color="primary" %}} 

This page lists public API changes that were introduced in Aspose.Imaging 2.4.0. It includes not only new and obsoleted public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Imaging which may affect the existing code.

{{% /alert %}} 
### **Enhancements to the RasterImage**
#### **Added Cropping Feature for the RasterImage**
Aspose.Imaging for Java 2.4.0 has exposed the crop method for the RasterImage class to facilitate the users who wish to use Aspose.Imaging APIs to crop their images. There are two version of the said method, both behave differently as per requirement.

Demonstrates the usage of crop method accepting an instance of Rectangle.

**Java**

{{< highlight csharp >}}

 //Load an existing image into an instance of RasterImage class

RasterImage rasterImage = (RasterImage)Image.load(sourceImage);

//Before cropping, the image should be cached for better performance

if (!rasterImage.isCached())

{

    rasterImage.cacheData();

}

//Create an instance of Rectangle class with desired size

Rectangle rectangle = new Rectangle(10, 10, 100, 100);

//Perform the crop operation on object of Rectangle class

rasterImage.crop(rectangle);

//Save the results to disk

rasterImage.save(outputImage);

{{< /highlight >}}

Demonstrates the usage of crop method accepting 4 integer values denoting Left, Right, Top & Bottom. Based on these four values, the API moves the image boundaries toward the center of the image while discarding the outer portion.

**Java**

{{< highlight csharp >}}

 //Load an existing image into an instance of RasterImage class

RasterImage rasterImage = (RasterImage)Image.load(sourceImage);

//Before cropping, the image should be cached for better performance

if (!rasterImage.isCached())

{

    rasterImage.cacheData();

}

//Define shift values for all four sides

int leftShift = 10;

int rightShift = 10;

int topShift = 10;

int bottomShift = 10;

//Based on the shift values, apply the cropping on image

//Crop method will shift the image bounds toward the center of image

rasterImage.crop(leftShift, rightShift, topShift, bottomShift);

//Save the results to disk

rasterImage.save(outputImage);

{{< /highlight >}}

Please check the detailed article on [Cropping Images](/pages/createpage.action?spaceKey=imagingjava&title=Cropping+Images&linkCreation=true&fromPageId=15303045).
#### **Raw Data Control Properties Added to RasterImage**
We have added several properties to RasterImage class in order to assist with the [Raw Data Processing](/imaging/java/raw-data-processing-html/). Details of these properties are as follow,

1. Field com.aspose.imaging.RasterImage.isRawDataAvailable determines if raw data processing can be performed. If this property returns false you should not use any of the further properties or raw data methods otherwise you are not guaranteed to get the correct results.
1. Property RasterImage.RawCustomColorConverter specifies the custom color converter.
1. Property RasterImage.RawDataFormat defines the raw data pixel layout of the initial image.
1. Property RasterImage.RawDataSettings defines the whole raw data settings of the initial image.
1. Property RasterImage.RawDitheringMethod specifies the raw data dithering method.
1. Property RasterImage.RawFallbackIndex should be used for the indexed RGB raw data conversion.
1. Property RasterImage.RawIndexedColorConverter specifies the indexed color converter.
1. Property RasterImage.RawLineSize shows the raw pixel data row size in bytes.

Below provided code demonstrates the usage for a few of the aforesaid properties.

**Java**

{{< highlight csharp >}}

 RasterImage image = (RasterImage) Image.load(sourceFile);

// convert images supporting raw data processing.

if (image.isRawDataAvailable())

{

    // set the fallback index to 3 palette entry.

    image.setRawFallbackIndex(3);

    // ensure palette conversion is used on the image.

    image.setRawDitheringMethod(DitheringMethods.PaletteConversion);

    // the image will be converted according to above settings.

    image.save(outputFile);

}

{{< /highlight >}}
#### **Interface IPartialRawDataLoader added**
Interface com.aspose.imaging.IPartialRawDataLoader has been added to assist with the raw data processing. It allows loading of raw data by blocks similar to IPartialPixelLoader interface allowing loading of pixel data by blocks.
#### **Interface IIndexedColorConverter added**
Interface com.aspose.imaging.IIndexedColorConverter has been added to assist with the raw data processing for Index Color Conversion.
#### **Interface IColorConverter added**
Interface com.aspose.imaging.IColorConverter has been added with to assist with raw data processing for RGB Color Conversion.
#### **Interface IRasterImageRawDataLoader Added**
Interface com.aspose.imaging.IRasterImageRawDataLoader has been added to assist with raw data processing. It allows loading of raw data by using the LoadRawData method and returns the RawDataSettings property value.
#### **Interface IRasterImagePixelLoader Added**
Interface com.aspose.imaging.IRasterImagePixelLoader added that identifies if an object is capable of partial pixel loading.
### **Enhancements to the JPEG Image Format**
#### **Added Support for JFIF Data Segment**
JFIF segment is one of main identifiers of Jpeg image which contains the image resolution and may also contain small thumbnail image. Aspose.Imaging 2.4.0 adds the support for writing, reading and editing of JFIF data segment in jpeg images by providing JFIFData class.

{{% alert color="primary" %}} 

Presence of JFIF segment usually means, that jpeg file contains 3-component data in YCbCr format with aspect 4:2:2 ratio.

{{% /alert %}} 

The following code snippet demonstrates the creation of JFIF data segment.

**Java**

{{< highlight csharp >}}

 JpegImage image = (JpegImage)Image.load(sourceFile);

image.setJfif(new JFIFData());

{{< /highlight >}}
##### **JFIFData Members Summary**
1. JFIFData.DensityUnits: Byte value, can be 0 in case of no units(just aspect ratio) specified, 1 for pixels per inch, 2 for pixels per centimeter.
1. JFIFData.Thumbnail: Small thumbnail image, that can be inserted into jpeg file.
1. JFIFData.ThumbnailHeight & JFIFData.ThumbnailWidth: Height and width of thumbnail image. If these values are 0, thumbnail image is not presented in this file.
1. JFIFData.Version: JFIF segment version.
1. JFIFData.XDensity: Density on horizontal axis.
1. JFIFData.YDensity: Density on vertical axis.
#### **Class JpegLoadOptions Added**
JpegLoadOptionst class can affect loading of Jpeg image because user can pass ICC RGB color profile for color conversion during the Jpeg image loading. Below provided code snippet demonstrates the usage of JpegLoadOptionst class.

**Java**

{{< highlight csharp >}}

 JpegLoadOptions options = new JpegLoadOptions();

options.setIccProfile(new StreamSource(new FileInputStream("ICC-Profile-Path")));

{{< /highlight >}}
#### **Class JpegException Added**
JpegException class is responsible of handling Jpeg specific exceptions. Below code snippet demonstrates the usage of JpegException class.

**Java**

{{< highlight csharp >}}

 try

{

    JpegImage image = (JpegImage)Image.load(sourceFile);

    image.loadPixels(image.getBounds());



}

catch (JpegException exception)

{

    // specific processing

}

{{< /highlight >}}
#### **Property JpegImage.Jfif Added**
JpegImage.Jfif property adds support of writing, reading and editing of JFIF data segment in jpeg images. Below provided code snippet demonstrates the usage of JpegImage.Jfif property to create JFIF data segment.

**Java**

{{< highlight csharp >}}

 JpegImage image = (JpegImage) Image.load(sourceFile);

image.setJfif(new JFIFData());

{{< /highlight >}}

Below provided code snippet demonstrates the deletion of JFIF data segment.

**Java**

{{< highlight csharp >}}

 JpegImage image = (JpegImage)Image.load(sourceFile);

image.setJfif(null);

{{< /highlight >}}
#### **Enum JfifDensityUnits Added**
A new enumeration by the name of JfifDensityUnits has been added to the com.aspose.imaging.fileFormats.jpeg package. The possible values and their descriptions are provided below,

1. JfifDensityUnits.NoUnits: No units, Density properties just state pixel proportions.
1. JfifDensityUnits.PixelsPerCm: Pixels per centimeter.
1. JfifDensityUnits.PixelsPerInch: Pixels per inch.
#### **Enum Field ExifFileSource.Others Added**
A new field for EXIF 2.3 specification added to the ExifFileSource enumeration.

**Java**

{{< highlight csharp >}}

 JpegImage image = (JpegImage)Image.load(sourceFile);

image.getExifData().setFileSource(ExifFileSource.Others);

{{< /highlight >}}
#### **Enum Field JpegCompressionColorMode.Grayscale Added**
A new field by the name of Grayscale has been added to {JpegCompressionColorMode}} enumeration for setting compression color mode for grayscale images.

**Java**

{{< highlight csharp >}}

 JpegOptions  options = new JpegOptions();

options.setColorType(JpegCompressionColorMode.Grayscale);

{{< /highlight >}}
#### **Enum Field JpegCompressionColorMode.Ycck Added**
A new field by the name of Ycck has been added to {JpegCompressionColorMode}} enumeration for setting compression color mode for Ycck images.

**Java**

{{< highlight csharp >}}

 JpegOptions  options = new JpegOptions();

options.setColorType(JpegCompressionColorMode.Ycck);

{{< /highlight >}}
### **Changes in Reference to CAD Formats**
Following section explains the changes introduced in reference to CAD image formats. 
#### **Class CadLayoutDictionary Added**
Aspose.Imaging for Java 2.4.0 adds support of rendering only a specific layout of DXF file format. For this purpose, a new class CadLayoutDictionary has been added to the com.aspose.imaging.fileFormats.cad package. Below provided code snippet demonstrates the use of CadLayoutDictionary class.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

// dictionary keys by layout names

String layoutName = "Model";

CadLayout cadLayout = cadImage.getLayouts().get_Item(layoutName);

{{< /highlight >}}
#### **Classes CadCallout, CadCalloutData, CadCalloutLeader and CadCalloutLine Added**
The CadCallout, CadCalloutData, CadCalloutLeader & CadCalloutLine classes have been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile))

CadImage cadImage = (CadImage)image;

CadCallout cadCallout = (CadCallout) cadImage.getEntities()[0];

CadCalloutData cadCalloutData = cadCallout.getCalloutData();

CadCalloutLeader cadCalloutLeader = cadCalloutData.getLeader();

CadCalloutLine cadCalloutLine = cadCalloutLeader.getLeaderLine();

{{< /highlight >}}
#### **Classes CadPolylineBase, CadLwPolyline, CadPolyline and CadPolyline3D Added**
The CadPolylineBase, CadLwPolyline, CadPolyline & CadPolyline3D classes have been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadPolylineBase cadPolylineBase = (CadPolylineBase) cadImage.getEntities()[0];

CadLwPolyline cadLwPolyline= (CadLwPolyline) cadImage.getEntities()[1];

CadPolyline cadPolyline = (CadPolyline) cadImage.getEntities()[2];

CadPolyline3D cadPolyline3D = (CadPolyline3D) cadImage.getEntities()[3];

{{< /highlight >}}
#### **Cad2DVertex and Cad3DVertex Classes Added**
The Cad2DVertex & Cad3DVertex classes have been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

Cad2DVertex сad2DVertex = (Cad2DVertex) cadImage.getEntities()[0];

Cad3DVertex сad3DVertex = (Cad3DVertex) cadImage.getEntities()[1];

{{< /highlight >}}
#### **Class CadAlignedDimension Added**
The CadAlignedDimension class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadAlignedDimension cadAlignedDimension = (CadAlignedDimension) cadImage.getEntities()[0];

{{< /highlight >}}
### **Class CadAngularDimension Added**
The CadAngularDimension class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadAngularDimension cadAngularDimension = (CadAngularDimension)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadDiametricDimension Added**
The CadDiametricDimension class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadDiametricDimension cadDiametricDimension = (CadDiametricDimension)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadHelix Added**
The CadHelix class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadHelix cadHelix = (CadHelix)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadInsertObject Added**
The CadInsertObject class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadInsertObject cadInsertObject = (CadInsertObject)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadLine Added**
The CadLine class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadLine cadLine = (CadLine) cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadMesh Added**
The CadMesh class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadMesh cadEntity = (CadMesh)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadRadialDimension Added**
The CadRadialDimension class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadRadialDimension cadEntity = (CadRadialDimension)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadRotatedDimension Added**
The CadRotatedDimension class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadRotatedDimension cadRotatedDimension = (CadRotatedDimension)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Class CadTableEntity Added**
The CadTableEntity class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadTableEntity cadEntity = (CadTableEntity)cadImage.getEntities()[0];

{{< /highlight >}}
### **Class CadViewport Added**
The CadViewport class has been added to the com.aspose.imaging.fileFormats.cad.CadObjects package.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image

CadViewport cadViewport = (CadViewport)cadImage.getEntities()[0];

{{< /highlight >}}
#### **Classes CadApplicationCodesContainer and CadApplicationCodes Added**
These classes collectively enable the developers to read the application-defined codes. Below provided code snippet demonstrates the use of CadApplicationCodesContainer & CadApplicationCodes classes.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

CadBase cadBase = cadImage.getEntities()[0];

// or cadBase = cadImage.Objects[0];

// The following are equivalent ways

CadApplicationCodes codes1 = cadBase.getApplicationCodesContainer().getCodes("ACAD_REACTORS");

CadApplicationCodes cadReactorsCodes = cadImage.getEntities()[0].getApplicationCodesContainer().getAcadReactorsCodes();

// The following are equivalent ways

CadApplicationCodes codes2 = cadBase.getApplicationCodesContainer().getCodes("ACAD_XDICTIONARY");

CadApplicationCodes cadAcadXDictionaryCodes = cadImage.getEntities()[0].getApplicationCodesContainer().getAcadXDictionaryCodes();

// Any group codes

CadApplicationCodes codes3 = cadBase.getApplicationCodesContainer().getCodes("BLKREFS");

// iteration

for (CadApplicationCodes codes : cadBase.getApplicationCodesContainer().getCodes())

{

    // codes.Name = "ACAD_REACTORS" or "ACAD_XDICTIONARY" etc.

    // codes.CodesList - data

    /* for example, let a dxf file:

     *    ...

     *    102

     *    {ACAD_REACTORS

     *    330

     *    19DE5D

     *    102

     *    }

     *    ...

     *

     * then we have:

     *    codes.Name == "ACAD_REACTORS"

     *    CadCodeValue codeValue = codes.CodesList[0];

     *    codeValue.Code == 330

     *    codeValue.Attribute  == CadEntityAttribute.Cad330

     *    codeValue.Value == "19DE5D"

     *

     *    codes.GetValue(CadEntityAttribute.Cad330) return "19DE5D"

     */

}

{{< /highlight >}}
#### **Class CadBaseObject Added**
CadBaseObject class provides support of reading objects' section data. Below provided code snippet demonstrates the use of CadBaseObject class.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

for (CadBaseObject cadBaseObject : cadImage.getObjects())

{

    //...

}

{{< /highlight >}}
#### **Class CadLayout Added**
CadLayout class provides support of reading CAD Layout objects. Below provided code snippet demonstrates the use of CadLayout class.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

for (CadBaseObject cadBaseObject : cadImage.getObjects())

{

    if (cadBaseObject.equals(CadLayout)

    {

        CadLayout cadLayout = (CadLayout) cadBaseObject;

        //...

    }

}

{{< /highlight >}}
##### **CadLayout Members Summary**
1. CadLayout.LayoutName: Name of this layout, "Model" is also a layout.
1. CadLayout.MaxExtents: Maximum extents for this layout, defined by EXTMAX while this layout is current.
1. CadLayout.MinExtents: Minimum extents for this layout (defined by EXTMIN while this layout is current).
1. CadLayout.TabOrder: This number is an ordinal indicating this layout's ordering in the tab control that is attached to the AutoCAD drawing frame window. Note that the “Model” tab always appears as the first tab regardless of its tab order.
#### **Class CadPlotSettings Added**
CadPlotSettings class provides support of reading CAD PLOTSETTINGS object. Below provided code snippet demonstrates the use of CadPlotSettings class.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

CadImage cadImage = (CadImage)image;

for (CadBaseObject cadBaseObject : cadImage.getObjects())

{

    if (cadBaseObject.equals(CadPlotSettings)

    {

    	CadPlotSettings cadPlotSettings  = (CadPlotSettings) cadBaseObject;

        //...

    }

}

{{< /highlight >}}
##### **CadPlotSettings Members Summary**
1. CadPlotSettings.PageSetupName: The page setup name.
1. CadPlotSettings.PlotPaperSize: Physical paper width and height in millimeters.
1. CadPlotSettings.TopSize: Size, in millimeters, of unprintable margin on top of paper.
1. CadPlotSettings.RightSideSize: Size, in millimeters, of unprintable margin on right side of paper.
1. CadPlotSettings.BottomSize: Size, in millimeters, of unprintable margin on bottom of paper.
1. CadPlotSettings.LeftSideSize: Size, in millimeters, of unprintable margin on left side of paper.
