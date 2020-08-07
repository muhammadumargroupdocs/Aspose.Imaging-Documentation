---
title: How to Migrate to Aspose.Imaging 1.7.0 or Higher
type: docs
weight: 80
url: /java/how-to-migrate-to-aspose-imaging-1-7-0-or-higher/
---

{{% alert color="primary" %}} 

This page lists public API changes that were introduced in Aspose.Imaging for java 1.7.0. These changes should be considered, while migrating from earlier version of Aspose.Imaging. It includes new and obsoleted features along with any changes in the behavior of API.

{{% /alert %}} 
### **1. CreateOptions and SaveOptions Packages have been Replaced with ImageOptions**
CreateOptions and SaveOptions packages are obsolete and ImageOptions has replaced the aforesaid. Following code snippet describes the usage of new packages in place of the obsoleted ones.

{{< highlight java >}}

 //com.aspose.imaging.createoptions.BmpCreateOptions createOptions = new com.aspose.imaging.createoptions.BmpCreateOptions();

com.aspose.imaging.imageoptions.BmpOptions createOptions = new com.aspose.imaging.imageoptions.BmpOptions();

//image.Save(@"C:\out.bmp", new com.aspose.imaging.saveoptions.BmpSaveOptions());

image.Save(@"C:\out.bmp", new com.aspose.imaging.imageoptions.BmpOptions());


{{< /highlight >}}
### **2. Image Size (Width and Height)**
Width and Height properties of CreateOptions object implemented as parameters of Create method of Image class. Please find the following code, it describes depreciated properties and replaced parameters.

{{< highlight java >}}

 //com.aspose.imaging.createoptions.BmpCreateOptions createOptions = new com.aspose.imaging.createoptions.BmpCreateOptions();

com.aspose.imaging.imageoptions.BmpOptions createOptions = new com.aspose.imaging.imageoptions.BmpOptions();

//createOptions.Height = 500;

//createOptions.Width = 500;

//com.aspose.imaging.Image outimage = com.aspose.imaging.Image.Create(createOptions);

com.aspose.imaging.Image outimage = com.aspose.imaging.Image.create(createOptions,500,500);


{{< /highlight >}}
