---
title: IEnumRAWINPUTDEVIC:Next
ms.date: 03/30/2017
helpviewer_keywords:
- Next method [WPF]
ms.assetid: 3698b44d-510e-4d18-b32b-85f17188ee26
ms.openlocfilehash: c7450a9ababa9cf3cb02d572f5ed84f0791d74e4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972273"
---
# <a name="ienumrawinputdevicnext"></a>IEnumRAWINPUTDEVIC:Next
Listet die nächsten `celt` [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) -Strukturen in der Enumeratorliste auf und gibt Sie `rgelt` zusammen mit der tatsächlichen Anzahl der aufgelisteten Elemente in zurück `pceltFetched` .  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT Next(  
      [in] ULONG celt,  
      [out, size_is(celt), length_is(*pceltFetched)] RAWINPUTDEVICE *rgelt,  
      [out] ULONG *pceltFetched);  
```  
  
## <a name="parameters"></a>Parameter  
 `celt`  
  
 in Anzahl der [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) -Strukturen, die in zurückgegeben werden `rgelt` .  
  
 `rgelt`  
  
 [out] Array der Größe "celt" (oder größer), um die aufgelisteten RAWINPUTDEVICE-Strukturen zu empfangen.  
  
 `pceltFetched`  
  
 [out] Zeiger auf die Anzahl der Elemente, die tatsächlich in `rgelt` vorhanden sind. Der Aufrufer kann in `NULL` übergehen, wenn  `rgelt`eins beträgt.   
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert  
 HRESULT: S_OK, wenn die Anzahl der Elemente `celt` ist. Andernfalls S_FALSE.
