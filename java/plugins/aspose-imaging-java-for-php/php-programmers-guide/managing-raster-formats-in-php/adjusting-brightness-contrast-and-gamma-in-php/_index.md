---
title: Adjusting Brightness, Contrast and Gamma in PHP
type: docs
weight: 10
url: /java/adjusting-brightness-contrast-and-gamma-in-php/
---

## **Aspose.Imaging - Adjusting Brightness**
To Adjust Brightness of an image using **Aspose.Imaging Java for PHP**, call **adjust_brightness** method of **AdjustingColors** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function adjust_brightness($dataDir=null){

\# Load an existing image

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

\# Check if image is cached

if (!$image->isCached()) {

\# Cache image if not already cached

$image->cacheData();

}

\# Adjust the brightness

$image->adjustBrightness(70);

\# Save the image to disk

$image->save($dataDir . "adjust_brightness.jpg");

\# Display Status.

print "Adjust image brightness successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Imaging - Adjusting Contrast**
To Adjust Contrast of an image using **Aspose.Imaging Java for PHP**, call **adjust_contrast** method of **AdjustingColors** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function adjust_contrast($dataDir=null){

\# Load an existing image

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

\# Check if image is cached

if (!$image->isCached()) {

\# Cache image if not already cached

$image->cacheData();

}

\# Adjust the contrast

$image->adjustContrast(10);

\# Save the image to disk

$image->save($dataDir . "adjust_contrast.jpg");

\# Display Status.

print "Adjust image contrast successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Imaging - Adjusting Gamma**
To Adjust Gamma of an image using **Aspose.Imaging Java for PHP**, call **adjust_gamma** method of **AdjustingColors** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function adjust_gamma($dataDir=null){

\# Load an existing image

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

\# Check if image is cached

if (!$image->isCached()) {

\# Cache image if not already cached

$image->cacheData();

}

\# Adjust the gamma

$image->adjustGamma(2.2, 2.2, 2.2);

\# Save the image to disk

$image->save($dataDir."adjust_gamma.jpg");

\# Display Status.

print "Adjust image gamma successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Download Running Code**
Download **Adjusting Brightness, Contrast and Gamma (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingRasterFormats/AdjustingColors.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingRasterFormats/AdjustingColors.php)
