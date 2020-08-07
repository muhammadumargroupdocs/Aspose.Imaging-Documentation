---
title: Public API Changes in Aspose.Imaging 2.3.0
type: docs
weight: 200
url: /net/public-api-changes-in-aspose-imaging-2-3-0/
---

{{% alert color="primary" %}} 

This page lists public API changes that were introduced in Aspose.Imaging 2.3.0. It includes not only new and obsoleted public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Imaging which may affect the existing code.

{{% /alert %}} 
### **Added Crop Method for RasterImage Class**
Crop method for the RasterImage class has been added to facilitate the users who wish to use Aspose.Imaging APIs to crop their images. There are two version of the said method, both behave differently as per requirement.
#### **Sample**
Demonstrates the usage of Crop method accepting an instance of Rectangle.

**C#**

{{< highlight csharp >}}

 using (RasterImage rasterImage = (RasterImage)Image.Load(fileName))

{

    // before cropping the image should be cached

    if (!rasterImage.IsCached)

    {

        rasterImage.CacheData();

    }

    // specify rectangle

    Aspose.Imaging.Rectangle rectangle = new Aspose.Imaging.Rectangle(10, 10, 100, 100);

    rasterImage.Crop(rectangle);

    rasterImage.Save(outputFileName);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using rasterImage As RasterImage = CType(Image.Load(fileName), RasterImage)

	' before cropping the image should be cached

	If (Not rasterImage.IsCached) Then

		rasterImage.CacheData()

	End If

	' or specified rectangle

	Dim rectangle As New Aspose.Imaging.Rectangle(10, 10, 100, 100)

	rasterImage.Crop(rectangle)

	rasterImage.Save(outputFileName)

End Using

{{< /highlight >}}

Demonstrates the usage of Crop method accepting 4 integer values denoting Left, Right, Top & Bottom. Based on these four values, the API moves the image boundaries toward the center of the image while discarding the outer portion.

**C#**

{{< highlight csharp >}}

 using (RasterImage rasterImage = (RasterImage)Image.Load(fileName))

{

    // before cropping the image should be cached

    if (!rasterImage.IsCached)

    {

        rasterImage.CacheData();

    }

    // cropping by shifts

    int leftShift = 10;

    int rightShift = 10;

    int topShift = 10;

    int bottomShift = 10;

    rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);

    rasterImage.Save(outputFileName);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using rasterImage As RasterImage = CType(Image.Load(fileName), RasterImage)

	' before cropping the image should be cached

	If (Not rasterImage.IsCached) Then

		rasterImage.CacheData()

	End If

	' cropping by shifts

	Dim leftShift As Integer = 10

	Dim rightShift As Integer = 10

	Dim topShift As Integer = 10

	Dim bottomShift As Integer = 10

	rasterImage.Crop(leftShift, rightShift, topShift, bottomShift)

	rasterImage.Save(outputFileName)

End Using

{{< /highlight >}}

Please check the detailed article on [Cropping Images](/pages/createpage.action?spaceKey=imagingnet&title=Cropping+Images&linkCreation=true&fromPageId=14814882).
## **Changes in Reference to Jpeg Image Format**
{{% alert color="primary" %}} 

Following section explains the changes introduced in reference to Jpeg image format. 

{{% /alert %}} 
### **Class Aspose.Imaging.FileFormats.Jpeg.JFIFData Added**
Aspose.Imaging 2.3.0 adds support of writing, reading and editing of JFIF data segment in jpeg images by providing JFIFData class. Purpose of JFIFData class is to provide support for creating and manipulating of JFIF segment. JFIF segment is one of main identifiers of Jpeg image. JFIF data contains image resolution and may also contain small thumbnail image.

Presence of JFIF segment usually means, that jpeg file contains 3-component data in YCbCr format with aspect 4:2:2 ratio.
#### **Sample**
Demonstrates the creation of JFIF data segment.

**C#**

{{< highlight csharp >}}

 using (JpegImage image = (JpegImage)Image.Load(jpegFile))

{

     image.Jfif = new JFIFData();

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As JpegImage = CType(Image.Load(jpegFile), JpegImage)

     image.Jfif = New JFIFData()

End Using

{{< /highlight >}}
#### **JFIFData Members Summary**
Aspose.Imaging.FileFormats.Jpeg.JFIFData.DensityUnits
Byte value, can be 0 in case of no units(just aspect ratio) specified, 1 for pixels per inch, 2 for pixels per centimeter.

Aspose.Imaging.FileFormats.Jpeg.JFIFData.Thumbnail
Small thumbnail image, that can be inserted into jpeg file.

Aspose.Imaging.FileFormats.Jpeg.JFIFData.ThumbnailHeight
Aspose.Imaging.FileFormats.Jpeg.JFIFData.ThumbnailWidth
Height and width of thumbnail image. If these values are 0, thumbnail image is not presented in this file.

Aspose.Imaging.FileFormats.Jpeg.JFIFData.Version
JFIF segment version.

Aspose.Imaging.FileFormats.Jpeg.JFIFData.XDensity
Density on horizontal axis.

Aspose.Imaging.FileFormats.Jpeg.JFIFData.YDensity
Density on vertical axis.
### **Class Aspose.Imaging.ImageLoadOptions.JpegLoadOptions Added**
JpegLoadOptionst class can affect loading of Jpeg image because user can pass ICC RGB color profile for color conversion during the Jpeg image loading.
#### **Sample**
Demonstrates the usage of JpegLoadOptionst class.

**C#**

{{< highlight csharp >}}

 JpegLoadOptions options = new JpegLoadOptions();

options.IccProfile = new StreamSource(File.Open("path", FileMode.Open));

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim options As New JpegLoadOptions()

options.IccProfile = New StreamSource(File.Open("path", FileMode.Open))

{{< /highlight >}}
### **Class Aspose.Imaging.Exceptions.ImageFormats.JpegException Added**
JpegException class is responsible of handling Jpeg specific exceptions.
#### **Sample**
Demonstrates the usage of JpegException class.

**C#**

{{< highlight csharp >}}

 try

{

    using (JpegImage image = (JpegImage)Image.Load(jpegFile))

    {

        image.LoadPixels(image.Bounds);

    }

}

catch (JpegException exception)

{

    // specific processing

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Try

	Using image As JpegImage = CType(Image.Load(jpegFile), JpegImage)

		image.LoadPixels(image.Bounds)

	End Using

Catch exception As JpegException

	' specific processing

End Try

{{< /highlight >}}
##### **Class Constructors Summary**
1. Aspose.Imaging.Exceptions.ImageFormats.JpegException.#ctor(System.String)
1. Aspose.Imaging.Exceptions.ImageFormats.JpegException.#ctor(System.String,System.Exception)
### **Property Aspose.Imaging.FileFormats.Jpeg.JpegImage.Jfif Added**
JpegImage.Jfif property adds support of writing, reading and editing of JFIF data segment in jpeg images.
#### **Sample**
Demonstrates the usage of JpegImage.Jfif property to create JFIF data segment.

**C#**

{{< highlight csharp >}}

 using (JpegImage image = (JpegImage)Image.Load(jpegFile))

{

      image.Jfif = new JFIFData();

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As JpegImage = CType(Image.Load(jpegFile), JpegImage)

      image.Jfif = New JFIFData()

End Using

{{< /highlight >}}

Demonstrates deletion of JFIF data segment

**C#**

{{< highlight csharp >}}

 using (JpegImage image = (JpegImage)Image.Load(jpegFile))

{

      image.Jfif = null;

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As JpegImage = CType(Image.Load(jpegFile), JpegImage)

      image.Jfif = Nothing

End Using

{{< /highlight >}}
### **Property Aspose.Imaging.FileFormats.Jpeg.JpegImage.Comment Added**
JpegImage.Comment property added the support for Jpeg comment section defined by Jpeg recommendations. Comment are represented as char array in order to strictly follow the Jpeg standards.
#### **Sample**
Demonstrates the usage of JpegImage.Comment property.

**C#**

{{< highlight csharp >}}

 using (JpegImage image = (JpegImage)Image.Load(testFilePath))

{

    image.Comment = new char[4] { 'a', 'b', 'c', 'd' };

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As JpegImage = CType(Image.Load(testFilePath), JpegImage)

	image.Comment = New Char(3) { 'a', 'b', 'c', 'd' }

End Using

{{< /highlight >}}
## **Changes in Reference to CAD Image Formats**
{{% alert color="primary" %}} 

Following section explains the changes introduced in reference to CAD image formats. 

{{% /alert %}} 
### **Class Aspose.Imaging.FileFormats.Cad.CadLayoutDictionary Added**
Aspose.Imaging 2.3.0 adds support of rendering only a specific layout of DXF file format. For this purpose, a new class CadLayoutDictionary has been added to the Aspose.Imaging.FileFormats.Cad namespace.
#### **Sample**
Demonstrates the use of CadLayoutDictionary class.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    // dictionary keys by layout names

    string layoutName = "Model";

    CadLayout cadLayout = cadImage.Layouts[layoustName];

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	' dictionary keys by layout names

	Dim layoutName As String = "Model"

	Dim cadLayout As CadLayout = cadImage.Layouts(layoustName)

End Using

{{< /highlight >}}
### **Classes CadApplicationCodesContainer and CadApplicationCodes Added**
These classes collectively enable the developers to read the application-defined codes.
#### **Sample**
Demonstrates the use of CadApplicationCodesContainer & CadApplicationCodes classes.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    CadBase cadBase = cadImage.Entities[0];

    // or cadBase = cadImage.Objects[0];

    // The following are equivalent ways

    CadApplicationCodes codes1 = cadBase.ApplicationCodesContainer.GetCodes("ACAD_REACTORS");

    CadApplicationCodes cadReactorsCodes = cadImage.Entities[0].ApplicationCodesContainer.GetAcadReactorsCodes();

    // The following are equivalent ways

    CadApplicationCodes codes2 = cadBase.ApplicationCodesContainer.GetCodes("ACAD_XDICTIONARY");

    CadApplicationCodes cadAcadXDictionaryCodes = cadImage.Entities[0].ApplicationCodesContainer.GetAcadXDictionaryCodes();

    // Any group codes

    CadApplicationCodes codes3 = cadBase.ApplicationCodesContainer.GetCodes("BLKREFS");

    // iteration

    foreach (CadApplicationCodes codes in cadBase.ApplicationCodesContainer.Codes)

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

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	Dim cadBase As CadBase = cadImage.Entities(0)

	' or cadBase = cadImage.Objects[0];

	' The following are equivalent ways

	Dim codes1 As CadApplicationCodes = cadBase.ApplicationCodesContainer.GetCodes("ACAD_REACTORS")

	Dim cadReactorsCodes As CadApplicationCodes = cadImage.Entities(0).ApplicationCodesContainer.GetAcadReactorsCodes()

	' The following are equivalent ways

	Dim codes2 As CadApplicationCodes = cadBase.ApplicationCodesContainer.GetCodes("ACAD_XDICTIONARY")

	Dim cadAcadXDictionaryCodes As CadApplicationCodes = cadImage.Entities(0).ApplicationCodesContainer.GetAcadXDictionaryCodes()

	' Any group codes

	Dim codes3 As CadApplicationCodes = cadBase.ApplicationCodesContainer.GetCodes("BLKREFS")

	' iteration

	For Each codes As CadApplicationCodes In cadBase.ApplicationCodesContainer.Codes

		' codes.Name = "ACAD_REACTORS" or "ACAD_XDICTIONARY" etc.

		' codes.CodesList - data

'         for example, let a dxf file:

'         *    ...

'         *    102

'         *    {ACAD_REACTORS

'         *    330

'         *    19DE5D

'         *    102

'         *    }

'         *    ...

'         *

'         * then we have:

'         *    codes.Name == "ACAD_REACTORS"

'         *    CadCodeValue codeValue = codes.CodesList[0];

'         *    codeValue.Code == 330

'         *    codeValue.Attribute  == CadEntityAttribute.Cad330

'         *    codeValue.Value == "19DE5D"

'         *

'         *    codes.GetValue(CadEntityAttribute.Cad330) return "19DE5D"

'         

	Next codes

End Using

{{< /highlight >}}
### **Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadBaseObject Added**
CadBaseObject class provides support of reading objects' section data.
#### **Sample**
Demonstrates the use of CadBaseObject class.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    foreach (CadBaseObject cadBaseObject in cadImage.Objects)

     {

         ...

     }

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	For Each cadBaseObject As CadBaseObject In cadImage.Objects

		 ...

	Next cadBaseObject

End Using

{{< /highlight >}}
### **Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadLayout Added**
CadLayout class provides support of reading CAD Layout objects.
#### **Sample**
Demonstrates the use of CadLayout class.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    foreach (CadBaseObject cadBaseObject in cadImage.Objects)

    {

        if (cadBaseObject is CadLayout)

        {

            CadLayout cadLayout = cadBaseObject as CadLayout;

            ...

        }

    }

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	For Each cadBaseObject As CadBaseObject In cadImage.Objects

		If TypeOf cadBaseObject Is CadLayout Then

			Dim cadLayout As CadLayout = TryCast(cadBaseObject, CadLayout)

			...

		End If

	Next cadBaseObject

End Using

{{< /highlight >}}
#### **CadLayout Members Summary**
LayoutName
Name of this layout, "Model" is also a layout.

MaxExtents
Maximum extents for this layout, defined by EXTMAX while this layout is current:
cadImage.Header.HeaderProperties[CadConsts.CadHeaderAttribute.EXTMAX](/pages/createpage.action?spaceKey=imagingnet&title=CadConsts.CadHeaderAttribute.EXTMAX&linkCreation=true&fromPageId=14814882)[0](/pages/createpage.action?spaceKey=imagingnet&title=0&linkCreation=true&fromPageId=14814882)

MinExtents
Minimum extents for this layout (defined by EXTMIN while this layout is current).

TabOrder
This number is an ordinal indicating this layout's ordering in the tab control that is attached to the AutoCAD drawing frame window. Note that the “Model” tab always appears as the first tab regardless of its tab order.
### **Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadPlotSettings Added**
CadPlotSettings class provides support of reading CAD PLOTSETTINGS object.
#### **Sample**
Demonstrates the use of CadPlotSettings class.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    CadImage cadImage = (CadImage)image;

    foreach (CadBaseObject cadBaseObject in cadImage.Objects)

    {

        if (cadBaseObject is CadPlotSettings)

        {

            CadPlotSettings cadPlotSettings = cadBaseObject as CadPlotSettings;

            ...

        }

    }

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim cadImage As CadImage = CType(image, CadImage)

	For Each cadBaseObject As CadBaseObject In cadImage.Objects

		If TypeOf cadBaseObject Is CadPlotSettings Then

			Dim cadPlotSettings As CadPlotSettings = TryCast(cadBaseObject, CadPlotSettings)

			...

		End If

	Next cadBaseObject

End Using

{{< /highlight >}}
#### **CadPlotSettings Members Summary**
PageSetupName
The page setup name.

PlotPaperSize
Physical paper width and height in millimeters.

TopSize
Size, in millimeters, of unprintable margin on top of paper.

RightSideSize
Size, in millimeters, of unprintable margin on right side of paper.

BottomSize
Size, in millimeters, of unprintable margin on bottom of paper.

LeftSideSize
Size, in millimeters, of unprintable margin on left side of paper.
