---
title: Aspose.Imaging for Java 17.12 - Release Notes
type: docs
weight: 10
url: /java/aspose-imaging-for-java-17-12-release-notes/
---

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|IMAGINGJAVA-849|Support for converting CMYK PSD to CMYK TIFF|Feature|
|IMAGINGJAVA-870|TypeTool6ResourceProcessor.ReplaceTextInGlobalResources does not work|Enhancement|
|IMAGINGJAVA-869|Incorrect condition statement in DgImage.RawProcess|Enhancement|
|IMAGINGJAVA-868|Incorrect condition statement in DgImage.Unpack|Enhancement|
|IMAGINGJAVA-867|Improve Djvu performance|Enhancement|
|IMAGINGJAVA-866|Corrupted DngImage.Width and DngImage.Height after calling the Image.GetPixel method|Enhancement|
|IMAGINGJAVA-865|GIF image is not properly converted to Png|Enhancement|
|IMAGINGJAVA-864|Incorrect number conversion in OpenDocument support class: OdEnhancedGeometryReader.ReadEnd|Enhancement|
|IMAGINGJAVA-862|Image exception on load TIFF image|Enhancement|
|IMAGINGJAVA-861|Improve memory usage of Jpeg fomat through improving work with buffer|Enhancement|
|IMAGINGJAVA-860|OpenTypeInfoCacheProcessor.UpdateFontsCacheFromFolders throws exception and breaks the work if there are zero files in Fonts directory|Enhancement|
|IMAGINGJAVA-859|Image saving failed when saving JPEG2000 as PNG|Enhancement|
|IMAGINGJAVA-858|Exception on converting emf to SVG|Enhancement|
|IMAGINGJAVA-857|Fix PSD crop operation|Enhancement|
|IMAGINGJAVA-856|Fix PSD test rendering for specific case|Enhancement|
|IMAGINGJAVA-855|Exception on saving TIFF Image|Enhancement|
|IMAGINGJAVA-854|GIF not properly converted to PNG|Enhancement|
|IMAGINGJAVA-834|When PSD is converted to PNG, an ArgumentOutOfRangeException occurs|Enhancement|
|IMAGINGJAVA-783|Darker colors and color reproducibility|Enhancement|
|IMAGINGJAVA-618|Converting EMF to PNG in not producing correct outpout|Enhancement|
|IMAGINGJAVA-510|EMF image export error|Enhancement|
# **Public API changes:**
## **Added APIs:**
Please see corresponding cumulative [API changes for Aspose.Imaging for .Net 17.12](https://docs.aspose.com/display/imagingnet/Aspose.Imaging+for+.NET+17.12+-+Release+Notes) version
## **Removed APIs:**
` `Nothing
# **Usage examples:**
**IMAGINGJAVA-849 Support for converting CMYK PSD to CMYK Tiff [Java]** 
input files: [cmyk.psd](https://kiev.dynabic.com/jira/secure/attachment/22854/22854_cmyk.psd) - source file, [JapanWebCoated.icc](https://kiev.dynabic.com/jira/secure/attachment/22857/22857_JapanWebCoated.icc) - Icc profile.
output files: [cmyk_False.tiff](https://kiev.dynabic.com/jira/secure/attachment/22855/22855_cmyk_False.tiff) - cmyk tiff without Icc profile, [cmyk_True.tiff](https://kiev.dynabic.com/jira/secure/attachment/22856/22856_cmyk_True.tiff) - cmyk tiff with Icc profile.

{{< highlight java >}}

 public void test() throws IOException

{

String folder = "D:\\tiff\\";

//With IccProfile

this.psdToTiffCmyk(folder,true);

//Without IccProfile

this.psdToTiffCmyk(folder, false);

}

private void psdToTiffCmyk(String folder, boolean isIccProfile) throws IOException

{

String fileName = String.format("cmyk_%b.tiff", isIccProfile);

String inputFile = folder + "cmyk.psd";

String inputIccFile = folder + "JapanWebCoated.icc";

String outputFile = folder + fileName;

Image image = Image.load(inputFile);

try

{

if (isIccProfile)

{

FileInputStream f = new FileInputStream(inputIccFile);

final byte[] icc = new byte[f.available()];

f.read(icc);

f.close();

image.save(outputFile, new TiffOptions(TiffExpectedFormat.TiffLzwCmyk)

{{

setIccProfile(icc);

}});

}

else

{

image.save(outputFile, new TiffOptions(TiffExpectedFormat.TiffLzwCmyk));

}

}

finally

{

image.dispose();

}

}


{{< /highlight >}}

**IMAGINGJAVA-870** [**TypeTool6ResourceProcessor**](/pages/createpage.action?spaceKey=imagingjava&title=TypeTool6ResourceProcessor&linkCreation=true&fromPageId=60229174)**.[ReplaceTextInGlobalResources](/pages/createpage.action?spaceKey=imagingjava&title=ReplaceTextInGlobalResources&linkCreation=true&fromPageId=60229174)** **does not work. [Java]** 
Fix is related to saving PSD metadata after text update (part of it was just not saved), which can be checked by working with updated PSD file directly from Photoshop. If export to other format was the case for you, just don't bother with it.
**IMAGINGJAVA-869 Incorrect condition statement in** [**DgImage**](/pages/createpage.action?spaceKey=imagingjava&title=DgImage&linkCreation=true&fromPageId=60229174)**.[RawProcess](/pages/createpage.action?spaceKey=imagingjava&title=RawProcess&linkCreation=true&fromPageId=60229174)** **[Java]** 
input file: [Phantom1.dng](https://www.dropbox.com/s/1tdg0uswgq9q68e/Phantom1.DNG?dl=0)
output file: [phantom1.png](https://www.dropbox.com/s/f1ewcskl8xol28y/Phantom1.png?dl=0)

{{< highlight java >}}

 String inputFileName = "D:\\Phantom1.dng";

String outFileName = "D:\\Phantom1.png";

Image image = Image.load(inputFileName, new DngLoadOptions() {{ setFbdd(NoiseReductionType.Full); }});

try

{

image.save(outFileName, new PngOptions());

}

finally

{

image.dispose();

}


{{< /highlight >}}

**IMAGINGJAVA-868 Incorrect condition statement in** [**DgImage**](/pages/createpage.action?spaceKey=imagingjava&title=DgImage&linkCreation=true&fromPageId=60229174)**.Unpack [Java]** 
input file: [Phantom1.dng](https://www.dropbox.com/s/1tdg0uswgq9q68e/Phantom1.DNG?dl=0)
output file: [phantom1.png](https://www.dropbox.com/s/f1ewcskl8xol28y/Phantom1.png?dl=0)

{{< highlight java >}}

 String inputFileName = "D:\\Phantom1.dng";

String outFileName = "D:\\Phantom1.png";

Image image = Image.load(inputFileName, new DngLoadOptions());

try

{

image.save(outFileName, new PngOptions());

}

finally

{

image.dispose();

}


{{< /highlight >}}

**IMAGINGJAVA-867 Improve Djvu performance [Java]** 
Please download this file: [superhero.djvu](https://kiev.dynabic.com/jira/secure/attachment/22892/22892_superhero.djvu)
And execute follow code with current library and 17.10 library.
Time of execute in the current library less by 20% than in library 17.10.

{{< highlight java >}}

 String fileName = "superhero.djvu";

String outputFile = "result.tiff";

DjvuImage image = (DjvuImage) Image.load(fileName);

try

{

TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.Default);

try

{

exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(new IntRange(0, 10)));

image.save(outputFile, exportOptions);

}

finally

{

exportOptions.dispose();

}

}

finally

{

image.dispose();

}

{{< /highlight >}}

|**Configuration**|**time in Current lib**|**time in 17.10**|
| :- | :- | :- |
|Core i5 10GB Win 10 x64|10.905s|13.317s|
**IMAGINGJAVA-866 Corrupted** [**DngImage**](/pages/createpage.action?spaceKey=imagingjava&title=DngImage&linkCreation=true&fromPageId=60229174)**.Width and** [**DngImage**](/pages/createpage.action?spaceKey=imagingjava&title=DngImage&linkCreation=true&fromPageId=60229174)**.Height after calling the Image.[GetPixel](/pages/createpage.action?spaceKey=imagingjava&title=GetPixel&linkCreation=true&fromPageId=60229174)** **method. [Java]** 
input file: [berries-raw](https://www.dropbox.com/s/zasvoi1brpys7pj/berries-raw.dng?dl=0)

{{< highlight java >}}

 int expectedWidth;

int expectedHeight;

String inputFilename = "berries-raw.dng";

String outFileName = "result.tiff";

DngImage image = (DngImage) Image.load(inputFilename);

try

{

expectedWidth = image.getWidth();

expectedHeight = image.getHeight();

Color c = image.getPixel(3303, 1787);

System.out.println(c);

if (expectedWidth != image.getWidth())

{

throw new RuntimeException(String.format("Current file: Expected width = %d, Actual width = %d", expectedWidth, image.getWidth()));

}

if (expectedHeight != image.getHeight())

{

throw new RuntimeException(String.format("Current file: Expected height = %d, Actual height = %d", expectedHeight, image.getHeight()));

}

image.save(

outFileName,

new TiffOptions(TiffExpectedFormat.TiffNoCompressionRgb));

}

finally

{

image.dispose();

}

Image image2 = Image.load(outFileName);

try

{

if (expectedWidth != image2.getWidth())

{

throw new RuntimeException(String.format("Result file: Expected width = %d, Actual width = %d", expectedWidth, image2.getWidth()));

}

if (expectedHeight != image2.getHeight())

{

throw new RuntimeException(String.format("Result file: Expected height = %d, Actual height = %d", expectedHeight, image2.getHeight()));

}

}

finally

{

image2.dispose();

}


{{< /highlight >}}

**IMAGINGJAVA-865 Gif image is not properly converted to Png [Java]** 
input file: [gif.zip](https://kiev.dynabic.com/jira/secure/attachment/22757/gif.zip)

{{< highlight java >}}

 String path = "transbugs.gif";

Image m_oDocument = Image.load(path);

try

{

int m_iResolution = 98;

PngOptions OptionsIM = new PngOptions();

OptionsIM.setColorType(PngColorType.TruecolorWithAlpha);

ResolutionSetting oResIM = new ResolutionSetting(m_iResolution, m_iResolution);

OptionsIM.setResolutionSettings(oResIM);

m_oDocument.save(path + ".png", OptionsIM);

}

finally

{

m_oDocument.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-864 Incorrect number conversion in** [**OpenDocument**](/pages/createpage.action?spaceKey=imagingjava&title=OpenDocument&linkCreation=true&fromPageId=60229174) **support class:** [**OdEnhancedGeometryReader**](/pages/createpage.action?spaceKey=imagingjava&title=OdEnhancedGeometryReader&linkCreation=true&fromPageId=60229174)**.[ReadEnd](/pages/createpage.action?spaceKey=imagingjava&title=ReadEnd&linkCreation=true&fromPageId=60229174). [Java]** 
input file: [modifierTest.odg](https://kiev.dynabic.com/jira/secure/attachment/22852/modifiersTest.odg), this file contained a modifier with float value (decimal separator - ".")
output file: [modifierTest.pdf](https://kiev.dynabic.com/jira/secure/attachment/22853/modifiersTest.pdf)

{{< highlight java >}}

 Locale loc = new Locale( "ru", "RU" ) ;

Locale.setDefault( loc ) ;

String inputFileName = "D:\\Odg\\modifiersTest.odg";

String outputFileName = "D:\\Odg\\modifiersTest.pdf";

ImageOptionsBase options = new PdfOptions();

final OdgImage image = (OdgImage) Image.load(inputFileName);

try

{

options.setVectorRasterizationOptions(new MetafileRasterizationOptions()

{{

setPageWidth(image.getWidth());

setPageHeight(image.getHeight());

}});

image.save(outputFileName, options);

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-862 Image exception on load Tiff image [Java]** 
input file: [posterUfficio_crop.tif](https://kiev.dynabic.com/jira/secure/attachment/22773/22773_posterUfficio_crop.tif)
output file: [posterUfficio_crop.png](https://kiev.dynabic.com/jira/secure/attachment/22796/22796_posterUfficio_crop.png)

{{< highlight java >}}

 String inputFileName = "D:\\posterUfficio_crop.tif";

String outFileName = "D:\\posterUfficio_crop.png";

Image image = Image.load(inputFileName);

try

{

image.save(outFileName, new PngOptions());

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-859 Image saving failed when saving JPEG2000 as PNG [Java]** 
input file: [Input.jp2](https://kiev.dynabic.com/jira/secure/attachment/22889/22889_Input.jp2)

{{< highlight java >}}

 String inputImage = "Input.jp2";

String outputImage = "Ouput.png";

Image image = Image.load(inputImage);

try

{

image.save(outputImage, new PngOptions());

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-858 Exception on converting emf to svg [Java]** 
input file: [powerpoint_emf.zip](https://kiev.dynabic.com/jira/secure/attachment/22851/powerpoint_emf.zip)

{{< highlight java >}}

 String path = "C:\\Temp\\Errors\\";

Image image = Image.load(path + "powerpoint_emf.emf");

try

{

final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

emfRasterizationOptions.setBackgroundColor(Color.getWhite());

emfRasterizationOptions.setPageWidth(image.getWidth());

emfRasterizationOptions.setPageHeight(image.getHeight());

image.save(path + "owerpoint_emf.svg", new SvgOptions()

{{

setVectorRasterizationOptions(emfRasterizationOptions);

}});

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-857 Fix PSD crop operation [Java]** 
input file: [MSFT_DevEva_Web_Twitter-800x320_2-DVG.PSD](https://kiev.dynabic.com/jira/secure/attachment/22872/MSFT_DevEva_Web_Twitter-800x320_2-DVG.PSD)

{{< highlight java >}}

 PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

psdLoadOptions.setLoadEffectsResource(true);

PsdImage image = (PsdImage)Image.load("MSFT_DevEva_Web_Twitter-800x320_2-DVG.PSD", psdLoadOptions);

try

{

Rectangle rect = new Rectangle(10, 30, 100, 100);

image.crop(rect);

image.save("MSFT_DevEva_Web_Twitter-800x320_2-DVG_new_ethalon.png", new PngOptions() {{ setColorType(PngColorType.TruecolorWithAlpha); }});

}

finally

{

image.dispose();

}


{{< /highlight >}}

**IMAGINGJAVA-856 Fix PSD test rendering for specific case [Java]** 
input file: [1.psd](https://kiev.dynabic.com/jira/secure/attachment/22858/1.psd)

{{< highlight java >}}

 PsdImage image = (PsdImage)Image.load("1.psd");

try

{

image.save("1.png", new PngOptions() {{ setColorType(PngColorType.TruecolorWithAlpha); }});

}

finally

{

image.dispose();

}


{{< /highlight >}}

**IMAGINGJAVA-855 Exception on saving Tiff Image [Java]** 
input file: [Carelogic-1-11082017-3016-CH.tif](https://kiev.dynabic.com/jira/secure/attachment/22862/Carelogic-1-11082017-3016-CH.tif)

{{< highlight java >}}

 String sourceFilePath = "Carelogic-1-11082017-3016-CH.tif";

String outputFilePath = "Carelogic-1-11082017-3016-CH Out.tif";

int resolution = 96; // Set the output resolution to some non-zero value!

RasterImage image = (RasterImage)Image.load(sourceFilePath);

try

{

TiffOptions saveOptions = new TiffOptions(TiffExpectedFormat.Default);

saveOptions.setResolutionSettings(new ResolutionSetting(resolution, resolution));

saveOptions.setCompression(TiffCompressions.None);

saveOptions.setBitsPerSample(new int[] { 1 });

int width = image.getWidth() * resolution / (int)image.getHorizontalResolution();

int height = image.getHeight() * resolution / (int)image.getVerticalResolution();

image.resize(width, height); // No more exception here!

image.save(outputFilePath, saveOptions);

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-854 Gif not properly converted to png [Java]** 
input file: [6.gif](https://kiev.dynabic.com/jira/secure/attachment/22867/6.gif)

{{< highlight java >}}

 String file = "6.gif";

Image image = Image.load(file);

try

{

image.save(file + ".png", new PngOptions());

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-834 When PSD is converted to PNG, an** [**ArgumentOutOfRangeException**](/pages/createpage.action?spaceKey=imagingjava&title=ArgumentOutOfRangeException&linkCreation=true&fromPageId=60229174) **occurs** 
Input and output: [2620.zip](https://kiev.dynabic.com/jira/secure/attachment/22869/22869_2620.zip)

{{< highlight java >}}

 PsdImage input = (PsdImage)Image.load("Cloud_AzPlat_Banner3A_SB_EN_US_160x600.psd");

try

{

TextLayer textLayer;

for (Layer layer : input.getLayers())

{

if (layer instanceof TextLayer)

{

textLayer = (TextLayer)layer;

textLayer.updateText("123\u0003abc");

}

}

input.save("Cloud_AzPlat_Banner3A_SB_EN_US_160x600_updated.psd", new PsdOptions() {{ setCompressionMethod(CompressionMethod.RLE); }});

}

finally

{

input.dispose();

}

input = (PsdImage)Image.load("Cloud_AzPlat_Banner3A_SB_EN_US_160x600_updated.psd");

try

{

input.save("Cloud_AzPlat_Banner3A_SB_EN_US_160x600_updated.png", new PngOptions() {{ setColorType(PngColorType.TruecolorWithAlpha); }});

}

finally

{

input.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-783 Darker colors and color reproducibility**

{{< highlight java >}}

 public void test783()

{

License l = new License();

l.setLicense("Aspose.Imaging.Java.lic");

String path = "C:\\Temp\\Errors\\783\\";

// Load Tiff image with embedded Icc

{

String embeddedIccProfileTiff = path + "Cmyk-CmykProfile.tif";

TiffImage image = (TiffImage) Image.load(embeddedIccProfileTiff);

try

{

// get icc by tag

TiffDataType tag = image.getActiveFrame().getFrameOptions().getTagByType(TiffTags.IccProfile);

byte[] profileStream = (byte[]) tag.getValue();

AssertProfile(profileStream);

// icc property

byte[] profileStream2 = image.getActiveFrame().getFrameOptions().getIccProfile();

// Must be the same

Compare(profileStream, profileStream2);

AssertProfile(profileStream2);

}

finally

{

image.dispose();

}

}

// Load Psd image with embedded Icc

{

String embeddedIccProfilePsd = path + "NavyExchangeCmyk.psd";

PsdImage image = (PsdImage) Image.load(embeddedIccProfilePsd);

try

{

com.aspose.imaging.system.io.MemoryStream profileStream = (com.aspose.imaging.system.io.MemoryStream)image.getCmykColorProfile().getStream();

AssertProfile(profileStream.toArray());

}

finally

{

image.dispose();

}

}

// Convert Psd image with embedded Cmyk Icc to Tiff with embedded Cmyk Icc

{

String embeddedIccProfilePsd = path + "NavyExchangeCmyk.psd";

final byte[] sourceIccData;

PsdImage image = (PsdImage) Image.load(embeddedIccProfilePsd);

try

{

TiffOptions options = new TiffOptions(TiffExpectedFormat.TiffLzwRgba);

// add Icc profile tag

sourceIccData = ((com.aspose.imaging.system.io.MemoryStream) image.getCmykColorProfile().getStream()).toArray();

TiffUndefinedType tmp = new TiffUndefinedType(TiffTags.IccProfile);

tmp.setData(sourceIccData);

options.addTag(tmp);

image.save(embeddedIccProfilePsd + "_output.tiff", options);

}

finally

{

image.dispose();

}

// verify

TiffImage image2 = (TiffImage) Image.load(embeddedIccProfilePsd + "_output.tiff");

try

{

byte[] profileStream = image2.getActiveFrame().getFrameOptions().getIccProfile();

AssertProfile(profileStream);

Assert.assertTrue(Compare(profileStream, sourceIccData));

}

finally

{

image2.dispose();

}

}

}

private void AssertProfile(byte[] profileStream)

{

msAssert.isNotNull(profileStream);

msAssert.isFalse(Compare(profileStream, IccProfileHelper.getDefaultCmykProfile()));

msAssert.isFalse(Compare(profileStream, IccProfileHelper.getDefaultRgbProfile()));

}

private boolean Compare(byte[] data1, byte[] data2)

{

if (data1.length != data2.length)

{

return false;

}

for (int i = 0; i < data2.length; i++)

{

if (data1[i] != data2[i])

{

return false;

}

}

return true;

}

static class IccProfileHelper

{

/**

\* <p>

\* The cmyk profile path.

\* </p>

*/

static final String CmykProfilePath = "com/aspose/imaging/internal/System/Drawing/rswop.icm";

/**

\* <p>

\* The rgb profile path.

\* </p>

*/

static final String RgbProfilePath = "com/aspose/imaging/internal/System/Drawing/sRGB_v4_ICC_preference_displayclass.icc";

static byte[] getDefaultCmykProfile()

{

return getResource(CmykProfilePath);

}

static byte[] getDefaultRgbProfile()

{

return getResource(RgbProfilePath);

}

private static byte[] getResource(String resourceName)

{

InputStream stream = com.aspose.imaging.Image.class.getClassLoader().getResourceAsStream(resourceName);

if (stream == null)

throw new RuntimeException("Error loading icc profile resource");

try

{

byte[] buffer = new /*Byte*/ byte[stream.available()];

stream.read(buffer);

return buffer;

}

catch (IOException e)

{

throw new FrameworkException("Error loading icc profile resource", e);

}

}

}

{{< /highlight >}}

**IMAGINGJAVA-618 Converting EMF to PNG in not producing correct outpout**

{{< highlight java >}}

 String file = "image13.emf";

final Image image = Image.load(file);

try

{

final EmfRasterizationOptions vectorRasterizationOptions = new EmfRasterizationOptions()

{{

setPageWidth(image.getWidth());

setPageHeight(image.getHeight());

}};

image.save(file + ".Png", new PngOptions() {{

setVectorRasterizationOptions(vectorRasterizationOptions); }});

}

finally

{

image.dispose();

}

{{< /highlight >}}

**IMAGINGJAVA-510 Emf image export error** 
input file: [Picture1.zip](https://kiev.dynabic.com/jira/secure/attachment/20863/Picture1.zip)

{{< highlight java >}}

 String filePath = "Picture1.emf";

String outPath = "Picture1";

Image mf = Image.load(filePath);

try

{

EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

emfRasterizationOptions.setBackgroundColor(Color.getGray());

emfRasterizationOptions.setPageWidth(mf.getWidth());

emfRasterizationOptions.setPageHeight(mf.getHeight());

PngOptions pngOptions = new PngOptions();

pngOptions.setVectorRasterizationOptions(emfRasterizationOptions);

mf.save(outPath + "_IMAGINGNET-2007.png", pngOptions);

emfRasterizationOptions.setPageWidth(100);

emfRasterizationOptions.setPageHeight(100);

mf.save(outPath + "_IMAGINGNET-2007_small.png", pngOptions);

}

finally

{

mf.dispose();

}

{{< /highlight >}}
