---
Description: The NonDelegatingAddRef method increments the reference count on the object. This method implements the INonDelegatingUnknown::NonDelegatingAddRef method.
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: CUnknown.NonDelegatingAddRef method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# CUnknown.NonDelegatingAddRef method

The `NonDelegatingAddRef` method increments the reference count on the object. This method implements the **INonDelegatingUnknown::NonDelegatingAddRef** method.

## Syntax


```C++
ULONG NonDelegatingAddRef();
```



## Parameters

This method has no parameters.

## Return value

Returns the reference count.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



 

 



