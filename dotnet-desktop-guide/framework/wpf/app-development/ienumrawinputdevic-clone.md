---
title: IEnumRAWINPUTDEVIC:Clone
ms.date: 03/30/2017
helpviewer_keywords:
- Clone method [WPF]
ms.assetid: 2a6a1900-aa55-45fa-9382-241d569a2dc4
ms.openlocfilehash: cd634b4d4a88d83d425b787ed8493f9aa2504988
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972277"
---
# <a name="ienumrawinputdevicclone"></a><span data-ttu-id="bba10-102">IEnumRAWINPUTDEVIC:Clone</span><span class="sxs-lookup"><span data-stu-id="bba10-102">IEnumRAWINPUTDEVIC:Clone</span></span>
<span data-ttu-id="bba10-103">Erstellt einen weiteren Enumerator für Geräte für die unformatierte Eingabe, der denselben Zustand wie der aktuelle Enumerator aufweist und dieselbe Liste durchlaufen soll.</span><span class="sxs-lookup"><span data-stu-id="bba10-103">Creates another raw input device enumerator with the same state as the current enumerator to iterate over the same list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bba10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba10-104">Syntax</span></span>  
  
```cpp  
HRESULT Clone( [out] IEnumRAWINPUTDEVICE **ppenum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bba10-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="bba10-105">Parameters</span></span>  
 `ppenum`  
  
 <span data-ttu-id="bba10-106">vorgenommen Adresse der Ausgabevariablen, die den [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) -Schnittstellen Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="bba10-106">[out] Address of output variable that receives the [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) interface pointer.</span></span> <span data-ttu-id="bba10-107">Wenn die Methode nicht erfolgreich ist, ist der Wert dieser Ausgabevariablen nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="bba10-107">If the method is unsuccessful, the value of this output variable is undefined.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bba10-108">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bba10-108">Property Value/Return Value</span></span>  
 <span data-ttu-id="bba10-109">HRESULT: Diese Methode unterstützt die Standard Rückgabewerte E_INVALIDARG, E_OUTOFMEMORY und E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="bba10-109">HRESULT: This method supports the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bba10-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bba10-110">Remarks</span></span>  
 <span data-ttu-id="bba10-111">Diese Methode ermöglicht es, einen Punkt in der enumerationssequenz aufzuzeichnen, um zu diesem Zeitpunkt zu einem späteren Zeitpunkt zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="bba10-111">This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.</span></span> <span data-ttu-id="bba10-112">Der Aufrufer muss diesen neuen Enumerator getrennt vom ersten Enumerator freigeben.</span><span class="sxs-lookup"><span data-stu-id="bba10-112">The caller must release this new enumerator separately from the first enumerator.</span></span>
