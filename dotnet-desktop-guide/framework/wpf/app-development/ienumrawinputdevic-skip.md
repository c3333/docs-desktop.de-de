---
title: IEnumRAWINPUTDEVIC:Skip
ms.date: 03/30/2017
helpviewer_keywords:
- Skip method [WPF]
ms.assetid: c967b0f8-1c6a-459c-8c16-d4f08918ab65
ms.openlocfilehash: a74f71345a22f6d766c2d5966ca5d2cb33ab756e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977415"
---
# <a name="ienumrawinputdevicskip"></a><span data-ttu-id="fad49-102">IEnumRAWINPUTDEVIC:Skip</span><span class="sxs-lookup"><span data-stu-id="fad49-102">IEnumRAWINPUTDEVIC:Skip</span></span>
<span data-ttu-id="fad49-103">Weist den Enumerator an, die nächsten `celt` Elemente in der-Enumeration zu überspringen, sodass der nächste [IEnumRAWINPUTDEVIC: Next](ienumrawinputdevic-next.md) -Aufrufe diese Elemente nicht zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fad49-103">Instructs the enumerator to skip the next `celt` elements in the enumeration so that the next call to [IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md) will not return those elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fad49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fad49-104">Syntax</span></span>  
  
```cpp  
HRESULT Skip( [in] ULONG celt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fad49-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="fad49-105">Parameters</span></span>  
 `celt`  
  
 <span data-ttu-id="fad49-106">in Anzahl der Elemente, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fad49-106">[in] Number of elements to be skipped.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fad49-107">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fad49-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="fad49-108">HRESULT: S_OK, wenn die Anzahl der Elemente `celt` ist. Andernfalls S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="fad49-108">HRESULT: S_OK if the number of elements supplied is `celt`; S_FALSE otherwise.</span></span>
