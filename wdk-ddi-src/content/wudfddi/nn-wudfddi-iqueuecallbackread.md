---
UID : NN:wudfddi.IQueueCallbackRead
title : IQueueCallbackRead
author : windows-driver-content
description : An I/O queue notifies a driver when a read request is available for the driver.
old-location : wdf\iqueuecallbackread.htm
old-project : wdf
ms.assetid : ccae49a2-2081-44f2-b1f6-cb1e98b74e5d
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : IWDFWorkItem, IWDFWorkItem::GetParentObject, GetParentObject
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : wudfddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IQueueCallbackRead
req.alt-loc : wudfddi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : WUDFx.dll
req.irql : 
req.typenames : "*PPOWER_ACTION, POWER_ACTION"
req.product : Windows 10 or later.
---

# IQueueCallbackRead interface

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

An I/O queue notifies a driver when a read request is available for the driver. The I/O queue notifies the driver when an application calls the Microsoft Win32 <b>ReadFile</b> or <b>ReadFileEx</b> function. The driver can handle the notification by registering the <b>IQueueCallbackRead</b> interface.

## Methods

<p>The <b>IQueueCallbackRead</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [wudfddi.IQueueCallbackRead.OnRead](nf-wudfddi-iqueuecallbackread-onread.md) | The OnRead method is called to handle a read request when an application reads information from a device through the Microsoft Win32 ReadFile or ReadFileEx function. |

## Remarks

A driver registers the <b>IQueueCallbackRead</b> interface when it calls the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557020">IWDFDevice::CreateIoQueue</a> method to create an I/O queue or to configure the default I/O queue. For more information about creating or configuring an I/O queue, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/configuring-dispatch-mode-for-an-i-o-queue">Configuring Dispatch Mode for an I/O Queue</a>.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | wudfddi.h |
| **DLL** | WUDFx.dll |