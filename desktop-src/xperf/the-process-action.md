---
title: The Process Action
description: The Process Action
ms.assetid: ecba7f7d-000e-459b-bfe6-a351bc7abf33
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# The Process Action

The process action produces a text file that summarizes the various metrics regarding process. The usage for this action is:


```
-a process [{[-thread -image -vm]|-tree} -range T1 T2] 
```



The following table includes the individual options.



| Option                  | Description                                               |
|-------------------------|-----------------------------------------------------------|
| thread <br/>      | show threads <br/>                                  |
| image <br/>       | show images <br/>                                   |
| vm <br/>          | show allocated virtual memory ranges <br/>          |
| tree <br/>        | show process tree structure <br/>                   |
| range T1 T2 <br/> | Show data between times T1 and T2, both in use<br/> |
| withsid <br/>     | show sids in process reports <br/>                  |



 

If no option is given, only processes are shown.

 

 




