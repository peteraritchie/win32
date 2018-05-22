---
title: SCSI\_ADDRESS structure
description: The SCSI\_ADDRESS structure is used in conjunction with the IOCTL\_SCSI\_GET\_ADDRESS request to retrieve the address information, such as the target ID (TID) and the logical unit number (LUN) of a particular SCSI target.
ms.assetid: '2b3acd3d-b5da-4dd3-89f1-0b8a7d68e54c'
keywords: ["SCSI_ADDRESS structure Storage Devices", "PSCSI_ADDRESS structure pointer Storage Devices"]
topic_type:
- apiref
api_name:
- SCSI_ADDRESS
api_location:
- ntddscsi.h
api_type:
- HeaderDef
---

# SCSI\_ADDRESS structure

The SCSI\_ADDRESS structure is used in conjunction with the [**IOCTL\_SCSI\_GET\_ADDRESS**](ioctl-scsi-get-address.md) request to retrieve the address information, such as the target ID (TID) and the logical unit number (LUN) of a particular SCSI target.

> [!Note]  
> The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future. Instead, we recommend using the [Storport driver](https://msdn.microsoft.com/windows/hardware/drivers/storage/storport-driver) and [Storport miniport](https://msdn.microsoft.com/windows/hardware/drivers/storage/storport-miniport-drivers) driver models.

�

## Syntax


```C++
typedef struct _SCSI_ADDRESS {
  ULONG Length;
  UCHAR PortNumber;
  UCHAR PathId;
  UCHAR TargetId;
  UCHAR Lun;
} SCSI_ADDRESS, *PSCSI_ADDRESS;
```



## Members

<dl> <dt>

**Length**
</dt> <dd>

Contains the length of this structure in bytes.

</dd> <dt>

**PortNumber**
</dt> <dd>

Contains the number of the SCSI adapter.

</dd> <dt>

**PathId**
</dt> <dd>

Contains the number of the bus.

</dd> <dt>

**TargetId**
</dt> <dd>

Contains the number of the target device.

</dd> <dt>

**Lun**
</dt> <dd>

Contains the logical unit number.

</dd> </dl>

## Remarks

Legacy class drivers issue the [**IOCTL\_SCSI\_GET\_ADDRESS**](ioctl-scsi-get-address.md) request to the port driver to obtain the address of their devices.

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ntddscsi.h (include Ntddscsi.h)</dt> </dl> |



## See also

<dl> <dt>

[**IOCTL\_SCSI\_GET\_ADDRESS**](ioctl-scsi-get-address.md)
</dt> </dl>

�

�

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20SCSI_ADDRESS%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





