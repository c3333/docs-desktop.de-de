---
title: 'Vorgehensweise: Definieren des Verhaltens bei Größen- und Positionsänderungen in einem geteilten Fenster'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- split windows [Windows Forms], resizing
- splitter windows [Windows Forms], resizing
- SplitContainer control [Windows Forms], resizing
ms.assetid: 9bf73f36-ed2d-4a02-b15a-0770eff4fdfa
ms.openlocfilehash: 8cdcfdfaa135a92ed6a6e96d4a72de2c97f2493d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975678"
---
# <a name="how-to-define-resize-and-positioning-behavior-in-a-split-window"></a>Vorgehensweise: Definieren des Verhaltens bei Größen- und Positionsänderungen in einem geteilten Fenster
Die Bereiche des <xref:System.Windows.Forms.SplitContainer> Steuer Elements eignen sich gut für die Größenänderung und Bearbeitung durch Benutzer. Es gibt jedoch Zeiten, in denen Sie den Splitter Programm gesteuert steuern möchten – wo er positioniert ist und zu welchem Grad er verschoben werden kann.  
  
 Mit der <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> -Eigenschaft und den anderen Eigenschaften des- <xref:System.Windows.Forms.SplitContainer> Steuer Elements können Sie das Verhalten ihrer Benutzeroberfläche genau an Ihre Anforderungen anpassen. Diese Eigenschaften sind in der folgenden Tabelle aufgeführt.  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|<xref:System.Windows.Forms.SplitContainer.IsSplitterFixed%2A> -Eigenschaft|Bestimmt, ob der Splitter mithilfe der Tastatur oder der Maus verschoben werden kann.|  
|<xref:System.Windows.Forms.SplitContainer.SplitterDistance%2A> -Eigenschaft|Bestimmt den Abstand vom linken oder oberen Rand bis zur verschiebbaren Splitter Leiste in Pixel.|  
|<xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> -Eigenschaft|Bestimmt den minimalen Abstand in Pixel, dass der Splitter vom Benutzer verschoben werden kann.|  
  
 Im folgenden Beispiel wird die-Eigenschaft dahingehend geändert, dass <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> ein "Ausrichten von Trenn-Splitter"-Effekt erstellt wird. wenn der Benutzer den Splitter zieht, wird er in Einheiten von 10 Pixeln anstatt in der Standardeinstellung 1 erhöht.  
  
### <a name="to-define-splitcontainer-resize-behavior"></a>So definieren Sie das Verhalten der SplitContainer-Größenänderung  
  
1. Legen Sie die-Eigenschaft in einer-Prozedur <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A> auf die gewünschte Größe fest, damit das "ausrichten"-Verhalten des Splitters erreicht wird.  
  
     Im folgenden Codebeispiel wird im-Ereignis des Formulars der <xref:System.Windows.Forms.Form.Load> Splitter im-Steuerelement so festgelegt, dass beim Ziehen <xref:System.Windows.Forms.SplitContainer> 10 Pixel gesprungen werden.  
  
    ```vb  
    Private Sub Form1_Load(ByVal sender As System.Object, _  
        ByVal e As System.EventArgs) Handles MyBase.Load  
        Dim splitSnapper as new SplitContainer()  
        splitSnapper.SplitterIncrement = 10  
        splitSnapper.Dock = DockStyle.Fill  
        splitSnapper.Parent = me  
    End Sub  
    ```  
  
    ```csharp  
    private void Form1_Load(System.Object sender, System.EventArgs e)  
    {  
        SplitContainer splitSnapper = new SplitContainer();  
        splitSnapper.SplitterIncrement = 10;  
        splitSnapper.Dock = DockStyle.Fill;  
        splitSnapper.Parent = this;  
    }  
    ```  
  
     (Visual c#) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.Load += new System.EventHandler(this.Form1_Load);  
    ```  
  
     Das Verschieben des Splitters leicht nach links oder rechts hat keine erkennbaren Auswirkungen. Wenn der Mauszeiger jedoch 10 Pixel in beide Richtungen wechselt, wird der Splitter an der neuen Position ausgerichtet.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.SplitContainer>
- <xref:System.Windows.Forms.SplitContainer.SplitterIncrement%2A>
