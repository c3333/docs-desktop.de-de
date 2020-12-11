---
title: 'Forwardtranslateaccelerator-Funktion: Referenz zur nicht verwalteten WPF-API'
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ForwardTranslateAccelerator
api_location:
- PresentationHost_v0400.dll
ms.assetid: fff47a86-9d9f-4176-9530-10e1876e393f
ms.openlocfilehash: 5e477314117db7be35580b70b84fcc9ad9226e73
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977434"
---
# <a name="forwardtranslateaccelerator-function-wpf-unmanaged-api-reference"></a>Forwardtranslateaccelerator-Funktion (Referenz zur nicht verwalteten WPF-API)
Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.  
  
 Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Windows-Verwaltung verwendet.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT ForwardTranslateAccelerator(  
   MSG* pMsg,
   VARIANT_BOOL appUnhandled  
)  
```  
  
## <a name="parameters"></a>Parameter  
 pmsg  
 Ein Zeiger auf eine Meldung.  
  
 appunbehandelte  
 `true` , wenn der App bereits die Möglichkeit gegeben wurde, die Eingabe Nachricht zu verarbeiten, Sie aber nicht behandelt hat. andernfalls `false` .  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).  
  
 **DLL**  
  
 In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll  
  
 In den .NET Framework 4 und höher: PresentationHost_v0400.dll  
  
 **.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch

- [WPF – Referenz zur nicht verwalteten API](wpf-unmanaged-api-reference.md)
