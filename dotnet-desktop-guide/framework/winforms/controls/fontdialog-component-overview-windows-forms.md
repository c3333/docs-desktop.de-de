---
title: Übersicht über die FontDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- FontDialog
helpviewer_keywords:
- Font dialog box [Windows Forms], Windows Forms
- Font dialog box
- FontDialog component [Windows Forms], about FontDialog component
ms.assetid: daf46e57-1b4b-4b7a-bad0-b50ca7ba75dc
ms.openlocfilehash: 664b756dc068ca283e4f43edbdd0f3266f5d1142
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972106"
---
# <a name="fontdialog-component-overview-windows-forms"></a>Übersicht über die FontDialog-Komponente (Windows Forms)
Bei der Windows Forms <xref:System.Windows.Forms.FontDialog> Komponente handelt es sich um ein vorkonfiguriertes Dialogfeld, bei dem es sich um das Standard Dialogfeld für Windows- **Schriftart** handelt Verwenden Sie es in Ihrer Windows-basierten Anwendung als einfache Lösung für die Schriftart Auswahl, anstatt ein eigenes Dialogfeld zu konfigurieren.  
  
 Standardmäßig werden im Dialogfeld Listenfelder für Schriftart, Schriftart Stil und Größe angezeigt. Kontrollkästchen für Effekte wie "Strikeout" und "Unterstreichung" eine Dropdown Liste für das Skript. und ein Beispiel, wie die Schriftart angezeigt wird. (Das Skript bezieht sich auf verschiedene Zeichen Skripts, die für eine bestimmte Schriftart verfügbar sind, z. b. Hebräisch oder Japanisch.) Um das Dialogfeld Schriftart anzuzeigen, müssen Sie die- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode aufrufen.  
  
## <a name="key-properties"></a>Schlüsseleigenschaften  
 Die Komponente verfügt über eine Reihe von Eigenschaften, die ihre Darstellung konfigurieren. Die Eigenschaften, die die Dialogfeld Auswahl festlegen, lauten <xref:System.Windows.Forms.FontDialog.Font%2A> und <xref:System.Windows.Forms.FontDialog.Color%2A> . Die- <xref:System.Windows.Forms.FontDialog.Font%2A> Eigenschaft legt die Schriftart, den Stil, die Größe, das Skript und die Effekte fest, z `Arial, 10pt, style=Italic, Strikeout` . b..  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.FontDialog>
- [FontDialog-Komponente](fontdialog-component-windows-forms.md)
