---
title: 'Gewusst wie: Behandeln des ContextMenuOpening -Ereignisses'
ms.date: 03/30/2017
helpviewer_keywords:
- ContextMenuOpening properties [WPF]
ms.assetid: 789652fb-1951-4217-934a-7843e355adf4
ms.openlocfilehash: b3d0f5c77ebf8527e4854d4edf12d6fa8a4b5f0c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976681"
---
# <a name="how-to-handle-the-contextmenuopening-event"></a>Gewusst wie: Behandeln des ContextMenuOpening -Ereignisses
Das <xref:System.Windows.FrameworkElement.ContextMenuOpening> Ereignis kann in einer Anwendung behandelt werden, um entweder ein vorhandenes Kontextmenü vor der Anzeige anzupassen oder das Menü zu unterdrücken, das andernfalls angezeigt würde, indem die- <xref:System.Windows.RoutedEventArgs.Handled%2A> Eigenschaft `true` in den Ereignisdaten auf festgelegt wird. Der typische Grund für das Festlegen von <xref:System.Windows.RoutedEventArgs.Handled%2A> `true` in den Ereignisdaten besteht darin, das Menü vollständig durch ein neues Objekt zu ersetzen <xref:System.Windows.Controls.ContextMenu> , das manchmal das Abbrechen des Vorgangs und das Starten eines neuen geöffneten erfordert. Wenn Sie Handler für das- <xref:System.Windows.FrameworkElement.ContextMenuOpening> Ereignis schreiben, sollten Sie Zeit Steuerungsprobleme zwischen einem <xref:System.Windows.Controls.ContextMenu> -Steuerelement und dem-Dienst beachten, der für das Öffnen und Positionieren von Kontextmenüs für Steuerelemente im allgemeinen zuständig ist. In diesem Thema werden einige der Code Techniken für verschiedene Szenarien zum Öffnen von Kontextmenüs erläutert, und es wird ein Fall veranschaulicht, in dem das Problem mit der zeitlichen Steuerung auftritt.  
  
 Es gibt mehrere Szenarien für die Behandlung des <xref:System.Windows.FrameworkElement.ContextMenuOpening> Ereignisses:  
  
- Anpassen der Menü Elemente vor der Anzeige.  
  
- Ersetzt das gesamte Menü vor der Anzeige.  
  
- Vollständiges unterdrücken vorhandener Kontextmenüs und Anzeigen eines Kontextmenüs  
  
## <a name="example"></a>Beispiel  
  
## <a name="adjusting-the-menu-items-before-display"></a>Anpassen der Menü Elemente vor der Anzeige  
 Das Anpassen der vorhandenen Menü Elemente ist ziemlich einfach und ist wahrscheinlich das gängigste Szenario. Dies können Sie tun, um Kontextmenü Optionen als Reaktion auf aktuelle Zustandsinformationen in der Anwendung oder bestimmte Zustandsinformationen, die als Eigenschaft für das Objekt verfügbar sind, in dem das Kontextmenü angefordert wird, hinzuzufügen oder zu subtrahieren.  
  
 Das allgemeine Verfahren besteht darin, die Quelle des Ereignisses, d. h. das spezifische Steuerelement, auf das mit der rechten Maustaste geklickt wurde, zu erhalten und die- <xref:System.Windows.FrameworkElement.ContextMenu%2A> Eigenschaft daraus zu erhalten. In der Regel sollten Sie die Sammlung überprüfen, <xref:System.Windows.Controls.ItemsControl.Items%2A> um festzustellen, welche Kontextmenü Elemente bereits im Menü vorhanden sind, und dann <xref:System.Windows.Controls.MenuItem> die entsprechenden neuen Elemente zu oder aus der Auflistung hinzufügen oder daraus entfernen.  
  
 [!code-csharp[ContextMenuOpeningHandlers#AddItemNoHandle](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#additemnohandle)]  
  
## <a name="replacing-the-entire-menu-before-display"></a>Ersetzen des gesamten Menüs vor der Anzeige  
 Ein alternatives Szenario besteht darin, das gesamte Kontextmenü zu ersetzen. Sie könnten natürlich auch eine Variation des vorangehenden Codes verwenden, um alle Elemente eines vorhandenen Kontextmenüs zu entfernen und neue Elemente hinzuzufügen, beginnend mit dem Element 0. Der intuitivste Ansatz, alle Elemente im Kontextmenü zu ersetzen, besteht darin, einen neuen zu erstellen <xref:System.Windows.Controls.ContextMenu> , ihn mit Elementen zu füllen und dann die- <xref:System.Windows.FrameworkElement.ContextMenu%2A?displayProperty=nameWithType> Eigenschaft eines Steuer Elements auf den neuen festzulegen <xref:System.Windows.Controls.ContextMenu> .  
  
 Im folgenden finden Sie den einfachen Handlercode zum Ersetzen von <xref:System.Windows.Controls.ContextMenu> . Der Code verweist auf eine benutzerdefinierte `BuildMenu` Methode, die getrennt ist, da Sie von mehr als einem der Beispiel Handler aufgerufen wird.  
  
 [!code-csharp[ContextMenuOpeningHandlers#ReplaceNoReopen](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#replacenoreopen)]  
  
 [!code-csharp[ContextMenuOpeningHandlers#BuildMenu](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#buildmenu)]  
  
 Wenn Sie jedoch diese Art von Handler für verwenden <xref:System.Windows.FrameworkElement.ContextMenuOpening> , können Sie möglicherweise ein Problem mit der zeitlichen Steuerung verfügbar machen, wenn das Objekt, in dem Sie festlegen, <xref:System.Windows.Controls.ContextMenu> nicht über ein vorhandenes Kontextmenü verfügt. Wenn ein Benutzer mit der rechten Maustaste auf ein-Steuerelement klickt, <xref:System.Windows.FrameworkElement.ContextMenuOpening> wird auch dann ausgelöst, wenn der vorhandene <xref:System.Windows.Controls.ContextMenu> leer oder NULL ist. In diesem Fall wird allerdings, was <xref:System.Windows.Controls.ContextMenu> für das Quell Element festgelegt wurde, zu spät angezeigt, um angezeigt zu werden. Wenn der Benutzer mit der rechten Maustaste auf ein zweites Mal klickt, wird das neue angezeigt, <xref:System.Windows.Controls.ContextMenu> der Wert ist nicht NULL, und der Handler ersetzt das Menü ordnungsgemäß und zeigt es an, wenn der Handler ein zweites Mal ausgeführt wird. Dies deutet auf zwei mögliche Problem Umgehungen hin:  
  
1. Stellen Sie sicher, dass <xref:System.Windows.FrameworkElement.ContextMenuOpening> Handler immer für Steuerelemente ausgeführt werden, die mindestens über einen Platzhalter verfügen <xref:System.Windows.Controls.ContextMenu> , der durch den Handlercode ersetzt werden soll. In diesem Fall können Sie weiterhin den im vorherigen Beispiel gezeigten Handler verwenden, Sie möchten jedoch in der Regel einen Platzhalter <xref:System.Windows.Controls.ContextMenu> im anfänglichen Markup zuweisen:  
  
     [!code-xaml[ContextMenuOpeningHandlers#XAMLWithInitCM](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml#xamlwithinitcm)]  
  
2. Nehmen Sie an, dass der Anfangs <xref:System.Windows.Controls.ContextMenu> Wert auf der Grundlage einer vorläufigen Logik NULL sein kann. Sie können entweder <xref:System.Windows.Controls.ContextMenu> auf NULL prüfen oder ein Flag in Ihrem Code verwenden, um zu überprüfen, ob der Handler mindestens einmal ausgeführt wurde. Da Sie davon ausgehen, dass der <xref:System.Windows.Controls.ContextMenu> angezeigt wird, legt der Handler <xref:System.Windows.RoutedEventArgs.Handled%2A> `true` in den Ereignisdaten auf fest. Der, der <xref:System.Windows.Controls.ContextMenuService> für die Anzeige des Kontextmenüs zuständig ist, `true` stellt ein Wert für <xref:System.Windows.RoutedEventArgs.Handled%2A> in den Ereignisdaten eine Anforderung dar, die Anzeige für die Kontextmenü-/steuerungkombination abzubrechen, die das Ereignis ausgelöst hat.  
  
 Nachdem Sie das potenziell Fehler verdächtige Kontextmenü unterdrückt haben, besteht der nächste Schritt darin, eine neue bereitzustellen und diese dann anzuzeigen. Das Festlegen der neuen ist im Grunde das gleiche wie der vorherige Handler: Sie erstellen ein neues <xref:System.Windows.Controls.ContextMenu> und legen die-Eigenschaft der Steuerelement Quelle <xref:System.Windows.FrameworkElement.ContextMenu%2A?displayProperty=nameWithType> darauf fest. Der zusätzliche Schritt besteht darin, dass Sie jetzt die Anzeige des Kontextmenüs erzwingen müssen, da Sie den ersten Versuch unterdrückt haben. Um die Anzeige zu erzwingen, legen Sie die- <xref:System.Windows.Controls.Primitives.Popup.IsOpen%2A?displayProperty=nameWithType> Eigenschaft `true` innerhalb des-Handlers auf fest. Seien Sie vorsichtig, wenn Sie das Kontextmenü des Handlers öffnen, um das <xref:System.Windows.FrameworkElement.ContextMenuOpening> Ereignis erneut auszuführen. Wenn Sie den Handler erneut eingeben, wird er unendlich rekursiv. Aus diesem Grund müssen Sie immer `null` ein Flag suchen oder verwenden, wenn Sie ein Kontextmenü innerhalb eines- <xref:System.Windows.FrameworkElement.ContextMenuOpening> Ereignis Handlers öffnen.  
  
## <a name="suppressing-any-existing-context-menu-and-displaying-no-context-menu"></a>Unterdrücken eines beliebigen vorhandenen Kontextmenüs und Anzeigen eines Kontextmenüs  
 Das abschließende Szenario, das Schreiben eines Handlers, der ein Menü vollständig unterdrückt, ist nicht üblich. Wenn ein bestimmtes Steuerelement kein Kontextmenü anzeigen soll, gibt es wahrscheinlich geeignetere Möglichkeiten, dies zu gewährleisten, als indem das Menü nur dann unterdrückt wird, wenn ein Benutzer es anfordert. Wenn Sie den Handler jedoch verwenden möchten, um ein Kontextmenü zu unterdrücken und Nothing anzuzeigen, sollte der Handler einfach <xref:System.Windows.RoutedEventArgs.Handled%2A> auf `true` in den Ereignisdaten festlegen. Der <xref:System.Windows.Controls.ContextMenuService> , der für die Anzeige eines Kontextmenüs zuständig ist, überprüft die Ereignisdaten des Ereignisses, das für das Steuerelement ausgelöst wurde. Wenn das Ereignis an einer <xref:System.Windows.RoutedEventArgs.Handled%2A> beliebigen Stelle entlang der Route markiert wurde, wird die Kontextmenü-Aktion zum Öffnen des Ereignisses unterdrückt.  
  
 [!code-csharp[ContextMenuOpeningHandlers#ReplaceReopen](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenuOpeningHandlers/CSharp/Pane1.xaml.cs#replacereopen)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ContextMenu>
- <xref:System.Windows.FrameworkElement.ContextMenu%2A?displayProperty=nameWithType>
- [Übersicht über Basiselemente](base-elements-overview.md)
- [Übersicht über ContextMenu](../controls/contextmenu-overview.md)
