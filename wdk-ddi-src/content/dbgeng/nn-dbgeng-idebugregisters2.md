---
UID : NN:dbgeng.IDebugRegisters2
title : IDebugRegisters2
author : windows-driver-content
description : IDebugRegisters2 interface
old-location : debugger\idebugregisters2.htm
old-project : debugger
ms.assetid : f92a75a9-6578-4bbf-8d80-680493b4d284
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugSystemObjects4, IDebugSystemObjects4::SetImplicitThreadDataOffset, SetImplicitThreadDataOffset
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : dbgeng.h
req.include-header : Dbgeng.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDebugRegisters2
req.alt-loc : dbgeng.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugRegisters2 interface



## Methods

<p>The <b>IDebugRegisters2</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [dbgeng.IDebugRegisters2.GetDescription](nf-dbgeng-idebugregisters2-getdescription.md) | The GetDescription method returns the description of a register. |
| [dbgeng.IDebugRegisters2.GetDescriptionWide](nf-dbgeng-idebugregisters2-getdescriptionwide.md) | The GetDescriptionWide method returns the description of a register. |
| [dbgeng.IDebugRegisters2.GetFrameOffset](nf-dbgeng-idebugregisters2-getframeoffset.md) | The GetFrameOffset method returns the location of the stack frame for the current function. |
| [dbgeng.IDebugRegisters2.GetFrameOffset2](nf-dbgeng-idebugregisters2-getframeoffset2.md) | The GetFrameOffset2 method returns the location of the stack frame for the current function. |
| [dbgeng.IDebugRegisters2.GetIndexByName](nf-dbgeng-idebugregisters2-getindexbyname.md) | The GetIndexByName method returns the index of the named register. |
| [dbgeng.IDebugRegisters2.GetIndexByNameWide](nf-dbgeng-idebugregisters2-getindexbynamewide.md) | The GetIndexByNameWide method returns the index of the named register. |
| [dbgeng.IDebugRegisters2.GetInstructionOffset](nf-dbgeng-idebugregisters2-getinstructionoffset.md) | The GetInstructionOffset method returns the location of the current thread's current instruction. |
| [dbgeng.IDebugRegisters2.GetInstructionOffset2](nf-dbgeng-idebugregisters2-getinstructionoffset2.md) | The GetInstructionOffset2 method returns the location of the current thread's current instruction. |
| [dbgeng.IDebugRegisters2.GetNumberPseudoRegisters](nf-dbgeng-idebugregisters2-getnumberpseudoregisters.md) | The GetNumberPseudoRegisters method returns the number of pseudo-registers that are maintained by the debugger engine. |
| [dbgeng.IDebugRegisters2.GetNumberRegisters](nf-dbgeng-idebugregisters2-getnumberregisters.md) | The GetNumberRegisters method returns the number of registers on the target computer. |
| [dbgeng.IDebugRegisters2.GetPseudoDescription](nf-dbgeng-idebugregisters2-getpseudodescription.md) | The GetPseudoDescription method returns a description of a pseudo-register, including its name and type. |
| [dbgeng.IDebugRegisters2.GetPseudoDescriptionWide](nf-dbgeng-idebugregisters2-getpseudodescriptionwide.md) | The GetPseudoDescriptionWide method returns a description of a pseudo-register, including its name and type. |
| [dbgeng.IDebugRegisters2.GetPseudoIndexByName](nf-dbgeng-idebugregisters2-getpseudoindexbyname.md) | The GetPseudoIndexByName method returns the index of a pseudo-register. |
| [dbgeng.IDebugRegisters2.GetPseudoIndexByNameWide](nf-dbgeng-idebugregisters2-getpseudoindexbynamewide.md) | The GetPseudoIndexByNameWide method returns the index of a pseudo-register. |
| [dbgeng.IDebugRegisters2.GetPseudoValues](nf-dbgeng-idebugregisters2-getpseudovalues.md) | The GetPseudoValues method returns the values of a number of pseudo-registers. |
| [dbgeng.IDebugRegisters2.GetStackOffset](nf-dbgeng-idebugregisters2-getstackoffset.md) | The GetStackOffset method returns the current thread's current stack location. |
| [dbgeng.IDebugRegisters2.GetStackOffset2](nf-dbgeng-idebugregisters2-getstackoffset2.md) | The GetStackOffset2 method returns the current thread's current stack location. |
| [dbgeng.IDebugRegisters2.GetValue](nf-dbgeng-idebugregisters2-getvalue.md) | The GetValue method gets the value of one of the target's registers. |
| [dbgeng.IDebugRegisters2.GetValues](nf-dbgeng-idebugregisters2-getvalues.md) | The GetValues method gets the value of several of the target's registers. |
| [dbgeng.IDebugRegisters2.GetValues2](nf-dbgeng-idebugregisters2-getvalues2.md) | The GetValues2 method fetches the value of several of the target's registers. |
| [dbgeng.IDebugRegisters2.OutputRegisters](nf-dbgeng-idebugregisters2-outputregisters.md) | The OutputRegisters method formats and sends the target's registers to the clients as output. |
| [dbgeng.IDebugRegisters2.OutputRegisters2](nf-dbgeng-idebugregisters2-outputregisters2.md) | The OutputRegisters2 method formats and outputs the target's registers. |
| [dbgeng.IDebugRegisters2.SetPseudoValues](nf-dbgeng-idebugregisters2-setpseudovalues.md) | The SetPseudoValues method sets the value of several pseudo-registers. |
| [dbgeng.IDebugRegisters2.SetValue](nf-dbgeng-idebugregisters2-setvalue.md) | The SetValue method sets the value of one of the target's registers. |
| [dbgeng.IDebugRegisters2.SetValues](nf-dbgeng-idebugregisters2-setvalues.md) | The SetValues method sets the value of several of the target's registers. |
| [dbgeng.IDebugRegisters2.SetValues2](nf-dbgeng-idebugregisters2-setvalues2.md) | The SetValues2 method sets the value of several of the target's registers. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |
| **DLL** |  |

    ## See Also

        <dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugregisters.md">IDebugRegisters</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugRegisters2 interface%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>