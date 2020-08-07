---
title: Resizing Images in PHP
type: docs
weight: 50
url: /java/resizing-images-in-php/
---

## **Aspose.Imaging - Simple Resizing**
To do Simple image Resizing presentation using **Aspose.Imaging Java for PHP**, call **simple_image_resizing** method of **ResizeImage** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function simple_image_resizing($dataDir=null){

\# Load an existing image

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

\# Cache data if not cached previously

if (!$image->isCached()) {

$image->cacheData();

}

\# Specify only width

$new_width = $image->getWidth()/2;

$image->resizeWidthProportionally($new_width);

\# Specify only height

$new_height = $image->getHeight()/2;

$image->resizeHeightProportionally($new_height);

\# Save the image to disk

$image->save($dataDir . "simple_image_resizing.jpg");

\# Display Status.

print "Resized image successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Imaging - Resizing with ResizeType Enumeration**
To do Resizing with ResizeType Enumeration presentation using **Aspose.Imaging Java for PHP**, call **resizing_with_resizetype_enumeration** method of **ResizeImage** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function resizing_with_resizetype_enumeration($dataDir=null){

\# Load an existing image

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

\# Cache data if not cached previously

if (!$image->isCached()) {

$image->cacheData();

}

\# Specify only width

$new_width = $image->getWidth()/2;

$resizeType=new ResizeType();

$image->resizeWidthProportionally($new_width, $resizeType->LanczosResample);

\# Specify only height

$new_height = $image->getHeight()/2;

$image->resizeHeightProportionally($new_height, $resizeType->NearestNeighbourResample);

\# Save the image to disk

$image->save($dataDir . "resizing_with_resizetype_enumeration.jpg");

\# Display Status.

print "Resized image successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Download Running Code**
Download **Resizing Images (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingRasterFormats/ResizeImage.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingRasterFormats/ResizeImage.php)
