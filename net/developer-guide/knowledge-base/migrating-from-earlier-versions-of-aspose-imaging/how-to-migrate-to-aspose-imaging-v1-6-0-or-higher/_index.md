---
title: How to migrate to Aspose.Imaging v1.6.0 or higher
type: docs
weight: 210
url: /net/how-to-migrate-to-aspose-imaging-v1-6-0-or-higher/
---

﻿

{{% alert color="primary" %}} 

This page lists public API changes that were introduced in Aspose.Imaging v1.6.0. These changes should be considered, while migrating from earlier version of Aspose.Imaging. It includes new and obsoleted features along with any changes in the behavior of API.

{{% /alert %}} 
### **1. CreateOptions and SaveOptions namespaces have been deprecated and replaced with ImageOptions namespace**
﻿

CreateOptions and SaveOptions namespaces are obsolete and ImageOptions namespace has replaced the aforesaid namespaces. Following code snippet describes the usage of new namespace in place of the obsoleted ones.

{{< highlight java >}}

 //Aspose.Imaging.CreateOptions.BmpCreateOptions createOptions = new Aspose.Imaging.CreateOptions.BmpCreateOptions();

Aspose.Imaging.ImageOptions.BmpOptions createOptions = new Aspose.Imaging.ImageOptions.BmpOptions();

//image.Save(@"C:\out.bmp", new Aspose.Imaging.SaveOptions.BmpSaveOptions());

image.Save(@"C:\out.bmp", new Aspose.Imaging.ImageOptions.BmpOptions());


{{< /highlight >}}
### **2. Image Size (Width and Height)**
﻿

Width and Height properties of CreateOptions object implemented as parameters of Create method of Image class. Please find the following code, it describes depreciated properties and replaced parameters.

{{< highlight java >}}



//Aspose.Imaging.CreateOptions.BmpCreateOptions createOptions = new Aspose.Imaging.CreateOptions.BmpCreateOptions();

Aspose.Imaging.ImageOptions.BmpOptions createOptions = new Aspose.Imaging.ImageOptions.BmpOptions();

//createOptions.Height = 500;

//createOptions.Width = 500;

//Aspose.Imaging.Image outimage = Aspose.Imaging.Image.Create(createOptions);

Aspose.Imaging.Image outimage = Aspose.Imaging.Image.Create(createOptions,500,500);


{{< /highlight >}}
