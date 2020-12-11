---
title: 'Gewusst wie: Hinzufügen einer Klassenbehandlung für ein Routingereignis'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- routed events [WPF], class handlers
- task_core_add_class_handling_routed_properties [WPF]
- class handlers [WPF], routed events
ms.assetid: 15b7b06c-9112-4ee5-b30a-65d10c5c5df6
ms.openlocfilehash: 7b897954cbdab461dc0305c6290e67c1af5282c3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976570"
---
# <a name="how-to-add-class-handling-for-a-routed-event"></a>Gewusst wie: Hinzufügen einer Klassenbehandlung für ein Routingereignis
Routing Ereignisse können entweder von Klassen Handlern oder Instanzhandlern auf einem beliebigen Knoten in der Route behandelt werden. Klassen Handler werden zuerst aufgerufen und können von Klassen Implementierungen verwendet werden, um Ereignisse aus der instanzverarbeitung zu unterdrücken oder andere ereignisspezifische Verhaltensweisen für Ereignisse zu unterdrücken, die im Besitz von Basisklassen sind. In diesem Beispiel werden zwei eng miteinander verbundene Techniken zum Implementieren von Klassen Handlern veranschaulicht.  
  
## <a name="example"></a>Beispiel  
 Dieses Beispiel verwendet eine benutzerdefinierte-Klasse, die auf dem <xref:System.Windows.Controls.Canvas> Panel basiert. Der grundlegende Zweck der Anwendung besteht darin, dass die benutzerdefinierte-Klasse Verhaltensweisen auf die untergeordneten Elemente einführt, einschließlich des Abrufens von linken Maustaste Klicks und deren Behandlung, bevor die untergeordnete Element Klasse oder beliebige Instanzhandler aufgerufen werden.  
  
 Die- <xref:System.Windows.UIElement> Klasse macht eine virtuelle Methode verfügbar, die eine Klassen Behandlung für das- <xref:System.Windows.UIElement.PreviewMouseLeftButtonDown> Ereignis ermöglicht, indem das-Ereignis einfach überschrieben wird. Dies ist die einfachste Methode zum Implementieren der Klassen Behandlung, wenn eine solche virtuelle Methode irgendwo in der Hierarchie der Klasse verfügbar ist. Der folgende Code zeigt die <xref:System.Windows.UIElement.OnPreviewMouseLeftButtonDown%2A> Implementierung in "MyEditContainer", die von abgeleitet ist <xref:System.Windows.Controls.Canvas> . Die Implementierung markiert das Ereignis als behandelt in den Argumenten und fügt dann Code hinzu, um dem Quell Element eine grundlegende sichtbare Änderung zu verleihen.  
  
 [!code-csharp[ClassHandling#OnStarClassHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/ClassHandling/CSharp/SDKSampleLibrary/class1.cs#onstarclasshandler)]
 [!code-vb[ClassHandling#OnStarClassHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClassHandling/visualbasic/sdksamplelibrary/class1.vb#onstarclasshandler)]  
  
 Wenn für Basisklassen oder für diese spezielle Methode kein virtueller Dienst verfügbar ist, kann die Klassen Behandlung direkt mithilfe einer hilfsprogrammmethode der-Klasse hinzugefügt werden <xref:System.Windows.EventManager> <xref:System.Windows.EventManager.RegisterClassHandler%2A> . Diese Methode sollte nur innerhalb der statischen Initialisierung von Klassen aufgerufen werden, die eine Klassen Behandlung hinzufügen. In diesem Beispiel wird ein weiterer Handler für hinzugefügt <xref:System.Windows.UIElement.PreviewMouseLeftButtonDown> . in diesem Fall ist die registrierte Klasse die benutzerdefinierte Klasse. Im Gegensatz dazu ist die registrierte Klasse bei der Verwendung der virtualen tatsächlich die <xref:System.Windows.UIElement> Basisklasse. In Fällen, in denen Basisklassen und Unterklassen jeweils die Klassen Behandlung durchlaufen, werden die Unterklassen Handler zuerst aufgerufen. Das Verhalten in einer Anwendung wäre, dass dieser Handler zuerst sein Meldungs Feld anzeigt und dann die visuelle Änderung im Handler der virtuellen Methode angezeigt wird.  
  
 [!code-csharp[ClassHandling#StaticAndRegisterClassHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/ClassHandling/CSharp/SDKSampleLibrary/class1.cs#staticandregisterclasshandler)]
 [!code-vb[ClassHandling#StaticAndRegisterClassHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClassHandling/visualbasic/sdksamplelibrary/class1.vb#staticandregisterclasshandler)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.EventManager>
- [Markieren von Routingereignissen als behandelt und Klassenbehandlung](marking-routed-events-as-handled-and-class-handling.md)
- [Behandeln eines Routingereignisses](how-to-handle-a-routed-event.md)
- [Übersicht über Routingereignisse](routed-events-overview.md)
