---
title: 如何：在设计时复制并粘贴 ElementHost 控件
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, content copying and pasting
- interoperability [WPF]
- ElementHost control [Windows Forms], copying and pasting at design time
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: e570375d-2a68-44ba-b4f7-c781af2d20e8
ms.openlocfilehash: 43ebe50497df97511925bd2e413ab5b5988b7f57
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/14/2018
ms.locfileid: "45624783"
---
# <a name="how-to-copy-and-paste-an-elementhost-control-at-design-time"></a>如何：在设计时复制并粘贴 ElementHost 控件
此过程演示如何将复制在 Windows 窗体上的 Windows Presentation Foundation (WPF) 控件。  
  
> [!NOTE]
>  显示的对话框和菜单命令可能会与“帮助”中的描述不同，具体取决于你现用的设置或版本。 若要更改设置，请在 **“工具”** 菜单上选择 **“导入和导出设置”** 。 有关详细信息，请参阅[个性化设置 Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide)。  
  
### <a name="to-copy-and-paste-an-elementhost-control-at-design-time"></a>若要复制并粘贴 ElementHost 控件在设计时  
  
1.  添加新的 WPF<xref:System.Windows.Controls.UserControl>到 Windows 窗体项目。 使用控件类型的默认名称，`UserControl1.xaml`。 有关详细信息，请参阅[演练： 创建新 WPF 内容在设计时的 Windows 窗体上](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)。  
  
2.  在中**属性**窗口中，设置的值<xref:System.Windows.FrameworkElement.Width%2A>并<xref:System.Windows.FrameworkElement.Height%2A>的属性`UserControl1`到`200`。  
  
3.  将 <xref:System.Windows.Controls.Control.Background%2A> 属性的值设置为 `Blue`。  
  
4.  生成项目。  
  
5.  在 Windows 窗体设计器中打开 `Form1`。  
  
6.  从**工具箱**，将拖动的一个实例`UserControl1`拖到窗体。  
  
     `UserControl1` 的实例托管在名为 `elementHost1` 的新 <xref:System.Windows.Forms.Integration.ElementHost> 控件中。  
  
7.  选择`elementHost1` 后，按 CTRL + C 将它复制到剪贴板。  
  
8.  按 CTRL + V 粘贴复制的控件拖到窗体。  
  
     一个新<xref:System.Windows.Forms.Integration.ElementHost>名为控件`elementHost2`窗体上创建。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [演练：将 ElementHost 控件复制并粘贴到各个 Windows 窗体中](../../../../docs/framework/winforms/advanced/copy--paste-an-elementhost-control-into-forms.md)  
 [迁移和互操作性](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)  
 [使用 WPF 控件](../../../../docs/framework/winforms/advanced/using-wpf-controls.md)  
 [在 Visual Studio 中设计 XAML](/visualstudio/designers/designing-xaml-in-visual-studio)
