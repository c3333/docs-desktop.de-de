---
title: 'Gewusst wie: Erstellen eines Expanders mit einem ScrollViewer'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], Expander
- ScrollViewer control [WPF], with Expander control
- Expander control [WPF], creating
- controls [WPF], ScrollViewer
ms.assetid: 2ad124d2-2406-4157-aaf2-64e067298f01
ms.openlocfilehash: ef0bc5d344f7d465de9209708430d3e61d40d4f7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977654"
---
# <a name="how-to-create-an-expander-with-a-scrollviewer"></a>Gewusst wie: Erstellen eines Expanders mit einem ScrollViewer
In diesem Beispiel wird gezeigt, wie ein-Steuerelement erstellt <xref:System.Windows.Controls.Expander> wird, das komplexen Inhalt enthält, z. b. ein Bild und Text. Im Beispiel wird auch der Inhalt von <xref:System.Windows.Controls.Expander> in einem-Steuerelement eingeschlossen <xref:System.Windows.Controls.ScrollViewer> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt wird <xref:System.Windows.Controls.Expander> . Das Beispiel verwendet ein <xref:System.Windows.Controls.Primitives.BulletDecorator> -Steuerelement, das ein Bild und Text enthält, um zu definieren <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> . Ein- <xref:System.Windows.Controls.ScrollViewer> Steuerelement stellt eine Methode für den Bildlauf im erweiterten Inhalt bereit.  
  
 Beachten Sie, dass im Beispiel die- <xref:System.Windows.FrameworkElement.Height%2A> Eigenschaft für <xref:System.Windows.Controls.ScrollViewer> anstelle von für den Inhalt festgelegt wird. Wenn <xref:System.Windows.FrameworkElement.Height%2A> für den Inhalt festgelegt ist, kann der <xref:System.Windows.Controls.ScrollViewer> Benutzer nicht durch den Inhalt scrollen. Die- <xref:System.Windows.FrameworkElement.Width%2A> Eigenschaft wird für das-Steuerelement festgelegt <xref:System.Windows.Controls.Expander> , und diese Einstellung gilt für den <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> und den erweiterten Inhalt.  
  
 [!code-xaml[ExpanderRichContent#CreateExpander](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml#createexpander)]  
  
 [!code-csharp[ExpanderRichContent#CreateExpanderCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml.cs#createexpandercode)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Expander>
- [Übersicht über Expander-Steuerelemente](expander-overview.md)
- [Artikel zu Vorgehensweisen](expander-how-to-topics.md)
