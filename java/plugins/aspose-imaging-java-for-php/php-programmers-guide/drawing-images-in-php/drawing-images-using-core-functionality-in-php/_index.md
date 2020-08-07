---
title: Drawing Images using Core Functionality in PHP
type: docs
weight: 30
url: /java/drawing-images-using-core-functionality-in-php/
---

## **Aspose.Imaging - Drawing Images using Core Functionality**
To Draw Images using Core Functionality using **Aspose.Imaging Java for PHP**, simply invoke **DrawingImagesUsingCoreFunctionality** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create an instance of BmpOptions and set its various properties

$create_options = new BmpOptions();

$create_options->setBitsPerPixel(24);

\# Create an instance of FileCreateSource and assign it to Source property

$fileCreateSource=new FileCreateSource();

$create_options->setSource(new FileCreateSource($dataDir . "sample.bmp",false));

\# Create an instance of RasterImage

$image=new Image();

$raster_image = $image->create($create_options,500,500);

\# Get the pixels of the image by specifying the area as image boundary

$pixels = $raster_image->loadPixels($raster_image->getBounds());

$index = 0;

while ($index < sizeof($pixels)) {

\# Set the indexed pixel color to yellow

$color = new Color();

$pixels[$index] = $color->getYellow();

$index += 1;

}

$raster_image->savePixels($raster_image->getBounds(), $pixels);

\# save all changes

$raster_image->save();

print "Draw Images Using Core Functionality.".PHP_EOL;

}

{{< /highlight >}}
## **Download Running Code**
Download **Drawing Images using Core Functionality (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/DrawingImages/DrawingImagesUsingCoreFunctionality.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/DrawingImages/DrawingImagesUsingCoreFunctionality.php)
