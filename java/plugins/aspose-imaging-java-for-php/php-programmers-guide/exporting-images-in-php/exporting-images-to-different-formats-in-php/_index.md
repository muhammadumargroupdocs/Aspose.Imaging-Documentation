---
title: Exporting Images to Different Formats in PHP
type: docs
weight: 10
url: /java/exporting-images-to-different-formats-in-php/
---

## **Aspose.Imaging - Exporting Images to Different Formats**
To Export Images to Different Formats using **Aspose.Imaging Java for PHP**, simply invoke **ExportImageToDifferentFormats** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type Gif) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir . "sample.gif");

\# Export to BMP file format using the default options

$bmpOptions=new BmpOptions();

$image->save($dataDir . "output.bmp",new BmpOptions());

\# Export to JPEG file format using the default options

$image->save($dataDir . "output.jpg", new JpegOptions());

\# Export to PNG file format using the default options

$image->save($dataDir . "output.png", new PngOptions());

\# Export to TIFF file format using the default options

$tiffExpectedFormat=new TiffExpectedFormat();

$image->save($dataDir . "output.tiff", new TiffOptions($tiffExpectedFormat->Default));

print "Saved images.".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Exporting Images to Different Formats (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ExportImage/ExportImageToDifferentFormats.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ExportImage/ExportImageToDifferentFormats.php)
