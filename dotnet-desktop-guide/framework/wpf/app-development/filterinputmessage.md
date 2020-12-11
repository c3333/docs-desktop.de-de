---
title: FilterInputMessage
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
- FilterInputMessage method [WPF]
ms.assetid: 4d74c6cf-7d1d-49ff-96c1-231340ce54f5
ms.openlocfilehash: 1453946766e33843ae9e56f7a7f4dbf1678b81b5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976805"
---
# <a name="filterinputmessage"></a>FilterInputMessage
Wird immer dann von "PresentationHost.exe" aufgerufen, wenn eine Meldung empfangen wurde, es sei denn, E_NOTIMPL wurde zurückgegeben.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT FilterInputMessage( [in] MSG* pMsg ) ;  
```  
  
## <a name="parameters"></a>Parameter  
 `pMsg`  
  
 [in] Die WM_INPUT-Meldung, die an das Fenster gesendet wurde, das die unformatierte Eingabe erhält.  
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert  
 HRESULT:  
  
 S_OK – Der Filter hat die Meldung nicht verarbeitet, und weitere Verarbeitungsschritte können folgen.  
  
 S_FALSE – Der Filter hat diese Meldung verarbeitet, und es sollten keine weiteren Verarbeitungsschritte folgen.  
  
 E_NOTIMPL – wenn dieser Wert zurückgegeben wird, wird [filterinputmessage](filterinputmessage.md) nicht erneut aufgerufen. Dieser Wert wird möglicherweise von einer Hostanwendung zurückgegeben, die nur daran interessiert ist, benutzerdefinierte Status- und Fehlerbenutzeroberflächen für "PresentationHost.exe" bereitzustellen, und nicht dafür vorgesehen ist, unformatierte Eingabemeldungen von "PresentationHost.exe" weiterzuleiten.  
  
## <a name="remarks"></a>Bemerkungen  
 "PresentationHost.exe" ist das Ziel von verschiedenen Geräten für unformatierte Eingabe, einschließlich Tastatur, Mäusen und Fernsteuerungen. Manchmal hängt das Verhalten in der Hostanwendung von einer Eingabe ab, die andernfalls von "PresentationHost.exe" verarbeitet werden würde. Beispielsweise kann für eine Hostanwendung das Empfangen bestimmter Eingabemeldungen erforderlich sein, um bestimmen zu können, ob bestimmte Elemente der Benutzeroberfläche angezeigt werden sollen oder nicht.  
  
 Damit die Host Anwendung die erforderlichen Eingabe Nachrichten empfangen kann, um diese Verhaltensweisen zu ermöglichen, leitet PresentationHost.exe entsprechende unformatierte Eingabe Nachrichten an die gehostete Anwendung weiter, indem [filterinputmessage](filterinputmessage.md)aufgerufen wird.  
  
 Die gehostete Anwendung empfängt unformatierte Eingabe Nachrichten, indem Sie sich bei der Gruppe der unformatierten Eingabegeräte (Human [Interface Devices,](getrawinputdevices.md)Personal Interface Devices) registriert.  
  
## <a name="see-also"></a>Siehe auch

- [WM_INPUT Meldung](/windows/desktop/inputdev/wm-input)
