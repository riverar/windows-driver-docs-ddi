---
UID: NC:d3dkmddi.DXGKCB_FREEPAGESFROMMDL
title: DXGKCB_FREEPAGESFROMMDL
author: windows-driver-content
description: Implemented by the client driver to frees all the physical pages that are described by an MDL and was created by the DXGKCB_ALLOCATEPAGESFORMDL routine.
ms.assetid: 8d18ed12-1cbd-4908-ba06-d87e83fc175d
ms.author: windowsdriverdev
ms.date:
ms.topic: callback
ms.prod: windows-hardware
ms.technology: windows-devices
req.header: d3dkmddi.h
req.include-header:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.irql:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
topic_type:
-	apiref
api_type:
-	UserDefined
api_location:
-	d3dkmddi.h
api_name:
-	DXGKCB_FREEPAGESFROMMDL
product: 
- Windows
targetos: Windows
tech.root: display
---

# DXGKCB_FREEPAGESFROMMDL callback function

## -description

Implemented by the client driver to frees all the physical pages that are described by an MDL and was created by the [DXGKCB_ALLOCATEPAGESFORMDL](nc-d3dkmddi-dxgkcb_allocatepagesformdl.md) routine.

## -prototype

```
//Declaration

DXGKCB_FREEPAGESFROMMDL DxgkcbFreepagesfrommdl;

// Definition

NTSTATUS DxgkcbFreepagesfrommdl
(
	IN_CONST_HANDLE hAdapter
	IN_CONST_PDXGKARGCB_FREEPAGESFROMMDL pFreePagesFromMdl
)
{...}

DXGKCB_FREEPAGESFROMMDL


```

## -parameters

### -param hAdapter

Handle to a display adapter.

### -param pFreePagesFromMdl

Pointer to a DXGKARGCB_FREEPAGESFROMMDL structure that contains a handle to the pages for MDL.

## -returns

Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate NTSTATUS Values error code.

## -remarks

Register your implementation of this callback function by setting the appropriate member of DXGKARGCB_FREEPAGESFROMMDL and then calling DxgkCbFreePagesFromMdl.


## -see-also