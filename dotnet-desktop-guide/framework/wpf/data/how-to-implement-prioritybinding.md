---
title: 'Gewusst wie: Implementieren von PriorityBinding'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], PriorityBinding class
ms.assetid: d63b65ab-b3e9-4322-9aa8-1450f8d89532
ms.openlocfilehash: 694679183f92c9737bbdb511b4ebd5a4bf2185f1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978136"
---
# <a name="how-to-implement-prioritybinding"></a>Gewusst wie: Implementieren von PriorityBinding

<xref:System.Windows.Data.PriorityBinding> in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] funktioniert durch Angeben einer Liste von Bindungen. Die Liste der Bindungen ist von der höchsten Priorität bis zur niedrigsten Priorität geordnet. Wenn die Bindung mit der höchsten Priorität bei der Verarbeitung einen Wert erfolgreich zurückgibt, ist es nicht erforderlich, die anderen Bindungen in der Liste zu verarbeiten. Dies könnte der Fall sein, wenn die Bewertung mit der höchsten Priorität lange ausgewertet werden muss, wenn die nächsthöhere Priorität, die erfolgreich einen Wert zurückgibt, verwendet wird, bis eine Bindung einer höheren Priorität erfolgreich einen Wert zurückgibt.  
  
## <a name="example"></a>Beispiel  

 Um zu veranschaulichen <xref:System.Windows.Data.PriorityBinding> , wie funktioniert, wurde das- `AsyncDataSource` Objekt mit den folgenden drei Eigenschaften erstellt: `FastDP` , `SlowerDP` und `SlowestDP` .  
  
 Der Get-Accessor von `FastDP` gibt den Wert des `_fastDP` Datenmembers zurück.  
  
 Der Get-Accessor von `SlowerDP` wartet drei Sekunden, bevor er den Wert des `_slowerDP` Datenmembers zurückgibt.  
  
 Der Get-Accessor von `SlowestDP` wartet 5 Sekunden, bevor er den Wert des `_slowestDP` Datenmembers zurückgibt.  
  
> [!NOTE]
> Dieses Beispiel dient ausschließlich Demonstrationszwecken. Die .NET-Richtlinien werden zum Definieren von Eigenschaften empfohlen, die in der Größenordnung langsamer sind als ein Feld Satz. Weitere Informationen finden Sie unter [auswählen zwischen Eigenschaften und Methoden](/previous-versions/dotnet/netframework-4.0/ms229054(v=vs.100)).  
  
 [!code-csharp[PriorityBinding#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PriorityBinding/CSharp/Window1.xaml.cs#1)]
 [!code-vb[PriorityBinding#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PriorityBinding/VisualBasic/AsyncDataSource.vb#1)]  
  
 Die- <xref:System.Windows.Controls.TextBlock.Text%2A> Eigenschaft bindet an die oben genannte `AsyncDS` mithilfe von <xref:System.Windows.Data.PriorityBinding> :  
  
 [!code-xaml[PriorityBinding#2](~/samples/snippets/csharp/VS_Snippets_Wpf/PriorityBinding/CSharp/Window1.xaml#2)]  
  
 Wenn die Bindungs-Engine die- <xref:System.Windows.Data.Binding> Objekte verarbeitet, beginnt Sie mit dem ersten <xref:System.Windows.Data.Binding> , das an die-Eigenschaft gebunden ist `SlowestDP` . Wenn dies <xref:System.Windows.Data.Binding> verarbeitet wird, wird ein Wert nicht erfolgreich zurückgegeben, da er 5 Sekunden lang im Ruhezustand ist, sodass das nächste <xref:System.Windows.Data.Binding> Element verarbeitet wird. Der nächste gibt <xref:System.Windows.Data.Binding> einen Wert nicht erfolgreich zurück, da er drei Sekunden lang im Ruhezustand ist. Die Bindungs-Engine wechselt dann auf das nächste <xref:System.Windows.Data.Binding> Element, das an die- `FastDP` Eigenschaft gebunden ist. Dadurch wird <xref:System.Windows.Data.Binding> der Wert "fast Value" zurückgegeben. Der <xref:System.Windows.Controls.TextBlock> zeigt jetzt den Wert "schneller Wert" an.  
  
 Nach 3 Sekunden gibt die- `SlowerDP` Eigenschaft den Wert "langsamerer Wert" zurück. Der <xref:System.Windows.Controls.TextBlock> zeigt dann den Wert "langsamerer Wert" an.  
  
 Nach 5 Sekunden gibt die- `SlowestDP` Eigenschaft den Wert "Slowest Value" zurück. Diese Bindung hat die höchste Priorität, da Sie zuerst aufgeführt wird. Der <xref:System.Windows.Controls.TextBlock> zeigt jetzt den Wert "Langsamster Wert" an.  
  
 <xref:System.Windows.Data.PriorityBinding>Informationen dazu, was als erfolgreicher Rückgabewert einer Bindung angesehen wird, finden Sie unter.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Data.Binding.IsAsync%2A?displayProperty=nameWithType>
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
