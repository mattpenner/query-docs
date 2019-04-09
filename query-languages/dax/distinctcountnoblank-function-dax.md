---
title: "DISTINCTCOUNTNOBLANK function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.date: 03/13/2019
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# DISTINCTCOUNTNOBLANK

Counts the number of distinct values in a column.
  
## Syntax  
  
```dax
DISTINCTCOUNTNOBLANK (<column>)  
```
  
#### Parameters  

|Term  |Description|  
|---------|---------|
|column     | The column that contains the values to be counted |        

  
## Return value  
The number of distinct values in *column*.  
  
## Remarks  

Unlike [DISTINCTCOUNT](distinctcount-function-dax.md) function, DISTINCTCOUNTNOBLANK does not include the BLANK value. 
  
## Example  
The following example shows how to count the number of distinct sales orders in the column ResellerSales_USD[SalesOrderNumber].  
  
```dax
=DISTINCTCOUNT(ResellerSales_USD[SalesOrderNumber])  
```dax

DAX query

```DAX
EVALUATE
	ROW(
		"DistinctCountNoBlank", DISTINCTCOUNTNOBLANK(DimProduct[EndDate]),
		"DistinctCount", DISTINCTCOUNT(DimProduct[EndDate])
	)
```

|[DistinctCountNoBlank]  |[DistinctCount]  |
|---------|---------|
|2     |     3    |


  
## See also  
[DISTINCTCOUNT](distinctcount-function-dax.md)
  