---
UID: NF:video.VideoPortAcquireDeviceLock
title: VideoPortAcquireDeviceLock function
author: windows-driver-content
description: The VideoPortAcquireDeviceLock function acquires the device lock maintained by the video port driver.
old-location: display\videoportacquiredevicelock.htm
old-project: display
ms.assetid: eeb2d1ad-ad99-4099-9560-8653a627aa08
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: VideoPortAcquireDeviceLock, VideoPortAcquireDeviceLock function [Display Devices], VideoPort_Functions_4c588378-53be-496c-93f0-0d285b8a1a05.xml, display.videoportacquiredevicelock, video/VideoPortAcquireDeviceLock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: video.h
req.include-header: Video.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Videoprt.lib
req.dll: Videoprt.sys
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Videoprt.sys
api_name:
-	VideoPortAcquireDeviceLock
product:
- Windows
targetos: Windows
req.typenames: 
---

# VideoPortAcquireDeviceLock function


## -description


The <b>VideoPortAcquireDeviceLock</b> function acquires the device lock maintained by the video port driver.


## -parameters




### -param HwDeviceExtension [in]

Pointer to the miniport driver's device extension.


## -returns



None




## -remarks



Typically, the video port driver guarantees threaded synchronization into the miniport driver through the use of a device lock. However, a miniport driver must perform its own synchronization when being accessed by a child device. That is, a miniport driver must perform synchronization in routines that it exposes through <a href="https://msdn.microsoft.com/f16a7fa3-3471-4ccb-b1b4-982d33f930d3">HwVidQueryInterface</a> by acquiring the device lock maintained by the video port driver.

The miniport driver should release the device lock as quickly as possible by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff570356">VideoPortReleaseDeviceLock</a>.




## -see-also




<a href="https://msdn.microsoft.com/f16a7fa3-3471-4ccb-b1b4-982d33f930d3">HwVidQueryInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570356">VideoPortReleaseDeviceLock</a>
 

 

