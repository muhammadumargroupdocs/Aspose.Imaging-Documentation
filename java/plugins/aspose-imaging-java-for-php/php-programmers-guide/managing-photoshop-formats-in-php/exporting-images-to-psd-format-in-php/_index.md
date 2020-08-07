---
title: Exporting Images to PSD Format in PHP
type: docs
weight: 20
url: /java/exporting-images-to-psd-format-in-php/
---

## **Aspose.Imaging - Exporting Images to PSD Format**
To Export Images to PSD Format using **Aspose.Imaging Java for PHP**, simply invoke **ExportImageToPSD** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir."aspose.bmp");

\# Create an instance of PsdSaveOptions class

$save_options = new PsdOptions();

\# Set the CompressionMethod as Raw

\# Note: Other supported CompressionMethod is CompressionMethod.Rle [No Compression]

$compressionMethod=new CompressionMethod();

$save_options->setCompressionMethod($compressionMethod->Raw);

\# Set the ColorMode to GrayScale//Note: Other supported ColorModes are ColorModes.Bitmap and ColorModes.RGB

$colorModes=new ColorModes();

$save_options->setColorMode($colorModes->RGB);

\# Save the image to disk location with supplied PsdOptions settings

$image->save($dataDir."output.psd", $save_options);

\# Display Status.

print "Image exported to PSD successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Exporting Images to PSD Format (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingPhotoshopFormats/ExportImageToPSD.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingPhotoshopFormats/ExportImageToPSD.php)
