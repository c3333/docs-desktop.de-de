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
# <a name="processunhandledexception-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="085ef-102">Processunprocessdexception-Funktion (Referenz zur nicht verwalteten WPF-API)</span><span class="sxs-lookup"><span data-stu-id="085ef-102">ProcessUnhandledException Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="085ef-103">Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="085ef-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="085ef-104">Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Ausnahmebehandlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="085ef-104">Used by the Windows Presentation Foundation (WPF) infrastructure for exception handling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="085ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="085ef-105">Syntax</span></span>  
  
```cpp  
void __stdcall ProcessUnhandledException(  
   __in_ecount(1) BSTR errorMsg  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="085ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="085ef-106">Parameters</span></span>  
 <span data-ttu-id="085ef-107">ERRORMSG</span><span class="sxs-lookup"><span data-stu-id="085ef-107">errorMsg</span></span>  
 <span data-ttu-id="085ef-108">Die Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="085ef-108">The error message.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="085ef-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="085ef-109">Requirements</span></span>  
 <span data-ttu-id="085ef-110">**Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).</span><span class="sxs-lookup"><span data-stu-id="085ef-110">**Platforms:** See [.NET Framework System Requirements](/dotnet/framework/get-started/system-requirements).</span></span>  
  
 <span data-ttu-id="085ef-111">**DLL**</span><span class="sxs-lookup"><span data-stu-id="085ef-111">**DLL:**</span></span>  
  
 <span data-ttu-id="085ef-112">In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="085ef-112">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="085ef-113">In den .NET Framework 4 und höher: PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="085ef-113">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="085ef-114">**.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="085ef-114">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="085ef-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="085ef-115">See also</span></span>

- [<span data-ttu-id="085ef-116">WPF – Referenz zur nicht verwalteten API</span><span class="sxs-lookup"><span data-stu-id="085ef-116">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
