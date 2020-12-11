---
title: Funktion "kreateidispatchstaforwarder"-Referenz zur nicht verwalteten WPF-API
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CreateIDispatchSTAForwarder
api_location:
- PresentationHost_v0400.dll
ms.assetid: 57a02dfa-f091-4ace-9c06-1f4ab52b3527
ms.openlocfilehash: f7f60c53125eaaafe88b8777f3b560d5d1e083b2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976411"
---
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a>Funktion "kreateidispatchstaforwarder" (Referenz zur nicht verwalteten WPF-API)
Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.  
  
 Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Thread-und Windows-Verwaltung verwendet.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,
   __deref_out IDispatch **ppForwarder  
)  
```  
  
## <a name="parameters"></a>Parameter  
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert  
 pdispatchdelegat  
 Ein Zeiger auf eine- `IDispatch` Schnittstelle.  
  
 ppforwarder  
 Ein Zeiger auf die Adresse einer `IDispatch` Schnittstelle.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).  
  
 **DLL**  
  
 In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll  
  
 In den .NET Framework 4 und höher: PresentationHost_v0400.dll  
  
 **.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch

- [WPF – Referenz zur nicht verwalteten API](wpf-unmanaged-api-reference.md)
