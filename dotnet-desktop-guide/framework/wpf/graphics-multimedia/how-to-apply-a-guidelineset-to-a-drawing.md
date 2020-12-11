---
title: 'Gewusst wie: Anwenden eines Führungsliniensatzes auf eine Zeichnung'
ms.date: 03/30/2017
helpviewer_keywords:
- GuidelineSet property [WPF], applying to drawings
- graphics [WPF], GuidelineSet property
ms.assetid: 45f3e0b4-8820-45a7-b865-b8ea5b17b0c8
ms.openlocfilehash: 134236c5beca806b747d45f20764cc82ddd8a4e8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977765"
---
# <a name="how-to-apply-a-guidelineset-to-a-drawing"></a>Gewusst wie: Anwenden eines Führungsliniensatzes auf eine Zeichnung
In diesem Beispiel wird gezeigt, wie ein <xref:System.Windows.Media.GuidelineSet> auf einen angewendet wird <xref:System.Windows.Media.DrawingGroup> .  
  
 Die- <xref:System.Windows.Media.DrawingGroup> Klasse ist der einzige Typ von <xref:System.Windows.Media.Drawing> , der über eine-Eigenschaft verfügt <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> . Wenn Sie ein <xref:System.Windows.Media.GuidelineSet> auf einen anderen Typ von anwenden möchten <xref:System.Windows.Media.Drawing> , fügen Sie es einem hinzu, <xref:System.Windows.Media.DrawingGroup> und wenden Sie dann <xref:System.Windows.Media.GuidelineSet> auf den an <xref:System.Windows.Media.DrawingGroup> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden zwei <xref:System.Windows.Media.DrawingGroup> -Objekte erstellt, die fast identisch sind. der einzige Unterschied besteht darin, dass der zweite <xref:System.Windows.Media.DrawingGroup> <xref:System.Windows.Media.GuidelineSet> -Wert und der erste nicht ist.  
  
 Die folgende Abbildung zeigt die Ausgabe des Beispiels. Da der renderingunterschied zwischen den beiden- <xref:System.Windows.Media.DrawingGroup> Objekten so gering ist, werden Teile der Zeichnungen vergrößert.  
  
 ![Eine DrawingGroup mit und ohne ein GuidelineSet](./media/graphicsmm-drawinggroup-guidelineset.png "graphicsmm_drawinggroup_guidelineset")  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupGuidelineSetExample.cs#graphicsmmdrawinggroupguidelinesetexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupGuidelineSetExample.xaml#graphicsmmdrawinggroupguidelinesetexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.GuidelineSet>
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
