---
title: Public API Changes in Aspose.Imaging 2.4.0
type: docs
weight: 190
url: /net/public-api-changes-in-aspose-imaging-2-4-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Imaging API from version 2.3.0 to 2.4.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
### **Raw Data Control Properties Added to RasterImage Class**
We have added several properties to RasterImage class in order assist with the [Raw Data Processing](/imaging/net/raw-data-processing-html/). Details of these properties are as follow,

1. Property Aspose.Imaging.RasterImage.IsRawDataAvailable determines if raw data processing can be performed. If this property returns false you should not use any of the further properties or raw data methods otherwise you are not guaranteed to get the correct results.
1. Property Aspose.Imaging.RasterImage.RawCustomColorConverter specifies the custom color converter.
1. Property Aspose.Imaging.RasterImage.RawDataFormat defines the raw data pixel layout of the initial image.
1. Property Aspose.Imaging.RasterImage.RawDataSettings defines the whole raw data settings of the initial image.
1. Property Aspose.Imaging.RasterImage.RawDitheringMethod specifies the raw data dithering method.
1. Property Aspose.Imaging.RasterImage.RawFallbackIndex should be used for the indexed RGB raw data conversion.
1. Property Aspose.Imaging.RasterImage.RawIndexedColorConverter specifies the indexed color converter.
1. Property Aspose.Imaging.RasterImage.RawLineSize shows the raw pixel data row size in bytes.

Below provided code demonstrates the usage for a few of aforesaid properties,

**C#**

{{< highlight csharp >}}

 using (RasterImage image = (RasterImage)Aspose.Imaging.Image.Load(path))

{

    // convert images supporting raw data processing.

    if (image.IsRawDataAvailable)

    {

        // set the fallback index to 3 palette entry.

        image.RawFallbackIndex = 3;

        // ensure palette conversion is used on the image.

        image.RawDitheringMethod = DitheringMethods.PaletteConversion;

        // the image will be converted according to above settings.

        image.Save(outputPath);

    }

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As RasterImage = CType(Aspose.Imaging.Image.Load(path), RasterImage)

	' convert images supporting raw data processing.

	If image.IsRawDataAvailable Then

		' set the fallback index to 3 palette entry.

		image.RawFallbackIndex = 3

		' ensure palette conversion is used on the image.

		image.RawDitheringMethod = DitheringMethods.PaletteConversion

		' the image will be converted according to above settings.

		image.Save(outputPath)

	End If

End Using

{{< /highlight >}}
### **Class PixelDataFormat Added**
Class Aspose.Imaging.PixelDataFormat added with v2.4, is used to specify the format of pixel data layout. The class contains several useful properties to determine the data layout,

1. Property Aspose.Imaging.PixelDataFormat.PixelFormat returns the color space used. As of v2.4 the following properties are available: Grayscale, RGB, YCbCr, CMYK, YCCK.
1. Property Aspose.Imaging.PixelDataFormat.BitsPerPixel returns the total bits per pixel number.
1. Property Aspose.Imaging.PixelDataFormat.ChannelsCount returns the number of channels used per pixel.
1. Property Aspose.Imaging.PixelDataFormat.ChannelBits returns the bits counts for each channel.

To instantinate the PixelDataFormat you need to use one of the static properties available (as of v2.4), each of which determines the specific pixel data layout. 

1. Rgb32Bpp
1. CMYK
1. Rgb24Bpp
1. Rgb16Bpp555
1. RgbIndexed8Bpp
1. RgbIndexed4Bpp
1. RgbIndexed2Bpp
1. RgbIndexed1Bpp
1. YCbCr
1. Grayscale
1. Ycck 

We will keep on adding new static properties when new raw data formats will be available.
### **Interface IPartialRawDataLoader added**
Interface Aspose.Imaging.IPartialRawDataLoader has been added with Aspose.Imaging v2.4 in order to assist with the raw data processing. It allows loading of raw data by blocks similar to IPartialPixelLoader interface allowing loading of pixel data by blocks.

**C#**

{{< highlight csharp >}}

 /// <summary>

/// The raw data loader.

/// </summary>

private class MyLoader : IPartialRawDataLoader

{

    /// <summary>

    /// Processes the loaded data.

    /// </summary>

    /// <param name="rectangle">The data rectangle.</param>

    /// <param name="data">The raw data.</param>

    /// <param name="start">The start data point. If not equal to (left,top) meaning that it is not full rectangle we have.</param>

    /// <param name="end">The end data point. If not equal to (right,bottom) meaning that it is not full rectangle we have.</param>

    public void Process(Rectangle rectangle, byte[] data, Point start, Point end)

    {

        // perform pixel processing.

    }

}

/// <summary>

/// Loads the data.

/// </summary>

/// <param name="path">The image path.</param>

public static void LoadData(string path)

{

    using (RasterImage image = (RasterImage)Aspose.Imaging.Image.Load(path))

    {

        // loads raw data if possible partially.

        if (image.IsRawDataAvailable)

        {

            image.LoadRawData(image.Bounds, image.RawDataSettings, new MyLoader());

        }

    }

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 ''' <summary>

''' The raw data loader.

''' </summary>

Private Class MyLoader

	Implements IPartialRawDataLoader

	''' <summary>

	''' Processes the loaded data.

	''' </summary>

	''' <param name="rectangle">The data rectangle.</param>

	''' <param name="data">The raw data.</param>

	''' <param name="start">The start data point. If not equal to (left,top) meaning that it is not full rectangle we have.</param>

	''' <param name="end">The end data point. If not equal to (right,bottom) meaning that it is not full rectangle we have.</param>

	Public Sub Process(ByVal rectangle As Rectangle, ByVal data() As Byte, ByVal start As Point, ByVal [end] As Point)

		' perform pixel processing.

	End Sub

End Class

''' <summary>

''' Loads the data.

''' </summary>

''' <param name="path">The image path.</param>

Public Shared Sub LoadData(ByVal path As String)

	Using image As RasterImage = CType(Aspose.Imaging.Image.Load(path), RasterImage)

		' loads raw data if possible partially.

		If image.IsRawDataAvailable Then

			image.LoadRawData(image.Bounds, image.RawDataSettings, New MyLoader())

		End If

	End Using

End Sub

{{< /highlight >}}
### **Interface IIndexedColorConverter added**
Interface Aspose.Imaging.IIndexedColorConverter has been added with Aspose.Imaging v2.4 to assist with raw data processing for Index Color Conversion.
### **Interface IColorConverter added**
Interface Aspose.Imaging.IColorConverter has been added with Aspose.Imaging v2.4 to assist with raw data processing for RGB Color Conversion.
### **Interface IRasterImageRawDataLoader Added**
Interface Aspose.Imaging.IRasterImageRawDataLoader has been added into Aspose.Imaging v2.4 to assist with raw data processing. It allows loading of raw data by using the LoadRawData method and returns the RawDataSettings property value.
### **Interface IRasterImagePixelLoader Added**
Interface Aspose.Imaging.IRasterImagePixelLoader added with v2.4, identifies an object capable of partial pixel loading.

**C#**

{{< highlight csharp >}}

 using (Image image = Aspose.Imaging.Image.Load(path))

{

  // determine if partial pixel loading is possible.

  IRasterImagePixelLoader loader = image as IRasterImagePixelLoader;

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Aspose.Imaging.Image.Load(path)

  ' determine if partial pixel loading is possible.

  Dim loader As IRasterImagePixelLoader = TryCast(image, IRasterImagePixelLoader)

End Using

{{< /highlight >}}
### **GifImageException Class Added**
The GifImageException class has been added to Aspose.Imaging.Exceptions.ImageFormats namespace in order to handle errors triggered due to GIF file format.

**C#**

{{< highlight csharp >}}

 try

{

    using (Image image = Image.Load(fileName + ".gif"))

    {

    }

}

catch (GifImageException ex)

{

    ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Try

	Using image As Image = Image.Load(fileName & ".gif")

	End Using

Catch ex As GifImageException

	...

End Try

{{< /highlight >}}
### **Enum JfifDensityUnits Added**
A new enumeration by the name of JfifDensityUnits has been added to the Aspose.Imaging.FileFormats.Jpeg namespace. The possible values and their descriptions are provided below,

1. JfifDensityUnits.NoUnits - No units, Density properties just state pixel proportions.
1. JfifDensityUnits.PixelsPerCm - Pixels per centimeter
1. JfifDensityUnits.PixelsPerInch - Pixels per inch
### **Enum Field ExifFileSource.Others Added**
A new field for EXIF 2.3 specification added to the ExifFileSource enumeration.

**C#**

{{< highlight csharp >}}

 using (JpegImage image = (JpegImage)Image.Load(fileName))

{

    image.ExifData.FileSource = ExifFileSource.Others;

    ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As JpegImage = CType(Image.Load(fileName), JpegImage)

	image.ExifData.FileSource = ExifFileSource.Others

	...

End Using

{{< /highlight >}}
### **Enum Field ExifProperties.PhotographicSensitivity Added**
A new field by the name of PhotographicSensitivity has been added to {ExifProperties}} enumeration for EXIF 2.3 specification.

**C#**

{{< highlight csharp >}}

 using (TiffImage image = (TiffImage)Image.Load(fileName))

{

    TiffDataType tiffDataType = image.ExifData.Properties[(int)ExifProperties.PhotographicSensitivity];

    ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As TiffImage = CType(Image.Load(fileName), TiffImage)

	Dim tiffDataType As TiffDataType = image.ExifData.Properties(CInt(Fix(ExifProperties.PhotographicSensitivity)))

	...

End Using

{{< /highlight >}}
### **Enum Field JpegCompressionColorMode.Grayscale Added**
A new field by the name of Grayscale has been added to {JpegCompressionColorMode}} enumeration for setting compression color mode for grayscale images.

**C#**

{{< highlight csharp >}}

 JpegOptions  options = new JpegOptions();

options.ColorType = JpegCompressionColorMode.Grayscale;

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim options As New JpegOptions()

options.ColorType = JpegCompressionColorMode.Grayscale

{{< /highlight >}}
### **Enum Field JpegCompressionColorMode.Ycck Added**
A new field by the name of Ycck has been added to {JpegCompressionColorMode}} enumeration for setting compression color mode for Ycck images.

**C#**

{{< highlight csharp >}}

 JpegOptions  options = new JpegOptions();

options.ColorType = JpegCompressionColorMode.Ycck;

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim options As New JpegOptions()

options.ColorType = JpegCompressionColorMode.Ycck

{{< /highlight >}}
### **CadCallout, CadCalloutData, CadCalloutLeader and CadCalloutLine Classes Added**
The CadCallout, CadCalloutData, CadCalloutLeader & CadCalloutLine classes have been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    CadCallout cadCallout = cadImage.Entities[0] as CadCallout;

    CadCalloutData cadCalloutData = cadCallout.CalloutData;

    CadCalloutLeader cadCalloutLeader = cadCalloutData.Leader;

    CadCalloutLine cadCalloutLine = cadCalloutLeader.LeaderLine;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	Dim cadCallout As CadCallout = TryCast(cadImage.Entities(0), CadCallout)

	Dim cadCalloutData As CadCalloutData = cadCallout.CalloutData

	Dim cadCalloutLeader As CadCalloutLeader = cadCalloutData.Leader

	Dim cadCalloutLine As CadCalloutLine = cadCalloutLeader.LeaderLine

	...

End Using

{{< /highlight >}}
### **CadPolylineBase, CadLwPolyline, CadPolyline and CadPolyline3D Classes Added**
The CadPolylineBase, CadLwPolyline, CadPolyline & CadPolyline3D classes have been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    CadPolylineBase cadPolylineBase = cadImage.Entities[0] as CadPolylineBase;

    CadLwPolyline cadLwPolyline= cadImage.Entities[1] as CadLwPolyline;

    CadPolyline cadPolyline = cadImage.Entities[2] as CadPolyline;

    CadPolyline3D cadPolyline3D = cadImage.Entities[3] as CadPolyline3D;

    ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	Dim cadPolylineBase As CadPolylineBase = TryCast(cadImage.Entities(0), CadPolylineBase)

	Dim cadLwPolyline As CadLwPolyline= TryCast(cadImage.Entities(1), CadLwPolyline)

	Dim cadPolyline As CadPolyline = TryCast(cadImage.Entities(2), CadPolyline)

	Dim cadPolyline3D As CadPolyline3D = TryCast(cadImage.Entities(3), CadPolyline3D)

	...

End Using

{{< /highlight >}}
### **Cad2DVertex and Cad3DVertex Classes Added**
The Cad2DVertex & Cad3DVertex classes have been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     Cad2DVertex сad2DVertex = cadImage.Entities[0] as Cad2DVertex;

     Cad3DVertex сad3DVertex = cadImage.Entities[1] as Cad3DVertex;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim сad2DVertex As Cad2DVertex = TryCast(cadImage.Entities(0), Cad2DVertex)

	 Dim сad3DVertex As Cad3DVertex = TryCast(cadImage.Entities(1), Cad3DVertex)

	 ...

End Using

{{< /highlight >}}
### **CadAlignedDimension Class Added**
The CadAlignedDimension class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    CadAlignedDimension cadAlignedDimension = cadImage.Entities[0] as CadAlignedDimension;

    ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	Dim cadAlignedDimension As CadAlignedDimension = TryCast(cadImage.Entities(0), CadAlignedDimension)

	...

End Using

{{< /highlight >}}
### **CadAngularDimension Class Added**
The CadAngularDimension class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadAngularDimension cadAngularDimension = cadImage.Entities\[0\] as CadAngularDimension;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadAngularDimension As CadAngularDimension = cadImage.Entities\TryCast((0\), CadAngularDimension)

	 ...

End Using

{{< /highlight >}}
### **CadDiametricDimension Class Added**
The CadDiametricDimension class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadDiametricDimension cadDiametricDimension = cadImage.Entities[0] as CadDiametricDimension;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadDiametricDimension As CadDiametricDimension = TryCast(cadImage.Entities(0), CadDiametricDimension)

	 ...

End Using

{{< /highlight >}}
### **CadHelix Class Added**
The CadHelix class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadHelix cadHelix = cadImage.Entities[0] as CadHelix;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadHelix As CadHelix = TryCast(cadImage.Entities(0), CadHelix)

	 ...

End Using

{{< /highlight >}}
### **CadInsertObject Class Added**
The CadInsertObject class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadInsertObject cadInsertObject = cadImage.Entities[0] as CadInsertObject;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadInsertObject As CadInsertObject = TryCast(cadImage.Entities(0), CadInsertObject)

	 ...

End Using

{{< /highlight >}}
### **CadLine Class Added**
The CadLine class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadLine cadLine = cadImage.Entities[0] as CadLine;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadLine As CadLine = TryCast(cadImage.Entities(0), CadLine)

	 ...

End Using

{{< /highlight >}}
### **CadMesh Class Added**
The CadMesh class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadMesh cadEntity = cadImage.Entities[0] as CadMesh;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadEntity As CadMesh = TryCast(cadImage.Entities(0), CadMesh)

	 ...

End Using

{{< /highlight >}}
### **CadRadialDimension Class Added**
The CadRadialDimension class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadRadialDimension cadEntity = cadImage.Entities[0] as CadRadialDimension;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadEntity As CadRadialDimension = TryCast(cadImage.Entities(0), CadRadialDimension)

	 ...

End Using

{{< /highlight >}}
### **CadRotatedDimension Class Added**
The CadRotatedDimension class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadRotatedDimension cadRotatedDimension = cadImage.Entities[0] as CadRotatedDimension;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadRotatedDimension As CadRotatedDimension = TryCast(cadImage.Entities(0), CadRotatedDimension)

	 ...

End Using

{{< /highlight >}}
### **CadTableEntity Class Added**
The CadTableEntity class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadTableEntity cadEntity = cadImage.Entities[0] as CadTableEntity;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadEntity As CadTableEntity = TryCast(cadImage.Entities(0), CadTableEntity)

	 ...

End Using

{{< /highlight >}}
### **CadViewport Class Added**
The CadViewport class has been added to the Aspose.Imaging.FileFormats.Cad.CadObjects namespace.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

     CadImage cadImage = (CadImage)image;

     CadViewport cadViewport = cadImage.Entities[0] as CadViewport;

     ...

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	 Dim cadImage As CadImage = CType(image, CadImage)

	 Dim cadViewport As CadViewport = TryCast(cadImage.Entities(0), CadViewport)

	 ...

End Using

{{< /highlight >}}
### **Modified Cad Object Properties Types**
Changed the Cad special data types (such as CadShortParameter) of the Cad objects properties.

{{< highlight java >}}

 CadAttDef cadAttDef;

short length;

// was:

length = cadAttDef.FieldLength.Value;

// now

length = cadAttDef.FieldLength;  // access without ".Value"

{{< /highlight >}}
#### **CadAttDef**
*CadShortParameter to short:*

- CadAttDef.FieldLength
- CadAttDef.Flags
- CadAttDef.GenerationFlag
- CadAttDef.HorizontalAlignment
- CadAttDef.VerticalJustification

*CadStringParameter to string:*

- CadAttDef.Id
- CadAttDef.PromptString

*CadDoubleParameter to double:*

- CadAttDef.ObliqueAngle
- CadAttDef.ScaleX
- CadAttDef.Thickness
#### **CadBlockEntity**
*CadShortParameter to short:*

- CadBlockEntity.Flags

**CadHatchBoundaryPathContainer**

*CadParameter to short:*

- CadHatchBoundaryPathContainer.EdgeType

*CadParameter to int:*

- CadHatchBoundaryPathContainer.BoundaryObjectCount
#### **CadMultiLine**
*CadShortParameter to short:*

- CadMultiLine.NumberOfStyleElements
- CadMultiLine.NumberOfVertices

*CadStringParameter to string:*

- CadMultiLine.StyleName
#### **CadLayerTable**
*CadShortParameter to short:*

- CadDimensionStyleTable.ColorId
- CadDimensionStyleTable.Flags
- CadDimensionStyleTable.LineWeight

*CadStringParameter to string:*

- CadDimensionStyleTable.LineTypeName
- CadDimensionStyleTable.MaterialHanlde
- CadDimensionStyleTable.Name
- CadDimensionStyleTable.PlotStyleHandle

*CadBoolParameter to bool:*

- CadDimensionStyleTable.PlotFlag
#### **CadDimensionStyleTable**
*CadShortParameter to short:*

- CadDimensionStyleTable.Dimadec
- CadDimensionStyleTable.Dimalt
- CadDimensionStyleTable.Dimaltd
- CadDimensionStyleTable.Dimaltf
- CadDimensionStyleTable.Dimaltrnd
- CadDimensionStyleTable.Dimalttd
- CadDimensionStyleTable.Dimalttz
- CadDimensionStyleTable.Dimaltu
- CadDimensionStyleTable.Dimaltz
- CadDimensionStyleTable.Dimapost
- CadDimensionStyleTable.Dimasz
- CadDimensionStyleTable.Dimatfit
- CadDimensionStyleTable.Dimaunit
- CadDimensionStyleTable.Dimazin
- CadDimensionStyleTable.Dimblk
- CadDimensionStyleTable.Dimblk1
- CadDimensionStyleTable.Dimblk2
- CadDimensionStyleTable.Dimcen
- CadDimensionStyleTable.Dimclrd
- CadDimensionStyleTable.Dimclre
- CadDimensionStyleTable.Dimclrt
- CadDimensionStyleTable.Dimdec
- CadDimensionStyleTable.Dimdsep
- CadDimensionStyleTable.Dimfit
- CadDimensionStyleTable.Dimfrac
- CadDimensionStyleTable.Dimjust
- CadDimensionStyleTable.Dimlim
- CadDimensionStyleTable.Dimlunit
- CadDimensionStyleTable.Dimlwd
- CadDimensionStyleTable.Dimlwe
- CadDimensionStyleTable.Dimsah
- CadDimensionStyleTable.Dimsd1
- CadDimensionStyleTable.Dimsd2
- CadDimensionStyleTable.Dimse1
- CadDimensionStyleTable.Dimse2
- CadDimensionStyleTable.Dimsoxd
- CadDimensionStyleTable.Dimtad
- CadDimensionStyleTable.Dimtdec
- CadDimensionStyleTable.Dimtih
- CadDimensionStyleTable.Dimtix
- CadDimensionStyleTable.Dimtmove
- CadDimensionStyleTable.Dimtofl
- CadDimensionStyleTable.Dimtoh
- CadDimensionStyleTable.Dimtol
- CadDimensionStyleTable.Dimtolj
- CadDimensionStyleTable.Dimtzin
- CadDimensionStyleTable.Dimunit
- CadDimensionStyleTable.Dimupt
- CadDimensionStyleTable.Dimzin
- CadDimensionStyleTable.StandardFlag

*CadStringParameter to string:*

- CadDimensionStyleTable.Dimldrblk
- CadDimensionStyleTable.Dimpost
- CadDimensionStyleTable.Dimtxsty

*CadDoubleParameter to double:*

- CadDimensionStyleTable.Dimdle
- CadDimensionStyleTable.Dimdli
- CadDimensionStyleTable.Dimexe
- CadDimensionStyleTable.Dimexo
- CadDimensionStyleTable.Dimgap
- CadDimensionStyleTable.Dimlfac
- CadDimensionStyleTable.Dimrnd
- CadDimensionStyleTable.Dimscale
- CadDimensionStyleTable.Dimtfac
- CadDimensionStyleTable.Dimtm
- CadDimensionStyleTable.Dimtp
- CadDimensionStyleTable.Dimtsz
- CadDimensionStyleTable.Dimtvp
- CadDimensionStyleTable.Dimtxt
#### **CadLineTypeTableObject**
*CadShortParameter to short:*

- CadLineTypeTableObject.AlignmentCode
- CadLineTypeTableObject.Flags
- CadLineTypeTableObject.NumberOfLinetypeElements

*CadStringParameter to string:*

- CadLineTypeTableObject.Description
- CadLineTypeTableObject.Name

*CadDoubleParameter to double:*

- CadLineTypeTableObject.PatternLength
### **TiffStream Class Methods Renamed**
Following methods of the Aspose.Imaging.FileFormats.Tiff.FileManagement.TiffStream class have been renamed,

- ProcessReadDataShorts(System.Byte[]) *to* ProcessReadDataShort(System.Byte[])
- ProcessReadDataUShorts(System.Byte[]) *to* ProcessReadDataUShort(System.Byte[])
#### **Added Prefixes Indicating the Types of the Parameters:**
##### **ProcessWriteData Overrides:**
- ProcessWriteDataDouble(System.Double[],System.Byte[])
- ProcessWriteDataFloat(System.Single[],System.Byte[])
- ProcessWriteDataLong(System.Int32[],System.Byte[])
- ProcessWriteDataRational(Aspose.Imaging.FileFormats.Tiff.TiffRational[],System.Byte[])
- ProcessWriteDataShort(System.Int16[],System.Byte[])
- ProcessWriteDataULong(System.UInt32[],System.Byte[])
- ProcessWriteDataUShort(System.UInt16[],System.Byte[])
##### **Read Array Methods:**
- ReadDoubleArrayInt32(System.Int32)
- ReadDoubleArrayUInt32(System.UInt32)
- ReadFloatArrayInt32(System.Int32)
- ReadFloatArrayUInt32(System.UInt32)
- ReadRationalArrayInt32(System.Int32)
- ReadRationalArrayUInt32(System.UInt32)
- ReadSByteArrayInt32(System.Int32)
- ReadSByteArrayUInt32(System.UInt32)
- ReadSLongArrayInt32(System.Int32)
- ReadSLongArrayUInt32(System.UInt32)
- ReadSRationalArrayInt32(System.Int32)
- ReadSRationalArrayUInt32(System.UInt32)
- ReadSShortArrayInt32(System.Int32)
- ReadSShortArrayUInt32(System.UInt32)
- ReadUByteArrayInt32(System.Int32)
- ReadUByteArrayUInt32(System.UInt32)
- ReadULongArrayInt32(System.Int32)
- ReadULongArrayUInt32(System.UInt32)
- ReadUShortArrayInt32(System.Int32)
- ReadUShortArrayUInt32(System.UInt32)
### **Fields Removed From CadVertexBase**
Following fields have been removed from the class Aspose.Imaging.FileFormats.Cad.CadObjects.CadVertexBase.

1. CadVertexBase.bugle
1. CadVertexBase.curveFitTangentDirection
1. CadVertexBase.endingWidth
1. CadVertexBase.flags
1. CadVertexBase.meshVertexIndex1
1. CadVertexBase.meshVertexIndex2
1. CadVertexBase.meshVertexIndex3
1. CadVertexBase.meshVertexIndex4
1. CadVertexBase.startingWidth
1. CadVertexBase.vertexId
### **Method ReplaceField Removed**
Following overloads of the method ReplaceField have been removed from the class Aspose.Imaging.FileFormats.Cad.CadObjects.CadBaseObject.

1. CadBaseObject.ReplaceField(Cad2DPoint@, Cad2DPoint, string)
1. CadBaseObject.ReplaceField(Cad3DPoint@, Cad3DPoint, string)
1. CadBaseObject.ReplaceField(CadSize@, CadSize, string)
### **Enum SubSamplingMode Removed**
Aspose.Imaging.FileFormats.Jpeg.Enums.SubSamplingMode has been removed because sub-sampling settings are determined by JFIF/EXIF standards.

Following enumeration members have been removed too,

1. Field/Enum Aspose.Imaging.FileFormats.Jpeg.Enums.SubSamplingMode.ModeFull
1. Field/Enum Aspose.Imaging.FileFormats.Jpeg.Enums.SubSamplingMode.ModeH2V1
1. Field/Enum Aspose.Imaging.FileFormats.Jpeg.Enums.SubSamplingMode.ModeH2V2
1. Field/Enum Aspose.Imaging.FileFormats.Jpeg.Enums.SubSamplingMode.ModeNone
