---
title: 'Loadfromhistory-Funktion: Referenz zur nicht verwalteten WPF-API'
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- LoadFromHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: d037c062-a911-4949-b251-ccd3e48b1d17
ms.openlocfilehash: fa5851658fd21e222a277ea78ad8dcd53009bf17
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977686"
---
# <a name="loadfromhistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="4f275-102">Loadfromhistory-Funktion (Referenz zur nicht verwalteten WPF-API)</span><span class="sxs-lookup"><span data-stu-id="4f275-102">LoadFromHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="4f275-103">Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4f275-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="4f275-104">Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Windows-Verwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f275-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f275-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f275-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadFromHistory_export(  
        IStream* pHistoryStream,
        IBindCtx* pBindCtx  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="4f275-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f275-106">Parameters</span></span>  
 <span data-ttu-id="4f275-107">"phistorystream"</span><span class="sxs-lookup"><span data-stu-id="4f275-107">pHistoryStream</span></span>  
 <span data-ttu-id="4f275-108">Ein Zeiger auf einen Stream von Verlaufs Informationen.</span><span class="sxs-lookup"><span data-stu-id="4f275-108">A pointer to a stream of history information.</span></span>  
  
 <span data-ttu-id="4f275-109">pbindctx</span><span class="sxs-lookup"><span data-stu-id="4f275-109">pBindCtx</span></span>  
 <span data-ttu-id="4f275-110">Ein Zeiger auf einen Bindungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="4f275-110">A pointer to a bind context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f275-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f275-111">Requirements</span></span>  
 <span data-ttu-id="4f275-112">**Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).</span><span class="sxs-lookup"><span data-stu-id="4f275-112">**Platforms:** See [.NET Framework System Requirements](/dotnet/framework/get-started/system-requirements).</span></span>  
  
 <span data-ttu-id="4f275-113">**DLL**</span><span class="sxs-lookup"><span data-stu-id="4f275-113">**DLL:**</span></span>  
  
 <span data-ttu-id="4f275-114">In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="4f275-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="4f275-115">In den .NET Framework 4 und höher: PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="4f275-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="4f275-116">**.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4f275-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f275-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f275-117">See also</span></span>

- [<span data-ttu-id="4f275-118">WPF – Referenz zur nicht verwalteten API</span><span class="sxs-lookup"><span data-stu-id="4f275-118">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
