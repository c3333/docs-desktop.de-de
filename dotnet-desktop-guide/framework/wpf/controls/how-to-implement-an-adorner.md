---
title: 'Gewusst wie: Implementieren eines Adorners'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], implementing
ms.assetid: 56ae32b6-0599-455c-b52f-2ff97e6f1ec2
ms.openlocfilehash: da318fee42b4628351217774de2a2225cfb21ee1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976908"
---
# <a name="how-to-implement-an-adorner"></a>Gewusst wie: Implementieren eines Adorners
Dieses Beispiel zeigt eine minimale adornerimplementierung.  
  
## <a name="notes-for-implementers"></a>Hinweise für Implementierer  
 Beachten Sie, dass für Adorner kein Renderingverhalten festgelegt ist. Damit wird sichergestellt, dass für das Rendering die Adorner-Implementierung verantwortlich ist.   Eine gängige Methode zum Implementieren des Renderingverhaltens ist das Überschreiben der <xref:System.Windows.UIElement.OnRender%2A> -Methode und das Verwenden eines oder mehrerer <xref:System.Windows.Media.DrawingContext> -Objekte zum Rendern der visuellen Elemente des Adorners (wie in diesem Beispiel gezeigt).  
  
## <a name="example"></a>Beispiel  
  
### <a name="description"></a>BESCHREIBUNG  
 Ein benutzerdefinierter Funktions Indikator wird erstellt, indem eine Klasse implementiert wird, die von der abstrakten-Klasse erbt <xref:System.Windows.Documents.Adorner> .  Der Beispiel Funktions Indikator zeigt einfach die Ecken eines <xref:System.Windows.UIElement> durch Kreise durch Überschreiben der- <xref:System.Windows.UIElement.OnRender%2A> Methode an.  
  
### <a name="code"></a>Code  
 [!code-csharp[Adorners_SimpleCircleAdorner#_SimpleCircleAdornerBody](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_simplecircleadornerbody)]
 [!code-vb[Adorners_SimpleCircleAdorner#_SimpleCircleAdornerBody](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_simplecircleadornerbody)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Adorner](adorners-overview.md)
