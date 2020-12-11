---
title: 'Gewusst wie: Festlegen des Titels eines Fensters auf einer Seite'
ms.date: 03/30/2017
helpviewer_keywords:
- windows [WPF], setting title from a page
- title of window [WPF], setting from a page
- pages [WPF], setting window title from
ms.assetid: fecf0d19-3eb6-4f8c-a44f-ff1b6f2b34b3
ms.openlocfilehash: 0f618af89965822b0df96a264997dabd9cae7608
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972284"
---
# <a name="how-to-set-the-title-of-a-window-from-a-page"></a>Gewusst wie: Festlegen des Titels eines Fensters auf einer Seite
Dieses Beispiel zeigt, wie Sie den Titel des Fensters festlegen, in dem ein <xref:System.Windows.Controls.Page> gehostet wird.  
  
## <a name="example"></a>Beispiel  
 Eine Seite kann den Titel des Fensters, in dem Sie gehostet wird, ändern, indem die-Eigenschaft wie folgt festgelegt wird <xref:System.Windows.Controls.Page.WindowTitle%2A> :  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowTitleXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowTitlePage.xaml#setpagewindowtitlexaml)]  
  
> [!NOTE]
> Wenn Sie die- <xref:System.Windows.Controls.Page.Title%2A> Eigenschaft einer Seite festlegen, wird der Wert des Fenster Titels nicht geändert. Stattdessen <xref:System.Windows.Controls.Page.Title%2A> gibt den Namen eines Seiten Eintrags im Navigationsverlauf an.
