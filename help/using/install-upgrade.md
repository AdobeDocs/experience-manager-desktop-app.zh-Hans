---
title: 安装和配置桌面应用程序
description: 安装并配置 [!DNL Adobe Experience Manager] 桌面应用程序以使用 [!DNL Adobe Experience Manager Assets] 服务器并在本地文件系统上下载资产。
feature: Desktop App,Release Information
exl-id: 422e51c1-c456-4151-bb43-4b3d29a58187
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '1449'
ht-degree: 0%

---

# 安装[!DNL Adobe Experience Manager]桌面应用程序 {#install-app-v2}

使用[!DNL Adobe Experience Manager]桌面应用程序，[!DNL Experience Manager]中的资产可轻松地在本地桌面上使用，并可在任何本地桌面应用程序中使用。 可以在桌面应用程序中预览和打开Assets。 它们可以在Finder或Explorer中显示以用于文档，并在本地编辑。 更改将保存回[!DNL Experience Manager]，并在上传时创建新版本。

通过此类集成，组织中的各种角色可以：

* 在[!DNL Experience Manager Assets]中集中管理资源。

* 访问任何本机桌面应用程序(包括第三方应用程序和Adobe Creative Cloud中的资源)中的资源。 在这样做时，用户可以轻松遵守各种标准，包括品牌推广。

要使用[!DNL Experience Manager]桌面应用，请执行以下操作：

* 确保您的[!DNL Experience Manager]版本与[!DNL Experience Manager]桌面应用程序兼容。

* 下载并安装应用程序。 请参阅下面的[安装桌面应用程序](#install-v2)。

* 使用几个资源测试连接。 请参阅[如何浏览和搜索资源](using.md#browse-search-preview-assets)。

## 系统要求、先决条件和下载链接 {#tech-specs-v2}

有关详细信息，请参阅[[!DNL Experience Manager] 桌面应用发行说明](release-notes.md)。

## 从以前的版本升级 {#upgrade-from-previous-version}

如果您是桌面应用程序v1.x的用户，请了解该应用程序之前版本与最新版本之间的区别和相似之处。 查看[桌面应用程序的新增功能](introduction.md#whats-new-v2)和[该应用程序的工作方式](release-notes.md#how-app-works)。

>[!NOTE]
>
>两个版本的桌面应用程序不能同时存在于计算机上。 在安装版本之前，请卸载其他版本。

要从应用程序的先前版本进行升级，请按照以下说明操作：

1. 升级之前，请同步所有资产并将更改上传到[!DNL Experience Manager]。 这样做可避免在卸载应用程序时丢失任何编辑。

1. 卸载应用程序的先前版本。 卸载时，选择选项以清除缓存。

1. 重新启动计算机。

1. [下载](release-notes.md)和[安装](#install-v2)最新应用。 请按照下面的说明操作。

## 安装 {#install-v2}

要安装桌面应用程序，请执行以下步骤。 请先卸载任何现有的Adobe[!DNL Experience Manager]桌面应用程序v1.x，然后再安装最新的应用程序。 有关更多信息，请参阅上文。

1. 从[发行说明](release-notes.md)页面下载最新的安装程序。

1. 让[!DNL Experience Manager]部署的URL和凭据随时可用。

1. 如果您从其他版本的应用程序升级，请参阅[升级桌面应用程序](#upgrade-from-previous-version)。

1. 如果您使用[!DNL Experience Manager]作为[!DNL Cloud Service]、[!DNL Experience Manager] 6.4.4或更高版本或[!DNL Experience Manager] 6.5.0或更高版本，请跳过此步骤。 确保您的[!DNL Experience Manager]安装程序符合[发行说明](release-notes.md)中所述的兼容性要求。 如有必要，请下载适用的[兼容包](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/featurepack/adobe-asset-link-support)，并使用[!DNL Experience Manager]包管理器以[!DNL Experience Manager]管理员身份安装它。 若要安装包，请参阅[如何使用包](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/sites/administering/contentmanagement/package-manager)。

1. 运行安装程序二进制文件，并按照屏幕上的说明进行安装。

1. 在Windows上，安装程序可能会提示安装`Visual Studio C++ Redistributable 2015`。 按照屏幕上的说明进行安装。 如果安装失败，请手动安装。 从[此处](https://www.microsoft.com/en-us/download/details.aspx?id=52685)下载安装程序并安装`vc_redist.x64.exe`和`vc_redist.x86.exe`文件。 重新运行[!DNL Experience Manager]桌面应用程序安装程序。

1. 在出现提示时重新启动计算机。 启动并配置桌面应用程序。

1. 要将应用程序与[!DNL Experience Manager]存储库连接，请单击任务栏中的应用程序图标，然后启动应用程序。 以`https://[aem_server]:[port]/`格式提供[!DNL Experience Manager]服务器的地址。

   单击&#x200B;**[!UICONTROL Connect]**&#x200B;并提供凭据。

   ![桌面应用与输入服务器地址的连接屏幕](assets/connect_da2.png)

   *图：与输入服务器地址的连接屏幕。*

   选择&#x200B;**[!UICONTROL Remember Connection]**&#x200B;以避免每次登录桌面应用时都输入连接详细信息。

   >[!CAUTION]
   >
   >确保[!DNL Experience Manager]服务器的地址之前或之后没有前导或尾随空格。 否则，应用程序无法连接到[!DNL Experience Manager]服务器。

1. [可选]单击&#x200B;**[!UICONTROL I want to connect a different way]**，然后单击&#x200B;**[!UICONTROL Adobe login]**&#x200B;以使用Adobe的Experience Manager Assets服务(IMS)登录到Identity Management服务器。 IMS登录允许桌面应用程序自动执行访问令牌刷新，从而让用户保持登录状态长达14天。 单击&#x200B;**[!UICONTROL Direct login]**&#x200B;以使用用户的凭据对[!DNL Experience Manager]服务器执行标准登录。

   ![Adobe登录](assets/adobe-login.png)

1. 成功连接后，您可以查看[!DNL Experience Manager] DAM根文件夹中可用的文件夹和资产列表。 您可以在应用程序中浏览文件夹。

   ![登录时，应用程序显示DAM内容](assets/firstview_da2.png)

   *图：应用程序在登录后显示DAM内容*

1. （[!DNL Experience Manager] 6.5.1或更高版本）如果正在使用带有[!DNL Experience Manager] 6.5.1或更高版本的桌面应用程序，请将S3或Azure连接器升级到版本1.10.4或更高版本。 请参阅[Azure连接器](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/implementing/deploying/deploying/data-store-config#azure-data-store)或[S3连接器](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/implementing/deploying/deploying/data-store-config#amazon-s-data-store)。

   如果您是AdobeManaged Services (AMS)客户，请联系Adobe客户支持。

## 设置首选项 {#set-preferences}

要更改首选项，请单击![更多选项图标](assets/do-not-localize/more_options_da2.png)和&#x200B;**[!UICONTROL Preference]** ![首选项图标](assets/do-not-localize/preferences_icon_da2.png)。 在&#x200B;**[!UICONTROL Preferences]**&#x200B;窗口中，调整以下值：

* [!UICONTROL Launch the application on logon]。

* [!UICONTROL Show a window when the application starts]。

* **[!UICONTROL Cache Directory]**：应用程序的本地缓存的位置（它包含本地下载的资源）。

* **[!UICONTROL Network Drive Letter]**：用于映射到[!DNL Experience Manager] DAM的驱动器号。 如果您不确定，请不要更改此网络驱动器号。 该应用程序可以映射到Windows上的任何驱动器号。 如果两个用户放置来自不同驱动器号的资源，则他们看不到彼此放置的资源。 资源的路径会发生变化。 资产仍放置在二进制文件（如INDD）中，不会被删除。 应用会列出所有可用的驱动器号，默认使用最后一个可用的驱动器号，通常为`Z`。

* **[!UICONTROL Maximum Cache Size]**：硬盘上允许的缓存（以GB为单位），用于存储本地下载的资源。

* **[!UICONTROL Current cache size]**：本地下载资源的存储大小。 仅当使用应用程序下载资产后，才会显示信息。

* **[!UICONTROL Automatically download linked assets]**：下载原始文件时，将自动获取放置在受支持的本机Creative Cloud应用中的资源。

* **[!UICONTROL Maximum number of downloads]**： ![警告图标](assets/do-not-localize/caution-icon.png)请谨慎更改。 首次下载资源时（通过“显示”、“打开”、“编辑”、“下载”或类似选项），仅当批次包含的内容少于此数字时才下载资源。 默认值为 50。如果您不确定，请勿更改。 提高该值可能会导致等待时间较长，而降低该值可能会阻止您在一次尝试中下载所有必要的资源或文件夹。

* **[!UICONTROL Use legacy conventions when creating nodes for assets and folders]**： ![警告图标](assets/do-not-localize/caution-icon.png)请谨慎更改。 此设置允许应用程序在上传文件夹时模拟v1.10应用程序行为。 在v1.10中，在存储库中创建的节点名称会遵循用户提供的文件夹名称的空格和大小写。 但是，在应用程序的v2.1中，文件夹名称中的额外空格将转换为破折号。 例如，如果未选择该选项并保留v2.1中的默认行为，则上传`New Folder`或`new   folder`会在存储库中创建相同的节点。 如果选择该选项，则会在存储库中为上述两个文件夹创建不同的节点，这些节点与v1.10应用程序的行为相匹配。

  v2.1的默认行为保持不变：它用存储库节点名称中的破折号替换文件夹名称中的多个空格，并将节点名称转换为小写。

* **[!UICONTROL Upload Acceleration]**： ![警告图标](assets/do-not-localize/caution-icon.png)请谨慎更改。 上传资产时，应用程序可以使用并发上传来提高上传速度。 您可以通过向右移动滑块来提高上载的并发性。 最左侧的滑块表示无并发（单线程上传），中间位置对应于10个并发线程，最右侧的限制上限对应于20个并发线程。 并发限制越高则资源密集程度越高。

要更新不可用的首选项，请先注销[!DNL Experience Manager]服务器，然后再更新。 更新首选项后，单击![保存首选项](assets/do-not-localize/save_preferences_da2.png)。

![桌面应用首选项和设置](assets/preferences_da2.png)

*图：桌面应用首选项。*

### 代理支持 {#proxy-support}

[!DNL Experience Manager]桌面应用程序使用系统预定义的代理通过HTTPS连接到Internet。 应用程序只能使用不需要额外身份验证的网络代理进行连接。

如果配置或修改Windows代理服务器设置（“Internet选项”>“局域网设置”），请重新启动[!DNL Experience Manager]桌面应用以使更改生效。 代理配置将在您启动桌面应用程序时应用。 关闭并重新启动应用程序，以使任何更改生效。

如果您的代理需要身份验证，IT团队可以在代理服务器设置中允许[!DNL Experience Manager Assets] URL以允许应用程序流量通过。

## 卸载应用程序 {#uninstall-the-app}

要在Windows上卸载应用程序，请执行以下步骤：

1. 将所有更改上载到[!DNL Experience Manager]以避免丢失任何编辑。 查看[编辑资源并将更新的资源上传到 [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets)。 注销并[!UICONTROL Exit]应用。

1. 在删除任何其他OS应用程序时，请同时删除应用程序。 从Windows上的“Add and remove programs（添加和删除程序）”卸载它。

1. 要删除缓存和日志，请选中必要的复选框。

   ![卸载对话框以删除日志和缓存](assets/uninstall_da2.png)

1. 按照屏幕上的说明操作。 完成后，重新启动计算机。

要在Mac上卸载应用程序，请执行以下步骤：

1. 将所有更改上载到[!DNL Experience Manager]以避免丢失任何编辑。 查看[编辑资源并将更新的资源上传到 [!DNL Experience Manager]](using.md#edit-assets-upload-updated-assets)。 注销并[!UICONTROL Exit]应用。

1. 从`/Applications`中删除`Adobe Experience Manager Desktop.app`。

或者，要清理Mac上的内部应用程序缓存并卸载应用程序，您可以在终端中运行以下命令：

```shell
/Applications/Adobe Experience Manager Desktop/Contents/Resources/uninstall-osx/uninstall.sh
```
