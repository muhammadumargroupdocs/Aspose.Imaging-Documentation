---
title: Dithering for Raster Images in PHP
type: docs
weight: 40
url: /java/dithering-for-raster-images-in-php/
---

## **Aspose.Imaging - Dithering for Raster Images**
To do Dithering for Raster Images using **Aspose.Imaging Java for PHP**, simply invoke **DitheringImage** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

\# Perform Floyd Steinberg dithering on the current image

$ditheringMethod=new DitheringMethod();

$image->dither($ditheringMethod->ThresholdDithering, 4);

\# Save the image to disk

$image->save($dataDir . "DitheringImage.jpg");

\# Display Status.

print "Dithering image successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Dithering for Raster Images (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingRasterFormats/DitheringImage.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingRasterFormats/DitheringImage.php)
