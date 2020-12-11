---
title: 'Savetohistory-Funktion: Referenz zur nicht verwalteten WPF-API'
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- SaveToHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: 6dd101a3-44ad-4143-b228-772156f9b8ff
ms.openlocfilehash: f8cd39fce3f9bc41c315d4e19f95fd19d8bf9d93
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977487"
---
# <a name="savetohistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="9ae92-102">Savetohistory-Funktion (Referenz zur nicht verwalteten WPF-API)</span><span class="sxs-lookup"><span data-stu-id="9ae92-102">SaveToHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="9ae92-103">Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="9ae92-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="9ae92-104">Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Windows-Verwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ae92-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ae92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ae92-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveToHistory(  
   __in_ecount(1) IStream* pHistoryStream  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ae92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ae92-106">Parameters</span></span>  
 <span data-ttu-id="9ae92-107">"phistorystream"</span><span class="sxs-lookup"><span data-stu-id="9ae92-107">pHistoryStream</span></span>  
 <span data-ttu-id="9ae92-108">Ein Zeiger auf den Verlaufs Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="9ae92-108">A pointer to the history stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ae92-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ae92-109">Requirements</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ae92-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ae92-110">Requirements</span></span>  
 <span data-ttu-id="9ae92-111">**Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).</span><span class="sxs-lookup"><span data-stu-id="9ae92-111">**Platforms:** See [.NET Framework System Requirements](/dotnet/framework/get-started/system-requirements).</span></span>  
  
 <span data-ttu-id="9ae92-112">**DLL**</span><span class="sxs-lookup"><span data-stu-id="9ae92-112">**DLL:**</span></span>  
  
 <span data-ttu-id="9ae92-113">In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="9ae92-113">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="9ae92-114">In den .NET Framework 4 und höher: PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="9ae92-114">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="9ae92-115">**.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ae92-115">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ae92-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ae92-116">See also</span></span>

- [<span data-ttu-id="9ae92-117">WPF – Referenz zur nicht verwalteten API</span><span class="sxs-lookup"><span data-stu-id="9ae92-117">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
