---
title: Aspose.Imaging for Java 18.2 - Release Notes
type: docs
weight: 80
url: /java/aspose-imaging-for-java-18-2-release-notes/
---

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|IMAGINGJAVA-896|Implement [Jpeg DCT extended sequential, Huffman. 12-bit] decoder. |Feature|
|IMAGINGJAVA-892|Support tiff deflate images with alpha |Feature|
|IMAGINGJAVA-891|Support for converting image to gray scale with setting 16bit or 8 bit |Feature|
|IMAGINGJAVA-748|PSD to PDF conversion|Feature|
|IMAGINGJAVA-903|Unable to convert 360MB TIFF file to PDF |Enhancement|
|IMAGINGJAVA-902|Converting EMF to SVG format is not working properly. It is generating SVG file but SVG file is empty |Enhancement|
|IMAGINGJAVA-901|Converting WMF to SVG format is not working properly. It is generating SVG file but SVG file is empty |Enhancement|
|IMAGINGJAVA-900|Applying MedianFilterOptions on an image is blurring the resultant image |Enhancement|
|IMAGINGJAVA-899|System.IndexOutOfRangeException when load pixels from Tiff image |Enhancement|
|IMAGINGJAVA-898|Chart axis values are improperly positioned when exporting SVG to PNG |Enhancement|
|IMAGINGJAVA-897|Improve performance Jpeg2000 decoder |Enhancement|
|IMAGINGJAVA-895|Incorrect exporting EMF+ to SVG |Enhancement|
|IMAGINGJAVA-894|Support the [interlaced Gif to non-interlaced PNG] conversion |Enhancement|
|IMAGINGJAVA-893|Fix PSD export of multiple styles for a single text layer |Enhancement|
|IMAGINGJAVA-882|JP2 Image export failed|Enhancement|
|IMAGINGJAVA-863|EMF to PDF generated blank document|Enhancement|
|IMAGINGJAVA-836|File Format property not working for PNG|Enhancement|
|IMAGINGJAVA-832|EMF image is not converted properly|Enhancement|
|IMAGINGJAVA-829|Coordinate of left top corner is incorrect at update|Enhancement|
|IMAGINGJAVA-762|Improper export of SVG export to PNG, JPEG and BMP formats|Enhancement|
# **Public API changes:**
## **Added APIs:**
Please see corresponding cumulative [API changes for Aspose.Imaging for .Net 18.2](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+18.2+-+Release+Notes) version
## **Removed APIs:**
Please see corresponding cumulative [API changes for Aspose.Imaging for .Net 18.2](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+18.2+-+Release+Notes) version
# **Usage examples:**
**IMAGINGJAVA-896 Implement [Jpeg DCT extended sequental, Huffman. 12-bit] decoder. [Java]**

{{< highlight java >}}

 String dir = "";

String[] sourceFileNames = new String[]

{

"Grayscale 12-bit.jpg",

"YCbCr 12-bit.jpg",

"Grayscale 12-bit NewView.jpg", // generated with NewView Graphics' File Viewer

"YCbCr 12-bit NewView.jpg", // generated with NewView Graphics' File Viewer

};

String[] outputFileNames = new String[]

{

"Decoded Grayscale Jpeg 12-bit.png",

"Decoded YCbCr Jpeg 12-bit.png",

"Decoded Grayscale Jpeg 12-bit.png",

"Decoded YCbCr Jpeg 12-bit.png",

};

PngOptions options = new PngOptions();

for (int i = 0; i < sourceFileNames.length; ++i)

{

// Load Jpeg DCT 12-bit and save it to PNG.

Image image = Image.load(dir + sourceFileNames[i]);

try

{

image.save(dir + outputFileNames[i], options);

}

finally

{

image.dispose();

}

}

{{< /highlight >}}

**IMAGINGJAVA-892 Support tiff deflate images with alpha [Java]** 
input file: [Alpha.png](https://kiev.dynabic.com/jira/secure/attachment/23076/23076_Alpha.png)

{{< highlight java >}}

 String inputFile = "C:\\Temp\\Errors\\Alpha.png";

String outputFileTiff = "C:\\Temp\\Alpha.tiff";

String outputFilePng = "C:\\Temp\\Alpha1.png";

Image image = Image.load(inputFile);

try

{

TiffOptions options = new TiffOptions(TiffExpectedFormat.TiffDeflateRgba);

image.save(outputFileTiff, options);

}

finally

{

image.dispose();

}

image = Image.load(outputFileTiff);

try

{

Assert.assertEquals(((RasterImage)image).hasAlpha(), true);

PngOptions options = new PngOptions();

options.setColorType(PngColorType.TruecolorWithAlpha);

image.save(outputFilePng, options);

}

finally

{

image.dispose();

}

{{< /highlight >}}

Result file "Alpha1.png" must equal the input file - "Alpha.png"
**IMAGINGJAVA-891 Support for converting image to grayscale with setting 16bit or 8 bit [Java]**

{{< highlight java >}}

 String srcDir = "IMAGINGNET-2160\\";

String outputFolder = "C:\\temp\\";

int[] colorTypes = new int[]

{

JpegCompressionColorMode.Grayscale,

JpegCompressionColorMode.YCbCr,

JpegCompressionColorMode.Rgb,

JpegCompressionColorMode.Cmyk,

JpegCompressionColorMode.Ycck,

};

String[] sourceFileNames = new String[]

{

"Rgb.jpg",

"Rgb.jpg",

"Rgb.jpg",

"Rgb.jpg",

"Rgb.jpg",

};

JpegOptions options = new JpegOptions();

options.setBitsPerChannel((byte)12);

for (int i = 0; i < colorTypes.length; ++i)

{

options.setColorType(colorTypes[i]);

String fileName = JpegCompressionColorMode.getName(JpegCompressionColorMode.class, colorTypes[i]) + " 12-bit.jpg";

String referencePath = srcDir + fileName;

String outputPath = outputFolder + fileName;

Image image = Image.load(srcDir + sourceFileNames[i]);

try

{

image.save(outputPath, options);

}

finally

{

image.dispose();

}

}

{{< /highlight >}}

**IMAGINGJAVA-748 Psd to pdf conversion** 
Input file: [FromRasterImageEthalon.psd](https://kiev.dynabic.com/jira/secure/attachment/23104/FromRasterImageEthalon.psd)

{{< highlight java >}}

 String sourceFileName = "FromRasterImageEthalon.psd";

String outputfile = "result.pdf";

Image image = Image.load(sourceFileName);

try

{

PsdImage psdImage = (PsdImage)image;

PdfOptions exportOptions = new PdfOptions();

exportOptions.setPdfDocumentInfo(new com.aspose.imaging.fileformats.pdf.PdfDocumentInfo());

psdImage.save(outputfile, exportOptions);

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-902 Converting EMF to SVG format is not working properly. It is generating SVG file but SVG file is empty [Java]** 
Input files: [images.zip](https://kiev.dynabic.com/jira/secure/attachment/22951/images.zip)

{{< highlight java >}}

 String[] fileNames = {"000096_image86.emf", "000096_image84.emf", "000097_image2.emf", "000097_image3.emf"};

String baseFolder = "C:\\Temp\\Errors\\902\\";

for (String fileName : fileNames)

{

String sourcePath = baseFolder + fileName;

String destPath = sourcePath + ".svg";

Image image = Image.load(sourcePath);

try

{

final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

emfRasterizationOptions.setBackgroundColor(Color.getWhite());

emfRasterizationOptions.setPageWidth(image.getWidth());

emfRasterizationOptions.setPageHeight(image.getHeight());

image.save(destPath, new SvgOptions()

{{

setVectorRasterizationOptions(emfRasterizationOptions);

}});

}

finally

{

image.dispose();

}

}

{{< /highlight >}}

**IMAGINGJAVA-901 Converting WMF to SVG format is not working properly. It is generating SVG file but SVG file is empty [Java]** 
Input file: [000096_image73.wmf](https://kiev.dynabic.com/jira/secure/attachment/21489/21489_000096_image73.wmf)
Output file: [000096_image73.wmf.svg]()

{{< highlight java >}}

 String sourcePath = "000096_image73.wmf";

String destPath = sourcePath + ".svg";

Image image = Image.load(sourcePath);

try

{

final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

emfRasterizationOptions.setBackgroundColor(Color.getWhite());

emfRasterizationOptions.setPageWidth(image.getWidth());

emfRasterizationOptions.setPageHeight(image.getHeight());

image.save(destPath, new SvgOptions() {{ setVectorRasterizationOptions(emfRasterizationOptions); }});

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-900 Applying MedianFilterOptions on an image is bluring the resultant image [Java]** 
Input file: [skewpng.tiff](https://kiev.dynabic.com/jira/secure/attachment/21540/skewpng.tiff)

{{< highlight java >}}

 String dir = "C:\\Temp\\Errors\\";

String inputFileName = "skewpng.tiff";

for (int size = 1; size < 6; ++size)

{

String outputFileName = String.format("skewpng median filter %1$dx%1$d.tiff", size);

MedianFilterOptions options = new MedianFilterOptions(size);

RasterImage image = (RasterImage)Image.load(dir + inputFileName);

try

{

image.filter(image.getBounds(), options);

image.save(dir + outputFileName);

}

finally

{

image.dispose();

}

}

{{< /highlight >}}

**IMAGINGJAVA-899 System.IndexOutOfRangeException when load pixels from Tiff image [Java]** 
Input file: [UnspecifiedAlpha.tif](https://kiev.dynabic.com/jira/secure/attachment/21559/UnspecifiedAlpha.tif)

{{< highlight java >}}

 String sourceFilePath = "UnspecifiedAlpha.tif";

String outputFilePath = "UnspecifiedAlpha PackBits Out.jpg";

BlackBoxTestsController.setMaxAllocatedBytesCount(512);

try

{

TiffImage image = (TiffImage)Image.load(sourceFilePath);

try

{

image.save(outputFilePath, new JpegOptions(), image.getBounds());

}

finally

{

image.dispose();

}

}

finally

{

BlackBoxTestsController.setMaxAllocatedBytesCount(0);

}

{{< /highlight >}}

**IMAGINGJAVA-898 chart axis values are improperly positioned when exporting SVG to PNG [Java]** 
Input file : [SvgData.svg](https://kiev.dynabic.com/jira/secure/attachment/22953/22953_SvgData.svg)

{{< highlight java >}}

 String path = "Errors\\";

StringBuilder svgContent = new StringBuilder();

FileReader input = new FileReader(path + "SvgData.svg");

try

{

BufferedReader br = new BufferedReader(input);

String s;

while ((s = br.readLine()) != null)

{

svgContent.append(s).append("\n");

}

}

finally

{

input.close();

}

byte[] data = svgContent.toString().getBytes("UTF-8");

SvgImage svgImage = (SvgImage)Image.load(new ByteArrayInputStream(data));

try

{

svgImage.save(path + "SvgData.png", new PngOptions());

}

finally

{

svgImage.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-897 Improve performance Jpeg2000 decoder [Java]**

{{< highlight java >}}

 @Test

public void testByBounds()

{

String p = "C:\\Temp\\Errors\\122\\jpeg2000\\";

testByBounds(p + "testBig.j2k", 0, 6 * 5);

testByBounds(p + "multi.jpx", 0, 15 * 5);

}

private static void testByBounds(String filePath, int height, int C)

{

int t = 0;

StopWatch sw = new StopWatch();

double time = 0;

RasterImage image = (RasterImage)Image.load(filePath);

try

{

for (int i = 0; i < C; i++)

{

sw.start();

int[] pixels = image.loadArgb32Pixels(

height == 0 ? image.getBounds()

: new Rectangle(0, i, image.getWidth(), height));

sw.stop();

time += sw.getElapsed();

t += pixels.length;

pixels = null;

BlackBoxGC.freeMem();

}

}

finally

{

image.dispose();

}

System.out.println("ByBounds " + filePath + " : " + time + " " + t);

}

public class StopWatch {

private long m_endTimeStamp;

private long m_startTimeStamp;

private boolean m_isRunning;

public void start()

{

m_isRunning = true;

m_startTimeStamp = System.nanoTime();

}

public void stop()

{

m_isRunning = false;

m_endTimeStamp = System.nanoTime();

}

public void reset()

{

m_startTimeStamp = 0;

m_endTimeStamp = 0;

}

/**

\* Returns the seconds between Start and Stop methods calling.

\* @return Seconds between Start and Stop methods calling.

*/

public double getElapsed() {

double elapsed = m_endTimeStamp - m_startTimeStamp;

return elapsed / 1000000000.0;

}

public boolean isRunning()

{

return m_isRunning;

}

}


{{< /highlight >}}

|**File**|**old (sec)**|**new (sec)**|**Performance (%)**|
| :- | :- | :- | :- |
|testBig.j2k|99.95|98.76|1.2%|
|multi.jpx|105.8|94.08|12.4%|
**IMAGINGJAVA-895 Incorrect exporting Emf+ to Svg [Java]** 
Input file: [22955_powerpoint_emf.emf](https://kiev.dynabic.com/jira/secure/attachment/22955/22955_powerpoint_emf.emf)

{{< highlight java >}}

 String fileName = "powerpoint_emf.emf";

String baseFolder = "C:\\Temp\\Errors\\";

String inputFile = baseFolder + fileName;

String outputFile = baseFolder + fileName+".svg";

Image image = Image.load(inputFile);

try

{

final EmfRasterizationOptions rasterizationOptions = new EmfRasterizationOptions();

rasterizationOptions.setPageWidth(image.getWidth());

rasterizationOptions.setPageHeight(image.getHeight());

image.save(outputFile, new SvgOptions() {{ setVectorRasterizationOptions(rasterizationOptions); }});

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-894 Support the [interlaced Gif to non-interlaced Png] conversion [Java]** 
Input files: [6.gif](https://kiev.dynabic.com/jira/secure/attachment/23087/6.gif), [transbugs.gif](https://kiev.dynabic.com/jira/secure/attachment/23088/transbugs.gif)

{{< highlight java >}}

 //Please use the following code to convert transparent interlaced Gif to transparent interlaced Png:

{

String inputPath = "transbugs.gif";

String outputPath = "transbugs.gif.interlaced.png";

PngOptions options = new PngOptions();

options.setColorType(PngColorType.TruecolorWithAlpha);

options.setProgressive(true);

Image image = Image.load(inputPath);

try

{

image.save(outputPath, options);

}

finally

{

image.dispose();

}

}

//Please use the following code to convert non-transparent interlaced Gif to non-transparent interlaced Png:

{

String inputPath = "6.gif";

String outputPath = "6.gif.interlaced.png";

PngOptions options = new PngOptions();

options.setColorType(PngColorType.Truecolor);

options.setProgressive(true);

Image image = Image.load(inputPath);

try

{

image.save(outputPath, options);

}

finally

{

image.dispose();

}

}

{{< /highlight >}}

**IMAGINGJAVA-893 Fix PSD export of multiple styles for a single text layer [Java]** 
Input file and ethalon: [2664.zip](https://kiev.dynabic.com/jira/secure/attachment/23050/2664.zip)

{{< highlight java >}}

 String inputFile = "original.psd";

String outputFile = "exported.png";

Image image = Image.load(inputFile);

try

{

PngOptions options = new PngOptions();

options.setColorType(PngColorType.TruecolorWithAlpha);

image.save(outputFile, options);

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-863 Emf to pdf generated blank document** 
Input file: [IMAGINGNET-2654_example.zip](https://kiev.dynabic.com/jira/secure/attachment/23093/IMAGINGNET-2654_example.zip)

{{< highlight java >}}

 String filePath = "1003.emf";

com.aspose.imaging.fileformats.emf.EmfImage image =

(com.aspose.imaging.fileformats.emf.EmfImage) com.aspose.imaging.Image.load(filePath);

try

{

com.aspose.imaging.imageoptions.EmfRasterizationOptions emfRasterization =

new com.aspose.imaging.imageoptions.EmfRasterizationOptions();

emfRasterization.setPageWidth(image.getWidth());

emfRasterization.setPageHeight(image.getHeight());

emfRasterization.setBackgroundColor(com.aspose.imaging.Color.getWhiteSmoke());

com.aspose.imaging.imageoptions.PdfOptions pdfOptions =

new com.aspose.imaging.imageoptions.PdfOptions();

pdfOptions.setVectorRasterizationOptions(emfRasterization);

image.save(filePath + ".pdf", pdfOptions);

PngOptions pngOptions = new PngOptions();

pngOptions.setVectorRasterizationOptions(emfRasterization);

image.save(filePath + ".png", pngOptions);

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-836 File Format property not working for png**

{{< highlight java >}}

 Image image = Image.load("1509720284.png");

try

{

long format = image.getFileFormat();

System.out.println("Format: " + FileFormat.getName(FileFormat.class, format));

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-829 Coordinate of left top corner is incorrect at update** 
Input file: [2635.zip](https://kiev.dynabic.com/jira/secure/attachment/22944/2635.zip)

{{< highlight java >}}

 String sourceFileName = "logodpwit_006.psd";

String outFileNamePngClient = "logodpwit_006_client.png";

String outFileNamePngTopLeftPart = "logodpwit_006_topLeftPart.png";

String outFileNamePngTopLeftFull = "logodpwit_006_topLeftFull.png";

String outFileNamePngBottomRightPart = "logodpwit_006_bottomRightPart.png";

String outFileNamePngBottomRightFull = "logodpwit_006_bottomRightFull.png";

PngOptions pngOptions = new PngOptions() {{ setColorType(PngColorType.TruecolorWithAlpha); }};

PsdImage image;

TextLayer textLayer;

image = (PsdImage)Image.load(sourceFileName);

try

{

for (Layer layer : image.getLayers())

{

if (!(layer instanceof TextLayer))

{

continue;

}

textLayer = (TextLayer)layer;

if (textLayer.getName().equals("Layer II"))

{

// client's case

textLayer.updateText(textLayer.getText(), new Point(583, 457));

}

}

image.save(outFileNamePngClient, pngOptions);

}

finally

{

image.dispose();

}

image = (PsdImage)Image.load(sourceFileName);

try

{

for (Layer layer : image.getLayers())

{

if (!(layer instanceof TextLayer))

{

continue;

}

textLayer = (TextLayer)layer;

if (textLayer.getName().equals("Layer II"))

{

// partially visible on top left

textLayer.updateText(textLayer.getText(), new Point(-5, -50));

}

}

image.save(outFileNamePngTopLeftPart, pngOptions);

}

finally

{

image.dispose();

}

image = (PsdImage)Image.load(sourceFileName);

try

{

for (Layer layer : image.getLayers())

{

if (!(layer instanceof TextLayer))

{

continue;

}

textLayer = (TextLayer)layer;

if (textLayer.getName().equals("Layer II"))

{

// partially visible on top left

textLayer.updateText(textLayer.getText(), new Point(-50, -200));

}

}

image.save(outFileNamePngTopLeftFull, pngOptions);

}

finally

{

image.dispose();

}

image = (PsdImage)Image.load(sourceFileName);

try

{

for (Layer layer : image.getLayers())

{

if (!(layer instanceof TextLayer))

{

continue;

}

textLayer = (TextLayer)layer;

if (textLayer.getName().equals("Layer II"))

{

// partially visible on top left

textLayer.updateText(textLayer.getText(), new Point(image.getBounds().getRight() - 50, image.getBounds().getBottom() - 200));

}

}

image.save(outFileNamePngBottomRightPart, pngOptions);

}

finally

{

image.dispose();

}


image = (PsdImage)Image.load(sourceFileName);

try

{

for (Layer layer : image.getLayers())

{

if (!(layer instanceof TextLayer))

{

continue;

}

textLayer = (TextLayer)layer;

if (textLayer.getName().equals("Layer II"))

{

// partially visible on top left

textLayer.updateText(textLayer.getText(), new Point(image.getBounds().getRight() + 50, image.getBounds().getBottom() + 200));

}

}

image.save(outFileNamePngBottomRightFull, pngOptions);

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-762 Improper export of SVG export to PNG, Jpeg and BMP formats** 
Input file: [file1.svg](https://kiev.dynabic.com/jira/secure/attachment/22949/22949_file1.svg)

{{< highlight java >}}

 String fileName = "file1.svg";

String baseFolder = "Errors\\";

String inputFile = baseFolder + fileName;

String outputFile = baseFolder + fileName + ".png";

final Image image = Image.load(inputFile, new SvgLoadOptions() {{ setDefaultHeight(1275); setDefaultWidth(1200); }});

try

{

image.save(outputFile,

new PngOptions()

{{

setVectorRasterizationOptions(new SvgRasterizationOptions() {{

setPageSize(Size.to_SizeF(image.getSize()));

}});

}});

}

finally

{

image.dispose();

}

{{< /highlight >}}
