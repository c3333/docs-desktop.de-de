---
title: Übersicht über das ToolBar-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- ToolBar
helpviewer_keywords:
- toolbars [Windows Forms], about toolbars
- ToolBar control [Windows Forms], about ToolBar controls
ms.assetid: d426b203-0216-4dbe-b834-1641e50a9c29
ms.openlocfilehash: f364e052258703331496f8103b48953a90aa3a9b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976206"
---
# <a name="toolbar-control-overview-windows-forms"></a>Übersicht über das ToolBar-Steuerelement (Windows Forms)
> [!NOTE]
> Obwohl das <xref:System.Windows.Forms.ToolStrip>-Steuerelement das <xref:System.Windows.Forms.ToolBar>-Steuerelement ersetzt und funktionell erweitert, wird das <xref:System.Windows.Forms.ToolBar>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten.  
  
 Das <xref:System.Windows.Forms.ToolBar>-Steuerelement von Windows Forms wird in Formularen als eine Steuerleiste verwendet, auf der eine Zeile aus Dropdownmenüs und Bitmapschaltflächen angezeigt wird, die Befehle aktivieren. Daher kann ein Klicken auf eine Symbolleistenschaltfläche mit dem Auswählen eines Menübefehls identisch sein. Die Schaltflächen können so konfiguriert werden, dass sie so angezeigt werden und sich so verhalten wie Schaltflächen, Dropdownmenüs oder Trennzeichen. In der Regel enthält eine Symbolleiste Schaltflächen und Menüs, die Elementen in der Menüstruktur einer Anwendung entsprechen. Dadurch wird schneller Zugriff auf die am häufigsten verwendeten Funktionen und Befehle einer Anwendung ermöglicht.  
  
## <a name="working-with-the-toolbar-control"></a>Arbeiten mit dem ToolBar-Steuerelement  
 Ein <xref:System.Windows.Forms.ToolBar> Steuerelement wird in der Regel am oberen Rand des übergeordneten Fensters "angedockt", aber es kann auch an eine beliebige Seite des Fensters angedockt werden. Eine Symbolleiste kann QuickInfos anzeigen, wenn der Benutzer mit dem Mauszeiger auf eine Schaltfläche der Symbolleiste zeigt. QuickInfos sind kleine Popupfenster, die den Zweck der Schaltfläche oder des Menüs kurz beschreiben. Um Quick Infos anzuzeigen, muss die- <xref:System.Windows.Forms.ToolBar.ShowToolTips%2A> Eigenschaft auf festgelegt werden `true` .  
  
> [!NOTE]
> Bestimmte Anwendungen verfügen über mit der Symbolleiste vergleichbare Steuerelemente, die über dem Anwendungsfenster „gleiten“ und neu positioniert werden können. Das Windows Forms-Steuerelement „ToolBar“ kann diese Aktionen nicht ausführen.  
  
 Wenn die <xref:System.Windows.Forms.ToolBar.Appearance%2A> -Eigenschaft auf festgelegt ist <xref:System.Windows.Forms.ToolBarAppearance> , werden die Schaltflächen der Symbolleiste ausgelöst und dreidimensional angezeigt. Sie können die <xref:System.Windows.Forms.ToolBar.Appearance%2A> -Eigenschaft der Symbolleiste auf festlegen <xref:System.Windows.Forms.ToolBarAppearance> , um der Symbolleiste und deren Schaltflächen ein flaches aussehen zu verschaffen. Wenn der Mauszeiger über eine flache Schaltfläche bewegt wird, wird die Schaltfläche dreidimensional dargestellt. Symbolleistenschaltflächen können mithilfe von Trennzeichen in logische Gruppen eingeteilt werden. Ein Trennzeichen ist eine Symbolleisten-Schaltfläche, auf die die- <xref:System.Windows.Forms.ToolBarButton.Style%2A> Eigenschaft festgelegt <xref:System.Windows.Forms.ToolBarButtonStyle> Es wird als leerer Zwischenraum auf der Symbolleiste dargestellt. Wenn die Symbolleiste flach dargestellt wird, werden die Trennlinien als Linien und nicht als Zwischenraum zwischen den Schaltflächen dargestellt.  
  
 Mit dem- <xref:System.Windows.Forms.ToolBar> Steuerelement können Sie Symbolleisten erstellen, indem Sie einer Auflistung Objekte hinzufügen <xref:System.Windows.Forms.Button> <xref:System.Windows.Forms.ToolBar.Buttons%2A> . Mit dem Auflistungs-Editor können Sie einem Steuerelement Schaltflächen hinzufügen <xref:System.Windows.Forms.ToolBar> <xref:System.Windows.Forms.Button> . jedem Objekt muss Text oder ein Bild zugewiesen sein. Sie können jedoch beides zuweisen. Das Bild wird von einer verknüpften [ImageList](imagelist-component-windows-forms.md)-Komponente zur Verfügung gestellt. Zur Laufzeit können Sie <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection> mithilfe der <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection.Add%2A> -Methode und der-Methode Schaltflächen hinzufügen oder entfernen <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection.Remove%2A> . Um die Schaltflächen eines zu programmieren <xref:System.Windows.Forms.ToolBar> , fügen Sie den <xref:System.Windows.Forms.ToolBar.ButtonClick> Ereignissen des Code hinzu <xref:System.Windows.Forms.ToolBar> , indem Sie die- <xref:System.Windows.Forms.ToolBarButtonClickEventArgs.Button%2A> Eigenschaft der-Klasse verwenden, <xref:System.Windows.Forms.ToolBarButtonClickEventArgs> um zu bestimmen, auf welche Schaltfläche geklickt wurde.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolBar>
- [ToolBar-Steuerelement](toolbar-control-windows-forms.md)
- [Vorgehensweise: Hinzufügen von Schaltflächen zu einem ToolBar-Steuerelement](how-to-add-buttons-to-a-toolbar-control.md)
- [Vorgehensweise: Definieren eines Symbols für eine Symbolleistenschaltfläche](how-to-define-an-icon-for-a-toolbar-button.md)
- [Vorgehensweise: Auslösen von Menüereignissen für Symbolleistenschaltflächen](how-to-trigger-menu-events-for-toolbar-buttons.md)
