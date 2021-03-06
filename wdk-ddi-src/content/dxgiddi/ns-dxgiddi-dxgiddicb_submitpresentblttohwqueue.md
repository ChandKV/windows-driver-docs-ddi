---
UID: NS:dxgiddi.DXGIDDICB_SUBMITPRESENTBLTTOHWQUEUE
title: DXGIDDICB_SUBMITPRESENTBLTTOHWQUEUE
author: windows-driver-content
description:
ms.assetid: 23ad4e9d-d5eb-4cd9-80bd-194a6a276e63
ms.author: windowsdriverdev
ms.date:
ms.topic: struct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.keywords: DXGIDDICB_SUBMITPRESENTBLTTOHWQUEUE, DXGIDDICB_SUBMITPRESENTBLTTOHWQUEUE,
req.header: dxgiddi.h
req.include-header:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.ddi-compliance:
req.unicode-ansi:
req.max-support:
req.typenames: DXGIDDICB_SUBMITPRESENTBLTTOHWQUEUE
topictype:
-	apiref
apitype:
-	HeaderDef
apilocation:
-	dxgiddi.h
apiname:
-	DXGIDDICB_SUBMITPRESENTBLTTOHWQUEUE
product: Windows
targetos: Windows
---

# DXGIDDICB_SUBMITPRESENTBLTTOHWQUEUE structure

## -description

Contains arguments needed for the [PfnddxgiddiSubmitPresentBltToHwQueuecb](nc-dxgiddi-pfnddxgiddi_submitpresentblttohwqueuecb.md) function.

## -struct-fields

### -field hSrcAllocation

[in] The allocation of which content will be presented.

### -field hDstAllocation

[in] The destination allocation of the present.

### -field pDXGIContext

Fill this with the value in [DXGI_DDI_ARG_PRESENT.pDXGIContext](ns-dxgiddi-dxgi_ddi_arg_present.md).

### -field hHwQueue

Hardware queue being submitted to.

### -field HwQueueProgressFenceId

Hardware queue progress fence ID that will be signaled when the Present Blt is done on the GPU.

### -field PrivateDriverDataSize

The size of pPrivateDriverData.

### -field pPrivateDriverData

[in] Private driver data to pass to DdiPresent.

