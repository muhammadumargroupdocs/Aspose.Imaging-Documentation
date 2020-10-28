---
title: Manipulating TIFF Images
type: docs
weight: 240
url: /java/manipulating-tiff-images/
---

## **Add Frames with Different Settings**
TIFF is a very flexible format and it allows different frames to be added, with different dimensions, compression and other settings. Aspose.Imaging APIs allow you to add any TIFF frame of any size which helps in creating complex documents. If there is a requirement to adjust the frames during the add process to make them all equal, perform the following steps:

1. Create a new blank frame with the desired options or copy the source frame with the output options specified using the [createFrameFrom](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.tiff/TiffFrame#createFrameFrom-com.aspose.imaging.fileformats.tiff.TiffFrame-com.aspose.imaging.imageoptions.TiffOptions-) method.
1. Resize the source frame/image to the desired dimensions using the Resize method.
1. Add the source frame/image pixels to the new frame.
1. Add the new frame to the output TIFF image.
## **Export Multi Page frames to different Image format**
Sometimes you need to export Multi-page TIFF frames to some other image file format. This article will demonstrate how we can perform this task using Aspose.Imaging for Java API. We will use [TiffImage](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.tiff/TiffImage), [TiffFrame](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.tiff/TiffFrame), [BmpOptions](https://apireference.aspose.com/java/imaging/com.aspose.imaging.imageoptions/BmpOptions) and [BmpImage](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.bmp/BmpImage) classes to export TIFF frames to BMP image format. First, we will create instance of TIFF image and load images from local disk. Now we will iterate over TIFF frames and copy pixels of active frame using [loadPixels](https://apireference.aspose.com/java/imaging/com.aspose.imaging/RasterImage#loadPixels-com.aspose.imaging.Rectangle-) method into Colors array and create an instance of BmpOptions for BMP image settings. Set the desired setting for BMP image creation. Create a new BMP image using BmpOptions object and save BMP image using frame pixels, copied in Colors array.

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\dataDir\\";

try (TiffImage multiImage = (TiffImage)Image.load(dataDir + "SampleTiff1.tiff"))

{

    // Create an instance of int to keep track of frames in TiffImage

    int frameCounter = 0;

    // Iterate over the TiffFrames in TiffImage

    for (TiffFrame tiffFrame : multiImage.getFrames())

    {

        multiImage.setActiveFrame(tiffFrame);

        // Load Pixels of TiffFrame into an array of Colors

        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());

        // Create an instance of bmpCreateOptions

        try(BmpOptions bmpCreateOptions = new BmpOptions())

        {

            bmpCreateOptions.setBitsPerPixel(24);

            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved

            bmpCreateOptions.setSource(new FileCreateSource(String.format("%s\\ConcatExtractTIFFFramesToBMP_out%s.bmp", dataDir, frameCounter), false));

            // Create a new bmpImage

            try(BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))

            {

                // Save the bmpImage with pixels from TiffFrame

                bmpImage.savePixels(tiffFrame.getBounds(), pixels);

                bmpImage.save();

            }

        }

        frameCounter++;

    }

}

{{< /highlight >}}

Please note, the above provided code snippet requires setting the valid license for Aspose.Imaging for Java API. This is because Aspose.Imaging APIs restrict the usage of core features such as [loadPixels](https://apireference.aspose.com/java/imaging/com.aspose.imaging/RasterImage#loadPixels-com.aspose.imaging.Rectangle-) & [savePixels](https://apireference.aspose.com/java/imaging/com.aspose.imaging/RasterImage#savePixels-com.aspose.imaging.Rectangle-com.aspose.imaging.Color:A-) in evaluation mode. Please check the details for [Evaluation Version Limitations](/imaging/java/licensing/).
### **Extract TIFF Frames to Other Image Format using Core Functionality**
1. Create an instance of the TIFF image and load images from local disk.
1. Iterate over the TIFF frames and copy pixels of the active frame using loadPixels method into the Colors array.
1. Create an instance of any ImageOptionsBase for desired format and set mandatory properties. For the sake of elaboration, we will use JpegOptions.
1. Create a new JPEG image using the JpegOptions object and save JPEG image using frame pixels copied in the Colors array.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-ExtractTIFFFramestoOtherImageFormatusingCoreFunctionality.java" >}}

{{% alert color="primary" %}} 

Please note, the above provided code snippet requires setting the valid license for Aspose.Imaging for Java API. This is because Aspose.Imaging APIs restrict the usage of core features such as loadPixels & savePixels in evaluation mode. Please check the details for [Evaluation Version Limitations_Imaging](/pages/createpage.action?spaceKey=imagingjava&title=Evaluation+Version+Limitations_Imaging&linkCreation=true&fromPageId=15303064).

{{% /alert %}} 
### **Extract TIFF Frames to Other Image Format**
1. Create an instance of the TiffImage and load images from local disk or stream.
1. Retrieve the collection of frames in an array of type TiffFrame.
1. Create an instance of any ImageOptionsBase for desired format and set mandatory properties. For the sake of elaboration, we will use JpegOptions.
1. Call TiffFrame.save method with destination path and an instance of appropriate ImageOptionsBase.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingTIFFImages-ExtractTIFFFramestoOtherImageFormat-ExtractTIFFFramestoOtherImageFormat.java" >}}
## **Adding Multiple images inside Tiff Frames**
This article will demonstrate how we can we add multiple images inside single tiff using Aspose.Imaging for Java API. We will use [TiffImage](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.tiff/TiffImage), [TiffFrame](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.tiff/TiffFrame) classes to add multiple images inside tiff frames. Below provided code snippet demonstrates this concept.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingTIFFImages-MultipleImageToTiff-MultipleImageToTiff.java" >}}

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\DataDir\\";

Image tempImage = com.aspose.imaging.Image.load(dataDir + "Image1.png");

int width;

int height;

width = tempImage.getWidth();

height = tempImage.getHeight();

try (com.aspose.imaging.imageoptions.TiffOptions tiffOptions = new com.aspose.imaging.imageoptions.TiffOptions(TiffExpectedFormat.Default))

{

    tiffOptions.setSource(new com.aspose.imaging.sources.FileCreateSource(dataDir + "MultiPage.tiff", false));

    //Create an instance of Image and initialize it with instance of BmpOptions by calling Create method

    try (TiffImage tiffImage = (TiffImage) com.aspose.imaging.Image.create(tiffOptions, width, height))

    {

        //do some image processing

        File di = new File(dataDir);

        File[] files = di.listFiles(new FileFilter()

        {

            @Override

            public boolean accept(File pathname)

            {

                return pathname.getName().toLowerCase().endsWith(".img");

            }

        });

        if (files == null)

        {

            System.err.println("No file is found!");

            return;

        }

        int index = 0;

        for (File file : files)

        {

            try (com.aspose.imaging.Image inputImage = com.aspose.imaging.Image.load(file.getAbsolutePath()))

            {

                inputImage.resize(width, height, ResizeType.NearestNeighbourResample);

                if (index > 0)

                {

                    TiffFrame newframe = new TiffFrame(tiffOptions, width, height);

                    tiffImage.addFrame(newframe);

                }

                TiffFrame frame = tiffImage.getFrames()[index];

                frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));

                index++;

            }

        }

        // save all changes

        tiffImage.save(dataDir + "output.tiff");

    }

}

{{< /highlight >}}
## **Concatenate Multiple TIFF Images**
This article exhibits the usage of Aspose.Imaging for Java API to concatenate Tiff frames to a single Tiff image. We will use TiffImage and TiffFrame classes to concatenate multiple TIFF frames. We can use both standard methods, from file and from stream, to concatenate TIFF images.
### **Images Having Single Frame**
{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\dataDir\\";

// Create a copy of original image to avoid any alteration

FileSystem fileSystem = FileSystems.getDefault();

Files.copy(fileSystem.getPath(dataDir + "demo.tif"), fileSystem.getPath(dataDir + "TestDemo.tif"), StandardCopyOption.REPLACE_EXISTING);

// Create an instance of TiffImage and load the copied destination image

try (TiffImage image = (TiffImage)Image.load(dataDir + "TestDemo.tif"))

{

    // Create an instance of TiffImage and load the source image

    try (TiffImage image1 = (TiffImage)Image.load(dataDir + "sample.tif"))

    {

        // Create an instance of TIffFrame and copy active frame of source image, Add copied frame to destination image and  Save the image with changes.

        TiffFrame frame = TiffFrame.copyFrame(image1.getActiveFrame());

        image.addFrame(frame);

        image.save(dataDir + "ConcatTIFFImages_out.tiff");

    }

}

{{< /highlight >}}
#### **Concatenating Images from Disk**
Firstly, we will create instances of images and load images from the local disk, then we will copy the active frame of source image using [Copyframe](http://www.aspose.com/api/java/imaging/aspose.imaging.fileformats.tiff/tiffframe/methods/copyframe) method of [TiffFrame](http://www.aspose.com/api/java/imaging/aspose.imaging.fileformats.tiff/tiffframe) class and add that copied frame to destination image with the help of [Addframe](http://www.aspose.com/api/java/imaging/aspose.imaging.fileformats.tiff/tiffimage/methods/addframe) method of [TiffImage](http://www.aspose.com/api/java/imaging/aspose.imaging.fileformats.tiff/tiffimage) class. Finally we will save image back to local disk.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-images-ConcatTIFFImages-ConcatTIFFImages.java" >}}
### **Images Having Several Frames**
{{< highlight java >}}

 String dataDir = "D:\\DataDIr\\";

List<String> files = Arrays.asList(dataDir + "TestDemo.tiff", dataDir + "sample.tiff");

TiffOptions createOptions = new TiffOptions(TiffExpectedFormat.Default);

createOptions.setBitsPerSample(new int[] { 1 });

createOptions.setOrientation(TiffOrientations.TopLeft);

createOptions.setPhotometric(TiffPhotometrics.MinIsBlack);

createOptions.setCompression(TiffCompressions.CcittFax3);

createOptions.setFillOrder(TiffFillOrders.Lsb2Msb);

// Create a new image by passing the TiffOptions and size of first frame, we will remove the first frame at the end, cause it will be empty

TiffImage output = null;

try

{

    List<TiffImage> images = new ArrayList<TiffImage>();

    try

    {

        for (String file : files)

        {

            // Create an instance of TiffImage and load the source image

            TiffImage input = (TiffImage)Image.load(file);

            images.add(input); // Do not dispose before data is fetched. Data is fetched on 'Save' later.

            for (TiffFrame frame : input.getFrames())

            {

                if (output == null)

                {

                    // Create a new tiff image with first frame defined.

                    output = new TiffImage(TiffFrame.copyFrame(frame));

                }

                else

                {

                    // Add copied frame to destination image

                    output.addFrame(TiffFrame.copyFrame(frame));

                }

            }

        }

        if (output != null)

        {

            // Save the result

            output.save(dataDir + "ConcatenateTiffImagesHavingSeveralFrames_out.tif", createOptions);

        }

    }

    finally

    {

        for (TiffImage image : images)

        {

            image.close();

        }

    }

}

finally

{

    if (output != null)

    {

        output.close();

    }

}

{{< /highlight >}}
### **Add Different Images as Separate Frames in a Multi-Page TIFF**
TIFF is a flexible format allowing different frames to be added, with different dimensions, compression and other settings. This example demonstrates the usage of Aspose.Imaging for Java API to accomplish this task with core functionality.

In order to demonstrate the usage of Aspose.Imaging for Java API to add different images as frames to the resultant TIFF image, we will iterate over a list of files (.jpg) and convert them to TiffFrame before adding to the resultant TiffImage.

The following code snippet re-size all loaded images before adding them to the TiffImage

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingTIFFImages-AddDifferentImagesasSeparateFramesinaMultiPageTIFF-AddDifferentImagesasSeparateFramesinaMultiPageTIFF.java" >}}


Please note, the above provided code snippet requires setting the valid license for Aspose.Imaging for Java API. This is because Aspose.Imaging APIs restrict the usage of core features such as loadPixels & savePixels in evaluation mode. Please check the details for [Evaluation Version Limitations_Imaging](/pages/createpage.action?spaceKey=imagingjava&title=Evaluation+Version+Limitations_Imaging&linkCreation=true&fromPageId=15303064).
## **Data Recovery Options**
Sometimes you may encounter a TIFF image that cannot be rendered properly while using traditional image viewers such as Windows Photo Viewer because the image is damaged or corrupted. When loaded with Aspose.Imaging, such images may throw exceptions and you may not be able to process them further.

Aspose.Imaging for Java 2.4.0 and later supports data recovery modes for TIFF images. The data recovery allows you to load a TIFF file that has improper data layout or corrupted data strips. Data recovery replaces the corrupted data with any color specified, and you can retrieve the rest of the data for further processing without experiencing any exception.

{{% alert color="primary" %}} 

This mechanism is especially useful for TIFF file format since it stores the data in strips. When a strip is damaged the other strips may still retain the correct information.

{{% /alert %}} 

Aspose.Imaging provides two recovery modes which provide different results.

1. ConsistentRecover: The consistent recovery mode tries to recover all data as long as corruption does not break the file format and allows further processing.
1. MaximalRecover: The maximal recovery mode recovers all data even if the file format has a corrupted structure and further processing may yield unexpected effects.

Below is sample code that shows how to use the data recovery mode.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingTIFFImages-DataRecovery-DataRecovery.java" >}}

When a damaged or corrupted TIFF file is loaded or saved without using data recovery you may get an error of type com.aspose.imaging.exceptions.CompressorException.


## **TiffOptions Configuration**
Developers can adjust different properties of TiffOptions class to get desired results. In this document, we will focus on 4 main properties that controls the resultant image attributes.

These properties are listed below.

1. TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

{{% alert color="primary" %}} 

Whenever we initialize an empty TiffOptions structure, each option is set to its default value. For instance compression is set to None, BitsPerSample is set as 1 and Photometric as MinIsWhite. Saving into this format will make the final image black n white and this is expected behavior for such settings. In order to get the colored results you have to set all the above mentioned properties to values that correspond to desired color space or you can initialize the TiffOptions structure with predefined settings as discussed ahead.

{{% /alert %}} 

Provided below is a table describing the expected parameter values that you can set in order to achieve desired results. Please note, you should set all 4 columns through TiffOptions in order to save any loaded/created image to TIFF file format.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16 (palette, color mode) single channel only|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (gray-scale mode) single channel only|None|
|Palette|LZW/Uncompressed|8 (palette, color mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (gray-scale mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|RGB|LZW/Uncompressed|[8,8,8] (3 RGB channels)|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 RGB channels and additional alpha channel may be set through TiffOptions.AlphaStorage) Actually any additional channels count is supported but each channel must have 8 bit size like [8,8,8,8,8,8]|None/Horizontal|
All 4 properties should be set through TiffOptions in order to save any image format to Tiff format.

{{% alert color="primary" %}} 

When employing different combinations, some viewers (including the Windows Photo Viewer) may refuse to render the resultant image due to the limited support they offer. In such case, please pick different viewer for your testing.

{{% /alert %}} 
### **Predefined Settings for TiffOptions Class**
In order to facilitate the users and to avoid the miss-configuration of the TiffOptions instance, the Aspose.Imaging for .NET API has exposed another constructor that accepts a parameter of type TiffExpectedFormat. Based on the selected value from the TiffExpectedFormat enumeration, the API auto configures all the mandatory properties for the TiffOptions instance in order to produce the desired results.

Before we move towards the sample code, here is the list of the TiffExpectedFormat fields and their details for better understanding of the usage.

1. TiffExpectedFormat.Default: Setting the field to Default acts similar to the default constructor of TiffOptions class with no compression set and BitsPerPixel set to 1 in order to produce a black n white result. It is advised to use this field when other format specific properties are to be set manually according to the desired results.
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

The following code snippet elaborates the usage of TiffExpectedFormat fields while creating an instance of TiffOptions class.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingTIFFImages-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Support for Deflate and Adobe Deflate Compression**
The TIFF (Tagged Image File Format) file format supports various types of compression whereas the compression type is stored as a tag (an integer value) in the file. One of such compression methods is Adobe Deflate (previously known as Deflate). Since the release of Aspose.Imaging for Java 2.8.0, the API supports this compression method for loading, converting & creating TIFF images.
### **Loading Image**
Aspose.Imaging for Java API hides all the ugly details from the user and provides an easy to use mechanism to load images for further processing. In order to load a TIFF image having Adobe Deflate compression, user has to pass the file path location or stream object to the Image.Load method and cast the object to [TiffImage](http://www.aspose.com/api/net/imaging/aspose.imaging.fileformats.tiff/tiffimage) as per requirement.
### **Support Tiff deflate Images with Alpha**
Aspose.Imaging for Java API hides all the ugly details from the user and provides an easy to use mechanism to load images for further processing. In order to load a TIFF image and save that with Deflate compression with Alpha, user has to pass the file path location or stream object to the Image.load method and cast the object to [TiffImage](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.tiff/TiffImage) as per requirement.
### **Saving Image**
Converting any raster image to TIFF with Deflate/Adobe Deflate compression is easy as follow.

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\ImageData\\";

// Create an instance of TiffOptions and set its various properties

TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);

options.setBitsPerSample(new int[] { 8, 8, 8 });

options.setPhotometric(TiffPhotometrics.Rgb);

options.setXresolution(new TiffRational(72));

options.setYresolution(new TiffRational(72));

options.setResolutionUnit(TiffResolutionUnits.Inch);

options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);

// Set the Compression to AdobeDeflate

options.setCompression(TiffCompressions.AdobeDeflate);

// Or Deflate         

// Options.Compression = TiffCompressions.Deflate;

// Load an existing image in an instance of RasterImage

try (RasterImage image = (RasterImage)Image.load(dataDir + "SampleTiff1.tiff"))

{

    // Create a new TiffImage from the RasterImage and Save the resultant image while passing the instance of TiffOptions

    try (TiffImage tiffImage = new TiffImage(new TiffFrame(image)))

    {

        tiffImage.save(dataDir + "SavingRasterImage_out.tiff", options);

    }

}

{{< /highlight >}}
### **Creating Image**
Below provided sample demonstrates the usage of Aspose.Imaging for Java API to create an image from scrach using the Adobe Deflate compression method.

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\ImageData\\";

// Create an instance of TiffOptions and set its various properties

TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);

options.setBitsPerSample(new int[] { 8, 8, 8 });

options.setPhotometric(TiffPhotometrics.Rgb);

options.setXresolution(new TiffRational(72));

options.setYresolution(new TiffRational(72));

options.setResolutionUnit(TiffResolutionUnits.Inch);

options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);

// Set the Compression to AdobeDeflate

options.setCompression(TiffCompressions.AdobeDeflate);

// Or Deflate

// Options.Compression = TiffCompressions.Deflate;

// Create a new TiffImage with specific size and TiffOptions settings

try (TiffImage tiffImage = new TiffImage(new TiffFrame(options, 100, 100)))

{

    // Loop over the pixels to set the color to red

    for (int i = 0; i < 100; i++)

    {

        tiffImage.getActiveFrame().setPixel(i, i, Color.getRed());

    }

    // Save resultant image

    tiffImage.save(dataDir);

}

{{< /highlight >}}
## **Compressing TIFF Images**
Aspose.Imaging for Java API can be used to convert other raster formats to TIFF image format and even change the compression of existing TIFF image. The API can also be used to store different images as frames in a TIFF image for archiving purposes while compressing the images to lowest data size. The image compression in any case should be performed by reducing the source data size regardless of the compression algorithm used. In order to achieve the best compression ratio we may use indexed color spaces. The below provided code snippet performs the best compression using 16 indexed colors only and LZW compression algorithm however the source colors are slightly dithered.

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\ImageData\\";

// Load an image through file path location or stream

try(Image image = Image.load(dataDir + "SampleTiff.tiff"))

{

    // Create an instance of TiffOptions for the resultant image

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

    // Set BitsPerSample, Compression, Photometric mode and graycale palette

    outputSettings.setBitsPerSample(new int[]{4});

    outputSettings.setCompression(TiffCompressions.Lzw);

    outputSettings.setPhotometric(TiffPhotometrics.Palette);

    outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));

    image.save(dataDir + "SampleTiff_out.tiff", outputSettings);

}

{{< /highlight >}}

Another approach which can be used since the release of Aspose.Imaging for Java v2.8.0 is by using the Adobe Deflate compression as demonstrated below.

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\ImageData\\";

// Load an image through file path location or stream

try(Image image = Image.load(dataDir + "SampleTiff.tiff"))

{

    // Create an instance of TiffOptions for the resultant image

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);

    // Set BitsPerSample, Photometric mode & Compression mode

    outputSettings.setBitsPerSample(new int[]{4});

    outputSettings.setCompression(TiffCompressions.AdobeDeflate);

    outputSettings.setPhotometric(TiffPhotometrics.Palette);

    // Set grayscale palette

    outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));

    image.save(dataDir + "SampleTiff_out.tiff", outputSettings);

}

{{< /highlight >}}
## **Splitting TIFF Frames**
A Tiff image can have multiple frames and a requirement may arise to split these frames into several images. This article demonstrates the use of Aspose.Imaging for Java API to achieve this requirement in an efficient manner with a few lines of code.
### **Saving Each Frame in TIFF Format**
Splitting the Tiff frames is easy and can be achieved in below simple steps.

1. Firstly, create an instance of [TiffImage](https://apireference.aspose.com/java/imaging/com.aspose.imaging.fileformats.tiff/TiffImage) and load a Tiff file from the disk/stream.
1. Iterate over the Tiff frame collection.
1. Save each frame to disc in Tiff format.

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\ImageData\\";

// Create an instance of TiffImage and load the file from disc

try (TiffImage multiImage = (TiffImage)Image.load(dataDir + "SampleTiff1.tiff"))

{

    // Initialize a variable to keep track of the frames in the image, Iterate over the tiff frame collection and Save the image

    int i = 0;

    for (TiffFrame tiffFrame : multiImage.getFrames())

    {

        tiffFrame.save(dataDir + i + "_out.tiff", new TiffOptions(TiffExpectedFormat.TiffJpegRgb));

		i++;

    }

}

{{< /highlight >}}
### **Saving Each Frame in Other Format**
Most of the process is the same as discussed above with a minor change, that is; while saving the frame to disc, you may pass an object of the ImageOptionBase according to the desired raster image format. Below provided code snippet demonstrates this concept by saving each frame in PNG format.

{{< highlight java >}}

 // The path to the documents directory.

String dataDir = "D:\\ImageData\\";

// Create an instance of TiffImage and load the file from disc

try (TiffImage multiImage = (TiffImage)Image.load(dataDir + "SampleTiff1.tiff"))

{

    // Initialize a variable to keep track of the frames in the image, Iterate over the tiff frame collection and Save the image

    int i = 0;

    for (TiffFrame tiffFrame : multiImage.getFrames())

    {

        tiffFrame.save(dataDir + i + "_out.png", new PngOptions());

		i++;

    }

}

{{< /highlight >}}
## **Memory strategy optimization**
Loading and saving of Tiff images can be proceeded using memory strategy optimization - ie limiting memory buffer size for operation.

{{< highlight java >}}

 // Setting a memory limit of 10 megabytes for target loaded image

try (Image image = Image.load("Default.tiff", new LoadOptions() {{ setBufferSizeHint(10); }}))

{

    image.save("Default_export.tiff", new TiffOptions(TiffExpectedFormat.Default));

}

try (Image image = Image.load("TiffCcitRle.tiff", new LoadOptions() {{ setBufferSizeHint(10); }}))

{

    image.save("TiffCcitRle_export.tiff", new TiffOptions(TiffExpectedFormat.TiffCcitRle));

}

try (Image image = Image.load("TiffDeflateRgb.tiff", new LoadOptions() {{ setBufferSizeHint(10); }}))

{

    image.save("TiffDeflateRgb_export.tiff", new TiffOptions(TiffExpectedFormat.TiffDeflateRgb));

}

try (Image image = Image.load("TiffJpegYCbCr.tiff", new LoadOptions() {{ setBufferSizeHint(10); }}))

{

    image.save("TiffJpegYCbCr_export.tiff", new TiffOptions(TiffExpectedFormat.TiffJpegYCbCr));

}

try (Image image = Image.load("TiffLzwCmyk.tiff", new LoadOptions() {{ setBufferSizeHint(10); }}))

{

    image.save("TiffLzwCmyk_export.tiff", new TiffOptions(TiffExpectedFormat.TiffLzwCmyk));

}

try (Image image = Image.load("TiffNoCompressionRgb.tiff", new LoadOptions() {{ setBufferSizeHint(10); }}))

{

    image.save("TiffNoCompressionRgb_export.tiff", new TiffOptions(TiffExpectedFormat.TiffNoCompressionRgb));

}

{{< /highlight >}}
## **Tiff image export in batch mode**
Aspose.Imaging library supports possibility of batch conversion before saving (exporting) Tiff images. This makes it possible not to keep in memory the resources of all processed pages at the same time, which will certainly give a significant performance boost with a lack of memory. With enough memory, the performance in standard mode and batch mode is the same, but the memory consumption in batch mode is much lower for multi-page tiff images (see illustrations below).

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Tiff-batch-mode-example.java" >}}
## **Support for extracting paths from TIFF**
#### **Clipping Path**
Clipping path is the Photoshop technique to remove the background from an image. Photoshop allows you to select a part of an image using Clipping Path and save the path within a file. Clipping Paths allow you to hide the part of an image you don't want to appear. Anything inside the clipping path will be visible, but anything outside of it will be transparent.

Other words Photoshop makes it possible to isolate certain parts of an image, without permanently changing the layer. This allows you to tweak the image at any point in the creative process. Clipping Paths are a traditional method of cutting out objects or people in Photoshop that allows you to create image files with transparent backgrounds. This approach works best with objects or people with "hard" edges around the object or person you want to cut out.
#### **Access Clipping Paths in TIFF image**
*PathResources* property allows you to access Clipping Paths in TIFF frame. The following code retrieves paths from TIFF image and displays their names in the console:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-Access-Clipping-Path-In-Tiff-Image.java" >}}
#### **Modify existing Clipping Paths**
You can easily modify already existing Clipping Paths. For instance, you can keep only one Clipping Path in the image:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-Modify-Clipping-Path-In-Tiff-Image.java" >}}
#### **Create Clipping Path manually**
You can manually create Clipping Path in TIFF image. In order to do that you need to create an instance of *PathResource* class. The following code demonstrates the way how you can create an empty path in TIFF image:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-Create-Clipping-Path-Manually.java" >}}

#### **Get existing Clipping Path**
The following code shows how to get existing Clipping Path from TIFF image:
{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-get-existing-clipping-path.java" >}}

#### **Change Clipping Path**
In case if you have multiple paths in TIFF image you can easily change which of them is Clipping Path:
{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-change-clipping-path.java" >}}

#### **Create Clipping Path from scratch**
The following source code sample demonstrates how to create paths in TIFF image from scratch:
{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-create-clipping-path-from-scratch.java" >}}

#### **Clipping Path content**
To create your own Clipping Paths you need to understand their content. Photoshop stores its paths as resources with IDs in the range 2000 through 2997. The name of the resource is the name given to the path when it was saved. If the file contains a resource with an ID of 2999, then this resource contains the name of the clipping path. Each path has a set of records to hold the data.

**Record classes:** 
*LengthRecord* - contains the number of Bezier knot records.
*BezierKnotRecord* - describes the knots of the path.
*ClipboardRecord* - contains four fixed-point numbers for the bounding rectangle.

More details you can find in [Adobe Photoshop File Formats Specification](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/).




