---
title: Aspose.Imaging Java For Jython
type: docs
weight: 30
url: /java/aspose-imaging-java-for-jython/
---

## **Introduction to Aspose.Imaging Java for Jython**
### **What is Jython?**
Jython is a Java implementation of Python that combines expressive power with clarity. Jython is freely available for both commercial and non-commercial use and is distributed with source code. Jython is complementary to Java and is especially suited for the following tasks:

- **Embedded scripting** - Java programmers can add the Jython libraries to their system to allow end users to write simple or complicated scripts that add functionality to the application.
- **Interactive experimentation** - Jython provides an interactive interpreter that can be used to interact with Java packages or with running Java applications. This allows programmers to experiment and debug any Java system using Jython.
- **Rapid application development** - Python programs are typically 2-10X shorter than the equivalent Java program. This translates directly to increased programmer productivity. The seamless interaction between Python and Java allows developers to freely mix the two languages both during development and in shipping products. 
## **Aspose.Imaging for Java**
Aspose.Imaging for Java is an imaging library that lets developers create, edit, draw or convert images in their Java applications with ease and performance. It offers broad spectrum of traditional image processing operations as well as most demanded features that makes it most widely used imaging engine.
## **Aspose.Imaging Java for Jython**
Project Aspose.Imaging Java for Jython shows how different tasks can be performed using Aspose.Imaging Java APIs in Jython. This project is aimed to provide useful examples for Jython developers who want to utilize Aspose.Imaging for Java in their Jython Projects using Jython Java Bridge.
## **System Requirements and Supported Platforms**
### **System Requirements**
**Following are the system requirements to use Aspose.Imaging Java for Jython:**

- Java 1.5 or above installed
- Downloaded Aspose.Imaging component
- Jython 2.7.0
### **Supported Platforms**
**Following are the supported platforms:**

- Aspose.Imaging 15.4 and above.
- Java IDE (Eclipse, NetBeans ...)
## **Download Installation and Usage**
### **Downloading**
**Download Examples from social coding websites**

Following releases of running examples are available to download on all of the below mentioned social coding sites:

- [CodePlex](https://asposeimagingjavajython.codeplex.com/releases/view/619260)
- [Github](https://github.com/aspose-imaging/Aspose.imaging-for-Java/releases/tag/Aspose.imaging_Java_for_Jython-v1.0.0)

**Download Aspose.Imaging for Java component**

- [Aspose.Imaging for Java](http://www.aspose.com/community/files/72/java-components/aspose.imaging-for-java/default.aspx)
### **Installing**
- Place downloaded Aspose.Imaging for Java jar file into "lib" directory.
- Replace "your-lib" with the downloaded jar filename in _*init*_.py file.
### **Using**
You can Draw ARC using following example code:

{{< highlight java >}}

 from asposeimaging import Settings

from com.aspose.imaging.fileformats.metafile import EmfMetafileImage

from com.aspose.imaging.imageoptions import BmpOptions

from com.aspose.imaging.sources import StreamSource

from com.aspose.imaging import Image

from com.aspose.imaging import Color

from com.aspose.imaging import Pen

from com.aspose.imaging import Graphics

from java.io import ByteArrayInputStream

from jarray import array

class DrawingArc:

    def __init__(self):



        dataDir = Settings.dataDir + 'DrawingImages/DrawingArc/'



        # Create an instance of BmpOptions and set its various properties

        create_options = BmpOptions()

        create_options.setBitsPerPixel(32)

        # Define the source property for the instance of BmpOptions

        ary = []

        create_options.setSource(StreamSource(ByteArrayInputStream(ary)))

        # Create an instance of Image

        image = Image

        image = image.create(create_options,100,100)

        # Create an instance of Color

        color = Color()

        # Create an instance of Pen

        pen = Pen

        # Create and initialize an instance of Graphics class

        graphic = Graphics(image)

        # Clear the image surface with Yellow color

        graphic.clear(color.getYellow())

        # Draw arc to screen.

        graphic.drawArc(Pen(color.getBlack()), 0, 0, 100, 200, 45, 270)

        # Save all changes.

        image.save(dataDir + "DrawArcExample.bmp")

        print "Arc have been drawn in image successfully!"

if __name__ == '__main__':        

    DrawingArc()

{{< /highlight >}}
## **Support, Extend and Contribute**
### **Support**
From the very first days of Aspose, we knew that just giving our customers good products would not be enough. We also needed to deliver good service. We are developers ourselves and understand how frustrating it is when a technical issue or a quirk in the software stops you from doing what you need to do. We're here to solve problems, not create them.

This is why we offer free support. Anyone who uses our product, whether they have bought them or are using an evaluation, deserves our full attention and respect.

You can log any issues or suggestions related to Aspose.Imaging Java for Jython using any of the following platforms:

- [CodePlex](https://asposeimagingjavajython.codeplex.com/workitem/list/basic)
- [Github](https://github.com/aspose-imaging/Aspose.Imaging-for-Java/issues)
### **Extend and Contribute**
Aspose.Imaging Java for Jython is open source and its source code is available on the major social coding websites listed below. Developers are encouraged to download the source code and contribute by suggesting or adding new feature or improving the existing ones, so that others could also benefit from it.
### **Source Code**
You can get the latest source code from one of the following locations

- [CodePlex](https://asposeimagingjavajython.codeplex.com/SourceControl/latest)
- [Github](https://github.com/aspose-imaging/Aspose.Imaging-for-Java)
