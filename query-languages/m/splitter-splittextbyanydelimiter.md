---
title: "Splitter.SplitTextByAnyDelimiter | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 12b5b409-8da2-4124-b964-d6b9b8eb980a
caps.latest.revision: 5
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Splitter.SplitTextByAnyDelimiter

  
## About  
Returns a function that splits text by any supported delimiter.  
  
```  
Splitter.SplitTextByEachDelimiter(delimiters as list, optional quoteStyle as nullable number) as function  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|Delimiters|The delimiter characters are used to identify at what points to split the string.  The delimiter character is not included in the split values.  A trailing delimiter character will yield an additional empty text value.  The split values contain all characters between the delimiters.  This function will always produce at least one value.|  
|optional quoteStyle|The quoteStyle acts as described in Lines.FromText.  By default, it is QuoteStyle.Csv.|  
  
## <a name="__toc360789919"></a>Remarks  
  
-   Splitter.SplitTextByAnyDelimiter is similar to Splitter.SplitTextByDelimiter except that multiple delimiters may be used to specify the points at which to break the text.  
  