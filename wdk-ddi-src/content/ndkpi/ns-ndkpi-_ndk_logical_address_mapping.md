---
UID: NS:ndkpi._NDK_LOGICAL_ADDRESS_MAPPING
title: "_NDK_LOGICAL_ADDRESS_MAPPING"
author: windows-driver-content
description: The NDK_LOGICAL_ADDRESS_MAPPING structure contains an array of adapter logical addresses.
old-location: netvista\ndk_logical_address_mapping.htm
old-project: netvista
ms.assetid: 7FB34813-5F89-4B9C-9594-B23E7D4736C6
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: NDK_LOGICAL_ADDRESS_MAPPING, NDK_LOGICAL_ADDRESS_MAPPING structure [Network Drivers Starting with Windows Vista], PNDK_LOGICAL_ADDRESS_MAPPING, PNDK_LOGICAL_ADDRESS_MAPPING structure pointer [Network Drivers Starting with Windows Vista], _NDK_LOGICAL_ADDRESS_MAPPING, ndkpi/NDK_LOGICAL_ADDRESS_MAPPING, ndkpi/PNDK_LOGICAL_ADDRESS_MAPPING, netvista.ndk_logical_address_mapping
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ndkpi.h
req.include-header: Ndkpi.h
req.target-type: Windows
req.target-min-winverclnt: None supported,Supported in NDIS 6.30 and later.
req.target-min-winversvr: Windows Server 2012
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
-	HeaderDef
api_location:
-	ndkpi.h
api_name:
-	NDK_LOGICAL_ADDRESS_MAPPING
product:
- Windows
targetos: Windows
req.typenames: NDK_LOGICAL_ADDRESS_MAPPING
---

# _NDK_LOGICAL_ADDRESS_MAPPING structure


## -description


The <b>NDK_LOGICAL_ADDRESS_MAPPING</b> structure contains an array of adapter logical addresses.


## -struct-fields




### -field AdapterContext

Reserved for the NDK provider's use. The NDK consumer must not modify this member.


### -field AdapterPageCount

	The number of entries in the array that is specified in the  <b>AdapterPageArray</b> member.



### -field AdapterPageArray

An array of adapter logical addresses. Each logical address in the array corresponds to a page, of <b>PAGE_SIZE</b> bytes in length, and must be <b>PAGE_SIZE</b>-aligned. The array of pages correspond to a virtually contiguous memory region.
The <b>NDK_LOGICAL_ADDRESS</b> datatype is defined as follows:

<pre class="syntax" xml:space="preserve"><code>typedef PHYSICAL_ADDRESS NDK_LOGICAL_ADDRESS;</code></pre>

## -remarks



<b>NDK_LOGICAL_ADDRESS_MAPPING</b> represents an adapter's view of physical memory. See <a href="https://msdn.microsoft.com/library/windows/hardware/hh439860">NDK_FN_BUILD_LAM</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/hh439910">NDK_FN_RELEASE_LAM</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439860">NDK_FN_BUILD_LAM</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh439910">NDK_FN_RELEASE_LAM</a>
 

 

