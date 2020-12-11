---
title: 'Gewusst wie: Binden eines Adorners an ein Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UIElements [WPF], binding adorners to
- adorners [WPF], binding to specified UIElements
ms.assetid: b2101611-a0ee-4137-bdb8-9b3673d2e6b9
ms.openlocfilehash: 951643602b09a522d23a6449aefa4be41e051a40
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976990"
---
# <a name="how-to-bind-an-adorner-to-an-element"></a>Gewusst wie: Binden eines Adorners an ein Element
In diesem Beispiel wird gezeigt, wie ein Funktions Indikator Programm gesteuert an eine angegebene gebunden wird <xref:System.Windows.UIElement> .  
  
## <a name="example"></a>Beispiel  
 Führen Sie die folgenden Schritte aus, um einen Funktions Indikator an einen bestimmten zu binden <xref:System.Windows.UIElement> :  
  
1. Ruft die- `static` Methode <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> auf, um ein-Objekt zu erhalten, <xref:System.Windows.Documents.AdornerLayer> das <xref:System.Windows.UIElement> zu schmücken ist. <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> durchläuft die visuelle Struktur, beginnend beim angegebenen **UIElement**, und gibt die erste gefundene Adornerebene zurück. (Falls keine Adorner-Ebenen gefunden werden, gibt die Methode NULL zurück.)  
  
2. Ruft die- <xref:System.Windows.Documents.AdornerLayer.Add%2A> Methode auf, um den Funktions Indikator an das **UIElement**-Ziel zu binden.  
  
 Im folgenden Beispiel wird ein SimpleCircleAdorner (siehe oben) an ein <xref:System.Windows.Controls.TextBox> benanntes *MyTextBox*-Element gebunden.  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornsingleelement)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornsingleelement)]  
  
> [!NOTE]
> Das Binden von Adornern an andere Elemente mit [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] wird derzeit nicht unterstützt.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Adorner](adorners-overview.md)
