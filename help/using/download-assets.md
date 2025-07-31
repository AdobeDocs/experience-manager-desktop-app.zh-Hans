---
title: 使用 [!DNL Experience Manager] 桌面应用程序下载资源
description: 使用 [!DNL Adobe Experience Manager] 桌面应用程序下载资源。
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 1%

---


# 在本地下载资产 {#download-assets-locally}

应用程序经常将资产从[!DNL Experience Manager]服务器下载到您的本地文件系统。 下载占用带宽和磁盘空间。 了解这些情况可以帮助您优化完成下载的等待时间。 您可以在本地文件系统上下载资产。 应用程序从[!DNL Experience Manager]服务器获取资产，并将相同的副本保存在本地文件系统中。

单击选项的&#x200B;**[!UICONTROL More actions]** ![更多选项图标](assets/do-not-localize/more2_da2.png)，然后单击![下载图标](assets/do-not-localize/download_cloud_da2.png)进行下载。

![资源的下载选项](assets/download_option_da2.png "资源的下载选项")

>[!NOTE]
>
>下载或上传大文件或许多文件时，应用程序会关闭对资源和文件夹的操作。 下载或上传完成后，这些操作将可用。

当您使用[!UICONTROL Open]操作在本机桌面应用程序中打开资产时，如果资产在本地尚不可用，则会本地下载该资产。 查看[打开资产](#openondesktop-v2)。

当您从应用程序中揭示资产或文件夹的位置时，资产或文件夹会首先在本地下载，然后在本地网络共享中的计算机上打开。 查看[打开资产](#openondesktop-v2)。

当您使用[!UICONTROL Edit]操作编辑本地桌面应用程序中的资产时，如果资产在本地尚不可用，则会本地下载该资产。 查看[编辑资源并将更新的资源上传到 [!DNL Experience Manager]](#edit-assets-upload-updated-assets)。

如果已安装应用程序并允许该应用程序，则它会在您从[!UICONTROL Desktop Actions] Web界面使用[!DNL Experience Manager]时完成操作。 应用程序先下载资产，然后完成操作。

## 下载多个资产 {#download-multiple-assets}

如果队列过大，或者遇到网络问题，下载多个资源可能会导致性能不佳。 此外，在下载文件夹时，您可能会无意中将许多资产排入下载队列。 为避免过长的等待时间，应用程序会限制单次下载的资产数量。 要了解如何对其进行配置，请参阅[设置首选项](install-upgrade.md#set-preferences)。 即使低于此限制，应用程序有时也可能在下载明显较大的文件夹之前寻求确认。

![应用程序确认下载相对大量资产](assets/download_confirmation_da2.png "应用程序确认下载相对大量资产")

如果选择并下载文件夹，则应用程序仅下载直接存储在[!DNL Experience Manager]中的文件夹中的资产。 它不会自动从子文件夹下载资产。

## 后续步骤 {#next-steps}

* [观看视频，开始使用Adobe Experience Manager桌面应用程序](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 通过右侧边栏中的[!UICONTROL Edit this page] ![编辑页面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![创建GitHub问题](assets/do-not-localize/github-issue.png)提供文档反馈

* 联系[客户关怀团队](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [上传资源](/help/using/upload-assets.md)
>* [了解用户界面](/help/using/user-interface.md)
>* [搜索](/help/using/search.md)

