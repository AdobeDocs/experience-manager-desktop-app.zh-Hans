---
title: 使用 [!DNL Experience Manager] 桌面应用程序
description: 正在使用 [!DNL Adobe Experience Manager] 桌面应用程序。
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---


# 在桌面上打开资产 {#openondesktop-v2}

您可以打开远程资产，以便在本机应用程序中查看。 资源将下载到本地文件夹。 然后，它们将在与文件格式关联的本机应用程序中启动。 您可以更改本机应用程序，以在Mac或Windows中打开特定的文件类型（扩展名）。

从资源菜单中单击&#x200B;**[!UICONTROL Open]**。 资产将下载到本地，并在本地应用程序中打开。 在状态栏中检查大型资产的下载进度和传输速度。

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>如果应用程序未反映预期的更改，请单击刷新图标![刷新图标](assets/do-not-localize/refresh.png)，或者右键单击应用程序界面并单击&#x200B;**[!UICONTROL Refresh]**。 在大型下载或上传正在进行时，操作不可用。

要打开资源的本地下载文件夹，请单击![更多操作图标](assets/do-not-localize/more2_da2.png)，然后单击![显示图标](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**&#x200B;操作。

## 使用资产或将资产放入本机文档 {#place-assets-in-native-documents}

在某些情况下，例如在将资源放入本机文档时，您可以在Windows资源管理器或Mac Finder中访问文件。 要访问本地下载文件的文件系统位置，请使用![显示图标](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**&#x200B;选项。

![显示资产的文件操作](assets/revealfile_action_da2.png "显示资产的文件操作")

单击文件夹上的&#x200B;**[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**，以使用本地计算机上预先选定的文件或文件夹打开Windows资源管理器或Mac Finder。 例如，在支持放置或链接本地文件的本地应用程序中放置[!DNL Experience Manager]文件时，选项非常有用。 若要了解如何在Adobe InDesign中放置文件，请参阅[放置图形](https://helpx.adobe.com/cn/indesign/using/placing-graphics.html)。

**[!UICONTROL Reveal File]**&#x200B;操作将打开本地网络共享。 它仅显示本地可用的资源。 也就是说，它会显示使用应用程序显示、下载或打开/编辑的资产。 本地网络共享没有将任何更改上传到[!DNL Experience Manager]。 要上载更改，请在应用程序中显式使用&#x200B;**[!UICONTROL Upload Changes]**&#x200B;或&#x200B;**[!UICONTROL Upload]**&#x200B;操作。

>[!NOTE]
>
>为了与[!DNL Experience Manager]桌面应用程序v1.x向后兼容，显示的文件是从本地网络共享提供的，仅公开本地可用文件。 显示文件的桌面路径与应用程序v1.x创建的路径相同。

>[!CAUTION]
>
>请勿使用&#x200B;**[!UICONTROL Reveal File]**&#x200B;选项编辑本机应用程序中的资产。 请改用&#x200B;**[!UICONTROL Edit]**&#x200B;操作。 要了解更多信息，请参阅[高级工作流：对相同的文件进行协作并避免编辑冲突](#adv-workflow-collaborate-avoid-conflicts)。

## 后续步骤 {#next-steps}

* [观看视频，开始使用Adobe Experience Manager桌面应用程序](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 通过右侧边栏中的[!UICONTROL Edit this page] ![编辑页面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![创建GitHub问题](assets/do-not-localize/github-issue.png)提供文档反馈

* 联系[客户关怀团队](https://experienceleague.adobe.com/zh-hans?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [了解用户界面](/help/using/user-interface.md)
>* [在桌面应用程序中管理Assets](/help/using/assets-management-tasks.md)
>* [搜索](/help/using/search.md)
