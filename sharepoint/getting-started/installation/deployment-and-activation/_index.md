---
title: Deployment and Activation
type: docs
weight: 30
url: /sharepoint/deployment-and-activation/
---

### **Deployment**
Aspose.Imaging for SharePoint performs the following actions during deployment:

- Installs **Aspose.Imaging.SharePoint.dll** into the Global Assembly Cache and adds a SafeControl entry in the **web.config** file.
- Installs feature manifest and other necessary files to the appropriate directories.
- Registers the feature in the SharePoint database and make it available for the activation at the feature scope.
### **Activation**
Aspose.Imaging for SharePoint is packaged as a site (site collection) level feature and can be activated and deactivated on site collections. 

During activation, the feature makes some changes to the virtual directory of the parent web application of the site collection:

- Adds conversion settings page to the sitemap file.
- Copies the necessary resource files to the **App_GlobalResources** folder in the virtual directory.
