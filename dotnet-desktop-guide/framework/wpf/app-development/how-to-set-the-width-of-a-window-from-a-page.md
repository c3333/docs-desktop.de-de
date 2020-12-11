---
title: 'Gewusst wie: Festlegen der Breite eines Fensters auf einer Seite'
ms.date: 03/30/2017
helpviewer_keywords:
- width of windows [WPF], setting from a page
- windows [WPF], setting width from a page
- pages [WPF], setting window width from
ms.assetid: 31601c92-7889-472a-b07e-bf675ad21c92
ms.openlocfilehash: 1e16b75ecb85550facdf24a5b9e341cf0c061178
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972283"
---
# <a name="how-to-set-the-width-of-a-window-from-a-page"></a>Gewusst wie: Festlegen der Breite eines Fensters auf einer Seite
In diesem Beispiel wird veranschaulicht, wie die Breite des Fensters von einem festgelegt wird <xref:System.Windows.Controls.Page> .  
  
## <a name="example"></a>Beispiel  
 Eine <xref:System.Windows.Controls.Page> kann die Breite des Host Fensters durch Festlegen von festlegen <xref:System.Windows.Controls.Page.WindowWidth%2A> . Diese Eigenschaft ermöglicht es dem <xref:System.Windows.Controls.Page> nicht, explizite Informationen über den Typ des Fensters zu haben, in dem es gehostet wird.  
  
> [!NOTE]
> Um die Breite eines Fensters mit festzulegen <xref:System.Windows.Controls.Page.WindowWidth%2A> , muss ein untergeordnetes Element eines <xref:System.Windows.Controls.Page> Fensters sein.  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowWidthXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowWidthPage.xaml#setpagewindowwidthxaml)]
