---
title: 'Gewusst wie: Programmgesteuertes Drucken von XPS-Dateien'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- printing XPS files programmatically [WPF]
- XPS files [WPF], printing programmatically
ms.assetid: 0b1c0a3f-b19e-43d6-bcc9-eb3ec4e555ad
ms.openlocfilehash: c9cd61c76ec4fbc75a7080e13294cc7fcdcb400f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977750"
---
# <a name="how-to-programmatically-print-xps-files"></a>Gewusst wie: Programmgesteuertes Drucken von XPS-Dateien

Sie können eine Überladung der- <xref:System.Printing.PrintQueue.AddJob%2A> Methode verwenden, um XPS-Dateien (XML Paper Specification) zu drucken, ohne ein-oder-Prinzip (grundsätzlich) zu öffnen <xref:System.Windows.Controls.PrintDialog> [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] .

Sie können XPS-Dateien auch mit den vielen <xref:System.Windows.Xps.XpsDocumentWriter.Write%2A?displayProperty=nameWithType> Methoden und drucken <xref:System.Windows.Xps.XpsDocumentWriter.WriteAsync%2A?displayProperty=nameWithType> . Weitere Informationen finden Sie unter [Drucken eines XPS-Dokuments](/previous-versions/dotnet/netframework-3.5/ms771525(v=vs.90)).

Eine weitere Möglichkeit zum Drucken von XPS ist die Verwendung der- <xref:System.Windows.Controls.PrintDialog.PrintDocument%2A?displayProperty=nameWithType> Methode oder der- <xref:System.Windows.Controls.PrintDialog.PrintVisual%2A?displayProperty=nameWithType> Methode. Weitere Informationen finden Sie unter [Aufrufen eines Druckdialogfelds](how-to-invoke-a-print-dialog.md).

## <a name="example"></a>Beispiel

Die wichtigsten Schritte bei der Verwendung der Methode mit drei Parametern <xref:System.Printing.PrintQueue.AddJob%28System.String%2CSystem.String%2CSystem.Boolean%29> lauten wie folgt. Das folgende Beispiel enthält Details.

1. Stellen Sie fest, ob es sich bei dem Drucker um einen XPSDrv-Drucker handelt. Weitere Informationen zu XPSDrv finden Sie unter Übersicht über das [Drucken](printing-overview.md) .

2. Wenn es sich bei dem Drucker nicht um einen XPSDrv-Drucker handelt, legen Sie das Apartment des Threads auf Singlethread fest.

3. Instanziieren Sie einen Druckerserver und ein Druckwarteschlangenobjekt.

4. Ruft die-Methode auf, gibt einen Auftrags Namen, die zu druckende Datei und ein Flag an, das <xref:System.Boolean> angibt, ob es sich bei dem Drucker um einen XPSDrv-Drucker handelt.

Im folgenden Beispiel wird gezeigt, wie alle XPS-Dateien in einem Verzeichnis gedruckt werden. Obwohl die Anwendung den Benutzer auffordert, das Verzeichnis anzugeben, erfordert die Methode mit drei Parametern <xref:System.Printing.PrintQueue.AddJob%28System.String%2CSystem.String%2CSystem.Boolean%29> keine [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] . Sie kann in jedem Codepfad verwendet werden, in dem Sie einen XPS-Dateinamen und-Pfad haben, den Sie übergeben können.

Die drei Parameter <xref:System.Printing.PrintQueue.AddJob%28System.String%2CSystem.String%2CSystem.Boolean%29> Überladung von <xref:System.Printing.PrintQueue.AddJob%2A> muss in einem Single Thread-Apartment ausgeführt werden, wenn der- <xref:System.Boolean> Parameter ist `false` . Dies muss sein, wenn ein nicht-XPSDrv-Drucker verwendet wird. Der Standard Apartment Zustand für .net ist jedoch mehrere Threads. Dieser Standard muss umgekehrt werden, da im Beispiel kein XPSDrv-Drucker angenommen wird.

Es gibt zwei Möglichkeiten, die Standardeinstellung zu ändern. Eine Möglichkeit besteht darin, einfach das (d. h <xref:System.STAThreadAttribute> `[System.STAThreadAttribute()]` . "") direkt oberhalb der ersten Zeile der-Methode der Anwendung `Main` (in der Regel " `static void Main(string[] args)` ") hinzuzufügen. Viele Anwendungen erfordern jedoch, dass die- `Main` Methode einen Multithread-Apartment Zustand aufweist. es gibt also eine zweite Methode: Platzieren Sie den-Befehl <xref:System.Printing.PrintQueue.AddJob%28System.String%2CSystem.String%2CSystem.Boolean%29> in einem separaten Thread, dessen Apartment Zustand auf festgelegt ist <xref:System.Threading.ApartmentState.STA> <xref:System.Threading.Thread.SetApartmentState%2A> . Im folgenden Beispiel wird dieses zweite Verfahren verwendet.

Dementsprechend beginnt das Beispiel mit dem Instanziieren eines <xref:System.Threading.Thread> -Objekts und dem übergeben einer **PrintXPS** -Methode als <xref:System.Threading.ThreadStart> Parameter. (Die **PrintXPS** -Methode wird später im Beispiel definiert.) Als nächstes wird der Thread auf ein einzelnes Thread Apartment festgelegt. Mit dem verbleibenden Code der `Main`-Methode wird der neue Thread gestartet.

In diesem Beispiel geht es im Wesentlichen um die `static`**BatchXPSPrinter.PrintXPS**-Methode. Nach dem Erstellen eines Druck Servers und einer Warteschlange wird der Benutzer von der-Methode zur Eingabe eines Verzeichnisses aufgefordert, das XPS-Dateien enthält Nachdem Sie überprüft haben, ob das Verzeichnis vorhanden ist und ob \* XPS-Dateien darin vorhanden sind, fügt die Methode jede dieser Dateien der Druck Warteschlange hinzu. Bei dem Beispiel wird davon ausgegangen, dass es sich bei dem Drucker nicht um einen XPSDrv-Drucker handelt, daher wird `false` der letzte Parameter der- <xref:System.Printing.PrintQueue.AddJob%28System.String%2CSystem.String%2CSystem.Boolean%29> Methode übergeben. Aus diesem Grund überprüft die-Methode das XPS-Markup in der Datei, bevor versucht wird, Sie in die Seitenbeschreibungssprache des Druckers zu konvertieren. Wenn die Validierung fehlschlägt, wird eine Ausnahme ausgelöst. Der Beispielcode fängt die Ausnahme ab, benachrichtigt den Benutzer darüber und fährt dann mit der Verarbeitung der nächsten XPS-Datei fort.

[!code-csharp[BatchPrintXPSFiles#BatchPrintXPSFiles](~/samples/snippets/csharp/VS_Snippets_Wpf/BatchPrintXPSFiles/CSharp/Program.cs#batchprintxpsfiles)]
[!code-vb[BatchPrintXPSFiles#BatchPrintXPSFiles](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BatchPrintXPSFiles/visualbasic/program.vb#batchprintxpsfiles)]

Wenn Sie einen XPSDrv-Drucker verwenden, können Sie den abschließenden Parameter auf `true` festlegen. Da XPS die Seitenbeschreibungssprache des Druckers ist, sendet die Methode die Datei an den Drucker, ohne Sie zu validieren oder in eine andere Seitenbeschreibungssprache zu wandeln. Wenn Sie zur Entwurfszeit unsicher sind, ob die Anwendung einen XPSDrv-Drucker verwendet, können Sie die Anwendung so ändern, dass Sie die <xref:System.Printing.PrintQueue.IsXpsDevice%2A> Eigenschaft und Verzweigung entsprechend der gefundenen Informationen liest.

Da zunächst nur wenige XPSDrv-Drucker direkt nach der Veröffentlichung von Windows Vista und Microsoft .NET Framework verfügbar sein werden, müssen Sie möglicherweise einen nicht-XPSDrv-Drucker als XPSDrv-Drucker verbergen. Fügen Sie hierzu auf dem Computer, der die Anwendung ausführt, im folgenden Registrierungsschlüssel die Datei „Pipelineconfig.xml“ zur Liste der Dateien hinzu:

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Print\Environments\Windows NT x86\Drivers\Version-3 \\ *\<PseudoXPSPrinter>* \dependentfiles

dabei *\<PseudoXPSPrinter>* ist eine beliebige Druck Warteschlange. Der Computer muss anschließend neu gestartet werden.

Diese Verschleierung ermöglicht Ihnen, `true` als letzten Parameter von zu übergeben <xref:System.Printing.PrintQueue.AddJob%28System.String%2CSystem.String%2CSystem.Boolean%29> , ohne dass eine Ausnahme ausgelöst wird. Da jedoch *\<PseudoXPSPrinter>* nicht wirklich ein XPSDrv-Drucker ist, wird nur der Garbage Print gedruckt.

> [!NOTE]
> Der Einfachheit halber verwendet das obige Beispiel das vorhanden sein einer \* XPS-Erweiterung als Test, dass es sich bei einer Datei um XPS handelt. XPS-Dateien müssen diese Erweiterung jedoch nicht haben. Die [isXPS.exe (isXPS-Konformitäts Tool)](/previous-versions/dotnet/netframework-4.0/aa348104(v=vs.100)) ist eine Möglichkeit, eine Datei für die XPS-Gültigkeit zu testen.

## <a name="see-also"></a>Siehe auch

- <xref:System.Printing.PrintQueue>
- <xref:System.Printing.PrintQueue.AddJob%2A>
- <xref:System.Threading.ApartmentState>
- <xref:System.STAThreadAttribute>
- [XPS-Dokumente](/windows/desktop/printdocs/documents)
- [Drucken eines XPS-Dokuments](/previous-versions/dotnet/netframework-3.5/ms771525(v=vs.90))
- [Managed and Unmanaged Threading (Verwaltetes und nicht verwaltetes Threading)](/previous-versions/dotnet/netframework-4.0/5s8ee185(v=vs.100))
- [isXPS.exe (isXPS Conformance Tool) (isXPS.exe (isXPS-Tool für Übereinstimmungstests))](/previous-versions/dotnet/netframework-4.0/aa348104(v=vs.100))
- [Dokumente in WPF](documents-in-wpf.md)
- [Übersicht über das Drucken](printing-overview.md)
