---
UID: NC:dispmprt.DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT
title: DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT
author: windows-driver-content
description: The OS calls the DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT callback function to discover what types of diagnostic the driver supports for the passed diagnostic category.
ms.assetid: ad14a3b9-d0bf-4292-8e53-7f51544d96c5
ms.author: windowsdriverdev
ms.date: 
ms.topic: callback
ms.prod: windows-hardware
ms.technology: windows-devices
req.header: dispmprt.h
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
-	dispmprt.h
api_name: 
-	DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT
product: 
- Windows
targetos: Windows
---

# DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT callback function

## -description

The OS calls the DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT callback function to discover what types of diagnostic the driver supports for the passed diagnostic category.

## -prototype

```
//Declaration

DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT DxgkddiQuerydiagnostictypessupport; 

// Definition

NTSTATUS DxgkddiQuerydiagnostictypessupport 
(
	IN_CONST_PVOID MiniportDeviceContext
	INOUT_PDXGKARG_QUERYDIAGNOSTICTYPESSUPPORT pArgQueryDiagnosticTypesSupport
)
{...}

DXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT *PDXGKDDI_QUERYDIAGNOSTICTYPESSUPPORT


```

## -parameters

### -param MiniportDeviceContext

A handle to a context block associated with a display adapter.

### -param pArgQueryDiagnosticTypesSupport

Pointer to a [DXGKARG_QUERYDIAGNOSTICTYPESSUPPORT](ns-dispmprt-_dxgkarg_querydiagnostictypessupport.md) structure.

## -returns

Returns NTSTATUS.


## -remarks




## -see-also