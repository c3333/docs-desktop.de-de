---
title: 'Gewusst wie: Formatieren von Steuerelementen auf einer Symbolleiste'
ms.date: 03/30/2017
helpviewer_keywords:
- styling controls on toolbar [WPF]
- toolbars [WPF]
- customizing controls on toolbar [WPF]
ms.assetid: ba6ae056-d6a9-4c24-90f8-467ab0bc0b1a
ms.openlocfilehash: 22d3375b1177e13a1673e9720c1c241d7d3bfa08
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974664"
---
# <a name="how-to-style-controls-on-a-toolbar"></a>Gewusst wie: Formatieren von Steuerelementen auf einer Symbolleiste
<xref:System.Windows.Controls.ToolBar>Definiert <xref:System.Windows.ResourceKey> Objekte, um den Stil der Steuerelemente in anzugeben <xref:System.Windows.Controls.ToolBar> .  Wenn Sie ein Steuerelement in einem formatieren möchten <xref:System.Windows.Controls.ToolBar> , legen Sie das- `x:key` Attribut des-Stils auf einen <xref:System.Windows.ResourceKey> in definierten fest <xref:System.Windows.Controls.ToolBar> .  
  
 <xref:System.Windows.Controls.ToolBar>Definiert die folgenden <xref:System.Windows.ResourceKey> Objekte:  
  
- <xref:System.Windows.Controls.ToolBar.ButtonStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.CheckBoxStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.ComboBoxStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.MenuStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.RadioButtonStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.SeparatorStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.TextBoxStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.ToggleButtonStyleKey%2A>  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden Stile für die Steuerelemente in einem definiert <xref:System.Windows.Controls.ToolBar> .  
  
 [!code-xaml[ToolBar_snip#ToolBarAllStyles](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbarallstyles)]  
[!code-xaml[ToolBar_snip#ToolBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbar)]  
  
## <a name="see-also"></a>Siehe auch

- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
