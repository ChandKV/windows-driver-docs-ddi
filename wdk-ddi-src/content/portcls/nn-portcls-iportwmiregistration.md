---
UID : NN:portcls.IPortWMIRegistration
title : IPortWMIRegistration
author : windows-driver-content
description : The IPortWMIRegistration interface is provided in Windows 7 and later versions of Windows. This interface allows the miniport driver to coordinate Event Tracing for Windows (ETW) registration between PortCls and the miniport driver.
old-location : audio\iportwmiregistration.htm
old-project : audio
ms.assetid : 0fb18e82-4853-459f-b8d3-4841ca3d8301
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : PcUnregisterIoTimeout
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : portcls.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IPortWMIRegistration
req.alt-loc : portcls.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Portcls.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IPortWMIRegistration interface

The <code>IPortWMIRegistration</code> interface is provided in Windows 7 and later versions of Windows. This interface allows the miniport driver to coordinate Event Tracing for Windows (ETW) registration between PortCls and the miniport driver.

ETW provides a mechanism to trace and log events that are raised by user-mode applications and kernel-mode drivers. For more information about ETW, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938554">Event Tracing for Windows</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=154129">Improve Debugging And Performance Tuning With ETW</a>.

## Methods

<p>The <b>IPortWMIRegistration</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [portcls.IPortWMIRegistration.RegisterWMIProvider](nf-portcls-iportwmiregistration-registerwmiprovider.md) | The RegisterWMIProvider method registers the Event Tracing for Windows (ETW) capability of the miniport driver with PortCls. |
| [portcls.IPortWMIRegistration.UnregisterWMIProvider](nf-portcls-iportwmiregistration-unregisterwmiprovider.md) | The UnregisterWMIProvider method unregisters the Event Tracing for Windows (ETW) interface that was previously registered with a call to the RegisterWMIProvider method. The unregistration disables the ETW registration with PortCls. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | portcls.h |
| **DLL** |  |