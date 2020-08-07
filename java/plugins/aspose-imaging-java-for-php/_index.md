---
title: Aspose.Imaging Java For PHP
type: docs
weight: 40
url: /java/aspose-imaging-java-for-php/
---

# **Introduction to Aspose.Imaging Java for PHP**
## **PHP / Java Bridge**
The PHP/Java Bridge is an implementation of a streaming, XML-based [network protocol](http://php-java-bridge.sourceforge.net/pjb/PROTOCOL.TXT), which can be used to connect a native script engine, for example PHP, Scheme or Python, with a Java virtual machine. It is up to 50 times faster than local RPC via SOAP, requires less resources on the web-server side. It is [faster](http://php-java-bridge.sourceforge.net/pjb/FAQ.html#performance) and more reliable than direct communication via the Java Native Interface, and it requires no additional components to invoke Java procedures from PHP or PHP procedures from Java.

Read more at [sourceforge.net](http://php-java-bridge.sourceforge.net/pjb/)
## **Aspose.Imaging for Java**
Aspose.Imaging for Java is an imaging library that lets developers create, edit, draw or convert images in their Java applications with ease and performance. It offers broad spectrum of traditional image processing operations as well as most demanded features that makes it most widely used imaging engine.
## **Aspose.Imaging Java for PHP**
Project Aspose.Imaging Java for PHP shows how different tasks can be performed using Aspose.Imaging Java APIs in PHP. This project is aimed to provide useful examples for PHP developers who want to utilize Aspose.Imaging for Java in their PHP Projects using PHP Java Bridge.
# **System Requirements and Supported Platforms**
## **System Requirements**
**Following are the system requirements to use Aspose.OCR Java for PHP:**

- Tomcat Server 8.0 or above installed.
- PHP/JavaBridge is configured.
- FastCGI is installed.
- Downloaded Aspose.OCR component.
## **Supported Platforms**
**Following are the supported platforms:**

- PHP 5.3 or above
- Java 1.8 or above
# **Downloads & Configure**
## **Download Required Libraries**
Download required libraries mentioned below. These are the required for executing Aspose.Imaging Java for PHP examples.

- [Aspose.Imaging for Java Component](http://www.aspose.com/community/files/72/java-components/aspose.imaging-for-java/default.aspx)
## **Download Examples from Social Coding Sites**
Following releases of running examples are available to download on below mentioned social coding sites:

**GitHub**

- [Aspose.Imaging Java for PHP](https://github.com/aspose-imaging/Aspose.Imaging-for-Java/tree/master/Plugins/Aspose_Imaging_Java_for_PHP)
  **CodePlex**
- [Aspose.Imaging Java for PHP](https://asposeimagingjavaphp.codeplex.com/)
# **Installation And Usage**
## **Installing**
It is very simple and easy to install Aspose.Imaging Java for PHP, please follow these simple steps:

1. Run following command. 

{{< highlight java >}}

 $ gem install asposeimagingjava

{{< /highlight >}}

1. Download required Aspose.Imaging for Java Component from following link.
   <http://www.aspose.com/community/files/72/java-components/aspose.imaging-for-java/default.aspx>
1. Create "jars" folder at root of the Aspose.Imaging Java for PHP and copy downloaded component into it.
## **Using**
Include the required files to export image to different formats.

{{< highlight java >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposeimagingjava'

include Asposeimagingjava

include Asposeimagingjava::ExportImageToDifferentFormats

initialize_aspose_imaging

{{< /highlight >}}

Let's understand the above code.

1. The first line makes sure that the Aspose.Imaging is loaded and available.
1. Include the files that are required to access the Aspose.Imaging
1. Initialize the libraries. The aspose JAVA classes are loaded from the path provided in the aspose.yml file
