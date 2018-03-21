---
UID: NS:minitape._STOR_ADDRESS
title: "_STOR_ADDRESS"
author: windows-driver-content
description: A general structure for holding a storage device address.
old-location: storage\stor_address.htm
old-project: storage
ms.assetid: 464AE3EA-D941-430F-8362-B66F4D00AE50
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PSTOR_ADDRESS, PSTOR_ADDRESS, PSTOR_ADDRESS structure pointer [Storage Devices], STOR_ADDRESS, STOR_ADDRESS structure [Storage Devices], STOR_ADDRESS_TYPE_BTL8, STOR_ADDRESS_TYPE_UNKNOWN, _STOR_ADDRESS, storage.stor_address, storport/PSTOR_ADDRESS, storport/STOR_ADDRESS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minitape.h
req.include-header: Storport.h, Scsi.h, Minitape.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 8.
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
-	HeaderDef
api_location:
-	Storport.h
api_name:
-	STOR_ADDRESS
product: Windows
targetos: Windows
req.typenames: STOR_ADDRESS, *PSTOR_ADDRESS
---

# _STOR_ADDRESS structure


## -description



   A general structure for holding a storage device address.


## -syntax


````
typedef struct _STOR_ADDRESS {
  USHORT Type;
  USHORT Port;
  ULONG  AddressLength;
  UCHAR  AddressData[ANYSIZE_ARRAY];
} STOR_ADDRESS, *PSTOR_ADDRESS;
````


## -struct-fields




### -field Type

The address type. This can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STOR_ADDRESS_TYPE_UNKNOWN"></a><a id="stor_address_type_unknown"></a><dl>
<dt><b>STOR_ADDRESS_TYPE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The address type is unknown.

</td>
</tr>
<tr>
<td width="40%"><a id="STOR_ADDRESS_TYPE_BTL8"></a><a id="stor_address_type_btl8"></a><dl>
<dt><b>STOR_ADDRESS_TYPE_BTL8</b></dt>
</dl>
</td>
<td width="60%">
The address is an 8-bit Bus-Target-LUN address.

</td>
</tr>
</table>
 


### -field Port

The host bus adapter (HBA) port number.


### -field AddressLength

The byte length of the <b>AddressData</b>. If <b>Type</b> is set to <b>STOR_ADDRESS_TYPE_BTL8</b>, this value is <b>STOR_ADDR_BTL8_ADDRESS_LENGTH</b>.


### -field AddressData

The address data specific to an address type.


## -see-also

<a href="..\storport\nf-storport-storportsetunitattributes.md">StorPortSetUnitAttributes</a>



<a href="..\storport\ns-storport-_stor_addr_btl8.md">STOR_ADDR_BTL8</a>



 

 

