---
title: 'Vorgehensweise: Anordnen von untergeordneten MDI-Formularen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- child forms [Windows Forms], arranging
- MDI [Windows Forms], arranging child forms
ms.assetid: a0786378-3206-4ccc-898e-7d3b38cc5089
ms.openlocfilehash: 7e4d5a80961ae37951251dffa30cb8e75b20be27
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972382"
---
# <a name="how-to-arrange-mdi-child-forms"></a>Vorgehensweise: Anordnen von untergeordneten MDI-Formularen
Anwendungen verfügen häufig über Menübefehle für Aktionen wie z. B. Nebeneinander anordnen, Überlappend anordnen und Anordnen, über die das Layout des geöffneten untergeordneten MDI-Formulars gesteuert wird. Sie können die <xref:System.Windows.Forms.Form.LayoutMdi%2A> -Methode mit einem der <xref:System.Windows.Forms.MdiLayout>-Enumerationswerte anwenden, um die untergeordneten Formulare in einem übergeordneten MDI-Enumerationswerteformular neu anzuordnen.  
  
 Mit <xref:System.Windows.Forms.MdiLayout>-Enumerationswerten werden untergeordnete Formulare als überlappend, nebeneinander oder untereinander bzw. in Form von untergeordneten Formularsymbolen im unteren Bereich des MDI-Formulars angeordnet. Diese Werte haben dieselbe Auswirkung wie die Windows-Befehle, die Fenster **kaskadieren**, Fenster **nebeneinander anzeigen**, **gestapelte Fenster anzeigen** und **den Desktop anzeigen**.  
  
 Diese Methoden werden häufig als Ereignishandler aufgerufen, die vom <xref:System.Windows.Forms.Control.Click>-Ereignis eines Menüelements abgerufen werden. Auf diese Weise kann ein Menüelement mit dem Text "Fenster überlappend anzeigen" den gewünschten Effekt auf untergeordnete MDI-Fenster haben.  
  
### <a name="to-arrange-child-forms"></a>So ordnen Sie untergeordnete Formulare an  
  
1. Verwenden Sie in einer Methode die <xref:System.Windows.Forms.Form.LayoutMdi%2A> -Methode zum Festlegen der <xref:System.Windows.Forms.MdiLayout> -Enumeration für das übergeordnete MDI-Formular. Im folgenden Beispiel wird der <xref:System.Windows.Forms.MdiLayout.Cascade?displayProperty=nameWithType> -Enumerationswert für die untergeordneten Fenster des übergeordneten MDI-Formulars (`Form1`) verwendet. Die-Enumeration wird im Code während des-Ereignis Handlers für das- <xref:System.Windows.Forms.Control.Click> Ereignis des Menü Elements **Cascade Windows** verwendet.  
  
    ```vb  
    Protected Sub CascadeWindows_Click(ByVal sender As System.Object, ByVal e As System.EventArgs)  
       Me.LayoutMdi(System.Windows.Forms.MdiLayout.Cascade)  
    End Sub  
    ```  
  
    ```csharp  
    protected void CascadeWindows_Click(object sender, System.EventArgs e){  
       this.LayoutMdi(System.Windows.Forms.MdiLayout.Cascade);  
    }  
    ```  
  
    > [!NOTE]
    > Sie könne Fenster auch nebeneinander oder als Symbole anordnen, indem Sie den verwendeten <xref:System.Windows.Forms.MdiLayout> -Enumerationswert ändern.  
  
2. Wenn Sie Visual C# verwenden, fügen Sie folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [MDI-Anwendungen (Multiple Document Interface)](multiple-document-interface-mdi-applications.md)
- [Vorgehensweise: Erstellen von übergeordneten MDI-Formularen](how-to-create-mdi-parent-forms.md)
- [Vorgehensweise: Erstellen von untergeordneten MDI-Formularen](how-to-create-mdi-child-forms.md)
- [Vorgehensweise: Bestimmen des aktiven untergeordneten MDI-Elements](how-to-determine-the-active-mdi-child.md)
- [Vorgehensweise: Senden von Daten an das aktive untergeordnete MDI-Element](how-to-send-data-to-the-active-mdi-child.md)
