---
title: 'Gewusst wie: Erstellen eines Stils für einen gezogenen GridView-Spaltenheader'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 0b999645-0313-4b33-80b9-19ece08b5459
ms.openlocfilehash: dbcdd38e0397b8e637aff962420a2959f33203df
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977655"
---
# <a name="how-to-create-a-style-for-a-dragged-gridview-column-header"></a>Gewusst wie: Erstellen eines Stils für einen gezogenen GridView-Spaltenheader
In diesem Beispiel wird gezeigt, wie die Darstellung einer gezogenen geändert wird, <xref:System.Windows.Controls.GridViewColumnHeader> Wenn der Benutzer die Position einer Spalte ändert.  
  
## <a name="example"></a>Beispiel  
 Wenn Sie einen Spaltenheader an eine andere Position in einer ziehen, die <xref:System.Windows.Controls.ListView> <xref:System.Windows.Controls.GridView> für den Ansichtsmodus verwendet, wird die Spalte an die neue Position verschoben. Beim Ziehen der Spaltenüberschrift wird zusätzlich zum ursprünglichen Header eine Gleit Komma Kopie der Kopfzeile angezeigt. Eine Spaltenüberschrift in einem <xref:System.Windows.Controls.GridView> wird durch ein- <xref:System.Windows.Controls.GridViewColumnHeader> Objekt dargestellt.  
  
 Um die Darstellung der Gleit Komma-und ursprünglichen Header anzupassen, können Sie festlegen, <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> um zu ändern <xref:System.Windows.Controls.GridViewColumnHeader> <xref:System.Windows.Style> . Diese <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> werden angewendet, wenn der <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> -Eigenschafts Wert `true` und der- <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> Eigenschafts Wert ist <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating> .  
  
 Wenn der Benutzer die Maustaste drückt und die Maustaste gedrückt hält, während der Mauszeiger an der angehalten <xref:System.Windows.Controls.GridViewColumnHeader> wird, ändert sich der <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> Eigenschafts Wert in `true` . Wenn der Benutzer den Zieh Vorgang startet, ändert sich die- <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> Eigenschaft ebenso in <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating> .  
  
 Im folgenden Beispiel wird gezeigt, wie festgelegt wird <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> , um die <xref:System.Windows.Controls.Control.Foreground%2A> <xref:System.Windows.Controls.Control.Background%2A> Farben und der ursprünglichen und gleitenden Header zu ändern, wenn der Benutzer eine Spalte an eine neue Position zieht.  
  
 [!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplatestart)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersstart)]  
[!code-xaml[ListViewHeaderRoleStyle#IsPressed](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#ispressed)]  
[!code-xaml[ListViewHeaderRoleStyle#Floating](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#floating)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersend)]  
[!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplateend)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.GridViewColumnHeader>
- <xref:System.Windows.Controls.GridViewColumnHeaderRole>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
- [Übersicht über ListView](listview-overview.md)
- [Übersicht über GridView](gridview-overview.md)
