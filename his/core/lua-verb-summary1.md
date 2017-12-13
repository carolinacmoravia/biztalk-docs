---
title: "LUA Verb Summary1 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d48f8077-9a1d-491c-9293-7e94f8427104
caps.latest.revision: 4
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# LUA Verb Summary
Logical unit application (LUA) application programs can establish and use SNA sessions with either the Request Unit Interface (RUI) application programming interface (API) or the Session Level Interface (SLI) API. If an LUA application establishes an SNA session using **RUI_INIT**, it cannot issue any SLI verbs for that session. Likewise, if an LUA application establishes an SNA session using **SLI_OPEN**, it cannot issue any RUI verbs for that session.  
  
 Following is a brief summary of each LUA verb or user-supplied routine. Each verb supplies parameters to LUA, which performs the desired function and returns parameters to the application:  
  
 [RUI_BID](../HIS2010/rui-bid2.md)  
 Allows the application to determine when information from the host is available to be read.  
  
 [RUI_INIT](../HIS2010/rui-init2.md)  
 Sets up the SSCP-LU session for an LUA application.  
  
 [RUI_PURGE](../HIS2010/rui-purge1.md)  
 Cancels an outstanding **RUI_READ**.  
  
 [RUI_READ](../HIS2010/rui-read1.md)  
 Receives data or status information sent from the host to the LUA application's LU, on either the SSCP session or the LU session.  
  
 [RUI_TERM](../HIS2010/rui-term1.md)  
 Ends the SSCP session for an LUA application. It also terminates the LU session if it is active.  
  
 [RUI_WRITE](../HIS2010/rui-write1.md)  
 Sends data to the host on either the SSCP session or the LU session.  
  
 [SLI_BID](../HIS2010/sli-bid1.md)  
 Notifies the SLI application that a message is waiting to be read using **SLI_RECEIVE**. It also provides the current status of the session to the LUA application.  
  
 [SLI_BIND_ROUTINE](../HIS2010/sli-bind-routine2.md)  
 An optional, user-supplied exit routine that notifies the LUA application that a BIND request has come from the host. It allows the routine to examine the request and formulate a response.  
  
 [SLI_CLOSE](../HIS2010/sli-close2.md)  
 Ends a session opened with **SLI_OPEN**.  
  
 [SLI_OPEN](../core/sli-open2.md)  
 Transfers control of the specified LU to the LUA application. It establishes a session between the SSCP and the specified LU, as well as an LU-LU session.  
  
 [SLI_PURGE](../HIS2010/sli-purge2.md)  
 Cancels **SLI_RECEIVE** verbs issued with a wait condition.  
  
 [SLI_RECEIVE](../HIS2010/sli-receive1.md)  
 Receives responses, SNA commands, and data into the buffer of an LUA application. It also provides the current status of the session to the LUA application.  
  
 [SLI_SEND](../HIS2010/sli-send1.md)  
 Sends responses, SNA commands, and data from an LUA application to a host LU.  
  
 [SLI_STSN_ROUTINE](../HIS2010/sli-stsn-routine2.md)  
 An optional, user-supplied exit routine that notifies the LUA application that a set and test sequence number (STSN) command has come from the host. It allows the routine to examine the request and formulate a response.