---
title: 'Gewusst wie: Binden der Eigenschaften von zwei Steuerelementen'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], binding properties of two controls
- binding properties of two controls [WPF]
- controls [WPF], binding properties of
ms.assetid: 06318fac-6afd-4c7d-a277-6d7ef50f47bc
ms.openlocfilehash: 28b5f65a57fc210f3d405020daa0d75c28b934c8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972448"
---
# <a name="how-to-bind-the-properties-of-two-controls"></a>Gewusst wie: Binden der Eigenschaften von zwei Steuerelementen

In diesem Beispiel wird gezeigt, wie die-Eigenschaft eines instanziierten Steuer Elements mithilfe der-Eigenschaft an die eines anderen gebunden wird <xref:System.Windows.Data.Binding.ElementName%2A> .

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.Controls.Panel.Background%2A> Eigenschaft eines <xref:System.Windows.Controls.Canvas> an die [SelectedItem. Content](xref:System.Windows.Controls.ContentControl.Content%2A) -Eigenschaft einer gebunden wird <xref:System.Windows.Controls.ComboBox> :

[!code-xaml[BindDptoDp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/BindDPtoDP/CS/Window1.xaml#1)]

Bei Rendern dieses Beispiels sieht es folgendermaßen aus:

![Screenshot, der ein Kombinations Feld mit ausgewähltem grünen Wert und einem grünen Quadrat anzeigt](./media/how-to-bind-the-properties-of-two-controls/data-binding-bind-background-canvas.png)

> [!NOTE]
> Die Bindungs Ziel Eigenschaft (in diesem Beispiel die- <xref:System.Windows.Controls.Panel.Background%2A> Eigenschaft) muss eine Abhängigkeits Eigenschaft sein. Weitere Informationen finden Sie unter [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).

## <a name="see-also"></a>Siehe auch

- [Angeben der Bindungs Quelle](how-to-specify-the-binding-source.md)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
