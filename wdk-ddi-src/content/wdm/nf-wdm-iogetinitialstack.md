---
UID: NF:wdm.IoGetInitialStack
title: IoGetInitialStack function
author: windows-driver-content
description: The IoGetInitialStack routine returns the base address of the current thread's stack.
old-location: kernel\iogetinitialstack.htm
tech.root: kernel
ms.assetid: 0d0d793f-c2c1-48ff-9e7f-ef2697255bfa
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IoGetInitialStack, IoGetInitialStack routine [Kernel-Mode Driver Architecture], k104_5e1ac4e5-b51e-4840-86e3-2ce67c634489.xml, kernel.iogetinitialstack, wdm/IoGetInitialStack
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Ntddk.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: IrqlIoApcLte, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: "<=APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	IoGetInitialStack
product:
- Windows
targetos: Windows
req.typenames: 
---

# IoGetInitialStack function


## -description


The <b>IoGetInitialStack</b> routine returns the base address of the current thread's stack.


## -parameters






## -returns



<b>IoGetInitialStack</b> returns the initial base address of the current thread's stack. 




## -remarks



Highest-level drivers can call this routine, particularly file systems attempting to determine whether they've been passed a pointer to a location on the current thread's stack. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549286">IoGetRemainingStackSize</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549299">IoGetStackLimits</a>
 

 

