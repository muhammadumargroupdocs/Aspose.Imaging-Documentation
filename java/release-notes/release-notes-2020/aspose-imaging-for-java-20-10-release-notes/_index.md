---
type: docs
weight: '60'
url: /java/aspose-imaging-for-java-20-10-release-notes/
title: Aspose.Imaging for JAVA 20.10 - Release notes
---
| **Key**         | **Summary**                                                                                                                                                              | **Category** |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| IMAGINGJAVA-1880 | Improve export of multi-page vector formats to multi-page raster formats                                                                                                                                  | Feature      |
| IMAGINGJAVA-1872 | Support of resize operation for Interlaced GIF images                                                                                                                                  | Feature      |
| IMAGINGJAVA-1881 | IndexOutOfRangeExceptions when exporting JPEG YCbCr to PNG Grayscale                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1879 | Gif to Png export adds transparent areas when not needed                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1878 | Aspose.Imaging 20.7: Saving each frame from particular tiff file to png produces incorrect images                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1867 | Raster images exports to Html5 Canvas with the wrong scale                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1866 | Exception : Array dimensions exceeded supported range on working with CDR file                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1865 | Aspose.Imaging 20.8: Saving particular ODG file to PNG raises exception                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1864 | File is corrupted or damaged exception was thrown when rendering TIFF document                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1863 | Watermark is incorrect when GIF image loaded and saved                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1862 | Incorrect output when exporting EMF to PNG                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1861 | Support of convertion for 16 bpp RGBA 5551 BMP to 32 bpp RGBA PNG                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1858 | Index was outside the bounds of the array exception when saving EMF                                                                                                                                  | Enhancement      |
| IMAGINGJAVA-1339 | Aspose.Imaging Emf save MSPaint compatibility                                                                                                                                  | Enhancement      |

**Public API changes:**
-----------------------

**Added APIs:**

Please see corresponding cumulative [API changes for Aspose.Imaging for .NET 20.10](https://docs.aspose.com/imaging/net/aspose-imaging-for-net-20-10-release-notes/) version

**Removed APIs:**

Please see corresponding cumulative [API changes for Aspose.Imaging for .NET 20.10](https://docs.aspose.com/imaging/net/aspose-imaging-for-net-20-10-release-notes/) version

**Usage Examples:**
-----------------------

**IMAGINGJAVA-1881 IndexOutOfRangeExceptions when exporting JPEG YCbCr to PNG Grayscale**

```
### Export of the YCbCr JPEG image as a Grayscale PNG.


try (Image image = Image.load("source.jpg"))
{
    image.save("output.png", new PngOptions() {{ setColorType(PngColorType.Grayscale); }});
}
```

**IMAGINGJAVA-1880 Improve export of multi-page vector formats to multi-page raster formats**

```
### Export CMX image with pages of different sizes to TIFF format
Aspose.Imaging allows you to specify rasterization options for each page during the export. The following source code sample demonstrates how to export multi-page CMX image to TIFF format:

try (VectorMultipageImage image = (VectorMultipageImage)Image.load("MultiPage2.cmx"))
{
	// Create page rasterization options
	VectorRasterizationOptions[] pageOptions = createPageOptions(image);

	// Create TIFF options
	TiffOptions options = new TiffOptions(TiffExpectedFormat.TiffDeflateRgb);
	MultiPageOptions multiPageOptions = new MultiPageOptions();
	multiPageOptions.setPageRasterizationOptions(pageOptions);
	options.setMultiPageOptions(multiPageOptions);

	// Export image to TIFF format
	image.save("MultiPage2.cmx.tiff", options);
}

private static <TOptions extends VectorRasterizationOptions> VectorRasterizationOptions[] createPageOptions(Class<TOptions> type, VectorMultipageImage image)
            throws InstantiationException, IllegalAccessException
{
	// Create page rasterization options for each page in the image
	List<VectorRasterizationOptions> ret = new LinkedList<VectorRasterizationOptions>();
	for (Image page : image.getPages())
	{
		ret.add(createPageOptions(type, page.getSize()));
	}
	return ret.toArray(new VectorRasterizationOptions[0]);
}

private static <TOptions extends VectorRasterizationOptions> VectorRasterizationOptions createPageOptions(Class<TOptions> type, Size pageSize)
		throws IllegalAccessException, InstantiationException
{
	// Create the instance of rasterization options
	TOptions options = type.newInstance();

	// Set the page size
	options.setPageSize(Size.to_SizeF(pageSize));
	return options;
}

### Export CDR image to PDF format
The following source code sample shows you how to export CDR image to PDF format:

try (VectorMultipageImage image = (VectorMultipageImage)Image.load("MultiPage2.cdr"))
{
	// Create page rasterization options
	VectorRasterizationOptions[] pageOptions = createPageOptions(CdrRasterizationOptions.class, image);

	// Create PDF options
	PdfOptions options = new PdfOptions();
	MultiPageOptions multiPageOptions = new MultiPageOptions();
	multiPageOptions.setPageRasterizationOptions(pageOptions);
	options.setMultiPageOptions(multiPageOptions);

	// Export image to PDF format
	image.save("MultiPage2.cdr.pdf", options);
}
```

**IMAGINGJAVA-1879 Gif to Png export adds transparent areas when not needed**

```
try (GifImage image = (GifImage)Image.load("2086.gif"))
{
	PngOptions pngOptions = new PngOptions();
	pngOptions.setFullFrame(true);
	pngOptions.setColorType(PngColorType.Truecolor);
	image.getPages()[1].save("Frame.png", pngOptions);
}
```

**IMAGINGJAVA-1878 Aspose.Imaging 20.7: Saving each frame from particular tiff file to png produces incorrect images**

```
try (TiffImage tiff = (TiffImage)Image.load("Camping.tiff"))
{
	int i = 0;
	for (TiffFrame frame : tiff.getFrames())
	{
		frame.save(String.format("converted-%d.png", ++i), new PngOptions());
	}
}
```

**IMAGINGJAVA-1872 Support of resize operation for Interlaced GIF images**

```
try (Image image = Image.load("cat_interlaced.gif"))
{
    // Perform resize operation
    image.resizeHeightProportionally(400, ResizeType.HighQualityResample);

    // Export image to any raster format
    image.save("cat_resized.png", new PngOptions());
}
```

**IMAGINGJAVA-1867 Raster images exports to Html5 Canvas with the wrong scale**

```
for (String fileName : new String[]{ "Progressive.png", "cat.jpg" })
{
	try (Image image = Image.load(fileName))
	{
		image.save(fileName + ".html", new Html5CanvasOptions());
	}
}
```

**IMAGINGJAVA-1866 Exception : Array dimensions exceeded supported range on working with CDR file**

```
String[] files = new String[] {"audi_icons_13.2.cdr", "laundry card curved.cdr", "Revised Creamy Cake Company 7x7x5inch.cdr", "royal.cdr"};
String baseFolder = "D:\\";
for (String fileName : files)
{
   String inputFilePath = baseFolder + fileName;
   String outputFilePath = inputFilePath + ".pdf";
   try (CdrImage image = (CdrImage) Image.load(inputFilePath))
   {
      image.save(outputFilePath, new PdfOptions());
   }
}
```

**IMAGINGJAVA-1865 Aspose.Imaging 20.8: Saving particular ODG file to PNG raises exception**

```
String baseFolder = "D:\\";
String inputFile = "abrak_2.odg";
String inputFileName = baseFolder + inputFile;
String outputFileName = inputFileName + ".png";
try (Image image = Image.load(inputFileName))
{
    image.save(outputFileName, new PngOptions());
}
```

**IMAGINGJAVA-1864 File is corrupted or damaged exception was thrown when rendering TIFF document**

```
try (Image image = Image.load("marveshja1.tiff"))
{
    image.save("marveshja1.png", new PngOptions());
}
```

**IMAGINGJAVA-1863 Watermark is incorrect when GIF image loaded and saved**

```
try (Image image = Image.load("2086.gif"))
{
    image.save("Result.gif");
}
```

**IMAGINGJAVA-1862 Incorrect output when exporting EMF to PNG**

```
String file = "MultiPage.cdr.emf";
String baseFolder = "D:\\";
String inputFileName = baseFolder + file;
String outputFileName = baseFolder + file + ".png";
try (Image image = Image.load(inputFileName))
{
	PngOptions saveOptions = new PngOptions();
	saveOptions.setVectorRasterizationOptions(new EmfRasterizationOptions());
	saveOptions.getVectorRasterizationOptions().setPageSize(Size.to_SizeF(image.getSize()));
	image.save(outputFileName, saveOptions);
}
```

**IMAGINGJAVA-1861 Support of convertion for 16 bpp RGBA 5551 BMP to 32 bpp RGBA PNG**

```
### Exporting RGB 16 Bpp BMP with 5,5,5,1 channels to RGBA 32 Bpp PNG


try (Image image = Image.load("tiger2.bmp"))
{
	PngOptions pngOptions = new PngOptions();
	pngOptions.setColorType(com.aspose.imaging.fileformats.png.PngColorType.TruecolorWithAlpha);
	image.save("tiger2.bmp.png", pngOptions);
}
```

**IMAGINGJAVA-1858 Index was outside the bounds of the array exception when saving EMF**

```
String baseFolder = "D:\\";
String file = "sample.emf";
String inputFileName = baseFolder + file;
String outputFileName = inputFileName + ".png";
try (Image image = Image.load(inputFileName))
{
   image.save(outputFileName, new PngOptions());
}
```

**IMAGINGJAVA-1339 Aspose.Imaging Emf save MSPaint compatibility**

```
Image image = Image.load("1.emf");
try
{
	image.save("out.emf");
}
finally
{
	image.close();
}
```
