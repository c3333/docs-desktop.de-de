---
title: Übersicht über nicht verwaltete apps
ms.date: 03/30/2017
ms.topic: overview
helpviewer_keywords:
- COM [Windows Forms]
- Windows Forms, unmanaged
- COM interop
- ActiveX controls [Windows Forms], about ActiveX controls
- Windows Forms, interop
ms.assetid: 0a26d99d-8135-4895-8760-c9a2b5f67f14
ms.openlocfilehash: 48599e11a99216d27029256d8ff4c7d1d4692c03
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975813"
---
# <a name="windows-forms-and-unmanaged-applications-overview"></a>Übersicht über Windows Forms und nicht verwaltete Anwendungen

Windows Forms-Anwendungen und-Steuerelemente können mit einigen Einschränkungen mit nicht verwalteten Anwendungen zusammenarbeiten. In den folgenden Abschnitten werden die von Windows Forms-Anwendungen und -Steuerelementen unterstützten und nicht unterstützten Szenarien und Konfigurationen beschrieben.  
  
## <a name="windows-forms-controls-and-activex-applications"></a>Windows Forms-Steuerelemente und ActiveX-Anwendungen  

 Mit Ausnahme von Microsoft Internet Explorer und Microsoft Foundation Classes (MFC) werden Windows Forms-Steuerelemente in Anwendungen, die auf das Hosting von ActiveX-Steuerelementen ausgelegt sind, nicht unterstützt. Andere Anwendungen und Entwicklungstools, die ActiveX-Steuerelemente hosten können, einschließlich der ActiveX-Testcontainer aus früheren Visual Studio-Versionen als Visual Studio .NET 2003, sind keine unterstützten Hosts für Windows Forms-Steuerelemente.  
  
 Diese Einschränkungen gelten auch für die Verwendung von Windows Forms-Steuerelementen mithilfe von COM-Interop (Component Object Model). Die Verwendung eines Windows Forms-Steuerelements mithilfe eines COM Callable Wrappers (CCW) wird nur in Internet Explorer unterstützt. Weitere Informationen zu COM-Interop finden Sie unter  
  
 [COM-Interop](/dotnet/visual-basic/programming-guide/com-interop/index).  
  
 Die folgende Tabelle zeigt die verfügbare Unterstützung für ActiveX-Hosting für Windows Forms-Steuerelemente.  
  
|Windows Forms-Version|Unterstützung|  
|---------------------------|-------------|  
|.NET Framework Version 1.0|Internet Explorer 5.01 und höhere Versionen|  
|.NET Framework Version 1.1 und höher|Internet Explorer 5.01 und höhere Versionen<br /><br /> Microsoft Foundation Classes (MFC) 7.0 und höher|  
  
## <a name="hosting-windows-forms-components-as-activex-controls"></a>Hosten von Windows Forms-Komponenten als ActiveX-Steuerelemente  

 In .NET Framework 1.1 wurde die Unterstützung auf MFC 7.0 und höhere Versionen erweitert. Diese Unterstützung umfasst alle Container, die mit dem ActiveX-Steuerelementcontainer aus MFC 7.0 und höher vollständig kompatibel sind.  
  
 Die Registrierung von Windows Forms-Steuerelementen als ActiveX-Steuerelementen wird jedoch nicht unterstützt. Ebenfalls wird das Aufrufen der `com.ms.win32.Ole32.CoCreateInstance` -Methode für Windows Forms-Steuerelementen nicht unterstützt. Nur die verwaltete Aktivierung von Windows Forms-Steuerelementen wird unterstützt. Nachdem Sie ein Windows Forms-Steuerelement erstellt haben, können Sie es in einer MFC-Anwendung hosten, wie bei einem ActiveX-Steuerelement.  
  
 Um Windows Forms-Steuerelemente in Ihrer nicht verwalteten Anwendung zu verwenden, müssen Sie entweder die CLR mithilfe der Hosting-APIs der nicht verwalteten CLR hosten oder die C++-Interop-Funktionen verwenden. Die Verwendung der C++-Interop-Funktionen ist die empfohlene Lösung.  
  
## <a name="windows-forms-in-com-client-applications"></a>Windows Forms in COM-Clientanwendungen  

 Wenn Sie ein Windows Form aus eine COM-Clientanwendung öffnen, z. B. einer Visual Basic 6.0-Anwendung oder einer MFC-Anwendung, kann das Formular unerwartetes Verhalten zeigen. Wenn Sie z. B. die TAB-Taste drücken, wechselt der Fokus nicht von einem Steuerelement zu einem anderen. Wenn Sie die EINGABETASTE drücken, während eine Befehlsschaltfläche den Fokus besitzt, wird das <xref:System.Windows.Forms.Control.Click> -Ereignis der Schaltfläche nicht ausgelöst. Auch bei Tastatureingaben oder Mausaktivitäten kann unerwartetes Verhalten auftreten.  
  
 Dieses Verhalten tritt auf, weil die nicht verwaltete Anwendung nicht die Unterstützung für Nachrichtenschleifen implementiert, die Windows Forms für eine ordnungsgemäße Funktion erfordert. Die von der COM-Clientanwendung bereitgestellte Nachrichtenschleife unterscheidet sich grundlegend von der Windows Forms-Nachrichtenschleife.  
  
 Die Nachrichtenschleife einer Anwendung ist eine interne Programmschleife, die Nachrichten aus der Nachrichtenwarteschlange eines Threads abruft, diese übersetzt und dann an die zu behandelnde Anwendung sendet. Die Nachrichtenschleife für ein Windows Form hat nicht dieselbe Architektur wie Nachrichtenschleifen, die von früheren Anwendungen, z. B. Visual Basic 6.0-Anwendungen und MFC-Anwendungen, bereitgestellt werden. Die Windows-Nachrichten, die in der Nachrichtenschleife bereitgestellt werden, werden möglicherweise anders behandelt, als vom Windows Form erwartet. Daher kann es zu unerwartetem Verhalten kommen. Einige Tastenkombinationen funktionieren möglicherweise nicht, einige Mausaktivitäten funktionieren eventuell nicht, oder einige Ereignisse werden möglicherweise nicht wie erwartet ausgelöst.  
  
## <a name="resolving-interoperability-issues"></a>Beheben von Interoperabilitätsproblemen  

 Sie können diese Probleme beheben, indem Sie das Formular in einer .NET Framework-Nachrichten Schleife anzeigen, die mit der-Methode erstellt wird <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> .  
  
 Damit ein Windows Form aus einer COM-Clientanwendung heraus ordnungsgemäß funktioniert, müssen Sie es in einer Windows Forms-Nachrichtenschleife ausführen. Hierzu können Sie einen der folgenden Ansätze verwenden:  
  
- Verwenden Sie die <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> -Methode, um das Windows Form anzuzeigen. Weitere Informationen finden Sie unter [Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen eines Windows Forms mit der ShowDialog-Methode](com-interop-by-displaying-a-windows-form-shadow.md).  
  
- Zeigen Sie jedes Windows Form in einem neuen Thread an. Weitere Informationen finden Sie unter [Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen jedes Windows Forms in einem eigenen Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md).  
  
## <a name="see-also"></a>Siehe auch

- [Windows Forms und nicht verwaltete Anwendungen](windows-forms-and-unmanaged-applications.md)
- [COM-Interop](/dotnet/visual-basic/programming-guide/com-interop/index)
- [COM-Interoperabilität in .NET Framework-Anwendungen](/dotnet/visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications)
- [Beispiele für COM-Interoperabilität](/previous-versions/visualstudio/visual-studio-2008/cxcz83xf(v=vs.90))
- [Aximp.exe (Windows Forms ActiveX Control Importer-Tool)](/dotnet/framework/tools/aximp-exe-windows-forms-activex-control-importer)
- [Verfügbarmachen von .NET Framework-Komponenten in COM](/dotnet/framework/interop/exposing-dotnet-components-to-co)
- [Verpacken einer Assembly für COM](/dotnet/framework/interop/packaging-an-assembly-for-co)
- [Registrieren von Assemblys bei COM](/dotnet/framework/interop/registering-assemblies-with-co)
- [Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen eines Windows Forms mit der ShowDialog-Methode](com-interop-by-displaying-a-windows-form-shadow.md)
- [Vorgehensweise: Unterstützen von COM-Interop durch das Anzeigen einzelner Windows Forms in einem eigenen Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md)
