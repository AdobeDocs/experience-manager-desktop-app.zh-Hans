---
title: 安装和配置桌面应用程序v1.10
description: 安装和配置 [!DNL Experience Manager] 要使用的桌面应用程序版本1.10 [!DNL Assets] 并将资产映射为桌面上的驱动器。
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# 安装和配置 [!DNL Experience Manager] 桌面应用程序v1.10 {#install-and-configure-aem-desktop-app}

使用 [!DNL Experience Manager] 桌面应用程序，中的资产 [!DNL Experience Manager] 可以在本地桌面上轻松访问，并可用于任何桌面应用程序。 Assets可在Mac Finder或Windows资源管理器中显示，在桌面应用程序中编辑，并且更改将保存回 [!DNL Experience Manager]，在上传时创建新版本。

通过这种集成，各种角色可以在Assets中集中管理公司内的资产，在Creative Cloud和其他应用程序中访问资产，以及轻松遵守各种标准，包括品牌策略。

要使用 [!DNL Experience Manager] 桌面应用程序，

* 确保您的 [!DNL Experience Manager] 服务器版本与 [!DNL Experience Manager] 桌面应用程序。 请参阅 [兼容性矩阵](release-notes-of-v1.md#compatibilitymatrix).

* 下载并安装应用程序。

* 使用几个资源测试连接。 请参阅 [在桌面上访问和打开资产](use-app-v1.md#openondesktop).

## 系统要求、先决条件和下载链接 {#system-requirements-prerequisites-and-download-links}

欲了解详细信息，请参见 [[!DNL Experience Manager] 桌面应用程序发行说明](release-notes-of-v1.md).

## 安装应用程序并将其连接到 [!DNL Experience Manager] 服务器 {#install-and-connect-aem-desktop-app-to-aem-server}

有关详细信息，请参阅 [安装并连接 [!DNL Experience Manager] 桌面应用程序目标 [!DNL Experience Manager] 服务器](use-app-v1.md#installandconnect).

>[!NOTE]
>
>只有一个实例 [!DNL Experience Manager] 桌面应用程序可以一次安装并处于活动状态。

## 文件处理 {#file-handling}

从桌面应用程序挂载的网络共享位置更改文件时，文件将分两阶段保存到该位置。 在第一阶段，文件将保存在本地。 用户可以保存文件并继续处理文件，而无需等待传输完成。

在第二阶段，桌面应用程序将更新的文件上传到 [!DNL Experience Manager] 服务器延迟（例如，30秒）。 此操作在后台进行。 使用查看资源状态选项可查看上传操作的状态。

1. 将资源上传到Assets。

1. 单击 [!DNL Experience Manager] 工具栏中的桌面应用程序图标。

1. 从菜单中，选择查看资源状态选项。

1. 在对话框中，查看上传操作的状态。

>[!NOTE]
>
>[!DNL Experience Manager] 桌面应用程序可以处理大小最大为40 GB的资产。

## 连接到 [!DNL Experience Manager] Dispatcher背后的实例 {#connect-to-an-aem-instance-behind-a-dispatcher}

Assets API中的复制和移动方法要求将以下其他标头传递到 [!DNL Experience Manager]：

* X目标
* X深
* X覆盖

[!DNL Experience Manager] 桌面连接到 [!DNL Experience Manager] 使用包含默认端口的URL。 因此， `virtualhosts` Dispatcher配置中的设置应包含默认端口号。 有关的更多信息 `virtualhosts` 配置，请参见 [识别虚拟主机](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#identifying-virtual-hosts-virtualhosts).

有关配置Dispatcher以传递这些其他标头的其他信息，请参阅 [指定HTTP标头](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#specifying-the-http-headers-to-pass-through-clientheaders).

### 代理支持 {#proxy-support}

此 [!DNL Experience Manager] 桌面应用程序使用系统预定义的代理通过HTTPS连接到Internet。 应用程序只能使用不需要额外身份验证的网络代理进行连接。

如果配置或修改Windows的代理服务器设置（“Internet选项”>“局域网设置”），请重新启动 [!DNL Experience Manager] 桌面应用程序，以使更改生效。

>[!NOTE]
>
>代理配置仅在启动桌面应用程序时应用。 关闭并重新启动应用程序，以使任何更改生效。

如果您的代理需要身份验证，IT团队可以在代理服务器设置中允许Experience Manager Assets URL，以允许应用程序流量通过。

## 自定义资源信息对话框 {#customize-the-asset-info-dialog}

您可以通过叠加以下一个或两个组件来自定义资源信息对话框：

* Granite用户界面页面位于 `/libs/dam/gui/content/assets/moreinfo`.

* HTL `/css/javascript` 组件位于 `/libs/dam/gui/components/admin/moreinfo`.

覆盖哪个组件取决于自定义的性质。 要更改哪些组件显示为资产信息对话框的一部分，请叠加Granite用户界面页面。 要更改对话框的HTML、CSS或JavaScript内容，请叠加HTL组件。

## 管理缓存 {#manage-cache}

在Windows上，缓存位于 `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`，其中是 [!DNL Experience Manager] 在桌面应用程序中配置的主机。 例如， `http://localhost:4502` 显示为 `http%3A%2F%2Flocalhost%3A4502%2F`.

在macOS X上，类似目录位于 `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### 用于管理缓存的应用程序内选项 {#in-app-option-to-manage-cache}

您可以控制可用于本地缓存的磁盘空间量。 为了更加流畅的体验，Assets服务器上的工件将缓存在本地。 您可以根据自己的要求更改默认值。 此外，您还可以清除缓存以重新获取所有资源。 要设置所需的选项，请单击应用程序的图标，然后单击 **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**.****

>[!NOTE]
>
>清除缓存时，它会保留未保存的更改。 任何未签入到中的资产 [!DNL Experience Manager] 服务器将保留，而不是删除。

### 在Windows上更改缓存的位置 {#change-location-of-cache-on-windows}

缓存的默认位置 [!DNL Experience Manager] 桌面应用程序如下所示：

* 在Windows中， `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* 在Mac中， `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

此 `EncodedAEMEndpoint` 是否已配置应用程序 [!DNL Experience Manager] 端点URL。 值是的定位URL的编码版本 [!DNL Experience Manager] 服务器。 例如，如果应用程序正在定位 `http://localhost:4502`，目录名称为 `http%3A%2F%2Flocalhost%3A4502`. 在此示例中，缓存目录的Windows路径为 `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

要将应用程序指向其他文件夹或其他驱动器，请编辑应用程序的配置文件。

1. 导航到应用程序的安装目录。 Windows上的默认位置为 `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. 编辑 `Adobe Experience Manager Desktop.exe.config` 使用文本编辑器的文件。

   需要管理员权限才能保存对此文件所做的更改。

1. 搜索字符串“ProxyCacheRoot”。 您会看到其值设置为缓存位置 `%LocalAppData%\Adobe\AssetsCompanion\Cache`. 只需将此值更改为任何有效路径即可。

   >[!NOTE]
   >
   >应用程序会自动创建 *&lt;encoded aem=&quot;&quot; endpoint=&quot;&quot;>* 子目录。 无法配置此行为。

>[!MORELIKETHIS]
>
* 观看 [简介 [!DNL Experience Manager] 桌面应用程序](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) （5分43秒）。
* [使用 [!DNL Experience Manager] 桌面应用程序](use-app-v1.md).
* [疑难解答 [!DNL Experience Manager] 桌面应用程序](troubleshoot-app-v1.md).
