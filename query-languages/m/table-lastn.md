---
title: "Table.LastN | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 2c13a433-66a0-4ab2-972c-85acf9dc9af0
caps.latest.revision: 7
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Table.LastN

  
## About  
Returns the last row(s) from a table, depending on the **countOrCondition** parameter.  
  
```  
Table.LastN(table as table, countOrCondition as any) as table  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|table|The Table to check.|  
|countOrCondition|Depending on the type, more than one row will be returned.|  
  
## <a name="__toc360789488"></a>Remarks  
  
-   If countOrCondition is a number, that many rows will be returned starting from the end of the table.  
  
-   If countOrCondition is a condition, the rows that meet the condition will be returned in ascending position until a row does not meet the condition.  
  
## Example  
  
```  
Table.LastN(Table.FromRecords({  
  
    [CustomerID = 1, Name = "Bob", Phone = "123-4567"],  
  
    [CustomerID = 2, Name = "Jim", Phone = "987-6543"],  
  
    [CustomerID = 3, Name = "Paul", Phone = "543-7890"]  
  
}), 1)  
```  
  
|CustomerID|Name|Phone|  
|--------------|--------|---------|  
|3|Paul|543-7890|  
  