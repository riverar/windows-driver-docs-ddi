---
UID: NF:sti.IStiDevice.Subscribe
title: IStiDevice::Subscribe
author: windows-driver-content
description: The IStiDevice::Subscribe method registers the caller to receive notifications of device events.
old-location: image\istidevice_subscribe.htm
tech.root: image
ms.assetid: 6266b311-6846-4615-a686-b68b00001fe7
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IStiDevice interface [Imaging Devices],Subscribe method, IStiDevice.Subscribe, IStiDevice::Subscribe, Subscribe, Subscribe method [Imaging Devices], Subscribe method [Imaging Devices],IStiDevice interface, image.istidevice_subscribe, sti/IStiDevice::Subscribe, stifnc_2c707880-5ace-4a2e-813e-1ee304cea41f.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sti.h
req.include-header: Sti.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sti.h
api_name:
-	IStiDevice.Subscribe
product:
- Windows
targetos: Windows
req.typenames: 
---

# IStiDevice::Subscribe


## -description


The<b> IStiDevice::Subscribe</b> method registers the caller to receive notifications of device events.


## -parameters




### -param lpSubsribe






#### - lpSubscribe [in, out]

Caller-supplied pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548355">STISUBSCRIBE</a> structure containing subscription parameter values.


## -returns



If the operation succeeds, the method returns S_OK. Otherwise, it returns one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



The<b> IStiDevice::Subscribe</b> method is typically called by applications that intercept events from devices and reroute them. The method allows these applications to be notified of <a href="https://msdn.microsoft.com/5f9be89c-8442-4894-b2f6-a4d3558464bf">Still Image Device Events</a> so they can then dispatch control to appropriate display applications.

Based on contents supplied in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548355">STISUBSCRIBE</a> structure, the caller can request to be notified of device events by Windows messages or by Win32 events (by means of <b>SetEvent</b> calls).

When the application receives notification of an event, it can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff543751">IStiDevice::GetLastNotificationData</a> to find out which event occurred. 

Before calling <b>IStiDevice::Subscribe</b>, clients of the <b>IStiDevice</b> COM interface must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff543778">IStillImage::CreateDevice</a> to obtain an <b>IStiDevice</b> interface pointer, which provides access to a specified device.




## -see-also




<a href="https://msdn.microsoft.com/86ce412e-007b-4ea9-9c09-766eee543852">IStiDevice</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543773">IStiDevice::UnSubscribe</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543796">IStillImage::LaunchApplicationForDevice</a>
 

 

