---
title: "#time | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 29343bca-dc38-442e-a1de-12d9b8dad23d
caps.latest.revision: 2
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# #time
<code>#time(<b>hour</b> as number, <b>minute</b> as number, <b>second</b> as number) as time</code>

## About
Creates a time value from whole numbers hour <code>hour</code>, minute <code>minute</code>, and (fractional) second <code>second</code>. Raises an error if these are not true: <ul> <li> 0 ≤ hour ≤ 24 </li> <li> 0 ≤ minute ≤ 59 </li> <li> 0 ≤ second ≤ 59 </li> <li> if hour is 24, then minute and second must be 0 </li> </ul>