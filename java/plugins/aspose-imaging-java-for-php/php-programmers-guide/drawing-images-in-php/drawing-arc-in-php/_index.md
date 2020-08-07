---
title: Drawing Arc in PHP
type: docs
weight: 10
url: /java/drawing-arc-in-php/
---

## **Aspose.Imaging - Drawing Arc**
To Draw Arc shape using **Aspose.Imaging Java for PHP**, simply invoke **DrawingArc** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create an instance of BmpOptions and set its various properties

$create_options = new BmpOptions();

$create_options->setBitsPerPixel(32);

\# Define the source property for the instance of BmpOptions

$ary=array();

$create_options->setSource(new StreamSource(new ByteArrayInputStream($ary)));

\# Create an instance of Image

$image=new Image();

$image = $image->create($create_options,100,100);

\# Create an instance of Color

$color = new Color();

\# Create an instance of Pen

$pen = new Pen();

\# Create and initialize an instance of Graphics class

$graphic = new Graphics($image);

\# Clear the image surface with Yellow color

$graphic->clear($color->getYellow());

\# Draw arc to screen.

$graphic->drawArc(new Pen($color->getBlack()), 0, 0, 100, 200, 45, 270);

\# Save all changes.

$image->save($dataDir . "DrawArcExample.bmp");

print "Arc have been drawn in image successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Drawing Arc (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/DrawingImages/DrawingArc.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/DrawingImages/DrawingArc.php)
