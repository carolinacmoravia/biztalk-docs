---
title: "Import PeopleSoft adapter binding files | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b2a9b19b-2d3d-45ea-bd92-a2501791b86a
caps.latest.revision: 12
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Import Binding Files

## Overview
Before you use [!INCLUDE[btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] to import a binding file, verify the following:  
  
-   The CLASSPATH is pointing to a specific location for the PeopleSoft-specific files. Verify that the location of these files is the same on the new computer—or edit the binding file.  
  
-   The folders for the responses must exist and be identical on the new computer—or edit the binding file.  
  
-   PeopleSoft Enterprise system passwords, if present in the configuration, are saved as ***** in the binding file. For more information, see [Deployment Limitations](../core/deployment-limitations3.md).  
  
> [!NOTE]
>  Deployment overwrites receive location configuration. When you deploy a binding file and assembly on a target computer, the send ports and receive locations are replaced with those in the XML binding file when they are imported.  
  
 For step-by-step directions about importing binding files, see the topic "How to Import Bindings into a BizTalk Group" in the [!INCLUDE[btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] documentation.  
  
## Clean the Target Computer  
To clean the target computer for deploying the new application, remove send ports and receive locations bound to the orchestration.  
  
If you do not have Microsoft [!INCLUDE[btsVStudioNoVersion](../includes/btsvstudionoversion-md.md)] installed on the target computer, you may remove the ports by running these scripts:  
  
**\<Microsoft BizTalk Server>\SDK\Samples\Admin\WMI\Remove Send Port\VBScript\RemoveSendPort.vbs**  
  
**\<Microsoft BizTalk Server>\SDK\Samples\Admin\WMI\Remove Receive Port\VBScript\RemoveReceivePort.vbs**  
  
For example, at a command prompt, run:  
  
**cscript RemoveSendPort.vbs \<Send port name>**  
  
## See Also  
[Import bindings & limitations](../core/deploying-biztalk-adapter-for-peoplesoft-enterprise.md)