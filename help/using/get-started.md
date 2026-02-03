---
title: 开始使用 [!DNL Experience Manager] 桌面应用程序
description: 了解 [!DNL Experience Manager] 桌面应用程序如何通过简化的工作流和生产力功能来增强内容创建和发布。
feature: Desktop App,Asset Management
exl-id: 6cf29b6a-74e6-4860-a25b-d3e91abbaa9d
source-git-commit: 2bf5ee7454846c288cc1c976d8f69c6bfed8eabf
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 0%

---

# 开始使用[!DNL Adobe Experience Manager]桌面应用程序 {#getting-started-desktop-app}

使用[!DNL Adobe Experience Manager]桌面应用程序访问本地桌面上[!DNL Adobe Experience Manager] DAM存储库中存储的数字资产。 然后，您可以在任何桌面应用程序中使用这些资产。 您可以在桌面应用程序中本地打开和编辑资产。 进行更改后，使用版本控制将它们上载回[!DNL Experience Manager]以与其他用户共享更新。 您还可以将新文件和文件夹层次结构上传到[!DNL Experience Manager]，创建文件夹，以及从[!DNL Experience Manager] DAM中删除资源或文件夹。

通过集成，组织中的各种角色可以在[!DNL Experience Manager Assets]中集中管理资源，并在Windows或macOS上的本机应用程序中访问本地桌面上的资源。

在注销后或首次打开应用程序时，请以[!DNL Experience Manager]格式提供`https://[aem-server-url]:[port]/`服务器的URL。 然后选择[!UICONTROL Connect]选项。 提供凭据以将应用程序与服务器连接。

>[!VIDEO](https://video.tv.adobe.com/v/32780?captions=chi_hans&quality=12&learn=on){transcript=true}

使用[!DNL Adobe Experience Manager]桌面应用程序执行的主要任务包括：

![您可以使用[!DNL Experience Manager]桌面应用程序完成的工作流和任务](assets/aem_desktop_app_usecases_v2.png)

## 桌面应用程序的工作原理 {#how-app-works2}

在开始使用应用程序之前，请先了解[应用程序的工作方式](release-notes.md#how-app-works)。 此外，请熟悉以下术语：

* **[!UICONTROL Desktop Actions]**：在Assets Web界面中，您可以在浏览器中浏览资源位置或签出并打开资源以在本机桌面应用程序中编辑。 这些操作可从Web界面中获取，并且可使用桌面应用程序功能。

* 文件状态为&#x200B;**[!UICONTROL Cloud Only]**：此类资源未下载到本地计算机上，仅在[!DNL Experience Manager]服务器上可用。

* 文件状态为&#x200B;**[!UICONTROL Available locally]**：资源已下载并在本地计算机上可用。 资产不变。

* 文件状态为&#x200B;**[!UICONTROL Edited locally]**：此类资源已在本地修改，更改仍保留在上传到[!DNL Experience Manager]服务器中。 上传后，状态将更改为[!UICONTROL Available locally]。 请参阅[编辑资源](upload-assets.md#edit-assets-upload-updated-assets)。

* 文件状态为&#x200B;**[!UICONTROL Editing conflict]**：如果您和其他人同时编辑某个资产，则应用程序指示发生了编辑冲突。 该应用程序还提供了保留或放弃更改的选项。 请参阅[如何避免编辑冲突](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts)。

* 文件状态为&#x200B;**[!UICONTROL Modified remotely]**：应用程序指示您下载的资源是否在[!DNL Experience Manager]服务器上发生更改。 该应用程序还提供了下载最新版本和更新本地副本的选项。 请参阅[如何避免编辑冲突](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts)。

* **[!UICONTROL Check-out]**：如果您正在编辑文件或打算编辑文件，请将状态切换为签出。 它在应用程序和[!DNL Experience Manager] Web界面中的资产上添加了锁图标。 锁定图标会向其他用户指示以避免同时编辑相同的资源，因为它会导致编辑冲突。

* **[!UICONTROL Check-in]**：将资产标记为可供其他用户编辑的安全资产，而不会导致编辑冲突。 上传更改时，锁定图标将自动移除。 切换签入状态也会删除锁定图标，但Adobe建议您避免手动签入而不上传更改。 如果您放弃更改，请手动切换签入。

* **[!UICONTROL Open]**&#x200B;操作：只需打开资源即可在本机应用程序中预览它。 Adobe建议您避免使用此操作编辑资源。 原因是它不会签出资产。 同时，其他用户也可以进行编辑，导致编辑冲突。

* **[!UICONTROL Edit]**&#x200B;操作：使用操作修改图像。 单击[!UICONTROL Edit]可签出资产并在该资产上添加一个锁定图标。 单击“编辑”后，如果不想编辑该资产，请单击[!UICONTROL Toggle check-in]。 要删除、重命名或移动[!DNL Experience Manager] DAM文件夹层次结构中的资产，请使用[!DNL Experience Manager] Web界面操作，而不是编辑操作。

* **[!UICONTROL Download]**&#x200B;操作：将资源下载到本地计算机。 您可以立即下载资产并稍后编辑；脱机工作并稍后上传更改。 Assets将下载到您文件系统的缓存文件夹中。

* **[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**&#x200B;操作：将资产下载到本地缓存文件夹时，应用程序将模拟本地网络驱动器。 它为每个资源提供本地路径。 要了解此路径，请使用应用程序中的相应显示选项。 在Creative Cloud应用程序中放置资源时，需要执行展现操作。 查看[放置资源](search.md#place-assets-in-native-documents)。

* **[!UICONTROL Open In Web]**&#x200B;操作：要在[!DNL Experience Manager] Web界面中查看资产，请在Web中打开该资产。 您可以从[!DNL Experience Manager]界面启动更多工作流，如更新元数据或资源发现。

* **[!UICONTROL Delete]**&#x200B;操作：从[!DNL Experience Manager] DAM存储库中删除资产。 该操作会删除Experience Manager服务器上资源的原始副本。 如果只想放弃对本地资产的修改，请参阅[放弃更改](upload-assets.md#edit-assets-upload-updated-assets)。

* **[!UICONTROL Upload Changes]**：仅在您明确上载到[!DNL Experience Manager]服务器时，桌面应用才会上载更新的资产。 在保存编辑时，更改仅保存在本地计算机上。 上传时，资产会自动签入，并且锁图标会被移除。 请参阅[编辑资源](upload-assets.md#edit-assets-upload-updated-assets)。

## 在[!DNL Experience Manager] Web界面中启用桌面操作 {#desktopactions-v2}

从浏览器的[!DNL Assets]用户界面中，您可以浏览资产位置或签出并打开资产以在桌面应用程序中编辑。 这些选项称为[!UICONTROL Desktop Actions]，默认不启用。 要启用此功能，请执行以下步骤。

1. 在[!DNL Assets]控制台中，单击工具栏中的&#x200B;**[!UICONTROL User]**&#x200B;图标。
1. 单击&#x200B;**[!UICONTROL My Preferences]**&#x200B;以显示&#x200B;**[!UICONTROL Preferences]**&#x200B;对话框。

1. 在[!UICONTROL User Preferences]对话框中，选择&#x200B;**[!UICONTROL Show Desktop Actions For Assets]**，然后单击&#x200B;**[!UICONTROL Accept]**。

   ![选择“显示Assets的桌面操作”以启用桌面操作](assets/enable_desktop_actions1.png)

## 从[!DNL Assets] Web界面开始 {#adv-workflow-start-from-aem-ui}

如有必要，请从Assets Web界面启动工作流。 该桌面应用程序与[!DNL Experience Manager]集成，以便在使用桌面操作请求时接管。

从Web界面启动工作流的一个特殊情况是资产发现。 Assets用户界面中的Omnisearch栏提供了丰富而高级的搜索体验。 您可能希望首先在Web上找到所需的资产，然后使用[!UICONTROL Desktop Actions]在应用程序中启动工作流。 一些示例示例示例示例包括使用Facet筛选搜索结果、查找从Adobe Stock许可的特定资源，或由您的组织实施的自定义项，该自定义项允许您更好地从Web界面中发现。

当您尝试在Assets Web界面上执行以下操作时，将会使用桌面应用程序功能：

* 允许[!UICONTROL Desktop Actions]、[!UICONTROL Open]和[!UICONTROL Edit]的[!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] 或 [!UICONTROL check-in]

例如，对于应用程序中签出的资产，Web界面上的可用操作为[!UICONTROL Open]、[!UICONTROL Reveal]和[!UICONTROL Check in]。

![Web界面中的[!DNL Experience Manager]桌面操作](assets/assets_web_actions_da2.png "Experience Manager Web界面中的")桌面操作

>[!NOTE]
>
>浏览器可能会提示您允许启动[!DNL Adobe Experience Manager]桌面。 要使每次从浏览器传输至应用程序时不会出现中断，请选中相应的复选框以允许应用程序接管任务。

使用Web界面无法找到以下信息或工作流。 使用桌面应用程序，因为Web界面不跟踪本地更改，并且不知道以下内容：

* 在本地编辑文件。
* 存在编辑冲突的文件以及解决该冲突的方法。
* 将本地更改上载到[!DNL Experience Manager]。
* 本地可用文件的各种状态。

相反，您可以使用&#x200B;**[!UICONTROL Open In Web]**&#x200B;操作从桌面应用程序开始在Web界面中打开资产。

## 后续步骤 {#next-steps}

* [观看视频，开始使用Adobe Experience Manager桌面应用程序](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 通过右侧边栏中的[!UICONTROL Edit this page] ![编辑页面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![创建GitHub问题](assets/do-not-localize/github-issue.png)提供文档反馈

* 联系[客户关怀团队](https://experienceleague.adobe.com/zh-hans?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [了解用户界面](/help/using/user-interface.md)
>* [发行说明和已知问题](/help/using/release-notes.md)
>* [安装或升级桌面应用程序](/help/using/install-upgrade.md)
