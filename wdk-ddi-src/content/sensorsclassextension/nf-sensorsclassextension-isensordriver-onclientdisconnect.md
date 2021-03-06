---
UID: NF:sensorsclassextension.ISensorDriver.OnClientDisconnect
title: ISensorDriver::OnClientDisconnect
author: windows-driver-content
description: The ISensorDriver::OnClientDisconnect method notifies the sensor driver that a client application has disconnected.
old-location: sensors\isensordriver_onclientdisconnect.htm
old-project: sensors
ms.assetid: 9484610b-4cbd-4c4e-9e60-ef052702325c
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: ISensorDriver interface [Sensor Devices],OnClientDisconnect method, ISensorDriver.OnClientDisconnect, ISensorDriver::OnClientDisconnect, OnClientDisconnect, OnClientDisconnect method [Sensor Devices], OnClientDisconnect method [Sensor Devices],ISensorDriver interface, Sensor_IFaces_f5f91a04-84b3-4302-9c26-845281651ed9.xml, sensors.isensordriver_onclientdisconnect, sensorsclassextension/ISensorDriver::OnClientDisconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sensorsclassextension.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 7,Available in Windows 7.
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: SensorsClassExtension.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SensorsClassExtension.lib
-	SensorsClassExtension.dll
api_name:
-	ISensorDriver.OnClientDisconnect
product:
- Windows
targetos: Windows
req.typenames: 
---

# ISensorDriver::OnClientDisconnect


## -description


The <b>ISensorDriver::OnClientDisconnect</b> method notifies the sensor driver that a client application has disconnected.


## -parameters




### -param pClientFile [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff558912">IWDFFile</a> interface that represents the file object for the client that disconnected.


### -param pwszSensorID [in]

<b>LPWSTR</b> that contains the ID for the sensor from which the client application is disconnecting.


## -returns



If the operation succeeds, this method returns S_OK. Otherwise, this method returns one of the error codes that are defined in Winerror.h.




## -remarks



The sensor class extension calls this method in the following instances:

<ul>
<li>
An application closes normally.

</li>
<li>
The user revokes permission for an application to access the device that contains the specified sensor.

</li>
<li>
The cleanup work from a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff545512">ISensorClassExtension::CleanupFile</a> has completed.

</li>
</ul>
You can use this call as a signal to update lists and reference counts of connected applications. 

For more information about how to use this method, see <a href="https://msdn.microsoft.com/1895EC5C-08C1-4976-83F2-CD5A2B55338D">Filtering data</a>.


#### Examples

The following example code demonstrates an implementation of <b>ISensorDriver::OnClientDisconnect</b>. This function uses an ATL simple map, named Clients, to keep track of connected clients. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff545573">ISensorDriver::OnClientConnect</a> for an example of how connected clients are added to the map.

The ClientData structure is defined as follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>// Struct to keep track of connected client status.
struct ClientData
{
    BOOL bListening;  // Client is listening to events.
    ULONG ulInterval;  // Interval requested by client.
};</pre>
</td>
</tr>
</table></span></div>
The function definition follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT CSensorDdi:: OnClientDisconnect(
        __in IWDFFile* pClientFile,
        __in LPWSTR pwszSensorID
        )
{
    if(NULL == pClientFile ||
       NULL == pwszSensorID)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;
    ClientData* pCD = NULL;
    BOOL bRet = FALSE;

    // Find this client in the map.
    pCD = Clients.Lookup(pClientFile);
    if(pCD == NULL)
    {
        hr = E_UNEXPECTED;
    }

    if(SUCCEEDED(hr))
    {
        // Free the client data memory.
        delete pCD;
        pCD = NULL;

        // Remove this client from the array.
        bRet = Clients.Remove(pClientFile);
        if(FALSE == bRet)
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545566">ISensorDriver</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545573">ISensorDriver::OnClientConnect</a>
 

 

