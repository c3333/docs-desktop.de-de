---
title: 'Gewusst wie: Aufrufen eines Druckdialogfelds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- invoking print dialogs [WPF]
- print dialogs [WPF], invoking
ms.assetid: e3a2c84c-74fe-45a4-8501-5813f9dbfed2
ms.openlocfilehash: f6e85afc40d5736de94ff7851d1db2c8007720d0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975346"
---
# <a name="how-to-invoke-a-print-dialog"></a><span data-ttu-id="a3412-102">Gewusst wie: Aufrufen eines Druckdialogfelds</span><span class="sxs-lookup"><span data-stu-id="a3412-102">How to: Invoke a Print Dialog</span></span>
<span data-ttu-id="a3412-103">Um die Möglichkeit zum Drucken von Ihrer Anwendung bereitzustellen, können Sie einfach ein-Objekt erstellen und öffnen <xref:System.Windows.Controls.PrintDialog> .</span><span class="sxs-lookup"><span data-stu-id="a3412-103">To provide the ability to print from you application, you can simply create and open a <xref:System.Windows.Controls.PrintDialog> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3412-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3412-104">Example</span></span>  
 <span data-ttu-id="a3412-105">Das- <xref:System.Windows.Controls.PrintDialog> Steuerelement stellt einen einzelnen Einstiegspunkt für die [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] -,-Konfigurations-und XPS-Auftrags Übermittlung bereit.</span><span class="sxs-lookup"><span data-stu-id="a3412-105">The <xref:System.Windows.Controls.PrintDialog> control provides a single entry point for [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)], configuration, and XPS job submission.</span></span> <span data-ttu-id="a3412-106">Das-Steuerelement ist einfach zu verwenden und kann mithilfe von Markup oder Code instanziiert werden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="a3412-106">The control is easy to use and can be instantiated by using [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] markup or code.</span></span> <span data-ttu-id="a3412-107">Im folgenden Beispiel wird veranschaulicht, wie das-Steuerelement im Code instanziiert und geöffnet wird und wie daraus gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="a3412-107">The following example demonstrates how to instantiate and open the control in code and how to print from it.</span></span> <span data-ttu-id="a3412-108">Außerdem wird gezeigt, wie sichergestellt wird, dass im Dialogfeld der Benutzer die Möglichkeit erhält, einen bestimmten Seitenbereich festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a3412-108">It also shows how to ensure that the dialog will give the user the option of setting a specific range of pages.</span></span> <span data-ttu-id="a3412-109">Im Beispielcode wird davon ausgegangen, dass sich die Datei "FixedDocumentSequence. XPS" im Stammverzeichnis des Laufwerks C: befindet.</span><span class="sxs-lookup"><span data-stu-id="a3412-109">The example code assumes that there is a file FixedDocumentSequence.xps in the root of the C: drive.</span></span>  
  
 [!code-csharp[printdialog#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PrintDialog/CSharp/Window1.xaml.cs#1)]
 [!code-vb[printdialog#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PrintDialog/visualbasic/window1.xaml.vb#1)]  
  
 <span data-ttu-id="a3412-110">Wenn das Dialogfeld geöffnet ist, können Benutzer aus den Druckern auswählen, die auf Ihrem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="a3412-110">Once the dialog is open, users will be able to select from the printers installed on their computer.</span></span> <span data-ttu-id="a3412-111">Sie haben auch die Möglichkeit, den [Microsoft XPS-Dokument-Writer](/windows/win32/printdocs/microsoft-xps-document-writer) auszuwählen, um eine XPS-Datei (XML Paper Specification) zu erstellen, anstatt Sie zu drucken.</span><span class="sxs-lookup"><span data-stu-id="a3412-111">They will also have the option of selecting the [Microsoft XPS Document Writer](/windows/win32/printdocs/microsoft-xps-document-writer) to create an XML Paper Specification (XPS) file instead of printing.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a3412-112">Das <xref:System.Windows.Controls.PrintDialog?displayProperty=nameWithType> WPF-Steuerelement, das in diesem Thema erläutert wird, sollte nicht mit der- <xref:System.Windows.Forms.PrintDialog?displayProperty=nameWithType> Komponente von Windows Forms verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="a3412-112">The <xref:System.Windows.Controls.PrintDialog?displayProperty=nameWithType> control of WPF, which is discussed in this topic, should not be confused with the <xref:System.Windows.Forms.PrintDialog?displayProperty=nameWithType> component of Windows Forms.</span></span>  
  
 <span data-ttu-id="a3412-113">Streng genommen können Sie die Methode verwenden, <xref:System.Windows.Controls.PrintDialog.PrintDocument%2A> ohne das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3412-113">Strictly speaking, you can use the <xref:System.Windows.Controls.PrintDialog.PrintDocument%2A> method without ever opening the dialog.</span></span> <span data-ttu-id="a3412-114">In diesem Sinne kann das Steuerelement als nicht gesehene Druckkomponente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3412-114">In that sense, the control can be used as an unseen printing component.</span></span> <span data-ttu-id="a3412-115">Aus Leistungsgründen wäre es jedoch besser, entweder die <xref:System.Printing.PrintQueue.AddJob%2A> -Methode oder eine der vielen <xref:System.Windows.Xps.XpsDocumentWriter.Write%2A> -und- <xref:System.Windows.Xps.XpsDocumentWriter.WriteAsync%2A> Methoden von zu verwenden <xref:System.Windows.Xps.XpsDocumentWriter> .</span><span class="sxs-lookup"><span data-stu-id="a3412-115">But for performance reasons, it would be better to use either the <xref:System.Printing.PrintQueue.AddJob%2A> method or one of the many <xref:System.Windows.Xps.XpsDocumentWriter.Write%2A> and <xref:System.Windows.Xps.XpsDocumentWriter.WriteAsync%2A> methods of the <xref:System.Windows.Xps.XpsDocumentWriter>.</span></span> <span data-ttu-id="a3412-116">Weitere Informationen hierzu finden Sie unter [Programm gesteuertes Drucken von XPS-Dateien](how-to-programmatically-print-xps-files.md).</span><span class="sxs-lookup"><span data-stu-id="a3412-116">For more about this, see [Programmatically Print XPS Files](how-to-programmatically-print-xps-files.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3412-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3412-117">See also</span></span>

- <xref:System.Windows.Controls.PrintDialog>
- [<span data-ttu-id="a3412-118">Dokumente in WPF</span><span class="sxs-lookup"><span data-stu-id="a3412-118">Documents in WPF</span></span>](documents-in-wpf.md)
- [<span data-ttu-id="a3412-119">Übersicht über das Drucken</span><span class="sxs-lookup"><span data-stu-id="a3412-119">Printing Overview</span></span>](printing-overview.md)
- [<span data-ttu-id="a3412-120">Microsoft XPS-Dokument-Generator</span><span class="sxs-lookup"><span data-stu-id="a3412-120">Microsoft XPS Document Writer</span></span>](/windows/win32/printdocs/microsoft-xps-document-writer)
