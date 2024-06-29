---
title: 使用 [!DNL Experience Manager] 桌面应用程序版本1.10。
description: 了解如何使用Adobe Experience Manager桌面应用程序版本1.10并优化您在桌面上使用资源的操作。
feature: Desktop App,Asset Management
exl-id: 2fdc1c8d-b822-4cca-ad06-bd875a00aa6d
source-git-commit: 5676e7ece8bb43f051dae72d17e15ab1c34caefc
workflow-type: tm+mt
source-wordcount: '2329'
ht-degree: 0%

---

# 使用 [!DNL Experience Manager] 桌面应用程序v1.10 {#use-aem-desktop-app-v1x}

使用应用程序，了解 [!DNL Experience Manager] 可以在本地桌面上轻松访问，并可用于任何桌面应用程序。 Assets可以轻松地显示在Mac Finder或Windows资源管理器中，在桌面应用程序中打开，并在本地进行更改 — 更改将保存回 [!DNL Experience Manager] 在存储库中创建一个新版本。

此集成实现了跨Creative Cloud和其他应用程序的集中资产管理和访问，确保符合品牌和其他标准。

您使用执行的主要任务 [!DNL Experience Manager] 桌面应用程序v1包括：

1. [与 [!DNL Experience Manager] 服务器](#installandconnect)
1. [直接在桌面应用程序上打开资产](#openondesktop)
1. [在桌面应用程序中编辑和签出资产](#workonassets)
1. [批量上传资源和文件夹](#bulkupload)

有关各种建议的操作和不建议，请参阅 [使用桌面应用程序的最佳实践](best-practices-for-v1.md). 如果您在使用应用程序时遇到问题，请参阅如何 [故障排除 [!DNL Experience Manager] 桌面应用程序](troubleshoot-app-v1.md).

>[!NOTE]
>
>在中引入了桌面应用程序 [!DNL Experience Manager] 6.1版本，名为 [!DNL Experience Manager Assets Companion App].

## [!DNL Experience Manager] 创意工作流程中的桌面应用程序接触点 {#aem-desktop-app-touch-points-in-the-creative-workflow}

[!DNL Experience Manager] 桌面应用程序，以及 [!DNL Assets]，集成在创意工作流程中，并提供以下接触点。

![[!DNL Experience Manager] 桌面应用程序接触点创作工作流](assets/aem_desktopapp_workflow.png)

[!DNL Experience Manager] 桌面应用程序接触点创作工作流

## 安装应用程序并将其连接到 [!DNL Experience Manager] 服务器 {#installandconnect}

在开始创建或编辑创意资产之前，请将桌面应用程序与 [!DNL Assets] 服务器，用于下载和上传存储库中的资产。 执行以下任务：

1. [安装应用程序](#installapp).
1. [设置您的首选项](#inapppref) 和连接详细信息。
1. [连接到 [!DNL Experience Manager] 服务器](#connect) 并将资产存储库装载为本地驱动器。
1. [启用桌面操作](#desktopactions) 在 [!DNL Experience Manager] 服务器。

此 [!DNL Experience Manager] 桌面应用程序使用HTTPS连接来连接到 [!DNL Experience Manager] 服务器来安全可靠地传输您的资产。

>[!NOTE]
>
>对于所有或部分安装和配置步骤，您可能需要您的 [!DNL Experience Manager] 管理员或系统管理员。

### 安装应用程序 {#installapp}

确保该应用程序支持您使用的Experience Manager服务器版本，以便使用Experience Manager桌面应用程序。 下载适用于您的操作系统(Mac或Windows)的安装文件（二进制文件）并安装应用程序。

根据您的网络和系统首选项，可能需要详细配置。 请参阅 [安装和配置 [!DNL Experience Manager] 桌面应用程序](install-configure-app-v1.md) 以了解更多详细信息。

1. 转到 [[!DNL Experience Manager] 桌面应用程序v1.10下载页面](/help/using/release-notes-of-v1.md) 并下载适用于您的操作系统的二进制文件。
1. 启动下载的安装文件，然后按照屏幕上的说明安装应用程序。

   >[!NOTE]
   >
   >只有一个实例 [!DNL Experience Manager] 桌面应用程序可以一次安装并处于活动状态。

### 了解应用程序内选项和首选项 {#inapppref}

该应用程序允许设置连接和断开连接 [!DNL Experience Manager] 服务器、查看上传状态、管理本地缓存等。 默认设置适用于应用程序的典型用户。 您可以调整设置以充分利用应用程序。 此外，还可充分利用与的集成 [!DNL Experience Manager] 服务器。 以下是各种设置：

**探索Assets** 打开本地驱动器， [!DNL Assets] 存储库已装载。 换句话说，就是要探索现在可在本地计算机上使用的资源。

**查看资源状态** 上传已更改的资源，或将新资源添加到时 [!DNL Assets] 存储库中，应用程序会在后台上传资源。 后台上传可促进顺利操作，无需等待上传完成，尤其是对于大型资产。 您可以在本地保存更改并放弃更改。 应用程序将这些资源发送到服务器需要一些时间，具体取决于可用带宽。 您可以检查上传的状态，以及一些更基本的信息。

**选项** 单击桌面应用程序任务栏中的选项，将应用程序设置为在启动时启动，然后连接到 [!DNL Experience Manager] 启动时的服务器，并更改其本地驱动器号 [!DNL Assets] 安装之后。

**高级>管理缓存** 您可以控制可用于本地缓存的磁盘空间量。 来自的工件 [!DNL Assets] 服务器缓存在本地，以便获得更流畅的体验。 您可以根据自己的要求更改默认值。 此外，您还可以清除缓存以重新获取所有资源。 清除缓存时，它会保留未保存的更改。 任何未签入到中的资产 [!DNL Experience Manager] 服务器将保留，而不是删除。

### 连接到 [!DNL Experience Manager] 服务器 {#connect}

该应用程序支持Mac和Windows上的代理配置。 应用程序启动时会读取配置。 如果修改代理设置，请重新启动应用程序以使更改生效。

>[!NOTE]
>
>如果修改代理设置，请重新启动应用程序以使更改生效。 否则，应用程序将继续使用之前配置的代理服务器。

1. 启动 [!DNL Experience Manager] 桌面应用程序。 映射 [!DNL Experience Manager] 使用应用程序实例，指定您的 [!DNL Experience Manager] 服务器格式 `https://[aem-server-url]:[port]`.

   ![在Mac上进行身份验证并提供 [!DNL Experience Manager] 服务器URL](assets/aem_desktop_app_server_url.png)

1. 在登录屏幕中，指定实例的用户名和密码。 指定替代项 [!DNL Experience Manager] 实例，选择 **[!UICONTROL Alternate Login URL]** 选项。

   ![提供 [!DNL Experience Manager] 打开登录屏幕上的服务器凭据 [!DNL Experience Manager] 桌面应用程序](assets/login_screen_v1.png)

### 在中启用桌面操作 [!DNL Experience Manager] Web界面 {#desktopactions}

在Assets用户界面中，您可以浏览资源位置或签出并打开资源以在桌面应用程序中编辑。 这些选项称为桌面操作，默认情况下不启用。 按照以下步骤启用它。

1. 在Assets界面中，单击/点按工具栏右上角的用户图标。
1. 单击 **[!UICONTROL My Preferences]** 以显示 **[!UICONTROL Preferences]** 对话框。

   ![[!DNL Experience Manager] 界面与用户首选项](assets/aem_ui_user_preferences.png)

1. 在 [!UICONTROL User Preferences] 对话框，选择 **[!UICONTROL Show Desktop Actions For Assets]**，然后单击 **[!UICONTROL Accept]**.

   ![Check [!UICONTROL Show Desktop Actions For Assets] 启用桌面操作](assets/enable_desktop_actions.png)

   *图：检查 [!UICONTROL Show Desktop Actions For Assets] 以启用桌面操作。*

## 在桌面上访问和打开资产 {#openondesktop}

当您单击 **打开** 要在本地计算机上打开资产，应用程序会将资产下载到其内部缓存。 应用程序将启动与所下载资源的文件类型关联的本机桌面应用程序。

在Mac上，选择 **打开** 在上下文菜单中，通过打开资产 [!DNL Experience Manager] 桌面应用程序。 在Windows上，从上下文菜单中选择在Web上打开以打开资产。 在资产状态窗口中，单击/点按 ![“在桌面上打开”图标](assets/do-not-localize/aemassets_icon_openondesktop.png) 以打开资产。

对于Adobe InDesign (INDD)文件，选择 **[!UICONTROL Open]** 从上下文菜单中。 单击此选项后，应用程序会将链接的资源下载到您的本地文件系统，然后在Adobe InDesign中打开INDD文件。 此方法确保在编辑INDD文件时所需的资源可在本地使用。

![上下文菜单选项，用于访问和打开资源，使用 [!DNL Experience Manager] 桌面应用程序](assets/aem_desktopapp_mac_context_menu.png)

*图：用于访问和打开资产的上下文菜单选项 [!DNL Experience Manager] 桌面应用程序。*

>[!NOTE]
>
>Adobe建议您转到Mac上的“查找器查看选项”并停用这些选项 **显示项目信息**， **显示项目预览**、和 **显示预览列** 对于已装载的 [!DNL Assets] 文件夹。 那个提高了性能。

### 中的其他选项 [!DNL Experience Manager] 界面 {#additional-options-in-aem-assets}

在您映射 [!DNL Assets] 存储库到本地驱动器，您可以启用其他图标，并为映射的资产和文件夹显示“文件夹上传”功能。

1. 打开 [!DNL Assets] 界面并将指针悬停在文件夹或资产上，以在卡片视图中将桌面操作显示为快速操作。

   ![在Assets UI中，打开快速操作菜单以查看桌面操作](assets/desktop_actions_in_card_view.png)

   *图：在Assets UI中，打开快速操作菜单以查看桌面操作。*

   单击 **桌面操作** 选择资源后工具栏中的选项，或从资源页面的工具栏中选择所需的选项。

1. 要在桌面应用程序中打开与特定文件扩展名关联的资产，请单击 **在桌面上打开** 快速操作 ![“在桌面上打开”图标](assets/do-not-localize/aemassets_icon_openondesktop.png).

   或者，选择 **打开** 从 **桌面操作** 工具栏中的菜单。

要在本地文件系统中找到特定资源，请单击 **展现** 快速操作 ![“显示”图标](assets/do-not-localize/aemassets_reveal_icon.png). 或者，选择 **展现** 从 **桌面操作** 工具栏中的菜单。

## 了解资源状态 {#understand-the-asset-statuses}

| ![Windows默认应用图标](assets/do-not-localize/win_default.png) | 应用程序已连接到服务器，并且所有资产都已同步。 |
--- |--- |
| ![Windows禁用图标](assets/do-not-localize/win_disabled.png) | 应用程序已启动，但未与服务器连接。 某些资源可能正在挂起同步。 |
| ![Windows文件同步图标](assets/do-not-localize/win_sync.png) | Assets正在同步。 正在上载或下载文件。 您可以从“资源状态”窗口中查看确切的状态并暂停传输。 |
| ![Windows重新连接图标](assets/do-not-localize/win_refresh.png) | 应用程序正在尝试重新连接。 网络问题可能会导致其断开连接。 |

## 处理您的资源 {#workonassets}

### 从签出资产 [!DNL Experience Manager] Web界面 {#check-out-assets-from-the-aem-web-interface}

[!DNL Experience Manager Assets] 可让您签出要编辑的资产，并在完成更改后重新签入这些资产。 签出资源后，只有您可以编辑、注释、发布、移动或删除资源。 签出资产会锁定资产并阻止其他用户执行任何这些操作。 要能够签出/签入资产，您需要具有资产的“写入”权限。

有两种方式可以从签出资产 [!DNL Experience Manager] web界面。 有关第一种方法的详细信息，请参见 [从Assets UI签入和签出文件](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/check-out-and-submit-assets). 对于第二种方法，请按照以下步骤签出并打开资产： [!DNL Experience Manager] 桌面应用程序已安装。

1. 打开 [!DNL Assets] 界面并将指针悬停在文件夹或资产上，以在卡片视图中将桌面操作显示为快速操作。

   ![卡片视图中的“属性”选项](assets/desktop_actions_in_card_view.png)

   选择资产后，单击/点按工具栏中的“桌面操作”图标，或从资产页面的工具栏中，也可以使用这些桌面操作。

1. 要打开资产，请单击/点按在桌面上打开快速操作 ![“在桌面上打开”图标](assets/do-not-localize/aemassets_icon_openondesktop.png).

   或者，从工具栏的“桌面操作”菜单中选择“打开”。

   >[!NOTE]
   >
   >编辑已打开但未签出的文件时，其他用户不知道您正在更新资产。

1. 要打开资源以在Adobe Creative Cloud应用程序中编辑，请单击 ![“编辑桌面”图标](assets/do-not-localize/aemassets_icon_editdesktop.png). 此选项还会签出要编辑的资产。 完成编辑后，签入资产以更新中的更改 [!DNL Assets].

   或者，从工具栏的“桌面操作”菜单中选择“编辑”。

1. 选择“打开”菜单选项。 选定的资产将在预览模式下打开。
1. 要编辑资源，请选择编辑选项。 资产将以编辑模式打开。

### 从macOS上的Finder中查看资源 {#check-out-assets-on-mac}

通过应用程序，您可以签出资产文件，以防止其他用户修改您正在处理的文件。

1. 从Mac上下文菜单中，选择打开AEM Assets文件夹选项以打开Finder。

   ![上下文菜单选项，用于访问和打开资源，使用 [!DNL Experience Manager] 桌面应用程序](assets/aem_desktopapp_mac_context_menu.png)

   *图：用于访问和打开资产的上下文菜单选项 [!DNL Experience Manager] 桌面应用程序。*

1. 导航到要签出的资产。
1. 右键单击资源，然后从上下文菜单中选择更多Assets信息。
1. 在资产信息对话框中，单击/点按签出图标以签出资产。 单击/点按“检出”图标后，可切换到“检入”图标。

   ![浏览到要签出的资源](assets/browse_assets_to_checkout.png)

1. 要签入资产以便其他用户可用，请单击/点按资产信息对话框中的签入图标。

### 在Windows上签出资产 {#check-out-assets-on-windows}

通过应用程序，您可以签出资产文件，以防止其他用户修改您正在处理的文件。

1. 从上下文菜单中，选择浏览Assets以打开资源管理器。
1. 在资源管理器中，导航到要签出的资源的位置。
1. 右键单击资产，然后从上下文菜单中选择在Web上打开。
1. 在“资源信息”对话框中，单击签出图标。 “检出”图标可切换到“检入”图标。

   ![签出图标可切换](assets/checkout_icon_toggles.png)

1. 在Explorer中查看资源。 资源上的锁图标 ![资产锁定图标](assets/do-not-localize/aemassets_icon_lockcheckout.png) 表示您已签出资源。

   >[!NOTE]
   >
   >锁定图标可能会在一段延迟后显示。 此 [!DNL Experience Manager] 桌面应用程序会缓存资源以供快速访问，因此可能需要几分钟才能更新锁定状态。

1. 要检入资产以便其他用户可用，请单击/点按资产中的检入图标。 **资源信息** 对话框。

### 使用Finder或Explorer并使用Web界面签入资源 {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface}

编辑完资源后，将资源保存在桌面应用程序中。 从上下文菜单中，选择 **更多Assets信息** 并单击“检入”。

资源将上传到 [!DNL Experience Manager] 服务器。 （可选）您可以通过选择 **查看资源状态** 从系统托盘图标。 或者，您可以从以下位置签入资产： [!DNL Experience Manager] web界面。 单击已签出的资源或将其选定。 在工具栏中，单击检入图标 ![签入图标](assets/do-not-localize/aemassets_icon_checkin.png).

资产上传至 [!DNL Experience Manager] 本地保存任何更改后会自动进行更改。 签入后，其他人便可以使用该资产 [!DNL Experience Manager] 用户进行编辑。

### 将资源和文件夹批量上传到 [!DNL Experience Manager] 服务器 {#bulkupload}

使用 [!DNL Experience Manager] 对于桌面应用程序，您可以将包含资产的整个文件夹从本地文件目录上传到 [!DNL Assets]. 这样，文件夹中的所有资产都会批量上传，而不必一次上传一个。

1. 在Assets UI中，单击/点按 **创建** 在工具栏中，然后从菜单中选择 **上传文件夹**.
1. 浏览到要上传的文件夹并将其选定。
1. 单击/点按确定。 Assets状态对话框显示上传的状态。

   ![在资产状态窗口中查看上传状态](assets/aem_desktopapp_bulkupload_status.png)

   在资产状态窗口中查看上传状态

   >[!NOTE]
   >
   >您可以通过单击/点按相应的图标来手动暂停或取消上传。

1. 文件夹上传后，关闭对话框并导航到Assets UI。 上传的文件夹会显示在Web界面中。

Adobe不建议复制粘贴或将更多文件或嵌套文件夹从本地文件系统拖到网络共享区域中。 由于技术限制和性能不佳，应用程序无法控制上传过程。

或者，在Finder或Explorer中选择文件/文件夹，复制它们，导航到网络共享区域中的目标文件夹，然后选择 **粘贴Assets** 从 [!DNL Experience Manager] 桌面应用程序上下文菜单。 这边， [!DNL Experience Manager] 桌面应用程序开始上传粘贴的资产，类似于 **上传文件夹** 中提供的选项 [!DNL Experience Manager] web界面。

>[!MORELIKETHIS]
>
>* [疑难解答 [!DNL Experience Manager] 桌面应用程序应用程序](troubleshoot-app-v1.md)
