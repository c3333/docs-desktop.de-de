---
title: 'Gewusst wie: Festlegen der Höhe eines Fensters auf einer Seite'
ms.date: 03/30/2017
helpviewer_keywords:
- windows [WPF], setting height from a page
- pages [WPF], setting window height from
- height of window [WPF], setting from a page
ms.assetid: 4e4488ff-ab5c-4ee9-81a4-e1addb55c5cc
ms.openlocfilehash: c1041af88241011b51c96d7b61423344a32b25ca
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972287"
---
# <a name="how-to-set-the-height-of-a-window-from-a-page"></a>Gewusst wie: Festlegen der Höhe eines Fensters auf einer Seite
In diesem Beispiel wird veranschaulicht, wie die Höhe des Fensters von einem festgelegt wird <xref:System.Windows.Controls.Page> .  
  
## <a name="example"></a>Beispiel  
 Ein <xref:System.Windows.Controls.Page> kann die Höhe des Host Fensters durch Festlegen von festlegen <xref:System.Windows.Controls.Page.WindowHeight%2A> . Diese Eigenschaft ermöglicht es dem <xref:System.Windows.Controls.Page> nicht, explizite Informationen über den Typ des Fensters zu haben, in dem es gehostet wird.  
  
> [!NOTE]
> Um die Höhe eines Fensters mit festzulegen <xref:System.Windows.Controls.Page.WindowHeight%2A> , muss ein untergeordnetes Element eines <xref:System.Windows.Controls.Page> Fensters sein.  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowHeightXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowHeightPage.xaml#setpagewindowheightxaml)]
