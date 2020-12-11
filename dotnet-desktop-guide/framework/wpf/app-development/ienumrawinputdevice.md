---
title: IEnumRAWINPUTDEVICE
ms.date: 03/30/2017
helpviewer_keywords:
- IEnumRAWINPUTDEVICE interface [WPF]
ms.assetid: 88c8b389-a48b-46b9-b895-8ed7b1e26fea
ms.openlocfilehash: 5249d7ea359db5d5c58ae87600f61048b465b4c1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977983"
---
# <a name="ienumrawinputdevice"></a><span data-ttu-id="71cd3-102">IEnumRAWINPUTDEVICE</span><span class="sxs-lookup"><span data-stu-id="71cd3-102">IEnumRAWINPUTDEVICE</span></span>
<span data-ttu-id="71cd3-103">Diese Schnittstelle listet die Geräte für die unformatierte Eingabe auf und wird nur von "PresentationHost.exe" verwendet.</span><span class="sxs-lookup"><span data-stu-id="71cd3-103">This interface enumerates the raw input devices, and is only used by PresentationHost.exe.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="71cd3-104">Diese API ist nur für die Verwendung auf dem lokalen Clientcomputer vorgesehen und wird nur zu diesem Zweck unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71cd3-104">This API is only intended and supported for use on the local client machine</span></span>  
  
## <a name="members"></a><span data-ttu-id="71cd3-105">Member</span><span class="sxs-lookup"><span data-stu-id="71cd3-105">Members</span></span>  
  
|<span data-ttu-id="71cd3-106">Member</span><span class="sxs-lookup"><span data-stu-id="71cd3-106">Member</span></span>|<span data-ttu-id="71cd3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71cd3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="71cd3-108">IEnumRAWINPUTDEVIC:Next</span><span class="sxs-lookup"><span data-stu-id="71cd3-108">IEnumRAWINPUTDEVIC:Next</span></span>](ienumrawinputdevic-next.md)|<span data-ttu-id="71cd3-109">Listet die nächsten `celt`-Elemente (RAWINPUTDEVICE-Strukturen) in der Liste des Enumerators auf, wobei die Rückgabe in `rgelt` zusammen mit der tatsächlichen Anzahl der aufgelisteten Elemente in `pceltFetched` erfolgt.</span><span class="sxs-lookup"><span data-stu-id="71cd3-109">Enumerates the next `celt` elements (that is, RAWINPUTDEVICE structures) in the enumerator's list, returning them in `rgelt` along with the actual number of enumerated elements in `pceltFetched`.</span></span>|  
|[<span data-ttu-id="71cd3-110">IEnumRAWINPUTDEVIC:Skip</span><span class="sxs-lookup"><span data-stu-id="71cd3-110">IEnumRAWINPUTDEVIC:Skip</span></span>](ienumrawinputdevic-skip.md)|<span data-ttu-id="71cd3-111">Weist den Enumerator an, die nächsten `celt` Elemente in der-Enumeration zu überspringen, sodass der nächste [IEnumRAWINPUTDEVIC: Next](ienumrawinputdevic-next.md) -Aufrufe diese Elemente nicht zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="71cd3-111">Instructs the enumerator to skip the next `celt` elements in the enumeration so that the next call to [IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md) will not return those elements.</span></span>|  
|[<span data-ttu-id="71cd3-112">IEnumRAWINPUTDEVIC:Reset</span><span class="sxs-lookup"><span data-stu-id="71cd3-112">IEnumRAWINPUTDEVIC:Reset</span></span>](ienumrawinputdevic-reset.md)|<span data-ttu-id="71cd3-113">Setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="71cd3-113">Resets the enumeration sequence to the beginning.</span></span>|  
|[<span data-ttu-id="71cd3-114">IEnumRAWINPUTDEVIC:Clone</span><span class="sxs-lookup"><span data-stu-id="71cd3-114">IEnumRAWINPUTDEVIC:Clone</span></span>](ienumrawinputdevic-clone.md)|<span data-ttu-id="71cd3-115">Erstellt einen weiteren Enumerator für Geräte für die unformatierte Eingabe, der denselben Zustand wie der aktuelle Enumerator aufweist und dieselbe Liste durchlaufen soll.</span><span class="sxs-lookup"><span data-stu-id="71cd3-115">Creates another raw input device enumerator with the same state as the current enumerator to iterate over the same list.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="71cd3-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71cd3-116">See also</span></span>

- [<span data-ttu-id="71cd3-117">Informationen zu roheingaben</span><span class="sxs-lookup"><span data-stu-id="71cd3-117">About Raw Input</span></span>](/windows/desktop/inputdev/about-raw-input)
