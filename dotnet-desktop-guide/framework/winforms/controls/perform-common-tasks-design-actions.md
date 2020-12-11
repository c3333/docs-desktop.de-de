---
title: Ausführen allgemeiner Aufgaben mithilfe von Designer Aktionen für Steuerelemente
ms.date: 02/13/2019
helpviewer_keywords:
- designer actions
ms.assetid: cac337e6-00f6-4584-80f4-75728f5ea113
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 342741b9ce032b1b8ec50a6c689d9109d12f5b3b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976231"
---
# <a name="walkthrough-perform-common-tasks-using-designer-actions"></a>Exemplarische Vorgehensweise: Ausführen allgemeiner Aufgaben mit Designaktionen

Wenn Sie Formulare und Steuerelemente für Ihre Windows Forms-Anwendung erstellen, gibt es viele Aufgaben, die Sie wiederholt ausführen. In der folgenden Liste sind einige der häufig ausgeführten Aufgaben aufgeführt, die Sie durchführen werden:

- Hinzufügen oder Entfernen einer Registerkarte auf einem <xref:System.Windows.Forms.TabControl> .
- Andocken eines Steuer Elements an das übergeordnete Element.
- Ändern der Ausrichtung eines <xref:System.Windows.Forms.SplitContainer> Steuer Elements.

Um die Entwicklung zu beschleunigen, bieten viele Steuerelemente Designer Aktionen, bei denen es sich um Kontextbezogene Menüs handelt, mit denen Sie häufige Aufgaben wie diese in einer einzigen Geste zur Entwurfszeit ausführen können. Diese Aufgaben werden als *Designer-Aktions Verben* bezeichnet.

Designer Aktionen bleiben während ihrer Lebensdauer im Designer an eine Steuerelement Instanz angefügt und sind immer verfügbar.

## <a name="create-the-project"></a>Erstellen des Projekts

Im ersten Schritt wird das Projekt erstellt und das Formular eingerichtet.

1. Erstellen Sie in Visual Studio ein Windows-basiertes Anwendungsprojekt mit dem Namen **DesignerAction sexample**.

2. Wählen Sie in der **Windows Forms-Designer** das Formular aus.

## <a name="use-designer-actions"></a>Designer Aktionen verwenden

Designer Aktionen sind immer zur Entwurfszeit für Steuerelemente verfügbar, die Sie bieten.

1. Ziehen <xref:System.Windows.Forms.TabControl> Sie ein aus der **Toolbox** auf das Formular. Beachten Sie das Designer-Aktions Symbol ( ![ kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ), das auf der Seite von angezeigt wird <xref:System.Windows.Forms.TabControl> .

2. Klicken Sie auf das Symbol Designer Aktionen. Wählen Sie im Kontextmenü, das neben dem Symbol angezeigt wird, das Element **Registerkarte hinzufügen** aus. Beachten Sie, dass der eine neue Registerkarte hinzugefügt wird <xref:System.Windows.Forms.TabControl> .

3. Ziehen Sie ein <xref:System.Windows.Forms.TableLayoutPanel> -Steuerelement aus der **Toolbox** auf das Formular.

4. Klicken Sie auf das Symbol Designer Aktionen. Wählen Sie im Kontextmenü, das neben dem Symbol angezeigt wird, das Element **Spalten hinzufügen** aus. Beachten Sie, dass dem Steuerelement eine neue Spalte hinzugefügt wird <xref:System.Windows.Forms.TableLayoutPanel> .

5. Ziehen Sie ein <xref:System.Windows.Forms.SplitContainer> -Steuerelement aus der **Toolbox** auf das Formular.

6. Klicken Sie auf das Symbol Designer Aktionen. Wählen Sie im Kontextmenü, das neben dem Symbol angezeigt wird, das Element **horizontale Splitter Ausrichtung** aus. Beachten Sie, dass die <xref:System.Windows.Forms.SplitContainer> Splitter Leiste des Steuer Elements nun horizontal ausgerichtet ist.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.TextBox>
- <xref:System.Windows.Forms.TabControl>
- <xref:System.Windows.Forms.SplitContainer>
- <xref:System.ComponentModel.Design.DesignerActionList>
