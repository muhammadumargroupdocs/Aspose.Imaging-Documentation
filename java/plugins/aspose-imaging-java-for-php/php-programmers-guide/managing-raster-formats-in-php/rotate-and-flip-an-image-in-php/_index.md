---
title: Rotate and Flip an Image in PHP
type: docs
weight: 60
url: /java/rotate-and-flip-an-image-in-php/
---

## **Aspose.Imaging - Rotate and Flip an Image**
To Rotate and Flip an Image using **Aspose.Imaging Java for PHP**, simply invoke **RotateAndFlipImage** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir . "test.jpg");

$rotateFlipType=new RotateFlipType();

$image->rotateFlip($rotateFlipType->Rotate270FlipNone);

\# Save the image to disk

$image->save($dataDir . "RotateFlip.jpg");

\# Display Status.

print "RotateFlip image successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Rotate and Flip an Image (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingRasterFormats/RotateAndFlipImage.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingRasterFormats/RotateAndFlipImage.php)
