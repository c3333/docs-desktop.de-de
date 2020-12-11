---
title: 'Gewusst wie: Verzieren der untergeordneten Elemente eines Bereichs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], binding to children of Panels
- Panel control [WPF], binding adorners to children
ms.assetid: 4cc9b972-b472-4e5c-bdf3-3702d7fbb1f5
ms.openlocfilehash: 4c5ac537bfd68e9c43583758047b2ec378d0bb57
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977040"
---
# <a name="how-to-adorn-the-children-of-a-panel"></a>Gewusst wie: Verzieren der untergeordneten Elemente eines Bereichs
In diesem Beispiel wird gezeigt, wie ein Funktions Indikator Programm gesteuert an die untergeordneten Elemente eines angegebenen gebunden wird <xref:System.Windows.Controls.Panel> .  
  
## <a name="example"></a>Beispiel  
 Führen Sie die folgenden Schritte aus, um einen Funktions Indikator an die untergeordneten Elemente eines zu binden <xref:System.Windows.Controls.Panel> :  
  
1. Deklarieren Sie ein neues <xref:System.Windows.Documents.AdornerLayer> -Objekt, und rufen Sie die- `static` <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> Methode auf, um eine Adornerebene für das Element zu finden, dessen untergeordnete Elemente geschmückt werden  
  
2. Listet die untergeordneten Elemente des übergeordneten Elements auf und ruft die- <xref:System.Windows.Documents.AdornerLayer.Add%2A> Methode auf, um einen Funktions Indikator an jedes untergeordnete Element zu binden.  
  
 Im folgenden Beispiel wird ein SimpleCircleAdorner (siehe oben) an die untergeordneten Elemente eines <xref:System.Windows.Controls.StackPanel> namens *myStackPanel* gebunden.  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornChildren](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornchildren)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornChildren](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornchildren)]  
  
> [!NOTE]
> Das Binden von Adornern an andere Elemente mit [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] wird derzeit nicht unterstützt.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Adorner](adorners-overview.md)
