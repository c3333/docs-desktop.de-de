---
title: 'Vorgehensweise: Suchen von Elementen, die mit einer ControlTemplate generiert wurden'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ControlTemplates [WPF], finding elements
- finding ControlTemplate elements [WPF]
ms.assetid: d7b25447-ceff-4bb4-9be5-fd7c40ef00af
ms.openlocfilehash: 064f70835443accef83ca5f3d912ace861c2216a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975079"
---
# <a name="how-to-find-controltemplate-generated-elements"></a>Vorgehensweise: Suchen von Elementen, die mit einer ControlTemplate generiert wurden
Dieses Beispiel zeigt, wie Sie Elemente finden, die von einem generiert werden <xref:System.Windows.Controls.ControlTemplate> .  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt einen Stil, der eine einfache <xref:System.Windows.Controls.ControlTemplate> für die- <xref:System.Windows.Controls.Button> Klasse erstellt:  
  
 [!code-xaml[FindGeneratedItems#CT](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#ct)]  
  
 Um nach dem Anwenden der Vorlage ein Element innerhalb der Vorlage zu finden, können Sie die- <xref:System.Windows.FrameworkTemplate.FindName%2A> Methode von aufzurufen <xref:System.Windows.Controls.Control.Template%2A> . Im folgenden Beispiel wird ein Meldungs Feld erstellt, in dem der tatsächliche Breitenwert von <xref:System.Windows.Controls.Grid> innerhalb der Steuerelement Vorlage angezeigt wird:  
  
 [!code-csharp[FindGeneratedItems#CTFindElement](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#ctfindelement)]
 [!code-vb[FindGeneratedItems#CTFindElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#ctfindelement)]  
  
## <a name="see-also"></a>Siehe auch

- [Suchen von Elementen, die mit einer DataTemplate generiert wurden](../data/how-to-find-datatemplate-generated-elements.md)
- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [WPF-XAML-Namescopes](../advanced/wpf-xaml-namescopes.md)
- [Strukturen in WPF](../advanced/trees-in-wpf.md)
