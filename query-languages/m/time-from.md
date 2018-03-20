---
title: "Time.From | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 25564202-a891-4255-b211-6c124044674e
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Time.From

  
## About  
Returns a time value from a value.  
  
```  
Time.From(value as any, optional culture as nullable text) as nullable time  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|value|Value to convert.|  
|optional culture|A text value corresponding to the culture values supported on your version of Windows, such as "en-US". If the culture is not specified, the current user culture is used. For a list of culture names, see [National Language Support (NLS) API Reference](http://msdn.microsoft.com/en-us/goglobal/bb896001.aspx).|  
  
Type to convert  
  
|**Type**|**Description**|  
|------------|-------------------|  
|text|Returns a time value from text value. For more details, see Time.FromText.|  
|datetime|The time component of a value.|  
|datetimezone|The time component of the local date and time equivalent of value.|  
|number|A time equivalent to the number of fractional days expressed by value. If value is negative or greater or equal to 1, an error is returned.|  
|any other type|An Expression.Error is thrown.|  
  
## <a name="__toc360789021"></a>Remarks  
  
-   If value is null, Time.From returns null.  
  
-   If value is time, the same value is returned.  
  
## Examples  
  
```  
Time.From(0.7575) equals #time(18,10,48)  
```  
  
```  
Time.From(#datetime(1899, 12, 30, 06, 45, 12)) equals #time(06,45,12)  
```  