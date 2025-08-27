---
title: 使用 [!DNL Experience Manager] 桌面应用程序上传资源
description: 使用 [!DNL Adobe Experience Manager] 桌面应用程序上传资源。
feature: Desktop App,Asset Management
exl-id: f082c712-dc04-4bed-bac8-fa78f93de1c7
source-git-commit: db592420ded4d2f7288982a1ea17618484c82537
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 1%

---

# 上传资产 {#upload-assets}

有权添加资产的AEM桌面应用程序用户可以添加资产（如图像、文档、视频或其他媒体）。

## 编辑资源并将更新的资源上传到[!DNL Experience Manager] {#edit-assets-upload-updated-assets}

当您想要进行更改并将更新的资产上传到[!DNL Experience Manager]服务器时，请打开资产进行编辑。 要避免与其他用户的编辑发生冲突，请使用应用程序启动编辑会话。 在开始编辑之前，请确保资产上没有任何锁图标，指示另一个用户正在编辑该资产。

要编辑资源，请搜索资源或浏览到资源的位置。 单击![更多图标](assets/do-not-localize/more2_da2.png)，然后单击&#x200B;**[!UICONTROL Edit]**。

使用&#x200B;**[!UICONTROL Toggle Check-out]**&#x200B;锁定资产，以防止在以下两种情况下与其他用户的编辑发生冲突：

* 您已开始编辑资产，但未先签出该资产（例如，只需打开它）。
* 您打算尽快开始编辑资产，不希望其他人编辑资产。

完成编辑后，应用程序将显示已更改资产的&#x200B;**[!UICONTROL Edited Locally]**&#x200B;状态。 在您将更改上传到[!DNL Experience Manager]之前，保存到资源的所有更改仅供本地使用。 要逐个上传一个资产或几个资产，请在资产选项中单击&#x200B;**[!UICONTROL Upload Changes]**。 它将在[!DNL Experience Manager]中创建该资源的版本。 使用[!DNL Assets]的Web界面，您可以在[时间线视图](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/activity-stream)中查看资产历史记录。

应用程序中的![上载更改选项](assets/upload_changes_single1_da2.png "应用程序中的“上载更改”选项")

查看大型资源预览时![上载更改选项](assets/upload_changes_single2_da2.png "查看大型资源预览时，上载更改选项")

有关协作编辑的最佳实践，请参阅[高级工作流程：对相同的文件进行协作并避免编辑冲突](#adv-workflow-collaborate-avoid-conflicts)。

在以下情况下，您可能需要放弃对本地资产的更改和编辑。 单击 **[!UICONTROL Discard Changes]**。

* 如果您不想在[!DNL Experience Manager]中本地保存更改。
* 保存一些更改后，开始更改原始资源。
* 停止编辑不再需要的资源。

如有必要，请切换签出。 更新的资产将从本地缓存文件夹中删除，并在编辑或打开时再次下载。

## 上传新资源并将其添加到[!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

用户可以向DAM存储库添加新资产。 例如，您可能是一位机构摄影师或承包商，希望将照片拍摄中的大量照片添加到[!DNL Experience Manager]存储库。 要向[!DNL Experience Manager]添加新内容，请在应用程序的顶部栏中选择![上传到云选项](assets/do-not-localize/upload_to_cloud_da2.png)。 浏览到本地文件系统中的资源文件，然后单击&#x200B;**[!UICONTROL Select]**。 或者，要上传资源，请将文件或文件夹拖动到应用程序界面上。 在Windows上，如果将资源拖动到应用程序内的文件夹中，则会将资源上传到该文件夹中。 如果上传时间较长，应用程序会显示进度条。

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

您可以从本地文件系统上传文件夹或单个文件。 上传文件夹时，将保留该文件夹的层次结构。 在批量上传资产之前，请参阅[批量上传](#bulk-upload-assets)。

要查看给定会话中转移的资产列表，请单击&#x200B;**[!UICONTROL View]** > **[!UICONTROL Assets transfers]**。 列表允许您查看和快速验证当前会话的文件传输。

![特定会话中已转移资产的列表](assets/assets_transfered_da2.png "特定会话中已转移资产的列表")

您可以在&#x200B;**[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]**&#x200B;设置中控制上载并发（加速）。 并发性越强，上传速度通常越快，但可能会占用大量资源，从而消耗本地计算机的处理能力。 如果遇到系统速度较慢的情况，请使用较低的并发值重新尝试上传。

>[!NOTE]
>
>此传输列表不是永久性的，如果您退出应用程序然后重新打开它，则此列表将不可用。

## 批量上传资产 {#bulk-upload-assets}

用户或组织（如摄影师或创意公司）可以在照片拍摄、修饰或从较大范围选择等活动中创建大量本地资产。 这些任务通常在[!DNL Experience Manager]之外完成。 他们可以直接从桌面应用程序将这些大型本地文件夹上传到[!DNL Assets]。 文件夹层次结构将保留，并且所有嵌套的子文件夹和包含的资产将上传。 上传的资产也可立即供同一服务器上的其他用户使用。 Assets将在后台上传，因此该操作不会绑定到Web浏览器会话。

![将多个本地文件夹从桌面批量上传到[!DNL Experience Manager]](assets/upload_local_folders_da2.png "将多个本地文件夹从桌面批量上传到Experience Manager")

上传后，如果预期更改未反映在应用程序中，请单击刷新图标![刷新图标](assets/do-not-localize/refresh.png)。

>[!NOTE]
>
>请勿使用上传功能跨两个[!DNL Experience Manager]部署迁移资产。 请参阅[迁移指南](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide)。

## 后续步骤 {#next-steps}

* [观看视频，开始使用Adobe Experience Manager桌面应用程序](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 通过右侧边栏中的[!UICONTROL Edit this page] ![编辑页面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![创建GitHub问题](assets/do-not-localize/github-issue.png)提供文档反馈

* 联系[客户关怀团队](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [下载资源](/help/using/download-assets.md)
>* [了解用户界面](/help/using/user-interface.md)
>* [搜索](/help/using/search.md)
