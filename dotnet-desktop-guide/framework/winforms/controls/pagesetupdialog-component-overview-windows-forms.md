---
title: Übersicht über die PageSetupDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- PageSetupDialog
helpviewer_keywords:
- Page Setup dialog box [Windows Forms], displaying
- PageSetupDialog component
ms.assetid: 791caacb-a5ca-4fca-bad9-1a5721ad697c
ms.openlocfilehash: a891cb8cc77007d7591d41461c94f61c077eb300
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976685"
---
# <a name="pagesetupdialog-component-overview-windows-forms"></a>Übersicht über die PageSetupDialog-Komponente (Windows Forms)

Bei der Windows Forms <xref:System.Windows.Forms.PageSetupDialog> Komponente handelt es sich um ein vorkonfiguriertes Dialogfeld, mit dem Seitendetails für das Drucken in Windows-basierten Anwendungen festgelegt werden. Verwenden Sie es in Ihrer Windows-basierten Anwendung als einfache Lösung, damit Benutzer Seiteneinstellungen festlegen können, anstatt ein eigenes Dialogfeld zu konfigurieren. Sie können es Benutzern ermöglichen, Rahmen-und Rand Anpassungen, Kopf-und Fußzeilen sowie hoch-oder Querformat festzulegen. Durch die Verwendung von Windows-Standarddialogfeldern erstellen Sie Anwendungen, deren Basisfunktionen Benutzern sofort vertraut sind.

## <a name="key-properties-and-methods"></a>Schlüsseleigenschaften und-Methoden

Verwenden Sie die- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode, um das Dialogfeld zur Laufzeit anzuzeigen. Diese Komponente verfügt über Eigenschaften, die Sie festlegen können, die sich auf eine einzelne Seite ( <xref:System.Drawing.Printing.PrintDocument> Klasse) oder ein beliebiges Dokument ( <xref:System.Drawing.Printing.PageSettings> Klasse) beziehen. Außerdem kann die- <xref:System.Windows.Forms.PageSetupDialog> Komponente verwendet werden, um bestimmte Druckereinstellungen zu bestimmen, die in der-Klasse gespeichert werden <xref:System.Drawing.Printing.PrinterSettings> .

Wenn Sie einem Formular hinzugefügt wird, wird die <xref:System.Windows.Forms.PageSetupDialog> Komponente in der Leiste am unteren Rand des Windows Forms-Designer in Visual Studio angezeigt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.PageSetupDialog>
- [PageSetupDialog-Komponente](pagesetupdialog-component-windows-forms.md)
