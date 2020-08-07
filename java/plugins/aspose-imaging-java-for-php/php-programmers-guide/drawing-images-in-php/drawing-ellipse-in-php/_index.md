---
title: Drawing Ellipse in PHP
type: docs
weight: 20
url: /java/drawing-ellipse-in-php/
---

## **Aspose.Imaging - Drawing Ellipse**
To Draw Ellipse shape using **Aspose.Imaging Java for PHP**, simply invoke **DrawingEllipse** module. Here you can see example code.

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

$solid_brush = new SolidBrush();

$rectangle = new Rectangle();

\# Draw a dotted ellipse shape by specifying the Pen object having red color and a surrounding Rectangle

$graphic->drawEllipse(new Pen($color->getRed()), new Rectangle(30, 10, 40, 80));

\# Draw a continuous ellipse shape by specifying the Pen object having solid brush with blue color and a surrounding Rectangle

$graphic->drawEllipse(new Pen(new SolidBrush($color->getBlue())), new Rectangle(10, 30, 80, 40));

\# Save all changes.

$image->save($dataDir . "DrawEllipseExample.bmp");

print "Ellipse have been drawn in image successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Drawing Ellipse (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/DrawingImages/DrawingEllipse.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/DrawingImages/DrawingEllipse.php)
