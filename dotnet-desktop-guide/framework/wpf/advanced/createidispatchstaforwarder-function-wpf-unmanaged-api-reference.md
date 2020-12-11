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
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="d8ed5-102">Funktion "kreateidispatchstaforwarder" (Referenz zur nicht verwalteten WPF-API)</span><span class="sxs-lookup"><span data-stu-id="d8ed5-102">CreateIDispatchSTAForwarder Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="d8ed5-103">Diese API unterstützt die Windows Presentation Foundation-Infrastruktur (WPF) und ist nicht für die direkte Verwendung im Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="d8ed5-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="d8ed5-104">Wird von der Windows Presentation Foundation (WPF)-Infrastruktur für die Thread-und Windows-Verwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8ed5-104">Used by the Windows Presentation Foundation (WPF) infrastructure for thread and windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8ed5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8ed5-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,
   __deref_out IDispatch **ppForwarder  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="d8ed5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8ed5-106">Parameters</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d8ed5-107">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8ed5-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="d8ed5-108">pdispatchdelegat</span><span class="sxs-lookup"><span data-stu-id="d8ed5-108">pDispatchDelegate</span></span>  
 <span data-ttu-id="d8ed5-109">Ein Zeiger auf eine- `IDispatch` Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d8ed5-109">A pointer to an `IDispatch` interface.</span></span>  
  
 <span data-ttu-id="d8ed5-110">ppforwarder</span><span class="sxs-lookup"><span data-stu-id="d8ed5-110">ppForwarder</span></span>  
 <span data-ttu-id="d8ed5-111">Ein Zeiger auf die Adresse einer `IDispatch` Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d8ed5-111">A pointer to the address of an `IDispatch` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8ed5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8ed5-112">Requirements</span></span>  
 <span data-ttu-id="d8ed5-113">**Plattformen:** Siehe [.NET Framework System Anforderungen](/dotnet/framework/get-started/system-requirements).</span><span class="sxs-lookup"><span data-stu-id="d8ed5-113">**Platforms:** See [.NET Framework System Requirements](/dotnet/framework/get-started/system-requirements).</span></span>  
  
 <span data-ttu-id="d8ed5-114">**DLL**</span><span class="sxs-lookup"><span data-stu-id="d8ed5-114">**DLL:**</span></span>  
  
 <span data-ttu-id="d8ed5-115">In den .NET Framework 3,0 und 3,5: PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="d8ed5-115">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="d8ed5-116">In den .NET Framework 4 und höher: PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="d8ed5-116">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="d8ed5-117">**.NET Framework Version:**[!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8ed5-117">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8ed5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8ed5-118">See also</span></span>

- [<span data-ttu-id="d8ed5-119">WPF – Referenz zur nicht verwalteten API</span><span class="sxs-lookup"><span data-stu-id="d8ed5-119">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
