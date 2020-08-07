---
title: Drawing Images using Graphics in PHP
type: docs
weight: 40
url: /java/drawing-images-using-graphics-in-php/
---

## **Aspose.Imaging - Drawing Images using Graphics**
To Draw Images using Graphics using **Aspose.Imaging Java for PHP**, simply invoke **DrawingImagesUsingGraphics** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create an instance of BmpOptions and set its various properties

$create_options = new BmpOptions();

$create_options->setBitsPerPixel(24);

\# Create an instance of FileCreateSource and assign it to Source property

$create_options->setSource(new FileCreateSource($dataDir . "DrawingImageUsingGraphics.bmp",false));

\# Create an instance of Image

$image=new Image();

$image = $image->create($create_options,500,500);

\# Create and initialize an instance of Graphics

$graphics = new Graphics($image);

\# Clear the image surface with white color

$color=new Color();

$graphics->clear($color->getWhite());

\# Create and initialize a Pen object with blue color

$pen = new Pen($color->getBlue());

\# Draw Ellipse by defining the bounding rectangle of width 150 and height 100

$graphics->drawEllipse($pen, new Rectangle(10, 10, 150, 100));

\# save all changes

$image->save();

print "Created image using graphics.".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Drawing Images using Graphics (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/DrawingImages/DrawingImagesUsingGraphics.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/DrawingImages/DrawingImagesUsingGraphics.php)
