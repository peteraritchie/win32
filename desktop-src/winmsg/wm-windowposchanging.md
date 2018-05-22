﻿---
Description: 'Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the SetWindowPos function or another window-management function.'
ms.assetid: '45ecd966-5222-4738-9e99-8a6edbdd435a'
title: 'WM\_WINDOWPOSCHANGING message'
---

# WM\_WINDOWPOSCHANGING message

Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](setwindowpos.md) function or another window-management function.

A window receives this message through its [**WindowProc**](windowproc.md) function.


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

This parameter is not used.

</dd> <dt>

*lParam* 
</dt> <dd>

A pointer to a [**WINDOWPOS**](windowpos.md) structure that contains information about the window's new size and position.

</dd> </dl>

## Return value

Type: **LRESULT**

If an application processes this message, it should return zero.

## Remarks

For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](defwindowproc.md) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window. This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md#class-styles) and CS\_BYTEALIGNWINDOW client styles. By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.

While this message is being processed, modifying any of the values in [**WINDOWPOS**](windowpos.md) affects the window's new size, position, or place in the Z order. An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

**Reference**
</dt> <dt>

[**DefWindowProc**](defwindowproc.md)
</dt> <dt>

[**EndDeferWindowPos**](enddeferwindowpos.md)
</dt> <dt>

[**SetWindowPos**](setwindowpos.md)
</dt> <dt>

[**WINDOWPOS**](windowpos.md)
</dt> <dt>

[**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md)
</dt> <dt>

[**WM\_MOVE**](wm-move.md)
</dt> <dt>

[**WM\_SIZE**](wm-size.md)
</dt> <dt>

[**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 



