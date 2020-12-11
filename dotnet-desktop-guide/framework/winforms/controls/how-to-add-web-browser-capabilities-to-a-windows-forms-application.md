---
title: Webbrowser Funktionen zur APP hinzufügen
description: Erfahren Sie, wie Sie mit dem Webbrowser-Steuerelement einer Windows Forms Anwendung Webbrowser Funktionen hinzufügen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- WebBrowser control [Windows Forms], adding Web browser capabilities to your application
- WebBrowser control [Windows Forms], examples
- Web browsers [.NET Framework], adding to Windows Forms
- examples [Windows Forms], WebBrowser control
- Windows Forms, adding Web browser functionality
ms.assetid: 3871f072-b57a-435b-9976-e5da28df04a7
ms.openlocfilehash: a5a33961ac8301bda86bb5f34e65ac159308987f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976234"
---
# <a name="how-to-add-web-browser-capabilities-to-a-windows-forms-application"></a>Vorgehensweise beim Hinzufügen von Webbrowser Funktionen zu einer Windows Forms Anwendung

Mit dem <xref:System.Windows.Forms.WebBrowser>-Steuerelement können Sie Webbrowserfunktionalität in Ihre Anwendung einbinden. Das Steuerelement verhält sich standardmäßig wie ein Webbrowser. Nach dem Laden einer Anfangs-URL durch Festlegen der <xref:System.Windows.Forms.WebBrowser.Url%2A>-Eigenschaft können Sie auf Hyperlinks klicken oder mit den entsprechenden Tastenkombinationen vorwärts oder rückwärts durch den Navigationsverlauf navigieren. Über das Kontextmenü, das durch Klicken mit der rechten Maustaste angezeigt wird, können standardmäßig zusätzliche Browserfunktionen aufgerufen werden. Sie können auch neue Dokumente öffnen, indem Sie sie auf dem Steuerelement ablegen. Das <xref:System.Windows.Forms.WebBrowser>-Steuerelement verfügt über verschiedene Eigenschaften, Methoden und Ereignisse, mit denen Sie ähnliche Benutzeroberflächenfeatures wie in Internet Explorer implementieren können.

Im folgenden Beispielcode werden eine Adressleiste, typische Browserschaltflächen, ein Menü **Datei**, eine Statusleiste und eine Titelleiste mit dem Titel der aktuellen Seite implementiert.

## <a name="example"></a>Beispiel

[!code-cpp[System.Windows.Forms.WebBrowser#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.WebBrowser/CPP/form1.cpp#0)]
[!code-csharp[System.Windows.Forms.WebBrowser#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.WebBrowser/CS/form1.cs#0)]
[!code-vb[System.Windows.Forms.WebBrowser#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.WebBrowser/VB/form1.vb#0)]
  
## <a name="compile-the-code"></a>Kompilieren des Codes

Für dieses Beispiel benötigen Sie Folgendes:

- Verweise auf die Assemblys `System`, `System.Drawing` und `System.Windows.Forms`.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.WebBrowser>
- [WebBrowser-Steuerelement](webbrowser-control-windows-forms.md)
