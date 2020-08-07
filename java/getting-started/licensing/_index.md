---
title: Licensing
type: docs
weight: 60
url: /java/licensing/
---

## **Evaluation Version Limitations**
You can download an evaluation version of Aspose.Imaging for Java from the [download page](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-imaging/). The evaluation version provides the same features as the fully licensed version of the component with a couple of restrictions. When you buy Aspose.Imaging, simply applying the license removes any restrictions from the installed evaluation.

The evaluation version of Aspose.Imaging for Java provides full product functionality, with only two limitations:

- **A watermark on each image**: Any image you save, modify or export has a watermark reading "Evaluation Only. Created with Aspose.Imaging. Copyright 2010-2019 Aspose Pty Ltd.". Small images, where the full watermark won't fit, has two diagonal lines across the image instead.
- **No support for core drawing functionality**: In evaluation mode, image pixels cannot be loaded or saved to the image. To draw images, use the advanced drawing functionality instead. This limitation affects functionality that depends on the core drawing functionality. Aspose.Imaging for Java allows you to register your own file format. However, this feature depends on the core drawing functionality so it makes no sense to use it in evaluation mode because you can't change the content of those files.

{{% alert color="primary" %}} 

If you want to test Aspose.Imaging for Java without the evaluation limitations, request a 30-day temporary license. Please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) for more information.

{{% /alert %}} 
## **About the License File**
Once you are happy with your evaluation of Aspose.Imaging, you can purchase a license on [Aspose website](https://purchase.aspose.com/default.aspx). Make yourself familiar with the different subscription types offered. If you have any questions, do not hesitate to contact [Aspose's sales team](https://company.aspose.com/contact). Every Aspose license comes with a one-year subscription for software upgrades. After the first year, renew your subscriptions to continue getting the latest features and fixes. Technical support is free and unlimited and is provided to both licensed and evaluation users through our [Support Forums](https://forum.aspose.com/). The license is an XML file that contains details such as the product name, number of licensed developers, subscription expiry date and so on. The file is digitally signed, so do not modify it: even inadvertently adding an extra line break invalidates the file. After buying Aspose.Imaging, you need to apply the license before you create, edit or otherwise manipulate images. If you forget to apply the license, any output images will have an evaluation watermark. You only need to set the license once per application or process that you develop.
## **Where to Apply a License in your Application**
Where you apply a license depends on the type of application you are developing. Follow these simple rules:

- Only apply the license once per application. Calling License.setLicense multiple times is not harmful but wastes processor time.
- Apply the license before calling any Aspose.Imaging for Java classes.
- **Java JavaFX/Swing/Console applications**: call License.setLicense in the startup code, before using any Aspose.Imaging for Java classes.
- **Class library**: call License.setLicense from a static constructor of the class that uses Aspose.Imaging. The static constructor executes before an instance of your class is created, making sure that the Aspose.Imaging license is properly set.
## **Applying the License**
You can easily download an evaluation version of Aspose.Imaging from [its download page](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-imaging/) or using [maven repository](https://repository.aspose.com/repo/). The evaluation version provides absolutely the same capabilities as the licensed version of Aspose.Imaging. Furthermore, evaluation version simply becomes licensed when you purchase a license and add a couple of lines of code to apply the license.
### **Using a File or a Stream**
If you want to avoid working with evaluation limitations, you need to set a license before using Aspose.Imaging. You only need to set a license once per application (or process).
### **Applying a license from a file**
The easiest way to apply a license is to put the license file in the same folder as the aspose-imaging-XX.X-jdk16.jar or used work directory. Then you can specify the file name in the code instead of a full path.

**Java**

{{< highlight java >}}

 // Instantiate an instance of license and apply the license using a full path

com.aspose.imaging.License license = new com.aspose.imaging.License();

license.setLicense("Aspose.Imaging.Java.lic");

{{< /highlight >}}

When you call the setLicense method, the license name should be same as that of your license file name. For example, if you change the license file name to "Aspose.Imaging.lic.xml" you should use this license name for the setLicense method.
### **Applying a license using a stream**
It is also possible to load a license from a stream as demonstrated below.



**Java**

{{< highlight java >}}

 // Instantiate an instance of license and apply the license using a stream

com.aspose.imaging.License license = new com.aspose.imaging.License();

license.setLicense(new java.io.FileInputStream("Aspose.Imaging.Java.lic"));

{{< /highlight >}}

Where to Apply a License in your Application

Where you apply a license depends on the type of application you are developing. Follow these simple rules:

- The license only needs to be set once per application domain. Calling License.setLicense multiple times is not harmful but wastes processor time.
- Apply the license before calling any Aspose.Imaging classes.
- **Java applications**: call License.setLicense in the startup code.
- **Class library**: call License.setLicense from a static constructor of the class that uses Aspose.Imaging. The static constructor executes before an instance of your class is created, making sure that the Aspose.Imaging license is properly set.
## **Using Multiple Aspose Products**
If you use more than one Aspose product in your application, for example Aspose.Imaging and Aspose.Cells, here are a few useful tips.

- **Apply the license for each Aspose product separately**. Even if you have a single license file for all components, for example 'Aspose.Total.lic', you still need to call License.setLicense separately for each Aspose product in your application.
- **Use a fully qualified license class name**. Each Aspose product has a License class in its namespace. For example, Aspose.Imaging has com.aspose.imaging.license.License and Aspose.Cells has com.aspose.cells.License. Using a fully qualified class name avoids any confusion about which license is applied to which product.
