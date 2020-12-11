---
title: 'Processunprocessdexception-Funktion: Referenz zur nicht verwalteten WPF-API'
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ProcessUnhandledException
api_location:
- PresentationHost_v0400.dll
ms.assetid: 495ce5f6-bb4d-4b30-807a-c3c35f1ca95c
ms.openlocfilehash: 7de12e0d21a6add88ce602ea00b7f7b3aaf0c197
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977238"
---
# <a name="processunhandledexception-function-wpf-unmanaged-api-reference"></a>Processunprocessdexception-Funktion (Referenz zur nicht verwalteten WPF-API)
Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.  
  
 Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Ausnahmebehandlung verwendet.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
void __stdcall ProcessUnhandledException(  
   __in_ecount(1) BSTR errorMsg  
)  
```  
  
## <a name="parameters"></a>Parameter  
 ERRORMSG  
 Die Fehlermeldung.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).  
  
 **DLL**  
  
 In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll  
  
 In den .NET Framework 4 und höher: PresentationHost_v0400.dll  
  
 **.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch

- [WPF – Referenz zur nicht verwalteten API](wpf-unmanaged-api-reference.md)
