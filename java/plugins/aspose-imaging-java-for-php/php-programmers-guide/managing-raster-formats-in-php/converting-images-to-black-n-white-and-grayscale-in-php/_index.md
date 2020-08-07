---
title: Converting Images to Black n White and Grayscale in PHP
type: docs
weight: 20
url: /java/converting-images-to-black-n-white-and-grayscale-in-php/
---

## **Aspose.Imaging - Binarization with Fixed Threshold**
Following code snippet demonstrates how Fixed Threshold Binarization can be applied to an image using **Aspose.Imaging Java for PHP**, call **binarization_with_fixed_threshold** method of **ConvertingRasterImages** module.

**PHP Code**

{{< highlight php >}}

 public static function binarization_with_fixed_threshold($dataDir=null){

$image=new Image();

$image = $image->load($dataDir."test.jpg");


\# Check if image is cached

if (!$image->isCached()) {

\# Cache image if not already cached

$image->cacheData();

}

\# Binarize image with predefined fixed threshold

$image->binarizeFixed(100);

\# Save the image to disk

$image->save($dataDir . "binarization_with_fixed_threshold.jpg");

\# Display Status.

print "Binarization image with Fixed Threshold successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Imaging - Binarization with Otsu Threshold**
Following code snippet demonstrates how Otsu Threshold Binarization can be applied to an image using **Aspose.Imaging Java for PHP**, call **binarization_with_otsu_threshold** method of **ConvertingRasterImages** module.

**PHP Code**

{{< highlight php >}}

 public static function binarization_with_otsu_threshold($dataDir=null)

{

\# Load an existing image

$image = new Image();

$image = $image->load($dataDir."test.jpg");

\# Check if image is cached

if (!$image->isCached()) {

\# Cache image if not already cached

$image->cacheData();

}

\# Binarize image with Otsu Thresholding

$image->binarizeOtsu();

\# Save the image to disk

$image->save($dataDir."binarization_with_otsu_threshold.jpg");

\# Display Status.

print "Binarization image with Otsu Threshold successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Imaging - Transform image to its grayscale representation**
Following code snippet demonstrates how to apply grayscale to an image using **Aspose.Imaging Java for PHP**, call **transform_image_to_grayscale** method of **ConvertingRasterImages** module.

**PHP Code**

{{< highlight php >}}

 public static function transform_image_to_grayscale($dataDir=null){

\# Load an existing image

$image=new Image();

$image = $image->load($dataDir."test.jpg");

\# Check if image is cached

if (!$image->isCached()) {

\# Cache image if not already cached

$image->cacheData();

}

\# Transform image to its grayscale representation

$image->grayscale();

\# Save the image to disk

$image->save($dataDir."transform_image_to_grayscale.jpg");

\# Display Status.

print "Transform image to its grayscale representation successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Download Running Code**
Download **Converting Images to Black n White and Grayscale (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingRasterFormats/ConvertingRasterImages.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingRasterFormats/ConvertingRasterImages.php)
