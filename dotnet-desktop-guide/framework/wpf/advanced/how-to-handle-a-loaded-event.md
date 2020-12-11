---
title: 'Gewusst wie: Behandeln eines geladenen Ereignisses'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- XAML [WPF], Loaded events
- events [WPF], Loaded
- Loaded events [WPF]
ms.assetid: 0cf8d003-8441-4df4-807a-6db09347e829
ms.openlocfilehash: 7ca95e195792f8fb4789c481e84dda51f2910434
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976286"
---
# <a name="how-to-handle-a-loaded-event"></a>Gewusst wie: Behandeln eines geladenen Ereignisses
Dieses Beispiel zeigt, wie das <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> -Ereignis und ein entsprechendes Szenario für die Behandlung dieses Ereignisses behandelt werden. Der Handler erstellt eine, <xref:System.Windows.Controls.Button> Wenn die Seite geladen wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] in Verbindung mit einer Code Behind-Datei verwendet.  
  
 [!code-xaml[FELoaded#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FELoaded#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml.cs#handler)]
 [!code-vb[FELoaded#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FELoaded/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.FrameworkElement>
- [Objektlebensdauer-Ereignisse](object-lifetime-events.md)
- [Übersicht über Routingereignisse](routed-events-overview.md)
- [Artikel zu Vorgehensweisen](base-elements-how-to-topics.md)
