---
title: Cropping Images in PHP
type: docs
weight: 30
url: /java/cropping-images-in-php/
---

## **Aspose.Imaging - Cropping by Shifts**
To Crop image by Shifts using **Aspose.Imaging Java for PHP**, call **crop_by_shifts** method of **CropImages** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function crop_by_shifts($dataDir=null){

\# Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir."test.jpg");

\# Before cropping, the image should be cached for better performance

if (!$image->isCached()) {

$image->cacheData();

}

\# Define shift values for all four sides

$left_shift = 10;

$right_shift = 10;

$top_shift = 10;

$bottom_shift = 10;

\# Based on the shift values, apply the cropping on image

\# Crop method will shift the image bounds toward the center of image

$image->crop($left_shift, $right_shift, $top_shift, $bottom_shift);

\# Save the image to disk

$image->save($dataDir . "CropByShifts.jpg");

\# Display Status.

print "Cropped image by shifts successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Imaging - Cropping by Rectangle**
To Crop image by Rectangle using **Aspose.Imaging Java for PHP**, call **crop_by_rectangle** method of **CropImages** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function crop_by_rectangle($dataDir=null){

\# Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

\# Before cropping, the image should be cached for better performance

if (!$image->isCached()) {

$image->cacheData();

}

\# Create an instance of Rectangle class with desired size

$rectangle = new Rectangle(10, 10, 100, 100);

\# Perform the crop operation on object of Rectangle class

$image->crop($rectangle);

\# Save the image to disk

$image->save($dataDir . "crop_by_rectangle.jpg");

\# Display Status.

print "Cropped image by rectangle successfully!".PHP_EOL;

}

{{< /highlight >}}
## **Download Running Code**
Download **Cropping Images (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingRasterFormats/CropImages.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingRasterFormats/CropImages.php)
