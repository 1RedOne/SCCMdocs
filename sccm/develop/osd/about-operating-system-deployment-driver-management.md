---
title: "OS Deployment Driver Management | Microsoft Docs"
ms.custom: ""
ms.date: "09/20/2016"
ms.prod: "configuration-manager"
ms.reviewer: ""
ms.suite: ""
ms.technology:
  - "configmgr-other"
ms.tgt_pltfrm: ""
ms.topic: "article"
applies_to:
  - "System Center Configuration Manager (current branch)"
ms.assetid: 789d981f-d0c5-447b-9d93-24d2e0eef5f0
caps.latest.revision: 7
author: "shill-ms"
ms.author: "v-suhill"
manager: "mbaldwin"
---
# About Operating System Deployment Driver Management
In System Center Configuration Manager, the driver catalog helps manage the cost and complexity of deploying an operating system in an environment that contains different types of computers and devices. By storing device drivers in the driver catalog and not with each individual operating system image, the number of operating system images that is needed is greatly reduced. For more information about the driver catalog, see [http://go.microsoft.com/fwlink/?LinkId=110504](http://go.microsoft.com/fwlink/?LinkId=110504).  

> [!NOTE]
>  Before a driver can be used, it must be added to a driver package. For more information, see [How to Create a Driver Package for a Windows Driver in Configuration Manager](../../develop/osd/how-to-create-a-driver-package-for-a-windows-driver.md).  

## Driver Catalog Management  
 With the Configuration Manager Operating System Deployment server Windows Management Instrumentation (WMI) classes you can manage the following:  

-   Driver import  

-   Driver packages  

-   Boot images  

-   Supported platforms  

### Driver Import  
 Using the [SMS_Driver](assetId:///SMS_Driver?qualifyHint=False&autoUpgrade=True) import methods, you can import the Windows drivers described by .inf and Txtsetup.oem files into the driver catalog. For more information, see [How to Import a Windows Driver Described by an INF File into Configuration Manager](../../develop/osd/how-to-import-a-windows-driver-described-by-an-inf-file.md) and [How to Import a Windows Driver Described by an OEM File into Configuration Manager](../../develop/osd/how-to-import-a-windows-driver-described-by-a-txtsetup-oem-file.md).  

 Before a driver can be used, it must be enabled. For more information, see [How to Enable or Disable a Windows Driver in Configuration Manager](../../develop/osd/how-to-enable-or-disable-a-windows-driver.md).  

### Driver Packages  
 Driver packages contain one or more Windows drivers. A driver package is an `SMS_DriverPackage` object and is distributed in the same way as an `SMS_Package` package. They both derive from [SMS_PackageBaseClass](assetId:///SMS_PackageBaseClass?qualifyHint=False&autoUpgrade=True).  

 For more information about creating a driver package, see [How to Create a Driver Package for a Windows Driver in Configuration Manager](../../develop/osd/how-to-create-a-driver-package-for-a-windows-driver.md).  

### Boot Images  
 Windows device drivers that have been imported into the driver catalog can be added to one or more boot images. Boot images are stored in [SMS_BootImagePackage](assetId:///SMS_BootImagePackage?qualifyHint=False&autoUpgrade=True) objects. In an `SMS_BootImagePackage` object, Windows drivers are kept in an array of referenced drivers. For more information, see [How to add a Windows Driver to a Configuration Manager Boot Image Package](../../develop/osd/how-to-add-a-windows-driver-to-a-configuration-manager-boot-image-package.md)  

### Supported Platforms  
 Windows drivers can be configured to support specific platforms. The supported platforms are stored in the driver package XML. For more information, see [How to Specify The Supported Platforms for a Driver](../../develop/osd/how-to-specify-the-supported-platforms-for-a-driver.md).  

### Driver Categories  
 You can associate categories with Windows device drivers. For more information, see [How to Add a Category to a Windows Driver](../../develop/osd/how-to-add-a-category-to-a-windows-driver.md)  

## See Also  
 [Operating System Deployment Driver Management](../../develop/osd/operating-system-deployment-driver-management.md)   
 [Configuration Manager Operating System Deployment](../../develop/osd/operating-system-deployment.md)