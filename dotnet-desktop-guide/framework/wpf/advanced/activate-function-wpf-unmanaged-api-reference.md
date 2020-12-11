---
title: Aktivieren der Funktion-WPF-Referenz zur nicht verwalteten API
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- Activate
api_location:
- PresentationHost_v0400.dll
ms.assetid: 1400329c-b598-465f-80f2-e3dabf044811
ms.openlocfilehash: c97069613a96009d0b9bb84e55c37b29c2d3ea5b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974683"
---
# <a name="activate-function-wpf-unmanaged-api-reference"></a>Funktion aktivieren (Referenz zur nicht verwalteten WPF-API)

Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.

Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Windows-Verwaltung verwendet.

## <a name="syntax"></a>Syntax

```cpp
void Activate(
    const ActivateParameters* pParameters,
    __deref_out_ecount(1) LPUNKNOWN* ppInner,
    );
```

## <a name="parameters"></a>Parameter

`pParameters`\
Ein Zeiger auf die Aktivierungs Parameter des Fensters.

`ppInner`\
Ein Zeiger auf die Adresse eines Einzelelement Puffers, der einen Zeiger auf ein- <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> Objekt enthält.

## <a name="requirements"></a>Anforderungen

**Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).

**DLL**

In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll

In den .NET Framework 4 und höher: PresentationHost_v0400.dll

**.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]

## <a name="see-also"></a>Siehe auch

- [WPF – Referenz zur nicht verwalteten API](wpf-unmanaged-api-reference.md)
