---
title: "TIME Function (DAX) | Microsoft Docs"
ms.custom: ""
ms.date: "12/28/2017"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "analysis-services"
  - "daxlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "sql13.as.daxref.TIME.f1"
helpviewer_keywords: 
  - "TIME function"
ms.assetid: 7dc334fe-9a86-4cbb-be50-f630c162e514
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# TIME Function (DAX)
Converts hours, minutes, and seconds given as numbers to a time in **datetime** format.  
  
## Syntax  
  
```  
TIME(hour, minute, second)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|**hour**|A number from 0 to 23 representing the hour.<br /><br />Any value greater than 23 will be divided by 24 and the remainder will be treated as the hour value.|  
|**minute**|A number from 0 to 59 representing the minute.<br /><br />Any value greater than 59 will be converted to hours and minutes.|  
|**second**|A number from 0 to 59 representing the second.<br /><br />Any value greater than 59 will be converted to hours, minutes, and seconds.|  
  
## Return Value  
A time (**datetime**).  
  
## Remarks  
In contrast to Microsoft Excel, which stores dates and times as serial numbers, DAX works with date and time values in a **datetime** format. Numbers in other formats are implicitly converted when you use a date/time value in a DAX function. If you need to use serial numbers, you can use formatting to change the way that the numbers are displayed.  
  
Time values are a portion of a date value, and in the serial number system are represented by a decimal number. Therefore, the **datetime** value 12:00 PM is equivalent to 0.5, because it is half of a day.  
  
You can supply the arguments to the TIME function as values that you type directly, as the result of another expression, or by a reference to a column that contains a numeric value. The following restrictions apply:  
  
-   Any value for **hours** that is greater than 23 will be divided by 24 and the remainder will be treated as the hour value.  
  
-   Any value for **minutes** that is greater than 59 will be converted to hours and minutes.  
  
-   Any value for **seconds** that is greater than 59 will be converted to hours, minutes, and seconds.  
  
-   For minutes or seconds, a value greater than 24 hours will be divided by 24 and the reminder will be treated as the hour value. A value in excess of 24 hours does not alter the date portion.  
  
To improve readability of the time values returned by this function, we recommend that you format the column or PivotTable cell that contains the results of the formula by using one of the time formats provided by Microsoft Excel.  
  
This DAX function may return different results when used in a model that is deployed and then queried in DirectQuery mode. For more information about semantic differences in DirectQuery mode, see  [http://go.microsoft.com/fwlink/?LinkId=219171](http://go.microsoft.com/fwlink/?LinkId=219171).  
  
## Example  
The following examples both return the time, 3:00 AM:  
  
```  
=TIME(27,0,0)   
=TIME(3,0,0)  
```  
  
## Example  
The following examples both return the time, 12:30 PM:  
  
```  
=TIME(0,750,0)   
=TIME(12,30,0)  
```  
  
## Example  
The following example creates a time based on the values in the columns, `intHours`, `intMinutes`, `intSeconds`:  
  
```  
=TIME([intHours],[intMinutes],[intSeconds])  
```  
  
## See Also  
[DATE Function &#40;DAX&#41;](date-function-dax.md)  
[Date and Time Functions &#40;DAX&#41;](date-and-time-functions-dax.md)  
  