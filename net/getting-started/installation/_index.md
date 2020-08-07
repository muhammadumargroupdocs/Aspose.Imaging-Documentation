---
title: Installation
type: docs
weight: 50
url: /net/installation/
---

## **Installing Aspose.Imaging for .NET through NuGet**
NuGet is the easiest way to download and install Aspose APIs for .NET. Open Microsoft Visual Studio and NuGet package manager. Search "aspose" to find the desired Aspose API. Click on "Install", the selected API will be downloaded and referenced in your project.

![todo:image_alt_text](installation_1.png)
## **Install or Update Aspose.Imaging using the Package Manager Console**
You can follow the steps below to reference the [Aspose.Imaging API](https://www.nuget.org/packages/Aspose.Imaging/) using the package manager console:

1. Open your solution/project in Visual Studio.
1. Select Tools -> Library Package Manager -> Package Manager Console from the menu to open package manager console.

![todo:image_alt_text](installation_2.png)

Type the command “**Install-Package Aspose.Imaging**” and press enter to install latest full release into your application. Alternatively you can add the "**-prerelease**" suffix to the command in order to specify that the latest release including hot fixes is to be installed as well.

![todo:image_alt_text](installation_3.png)

You will see that the "Installing Aspose.Imaging" tip appears down the bottom of the window indicating that the download is process. 

![todo:image_alt_text](installation_4.png)

Once downloaded you will see the following confirmation messages. If you are not familiar with the [Aspose EULA](https://company.aspose.com/legal/eula) then it is a good idea to read the license referenced in the URL. 

![todo:image_alt_text](installation_5.png)

You should now find that Aspose.Imaging has successfully been added and referenced in your application for you.

![todo:image_alt_text](installation_6.png)

In the package manager console, you can also use the command “**Update-Package Aspose.Imaging**” and press enter to check for any updates to the Aspose.Imgaing package and install them if present. You can also add the "-prerelease" suffix to update latest release.
## **Considerations When Running on a Shared Server Environment**
All Aspose .NET components are recommended to run with Full Trust permission set. This is because Aspose .NET component sometimes need to access registry settings and files located in places other than the virtual directory e.g. for reading fonts etc. Furthermore, Aspose.NET components are based on core .NET system classes, some of which also require Full Trust permission to run in some cases.

Internet Service Providers hosting multiple applications from different companies mostly enforce Medium Trust security level. In the case of .NET 2.0, such a security level may set the following constraints which could affect the ability of Aspose.Words to perform properly.

- **RegistryPermission** is not available. This means you cannot access the registry, which is required to enumerate installed fonts when rendering documents.
- **FileIOPermission** is restricted. This means you can only access files in your application’s virtual directory hierarchy. This potentially means fonts cannot be read during export.

For these reasons specified above, it is recommended that Aspose.Imaging to run on Full Trust permissions. You may find that some features of library will work when performing different tasks in Medium trust while some won't (rendering for example) which may due to calls to GDI+ image processing.
## **Working with .NET Core DLLs in Non-Windows Environment**
As Aspose.Imaging for .NET provides .NET Standard 2.0 (.NET Core 2.0) support, so it can be used in Core Applications running in Linux like operating systems. We are constantly working over improving the .NET Core support in our API. However, there are some following operations which we recommend our customers to perform, in order to get better results while using features of Aspose.Imaging for .NET:

Please install:

1. libgdiplus package
1. libc6-dev package
1. package with Microsoft compatible fonts: ttf-mscorefonts-installer. (e.g. *sudo apt-get install ttf-mscorefonts-installer*)
## **Working with .NET Core DLLs installed via MSI package**
**Please note:** if you use NetStandard dll installed via MSI package you should add necessary dependencies to work with netStandard version (please see release notes for more information).
