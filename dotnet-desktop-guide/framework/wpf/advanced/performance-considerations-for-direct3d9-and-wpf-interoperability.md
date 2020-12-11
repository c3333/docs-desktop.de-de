---
title: Überlegungen zur Leistung bei von Direct3D9 und WPF-Interop
titleSuffix: ''
ms.date: 03/30/2017
helpviewer_keywords:
- WPF [WPF], Direct3D9 interop performance
- Direct3D9 [WPF interoperability], performance
ms.assetid: ea8baf91-12fe-4b44-ac4d-477110ab14dd
ms.openlocfilehash: 2445732c27d210a41da26303d6a9ce07ef6fcc94
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976213"
---
# <a name="performance-considerations-for-direct3d9-and-wpf-interoperability"></a>Überlegungen zur Leistung für die Interoperabilität zwischen Direct3D9 und WPF
Von Direct3D9-Inhalte können mithilfe der-Klasse gehostet werden <xref:System.Windows.Interop.D3DImage> . Hosting von Direct3D9 Inhalte können sich auf die Leistung Ihrer Anwendung auswirken. In diesem Thema werden bewährte Methoden zum Optimieren der Leistung beim Hosting von von Direct3D9-Inhalten in einer Windows Presentation Foundation (WPF)-Anwendung beschrieben. Zu diesen bewährten Methoden gehört die Verwendung von <xref:System.Windows.Interop.D3DImage> und bewährten Methoden bei der Verwendung von Windows Vista, Windows XP und Multimonitor-anzeigen.  
  
> [!NOTE]
> Codebeispiele, die diese bewährten Methoden veranschaulichen, finden Sie unter [WPF-und von Direct3D9-Interoperation](wpf-and-direct3d9-interoperation.md).  
  
## <a name="use-d3dimage-sparingly"></a>D3DImage sparsam verwenden  
 Von Direct3D9-Inhalte, die in einer-Instanz gehostet werden, werden <xref:System.Windows.Interop.D3DImage> nicht so schnell wie in einer reinen Direct3D-Anwendung dargestellt. Das Kopieren der Oberfläche und das Leeren des Befehls Puffers kann zu kostspieligen Operationen werden. Wenn die Anzahl der <xref:System.Windows.Interop.D3DImage> Instanzen zunimmt, wird eine größere Leerung durchgeführt, und die Leistung wird beeinträchtigt. Daher sollten Sie sparsam verwenden <xref:System.Windows.Interop.D3DImage> .  
  
## <a name="best-practices-on-windows-vista"></a>Bewährte Methoden für Windows Vista  
 Für eine optimale Leistung unter Windows Vista mit einer Anzeige, die für die Verwendung des Windows-Anzeigetreiber Modells (WDDM) konfiguriert ist, erstellen Sie die von Direct3D9-Oberfläche auf einem `IDirect3DDevice9Ex` Gerät. Dadurch wird die Oberflächen Freigabe ermöglicht. Die Grafikkarte muss die `D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES` `D3DCAPS2_CANSHARERESOURCE` Treiberfunktionen und unter Windows Vista unterstützen. Alle anderen Einstellungen bewirken, dass die Oberfläche durch Software kopiert wird, wodurch die Leistung erheblich reduziert wird.  
  
> [!NOTE]
> Wenn Windows Vista eine Anzeige aufweist, die für die Verwendung des Windows XP-Anzeigetreiber Modells (XDDM) konfiguriert ist, wird die Oberfläche unabhängig von den Einstellungen immer durch Software kopiert. Mit den richtigen Einstellungen und der entsprechenden Grafikkarte sehen Sie unter Windows Vista eine bessere Leistung, wenn Sie WDDM verwenden, da Oberflächen Kopien in der Hardware ausgeführt werden.  
  
## <a name="best-practices-on-windows-xp"></a>Bewährte Methoden für Windows XP  
 Für eine optimale Leistung unter Windows XP, bei der das Windows XP-Anzeigetreiber Modell (XDDM) verwendet wird, erstellen Sie eine Sperr Bare Oberfläche, die beim Aufrufen der-Methode ordnungsgemäß verhält `IDirect3DSurface9::GetDC` . Intern überträgt die- `BitBlt` Methode die-Oberfläche über Geräte in der Hardware. Die- `GetDC` Methode funktioniert immer auf xrgb-Oberflächen. Wenn auf dem Client Computer jedoch Windows XP mit SP3 oder SP2 ausgeführt wird und der Client auch über den Hotfix für die Funktion "überlappendes Fenster" verfügt, funktioniert diese Methode nur auf ARGB-Oberflächen. Die Grafikkarte muss die `D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES` Treiber Funktion unterstützen.  
  
 Eine 16-Bit-Desktop Anzeige Tiefe kann die Leistung erheblich beeinträchtigen. Ein 32-Bit-Desktop wird empfohlen.  
  
 Wenn Sie für Windows Vista und Windows XP entwickeln, testen Sie die Leistung unter Windows XP. Der Video Arbeitsspeicher unter Windows XP ist von großer Bedeutung. Außerdem <xref:System.Windows.Interop.D3DImage> verwendet Windows XP mehr Video Arbeitsspeicher und Bandbreite als Windows Vista WDDM, aufgrund einer erforderlichen zusätzlichen Videospeicher Kopie. Daher können Sie erwarten, dass die Leistung bei Windows XP schlechter ist als bei Windows Vista für die gleiche Video Hardware.  
  
> [!NOTE]
> XDDM ist sowohl unter Windows XP als auch unter Windows Vista verfügbar. WDDM steht jedoch nur unter Windows Vista zur Verfügung.  
  
## <a name="general-best-practices"></a>Allgemeine bewährte Methoden  
 Verwenden Sie beim Erstellen des Geräts das `D3DCREATE_MULTITHREADED` Erstellungsflag. Dadurch wird die Leistung reduziert, das WPF-Renderingsystem ruft jedoch Methoden auf diesem Gerät von einem anderen Thread auf. Achten Sie darauf, dass Sie das Sperrprotokoll ordnungsgemäß befolgen, damit keine zwei Threads gleichzeitig auf das Gerät zugreifen.  
  
 Wenn Ihr Rendering in einem verwalteten WPF-Thread ausgeführt wird, wird dringend empfohlen, das Gerät mit dem Erstellungs Kennzeichen zu erstellen `D3DCREATE_FPU_PRESERVE` . Ohne diese Einstellung kann das D3D-Rendering die Genauigkeit von WPF-Vorgängen mit doppelter Genauigkeit verringern und Renderingprobleme einleiten.  
  
 Das Tick a <xref:System.Windows.Interop.D3DImage> ist schnell, es sei denn, Sie Kacheln eine nicht-pow2-Oberfläche ohne Hardwareunterstützung, oder wenn Sie ein-oder ein-oder ein- <xref:System.Windows.Media.DrawingBrush> oder- <xref:System.Windows.Media.VisualBrush> <xref:System.Windows.Interop.D3DImage>  
  
## <a name="best-practices-for-multi-monitor-displays"></a>Bewährte Methoden für die Anzeige mit mehreren Monitoren  
 Wenn Sie einen Computer verwenden, der über mehrere Monitore verfügt, sollten Sie die zuvor beschriebenen bewährten Methoden befolgen. Es gibt auch einige zusätzliche Überlegungen zur Leistung bei einer Konfiguration mit mehreren Monitoren.  
  
 Wenn Sie den Hintergrund Puffer erstellen, wird er auf einem bestimmten Gerät und Adapter erstellt, aber WPF zeigt möglicherweise den Front-Puffer auf jedem Adapter an. Das Kopieren zwischen Adaptern zum Aktualisieren des Front Puffers kann sehr kostspielig sein. Bei Windows Vista, das für die Verwendung von WDDM mit mehreren Grafikkarten und einem Gerät konfiguriert ist `IDirect3DDevice9Ex` , gibt es keine Leistungs Einbuße, wenn sich der Front-Puffer auf einem anderen Adapter, aber immer noch auf derselben Grafikkarte befindet. Bei Windows XP und XDDM mit mehreren Grafikkarten gibt es jedoch eine erhebliche Leistungs Einbuße, wenn der Front-Puffer auf einem anderen Adapter als der Hintergrund Puffer angezeigt wird. Weitere Informationen finden Sie unter [WPF-und von Direct3D9-Interoperation](wpf-and-direct3d9-interoperation.md).  
  
## <a name="performance-summary"></a>Leistungs Zusammenfassung  
 In der folgenden Tabelle wird die Leistung des Front-Puffer-Updates als Funktion des Betriebssystems, des Pixel Formats und der Oberfläche zur sperrensperrung angezeigt. Es wird davon ausgegangen, dass sich der Vorder-und Hintergrund Puffer auf demselben Adapter befinden. Abhängig von der Adapter Konfiguration sind Hardware Updates in der Regel viel schneller als Software Updates.  
  
|Surface-Pixel-Format|Windows Vista, WDDM und 9Ex|Weitere Windows Vista-Konfigurationen|Windows XP SP3 oder SP2 w/Hotfix|Windows XP SP2|  
|--------------------------|---------------------------------|----------------------------------------|--------------------------------------|--------------------|  
|D3DFMT_X8R8G8B8 (nicht Sperr fähig)|**Hardware Update**|Softwareupdate|Softwareupdate|Softwareupdate|  
|D3DFMT_X8R8G8B8 (Sperr fähig)|**Hardware Update**|Softwareupdate|**Hardware Update**|**Hardware Update**|  
|D3DFMT_A8R8G8B8 (nicht Sperr fähig)|**Hardware Update**|Softwareupdate|Softwareupdate|Softwareupdate|  
|D3DFMT_A8R8G8B8 (Sperr fähig)|**Hardware Update**|Softwareupdate|**Hardware Update**|Softwareupdate|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Interop.D3DImage>
- [Interaktion zwischen WPF und Direct3D9](wpf-and-direct3d9-interoperation.md)
- [Exemplarische Vorgehensweise: Erstellen von Direct3D9-Inhalten zum Hosten in WPF](walkthrough-creating-direct3d9-content-for-hosting-in-wpf.md)
- [Exemplarische Vorgehensweise: Hosten von Direct3D9-Inhalt in WPF](walkthrough-hosting-direct3d9-content-in-wpf.md)
