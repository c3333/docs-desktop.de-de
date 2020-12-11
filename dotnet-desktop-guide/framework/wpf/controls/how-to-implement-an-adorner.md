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
# <a name="how-to-implement-an-adorner"></a><span data-ttu-id="c6289-102">Gewusst wie: Implementieren eines Adorners</span><span class="sxs-lookup"><span data-stu-id="c6289-102">How to: Implement an Adorner</span></span>
<span data-ttu-id="c6289-103">Dieses Beispiel zeigt eine minimale adornerimplementierung.</span><span class="sxs-lookup"><span data-stu-id="c6289-103">This example shows a minimal adorner implementation.</span></span>  
  
## <a name="notes-for-implementers"></a><span data-ttu-id="c6289-104">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c6289-104">Notes for Implementers</span></span>  
 <span data-ttu-id="c6289-105">Beachten Sie, dass für Adorner kein Renderingverhalten festgelegt ist. Damit wird sichergestellt, dass für das Rendering die Adorner-Implementierung verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="c6289-105">It is important to note that adorners do not include any inherent rendering behavior; ensuring that an adorner renders is the responsibility of the adorner implementer.</span></span>   <span data-ttu-id="c6289-106">Eine gängige Methode zum Implementieren des Renderingverhaltens ist das Überschreiben der <xref:System.Windows.UIElement.OnRender%2A> -Methode und das Verwenden eines oder mehrerer <xref:System.Windows.Media.DrawingContext> -Objekte zum Rendern der visuellen Elemente des Adorners (wie in diesem Beispiel gezeigt).</span><span class="sxs-lookup"><span data-stu-id="c6289-106">A common way of implementing rendering behavior is to override the <xref:System.Windows.UIElement.OnRender%2A> method and use one or more <xref:System.Windows.Media.DrawingContext> objects to render the adorner's visuals as needed (as shown in this example).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c6289-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c6289-107">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="c6289-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6289-108">Description</span></span>  
 <span data-ttu-id="c6289-109">Ein benutzerdefinierter Funktions Indikator wird erstellt, indem eine Klasse implementiert wird, die von der abstrakten-Klasse erbt <xref:System.Windows.Documents.Adorner> .</span><span class="sxs-lookup"><span data-stu-id="c6289-109">A custom adorner is created by implementing a class that inherits from the abstract <xref:System.Windows.Documents.Adorner> class.</span></span>  <span data-ttu-id="c6289-110">Der Beispiel Funktions Indikator zeigt einfach die Ecken eines <xref:System.Windows.UIElement> durch Kreise durch Überschreiben der- <xref:System.Windows.UIElement.OnRender%2A> Methode an.</span><span class="sxs-lookup"><span data-stu-id="c6289-110">The example adorner simply adorns the corners of a <xref:System.Windows.UIElement> with circles by overriding the <xref:System.Windows.UIElement.OnRender%2A> method.</span></span>  
  
### <a name="code"></a><span data-ttu-id="c6289-111">Code</span><span class="sxs-lookup"><span data-stu-id="c6289-111">Code</span></span>  
 [!code-csharp[Adorners_SimpleCircleAdorner#_SimpleCircleAdornerBody](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_simplecircleadornerbody)]
 [!code-vb[Adorners_SimpleCircleAdorner#_SimpleCircleAdornerBody](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_simplecircleadornerbody)]  
  
## <a name="see-also"></a><span data-ttu-id="c6289-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6289-112">See also</span></span>

- [<span data-ttu-id="c6289-113">Übersicht über Adorner</span><span class="sxs-lookup"><span data-stu-id="c6289-113">Adorners Overview</span></span>](adorners-overview.md)
