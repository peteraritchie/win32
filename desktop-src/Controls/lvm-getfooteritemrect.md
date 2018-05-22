---
title: LVM\_GETFOOTERITEMRECT message
description: Gets the coordinates of a footer for a specified item in a list-view control. Send this message explicitly or by using the ListView\_GetFooterItemRect macro.
ms.assetid: '4a6055d3-1cc1-4c3d-a5f6-006617ff3bce'
keywords: ["LVM_GETFOOTERITEMRECT message Windows Controls"]
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
---

# LVM\_GETFOOTERITEMRECT message

Gets the coordinates of a footer for a specified item in a list-view control. Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](listview-getfooteritemrect.md) macro.

## Parameters

<dl> <dt>

*wParam* \[in\]
</dt> <dd>

The index of the item in the list-view control.

</dd> <dt>

*lParam* \[in, out\]
</dt> <dd>

A pointer to a [**RECT**](https://msdn.microsoft.com/library/windows/desktop/dd162897) structure to receive the coordinates. The calling application is responsible for allocating this structure. The coordinates received are expressed as client coordinates.

</dd> </dl>

## Return value

Returns **TRUE** if successful, or **FALSE** otherwise.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server�2008 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



�

�




