---
title: GetCustomUI
ms.date: 03/30/2017
helpviewer_keywords:
- custom error messages [WPF]
ms.assetid: e55180fc-35bb-4f80-a136-772b5eb3e4e5
ms.openlocfilehash: e9ef32912c2afb3c99e46e1e14bb3daa5a2e99af
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976804"
---
# <a name="getcustomui"></a><span data-ttu-id="ded8a-102">GetCustomUI</span><span class="sxs-lookup"><span data-stu-id="ded8a-102">GetCustomUI</span></span>
<span data-ttu-id="ded8a-103">Wird von PresentationHost.exe aufgerufen, um beim implementieren benutzerdefinierte Status-und Fehlermeldungen vom Host zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ded8a-103">Called by PresentationHost.exe to get custom progress and error messages from the host, if implemented.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ded8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded8a-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCustomUI( [out] BSTR* pwzProgressAssemblyName, [out] BSTR* pwzProgressClassName, [out] BSTR* pwzErrorAssemblyName, [out] BSTR* pwzErrorClassName );  
```  
  
## <a name="parameters"></a><span data-ttu-id="ded8a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ded8a-105">Parameters</span></span>  
 `pwzProgressAssemblyName`  
  
 <span data-ttu-id="ded8a-106">vorgenommen Ein Zeiger auf die Assembly, die die vom Host bereitgestellte Status-Benutzeroberfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="ded8a-106">[out] A pointer to the assembly that contains the host-supplied progress user interface.</span></span>  
  
 `pwzProgressClassName`  
  
 <span data-ttu-id="ded8a-107">vorgenommen Der Name der Klasse, die die vom Host bereitgestellte Status-Benutzeroberfläche ist, vorzugsweise eine XAML-Datei mit dem <xref:System.Windows.Controls.Page> Element der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="ded8a-107">[out] The name of the class that is the host-supplied progress user interface, preferably a XAML file with <xref:System.Windows.Controls.Page> is its top-level element.</span></span> <span data-ttu-id="ded8a-108">Diese Klasse befindet sich in der Assembly, die von angegeben wird `pwzProgressAssemblyName` .</span><span class="sxs-lookup"><span data-stu-id="ded8a-108">This class resides in the assembly that is specified by `pwzProgressAssemblyName`.</span></span>  
  
 `pwzErrorAssemblyName`  
  
 <span data-ttu-id="ded8a-109">vorgenommen Ein Zeiger auf die Assembly, die die vom Host bereitgestellte Fehler Benutzeroberfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="ded8a-109">[out] A pointer to the assembly that contains the host-supplied error user interface.</span></span>  
  
 `pwzErrorClassName`  
  
 <span data-ttu-id="ded8a-110">vorgenommen Der Name der Klasse, die die vom Host bereitgestellte Fehler Benutzeroberfläche ist, vorzugsweise eine XAML-Datei mit dem <xref:System.Windows.Controls.Page> Element der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="ded8a-110">[out] The name of the class that is the host-supplied error user interface, preferably a XAML file with <xref:System.Windows.Controls.Page> is its top-level element.</span></span> <span data-ttu-id="ded8a-111">Diese Klasse befindet sich in der Assembly, die von angegeben wird `pwzErrorAssemblyName` .</span><span class="sxs-lookup"><span data-stu-id="ded8a-111">This class resides in the assembly that is specified by `pwzErrorAssemblyName`.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ded8a-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ded8a-112">Property Value/Return Value</span></span>  
 <span data-ttu-id="ded8a-113">HRESULT: wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ded8a-113">HRESULT: Ignored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ded8a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ded8a-114">Remarks</span></span>  
 <span data-ttu-id="ded8a-115">Eine Host Anwendung kann über ein bestimmtes Design verfügen, das PresentationHost.exe der Standardbenutzer Oberflächen möglicherweise nicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="ded8a-115">A host application may have a specific theme that PresentationHost.exe’s default user interfaces may not conform to.</span></span> <span data-ttu-id="ded8a-116">Wenn dies der Fall ist, kann die Host Anwendung [GetCustomUI](getcustomui.md) implementieren, um den Fortschritt und Fehler Benutzerschnittstellen an PresentationHost.exe zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ded8a-116">If this is the case, the host application can implement [GetCustomUI](getcustomui.md) to return progress and error user interfaces to PresentationHost.exe.</span></span> <span data-ttu-id="ded8a-117">PresentationHost.exe wird immer [GetCustomUI](getcustomui.md) aufrufen, bevor die Standardbenutzer Oberflächen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ded8a-117">PresentationHost.exe will always call [GetCustomUI](getcustomui.md) before using its default user interfaces.</span></span>  
  
 <span data-ttu-id="ded8a-118">Diese Funktion wird während der PresentationHost-Initialisierung einmal aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ded8a-118">This function is called once during PresentationHost’s initialization.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ded8a-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ded8a-119">See also</span></span>

- [<span data-ttu-id="ded8a-120">IWpfHostSupport</span><span class="sxs-lookup"><span data-stu-id="ded8a-120">IWpfHostSupport</span></span>](iwpfhostsupport.md)
