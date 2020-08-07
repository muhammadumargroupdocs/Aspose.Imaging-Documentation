---
title: Converting Metafiles to Other Image Formats in PHP
type: docs
weight: 10
url: /java/converting-metafiles-to-other-image-formats-in-php/
---

## **Aspose.Imaging - Converting Metafiles to Other Image Formats**
To Convert Metafiles to Other Image Formats using **Aspose.Imaging Java for PHP**, simply invoke **ConvertMetafileToOtherFormats** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load a Metafile in an instance of EmfMetafileImage class

$metafile = new EmfMetafileImage($dataDir . "sample1.emf");

\# Save EMF to BMP using BmpOptions object

$metafile->save($dataDir . "EmfToBmp.bmp", new BmpOptions());

\# Save EMF to JPG using JpegOptions object

$metafile->save($dataDir . "EmfToJpg.jpg", new JpegOptions());

\# Save EMF to PNG using PngOptions object

$metafile->save($dataDir . "EmfToPng.png", new PngOptions());

\# Save EMF to GIF using GifOptions object

$metafile->save($dataDir . "EmfToGif.gif", new GifOptions());

\# Save EMF to TIFF using TiffOptions object with default settings

$tiffExpectedFormat=new TiffExpectedFormat();

$metafile->save($dataDir . "EmfToTiff.tiff", new TiffOptions($tiffExpectedFormat->Default));

\# Display Status.

print "Converted EMF to BMP, JPEG, PNG, GIF and TIFF formats successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Converting Metafiles to Other Image Formats (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ConvertingMetafilestoOtherImageFormats/ConvertMetafileToOtherFormats.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ConvertingMetafilestoOtherImageFormats/ConvertMetafileToOtherFormats.php)
