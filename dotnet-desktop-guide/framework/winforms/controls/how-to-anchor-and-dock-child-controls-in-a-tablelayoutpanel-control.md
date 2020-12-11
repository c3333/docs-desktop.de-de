---
title: 'Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.AnchorDock
helpviewer_keywords:
- layout [Windows Forms], child controls
- controls [Windows Forms], child
- child controls [Windows Forms], anchoring and docking
- TableLayoutPanel control [Windows Forms], child controls
ms.assetid: 0d267c35-25f1-49b8-8976-c64e8f0ddc0b
ms.openlocfilehash: 0e565b56c31d0776f6e89bbbe0b0681ae184758e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975739"
---
# <a name="how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control"></a>Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement
Das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement unterstützt die Eigenschaften <xref:System.Windows.Forms.Control.Anchor%2A> und <xref:System.Windows.Forms.Control.Dock%2A> in seinen untergeordneten Steuerelementen.  
  
### <a name="to-align-a-child-control-in-a-tablelayoutpanel-cell"></a>So richten Sie ein untergeordnetes Steuerelement in einer TableLayoutPanel-Zelle aus  
  
1. Erstellen Sie ein <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement auf dem Formular.  
  
2. Legen Sie den Wert der <xref:System.Windows.Forms.TableLayoutPanel> -und-Eigenschaften des-Steuer Elements <xref:System.Windows.Forms.TableLayoutPanel.ColumnCount%2A> <xref:System.Windows.Forms.TableLayoutPanel.RowCount%2A> auf **1** fest.  
  
3. Erstellen Sie ein <xref:System.Windows.Forms.Button>-Steuerelement im <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement. Das <xref:System.Windows.Forms.Button> nimmt die obere linke Ecke der Zelle ein.  
  
4. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Anchor%2A> -Steuerelements in `Left`. Das <xref:System.Windows.Forms.Button>-Steuerelement wird so verschoben, dass es sich am linken Rand der Zelle ausrichtet.  
  
    > [!NOTE]
    > Dieses Verhalten weicht vom Verhalten anderer Containersteuerelemente ab. Bei anderen Containersteuerelementen wird das untergeordnete Steuerelement nicht verschoben, wenn die <xref:System.Windows.Forms.Control.Anchor%2A>-Eigenschaft festgelegt wird, und der Abstand zwischen dem verankerten Steuerelement und der Grenze des übergeordneten Containers ist zum Zeitpunkt der Festlegung der <xref:System.Windows.Forms.Control.Anchor%2A>-Eigenschaft fixiert.  
  
5. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Anchor%2A> -Steuerelements in `Top, Left`. Das <xref:System.Windows.Forms.Button>-Steuerelement wird so verschoben, dass es die ober linke Ecke der Zelle einnimmt.  
  
6. Wiederholen Sie Schritt 5 mit dem Wert `Top, Right` , um das <xref:System.Windows.Forms.Button> Steuerelement in die obere rechte Ecke der Zelle zu verschieben. Wiederholen Sie diesen Schritt mit den Werten `Bottom, Left` und `Bottom, Right`.  
  
### <a name="to-stretch-a-child-control-in-a-tablelayoutpanel-cell"></a>So strecken Sie ein untergeordnetes Steuerelement in einer TableLayoutPanel-Zelle  
  
1. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Anchor%2A> -Steuerelements in `Left, Right`. Die Größe des <xref:System.Windows.Forms.Button>-Steuerelements wird so angepasst, dass es die gesamte Breite der Zelle einnimmt.  
  
    > [!NOTE]
    > Dieses Verhalten weicht vom Verhalten anderer Containersteuerelemente ab. In anderen Container Steuerelementen wird die Größe des untergeordneten Steuer Elements nicht geändert, wenn die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft auf oder festgelegt ist `Left, Right` `Top, Bottom` .  
  
2. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Anchor%2A> -Steuerelements in `Top, Bottom`. Die Größe des <xref:System.Windows.Forms.Button>-Steuerelements wird so angepasst, dass es die gesamte Höhe der Zelle einnimmt.  
  
3. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Anchor%2A> -Steuerelements in `Top, Bottom, Left, Right`. Die Größe des <xref:System.Windows.Forms.Button>-Steuerelements wird so geändert, dass es die gesamte Zelle ausfüllt.  
  
4. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Anchor%2A> -Steuerelements in `None`. Die Größe des <xref:System.Windows.Forms.Button>-Steuerelements wird geändert, und es wird mittig in der Zelle positioniert.  
  
5. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Dock%2A> -Steuerelements in <xref:System.Windows.Forms.DockStyle.Left>. Das <xref:System.Windows.Forms.Button>-Steuerelement wird so verschoben, dass es sich am linken Rand der Zelle ausrichtet. Das <xref:System.Windows.Forms.Button>-Steuerelement behält seine Breite, aber seine Höhe wird so angepasst, dass es die gesamte Zellenhöhe einnimmt.  
  
    > [!NOTE]
    > Dies ist dasselbe Verhalten, das in anderen Containersteuerelementen auftritt.  
  
6. Ändern Sie den Wert der <xref:System.Windows.Forms.Button> -Eigenschaft des <xref:System.Windows.Forms.Control.Dock%2A> -Steuerelements in <xref:System.Windows.Forms.DockStyle.Fill>. Die Größe des <xref:System.Windows.Forms.Button>-Steuerelements wird so geändert, dass es die gesamte Zelle ausfüllt.  
  
## <a name="example"></a>Beispiel  
 Die folgende Abbildung zeigt fünf Schaltflächen, die in fünf separaten <xref:System.Windows.Forms.TableLayoutPanel>-Zellen verankert sind.  
  
 ![TableLayoutPanel-Verankerung](./media/vs-tlpanchor.gif "VS_TLPanchor")  
  
 Die folgende Abbildung zeigt vier Schaltflächen, die in den Ecken von vier separaten <xref:System.Windows.Forms.TableLayoutPanel>-Zellen verankert sind.  
  
 ![TableLayoutPanel-Verankerung](./media/vs-tlpanchor2.gif "VS_TLPanchor2")  
  
 Die folgende Abbildung zeigt drei Schaltflächen, die durch die Verankerung in drei separaten <xref:System.Windows.Forms.TableLayoutPanel>-Zellen gestreckt wurden.  
  
 ![TableLayoutPanel-Verankerung](./media/vs-tlpanchor3.gif "VS_TLPAnchor3")  
  
 Das folgende Codebeispiel veranschaulicht alle Kombinationen aus <xref:System.Windows.Forms.Control.Anchor%2A>-Eigenschaftswerte für ein <xref:System.Windows.Forms.Button>-Steuerelement in einem <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement.  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.AnchorExampleForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.AnchorExampleForm/CS/TlpAnchorExampleForm.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.AnchorExampleForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.AnchorExampleForm/VB/TlpAnchorExampleForm.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System", "System.Data", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.TableLayoutPanel>
- [TableLayoutPanel-Steuerelement](tablelayoutpanel-control-windows-forms.md)
