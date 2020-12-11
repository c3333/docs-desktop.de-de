---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 4fc7a5021f9f8d9e6badcd3e13266fb8f4bfe7a4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976803"
---
# <a name="getrawinputdevices"></a><span data-ttu-id="f4883-102">GetRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="f4883-102">GetRawInputDevices</span></span>
<span data-ttu-id="f4883-103">Ermöglicht es der Datei "PresentationHost.exe", Geräte für die Eingabe von Rohdaten (Eingabegeräte, Human Interface Devices) zu erkennen, die für die Hostanwendung interessant sind.</span><span class="sxs-lookup"><span data-stu-id="f4883-103">Allows PresentationHost.exe to discover the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4883-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4883-104">Syntax</span></span>  
  
```cpp  
HRESULT GetRawInputDevices( [out] IEnumRAWINPUTDEVICE **ppEnum );  
```  
  
## <a name="parameters"></a><span data-ttu-id="f4883-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4883-105">Parameters</span></span>  
 `ppEnum`  
  
 <span data-ttu-id="f4883-106">vorgenommen Ein Zeiger auf ein [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) zum Auflisten der unformatierten Eingabegeräte.</span><span class="sxs-lookup"><span data-stu-id="f4883-106">[out] A pointer to an [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) for enumerating the raw input devices.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f4883-107">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4883-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="f4883-108">HRESULT:</span><span class="sxs-lookup"><span data-stu-id="f4883-108">HRESULT:</span></span>  
  
 <span data-ttu-id="f4883-109">S_OK- [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) wird nur von PresentationHost.exe verwendet, wenn S_OK zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4883-109">S_OK - [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) will only be used by PresentationHost.exe if S_OK is returned.</span></span>  
  
 <span data-ttu-id="f4883-110">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f4883-110">E_NOTIMPL</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f4883-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4883-111">Remarks</span></span>  
 <span data-ttu-id="f4883-112">Eingabegeräte für Rohdaten sind Eingabegeräte wie Tastaturen, Mäuse und weniger verbreitete Geräte wie Fernbedienungen.</span><span class="sxs-lookup"><span data-stu-id="f4883-112">Raw input devices are the set of input devices that includes keyboards, mice, and less traditional devices like remote controls.</span></span>  
  
 <span data-ttu-id="f4883-113">Nachdem die Liste der Eingabegeräte für Rohdaten abgerufen wurde, registriert "PresentationHost.exe" diese Geräte, um WM_INPUT-Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4883-113">Once the list of raw input devices has been retrieved, PresentationHost.exe registers with the devices to receive WM_INPUT notification messages.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4883-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4883-114">See also</span></span>

- [<span data-ttu-id="f4883-115">Getrawinputdevicelist</span><span class="sxs-lookup"><span data-stu-id="f4883-115">GetRawInputDeviceList</span></span>](/windows/desktop/api/winuser/nf-winuser-getrawinputdevicelist)
- [<span data-ttu-id="f4883-116">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="f4883-116">FilterInputMessage</span></span>](filterinputmessage.md)
