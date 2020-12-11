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
# <a name="getcustomui"></a>GetCustomUI
Wird von PresentationHost.exe aufgerufen, um beim implementieren benutzerdefinierte Status-und Fehlermeldungen vom Host zu erhalten.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT GetCustomUI( [out] BSTR* pwzProgressAssemblyName, [out] BSTR* pwzProgressClassName, [out] BSTR* pwzErrorAssemblyName, [out] BSTR* pwzErrorClassName );  
```  
  
## <a name="parameters"></a>Parameter  
 `pwzProgressAssemblyName`  
  
 vorgenommen Ein Zeiger auf die Assembly, die die vom Host bereitgestellte Status-Benutzeroberfläche enthält.  
  
 `pwzProgressClassName`  
  
 vorgenommen Der Name der Klasse, die die vom Host bereitgestellte Status-Benutzeroberfläche ist, vorzugsweise eine XAML-Datei mit dem <xref:System.Windows.Controls.Page> Element der obersten Ebene. Diese Klasse befindet sich in der Assembly, die von angegeben wird `pwzProgressAssemblyName` .  
  
 `pwzErrorAssemblyName`  
  
 vorgenommen Ein Zeiger auf die Assembly, die die vom Host bereitgestellte Fehler Benutzeroberfläche enthält.  
  
 `pwzErrorClassName`  
  
 vorgenommen Der Name der Klasse, die die vom Host bereitgestellte Fehler Benutzeroberfläche ist, vorzugsweise eine XAML-Datei mit dem <xref:System.Windows.Controls.Page> Element der obersten Ebene. Diese Klasse befindet sich in der Assembly, die von angegeben wird `pwzErrorAssemblyName` .  
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert  
 HRESULT: wird ignoriert.  
  
## <a name="remarks"></a>Bemerkungen  
 Eine Host Anwendung kann über ein bestimmtes Design verfügen, das PresentationHost.exe der Standardbenutzer Oberflächen möglicherweise nicht entspricht. Wenn dies der Fall ist, kann die Host Anwendung [GetCustomUI](getcustomui.md) implementieren, um den Fortschritt und Fehler Benutzerschnittstellen an PresentationHost.exe zurückzugeben. PresentationHost.exe wird immer [GetCustomUI](getcustomui.md) aufrufen, bevor die Standardbenutzer Oberflächen verwendet werden.  
  
 Diese Funktion wird während der PresentationHost-Initialisierung einmal aufgerufen.  
  
## <a name="see-also"></a>Siehe auch

- [IWpfHostSupport](iwpfhostsupport.md)
