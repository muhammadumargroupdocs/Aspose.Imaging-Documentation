---
title: ImageAttach for Dynamics CRM
type: docs
weight: 10
url: /net/imageattach-for-dynamics-crm/
---

**Contents Summary**

- [Introduction](#ImageAttachforDynamicsCRM-Introduction)
- [System Requirements and Supported Platforms](#ImageAttachforDynamicsCRM-SystemRequirementsandSupportedPlatforms) 
  - [System Requirements](#ImageAttachforDynamicsCRM-SystemRequirements)
  - [Supported Platforms](#ImageAttachforDynamicsCRM-SupportedPlatforms)
- [Downloading](#ImageAttachforDynamicsCRM-Downloading)
- [Installing or Uninstalling](#ImageAttachforDynamicsCRM-InstallingorUninstalling) 
  - [Installing Aspose .NET ImageAttach](#ImageAttachforDynamicsCRM-InstallingAspose.NETImageAttach)
  - [Applying License](#ImageAttachforDynamicsCRM-ApplyingLicense)
  - [Uninstalling Aspose .NET ImageAttach](#ImageAttachforDynamicsCRM-UninstallingAspose.NETImageAttach)
- [Using](#ImageAttachforDynamicsCRM-Using) 
  - [Configuring Aspose .NET ImageAttach](#ImageAttachforDynamicsCRM-ConfiguringAspose.NETImageAttach)
  - [Using Aspose .NET ImageAttach](#ImageAttachforDynamicsCRM-UsingAspose.NETImageAttach)
- [Video Demo](#ImageAttachforDynamicsCRM-VideoDemo)
- [Support, Extend and Contribute](#ImageAttachforDynamicsCRM-Support,ExtendandContribute) 
  - [Support](#ImageAttachforDynamicsCRM-Support)
  - [Extend and Contribute](#ImageAttachforDynamicsCRM-ExtendandContribute)
## **Introduction**
Aspose .NET ImageAttach is an open source add-on to be used with Microsoft Dynamics CRM. This add-on provide functionality to add images to a record and view them on the main form. Aspose .NET ImageAttach can be used with CRM on-premises as well as CRM Online.
Major features of this add-on are:

- Silverlight web-resource that can be added to any entity.
- Allow functionality to upload any type of image.
- Allow functionality to upload multiple images on the entity.
- Remove/Replace the images anytime.

This add on will work with all versions of **Microsoft Dynamics CRM 2013, 2015 and CRM Online**.
## **System Requirements and Supported Platforms**
### **System Requirements**
In order to install and use Aspose .NET ImageAttach for Microsoft Dynamics CRM you need to have one of the following CRM version installed.

Microsoft Dynamics CRM 2013 On-Premises.
Microsoft Dynamics CRM 2015 On-Premises.
Microsoft Dynamics CRM Online.

Please feel free to contact us if you find any issues in installing or using this Add-on.
### **Supported Platforms**
This add-on will work with all version of Microsoft Dynamics CRM:

- Microsoft Dynamics CRM 2013.
- Microsoft Dynamics CRM 2015.
- Microsoft Dynamics CRM Online
## **Downloading**
The addon is provided in the form of a solution. You can download the latest solution from:

- [CodePlex](https://asposenetcrm.codeplex.com/releases).
- [GitHub](https://github.com/asposemarketplace/asposenetcrm/releases).
- [BitBucket](https://bitbucket.org/asposemarketplace/aspose-.net-for-dynamics-crm/downloads).
- [SourceForge](https://sourceforge.net/projects/asposenetcrm/files/Aspose%20.NET%20ImageAttach/).
- [Code.MSDN](https://code.msdn.microsoft.com/Aspose-Net-ImageAttach-for-7583245a).
## **Installing or Uninstalling**
### **Installing Aspose .NET ImageAttach**
- Download the Solution File.
- Open CRM and go to Import Solution.
- Click Browse and select the downloaded solution file and click next.
- Click next and wait for the solution to import.
- Click close when the solution is imported successfully.
- Publish Customizations.
### **Applying License**
- Upload the License File in the WebResources.
- Copy the name of WebResouce, that will be later used in the configuration.
### **Uninstalling Aspose .NET ImageAttach**
- Go to solution and select "Aspose .NET ImageAttach".
- Press the Delete button.
## **Using**
### **Configuring Aspose .NET ImageAttach**
- Open Aspose Configurations in Advance Find.
- Click New and Create the following entries:
- **SaveToEntity**: 
  - 0=Do not save the Image in Entity Notes
  - 1= Save the Image in Entity Notes. (Default Option)
- **LicenseWebResourceName**: 
  - Webresource Name where the License Xml is Stored. (Default=Aspose_License.lic, included in the solution) 

![todo:image_alt_text](/download/thumbnails/14700546/2124258575)
### **Using Aspose .NET ImageAttach**
- Select Entity where you want to place Aspose .NET ImageAttach and Go to Customize Form.
- Click Insert => Webresources. 

![todo:image_alt_text](imageattach-for-dynamics-crm_1)

- Select Web resource as “Aspose_ImageAttach.xap” and Give a Name to the resource. 

![todo:image_alt_text](imageattach-for-dynamics-crm_2)

- Please ensure that “Pass record object-type code and unique identifier as parameters.” Checkbox is selected.
- Custom Parameter: If you are using multiple images on save form, then use this parameter to differentiate them by providing different names as shown in the image. If only one image web resource is used on the form then you can leave it blank.
- Save and Publish Customization.
- Open the Entity and use the web resource to Upload/Replace/Remove Image. 

![todo:image_alt_text](imageattach-for-dynamics-crm_3)
## **Video Demo**
Please check [the video](http://youtu.be/k_QVup-N3c8) below to see the plugin in action.
## **Support, Extend and Contribute**
### **Support**
We offer free support. Anyone who uses our product, whether they have bought them or are using an evaluation, deserves our full attention and respect.

You can log any issues or suggestions related to Aspose .NET ImageAttach using any of the following platforms:

- [Codeplex](http://goo.gl/rm1kdU)
- [Github](http://goo.gl/UBvjIV)
- [Sourceforge](http://goo.gl/EqZmTC)
- [Bitbucket](http://goo.gl/tzcGGP)
- [Code.MSDN](http://goo.gl/EiG9W0)
### **Extend and Contribute**
You can download the latest source code at:

- [CodePlex](https://asposenetcrm.codeplex.com/SourceControl/latest#Aspose .NET Document Merger/).
- [GitHub](https://github.com/asposemarketplace/asposenetcrm/tree/master/Aspose%20.NET%20ImageAttach/Source%20Code).
- [BitBucket](https://bitbucket.org/asposemarketplace/aspose-.net-for-dynamics-crm/src/7ce93ebc181bba2b22539bfe183c68872f812070/Aspose%20.NET%20ImageAttach/Source%20Code/?at=master).
- [SourceForge](http://sourceforge.net/p/asposenetcrm/code/ci/master/tree/Aspose%20.NET%20ImageAttach/Source%20Code/).
- [Code.MSDN](https://code.msdn.microsoft.com/Aspose-Net-ImageAttach-for-7583245a/view/SourceCode#content).

{{< highlight java >}}

 MemoryStream AsposeImageStream = new MemoryStream();

Aspose.Imaging.Image img = Aspose.Imaging.Image.Load(stream);

AsposeImageStream = new MemoryStream();

img.Save(AsposeImageStream);


{{< /highlight >}}
