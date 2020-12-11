---
title: Anzeigen asiatischer Zeichen mit der ImeMode-Eigenschaft
ms.date: 03/30/2017
helpviewer_keywords:
- Asian languages [Windows Forms], displaying with ImeMode
- Chinese characters [Windows Forms], displaying with ImeMode
- IME mode
- Japanese characters [Windows Forms], displaying with ImeMode
- international applications [Windows Forms], character display
- international characters
- Korean characters
- Asian languages
- Input Method Editor (IME), mode
- localization [Windows Forms], character sets
- globalization [Windows Forms], character sets
ms.assetid: c60ae399-0dab-4f07-9dea-6dbfb15ec0ae
ms.openlocfilehash: 25602e1a878443bd54411dfd6481581abebda5c7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972391"
---
# <a name="display-of-asian-characters-with-the-imemode-property"></a>Anzeigen asiatischer Zeichen mit der ImeMode-Eigenschaft
Die <xref:System.Windows.Forms.Control.ImeMode%2A> -Eigenschaft wird von Formularen und Steuerelementen verwendet, um einen bestimmten Modus für einen Eingabemethoden-Editor (IME) zu erzwingen. Der IME ist eine wichtige Komponente beim Schreiben von chinesischen, japanischen und koreanischen Skripts, da diese Schriftsysteme mehr Zeichen enthalten als für eine normale Tastatur codiert werden können. Beispiel: In ein bestimmtes Textfeld sollen nur ASCII-Zeichen eingetragen werden dürfen. In einem solchen Fall können Sie die <xref:System.Windows.Forms.Control.ImeMode%2A> -Eigenschaft auf festlegen, <xref:System.Windows.Forms.ImeMode> und Benutzer können nur ASCII-Zeichen für das jeweilige Textfeld eingeben. Der Standardwert der- <xref:System.Windows.Forms.Control.ImeMode%2A> Eigenschaft ist <xref:System.Windows.Forms.ImeMode> . Wenn Sie also die-Eigenschaft für ein Formular festlegen, erben alle Steuerelemente im Formular diese Einstellung. Weitere Informationen finden Sie unter <xref:System.Windows.Forms.Control.ImeMode%2A> und <xref:System.Windows.Forms.ImeMode> .  
  
## <a name="see-also"></a>Siehe auch

- [Globalisieren von Windows Forms Anwendungen](globalizing-windows-forms.md)
