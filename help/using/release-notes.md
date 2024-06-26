---
title: '"[!DNL Adobe Experience Manager] 桌面应用程序发行说明”'
description: 的发行详细信息、增强功能、新增功能、兼容性和下载链接 [!DNL Adobe Experience Manager] 桌面应用程序。
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: 5676e7ece8bb43f051dae72d17e15ab1c34caefc
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 12%

---

# [!DNL Adobe Experience Manager] 桌面应用程序发行说明 {#release-notes-v2}

下面是最新桌面应用程序版本2.3.0的发行信息。 发行日期为2023年7月14日。

最新版本的桌面应用程序包括以下错误修复和增强功能：

* 添加了对IMS登录的支持。 IMS集成允许桌面应用程序自动执行访问令牌刷新，允许用户保持登录最多14天。

* 改进了对企业代理和Web过滤的支持。


此 **支持 [!DNL Experience Manager] 版本** 为：

* [!DNL Experience Manager] as a [!DNL Cloud Service]. 请参阅 [发行说明](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/home).
* [!DNL Experience Manager] 6.5.0或更高版本，位于AdobeManaged Services (AMS)或内部部署。 请参阅 [service pack发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/release-notes/release-notes).

[!DNL Adobe Experience Manager] 桌面应用程序可用于以下内容 **操作系统**：

* macOS X 10.14或更高版本，带有最新的错误修复。
* Windows 10，带有最新的Service Pack和错误修复。

此 **下载URL** 支持的操作系统包括：

| 操作系统 | [!DNL Experience Manager] as a [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v2.3.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) |
| macOS Apple Silicon (M1) (v2.3.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) |
| Windows 64位(v2.3.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) |
| macOS (v2.2.2) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) |
| macOS Apple Silicon (M1) (v2.2.2) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) |
| Windows 64位(v2.2.2) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) |
| macOS (v2.2.1) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) |
| macOS Apple Silicon (M1) (v2.2.1) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) |
| Windows 64位(v2.2.1) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) |
| macOS (v2.2.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) |
| macOS Apple Silicon (M1) (v2.2.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) |
| Windows 64位(v2.2.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) |
| macOS (v2.1.5.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) |
| Windows 64位(v2.1.5.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) |
| Windows 32位(v2.1.5.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) |
| macOS (v2.1.4.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) |
| Windows 64位(v2.1.4.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) |
| Windows 32位(v2.1.4.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) |
| macOS (v2.1.3.4) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) |
| Windows 64位(v2.1.3.4) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) |
| Windows 32位(v2.1.3.1) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) |

## 支持不同的资源和文件类型 {#support-for-file-types}

该应用程序支持在中存储的资源 [!DNL Experience Manager] 用于表示二进制文件以进行基本操作。 在本机桌面应用程序中打开文件，取决于特定文件类型（如 PNG 或 JPG）与特定应用程序（如 Mac Preview 或 Adobe Photoshop）的操作系统关联。

一些文件类型支持将链接的资产放入二进制文件中。如果链接的资产位于中，则应用程序会预下载该资产 [!DNL Experience Manager] 在使用桌面应用程序打开此类二进制文件时的存储库。 当前支持的文件类型有：

* [!DNL Adobe InDesign] 文件（INDD格式）
* [!DNL Adobe Illustrator] 文件（AI格式）
* [!DNL Adobe Photoshop] 文件（PS格式）

支持该功能 [!DNL Adobe Creative Cloud] 2018和 [!DNL Adobe Creative Cloud] 以上应用程序的2019年版本。 该应用程序使用启发式的最佳匹配方法，将链接资产的本地桌面路径映射到 [!DNL Experience Manager] 服务器。 这是基于以下假设：

* 在本机应用程序中放置文件的路径使用全局桌面路径(从本地网络共享放置，如 [!UICONTROL Reveal] 选项)。

* 路径由本机应用程序存储在文件的XMP记录中。

* [!DNL Experience Manager] 已提取XMP记录，其中包含资源元数据记录的路径。

* 路径可以与中的资源进行匹配 [!DNL Experience Manager]，即放置的文件也位于 [!DNL Experience Manager] 在匹配路径下。

## 新增功能、增强功能和错误修复 {#what-is-new}

要了解详细信息，请参阅 [v2.0的新增功能](introduction.md#whats-new-v2).

**应用程序v2.2.2中的更新**

* （仅限Windows）安装2.2.0和2.2.1发行版后，桌面应用程序显示一个空白屏幕。

**应用程序v2.2.1中的更新**

* 单击时，桌面应用程序会显示会话超时错误消息 **[!UICONTROL Sign In]**.

* 在macOS上访问桌面应用程序v2.2.0时出现问题。

* 通过单击对资源进行排序时，桌面应用程序会显示错误消息 **[!UICONTROL Edited Locally]**.

**应用程序v2.2.0中的更新**

* 支持Apple硅(M1)。

* 在登录到桌面应用程序时能够记住连接字符串。

**应用程序v2.1.5.0中的更新**

* 上传包含中文字符的文件夹中的文件时，桌面应用程序停止响应(ASSETS-9237)。

* 桌面应用程序在文件名中使用短划线替换圆点(ASSETS-10955)。

**应用程序v2.1.4.0中的更新**

应用程序的新版本提供了错误修复。

**应用程序v2.1.3.4中的更新**

应用程序的新版本提供了错误修复。

**应用程序v2.1.3.3中的更新**

应用程序的新版本提供了错误修复。

**应用程序v2.1.3.2中的更新**

此版本的应用程序提供了错误修复。

**应用程序v2.1.3.1中的更新**

此版本中修复的错误为：

* 即使对于大型资产，资产上传和下载速度也得到了改进。 此版本修复了使用上传资产的问题 [!DNL desktop app] 上载超大文件时有时失败。

**应用程序v2.1.2.0中的更新**

* 的新选项 [!UICONTROL Clear Cookies] 会添加到应用程序的主菜单。 它有助于解决潜在的登录问题，例如，在将连接从服务器更改为另一个服务器时。 请参阅 [连接前清除Cookie](/help/using/troubleshoot.md#cannot-login-cookies-issue).

* 新增了一个选项，如果选中该选项，应用程序将可以在其中上传具有节点名称的文件夹和文件 [!DNL Adobe Experience Manager] 匹配本地文件和文件夹名称。 此过程可确保本地名称和上传名称之间的一致性。

  此行为类似于桌面应用程序版本1中的默认行为。 而在当前版本中，如果未启用选项，则使用空格和字符 `% ; # , + ? ^ { } "` 中的文件夹名称会替换为文件夹路径中的破折号。 此外，文件夹路径中的大写字符将转换为小写。 但是，在文件名中， `# % { } ? &` 替换为短划线；但会保留空格和大小写。 有关详细信息，请参阅， [应用程序首选项](/help/using/install-upgrade.md#set-preferences) 和 [上传和添加新资源](/help/using/using.md#upload-and-add-new-assets-to-aem).

**应用程序v2.1.1.0中的更新**

* 高级设置允许应用程序在上传文件夹时模拟v1.10应用程序行为。 在v1.10中，在存储库中创建的节点名称会遵循用户提供的文件夹名称的空格和大小写。 在版本2.1中，默认行为保持不变：文件夹名称中的多个空格在存储库节点名称中被替换为连字符，节点名称转换为小写。 请参阅 [应用程序首选项](/help/using/install-upgrade.md#set-preferences).

**应用程序v2.1.0.0中的更新**

* 要上传资源，用户现在可以直接从Windows资源管理器或Mac Finder将文件或文件夹拖动到应用程序界面上。 除了应用程序中提供的上传选项外，此过程还有效。 请参阅 [上传资产](/help/using/using.md#upload-and-add-new-assets-to-aem) <!-- CQ-4309527 -->

**应用程序v2.0.3中的更新**

此版本中修复的错误为：

* 修复了Windows上尝试访问DAM存储库的应用程序用户的登录问题 [!DNL Adobe Experience Manager] 6.5.5.0。

**应用程序v2.0.2中的更新**

错误修复和更新包括：

* 现在提供上传加速设置以提高上传性能。 打开此设置后，应用程序会通过使用更多的本地CPU线程而更快地上传，并且会更加耗费资源。

* 修复了包含特定GB18030字符的文件名或路径时上传资源。 <!-- CQ-4283494 -->

* 在搜索结果中切换到其他排序类型后，可以按相关性排序选项。 <!-- CQ-4286874 -->

* 现在，桌面应用程序会列出子文件夹，而无需显式刷新。 <!-- CQ-4285711 -->

* (Windows)修复了某些Windows计算机上应用程序界面不可用的罕见问题。 用户无法单击应用程序界面，因为它似乎因界面元素的单击区域向侧“偏移”而被扭曲。 <!-- CQ-4280785 -->

**应用程序v2.0.1中的更新**

错误修复和更新包括：

* 允许配置选项 `%Temp%` 要匹配的目录 `%APPDATA%` 路径。 <!-- CQ-4282665 -->

* 允许用户登录 [!DNL Experience Manager] 通过Okta SAML身份验证进行创作。 <!-- CQ-4278134 -->

## 安装说明 {#installation-instructions-v2}

要了解如何安装和配置应用程序，请参阅 [安装 [!DNL Experience Manager] 桌面应用程序](install-upgrade.md).

如果您是从以前的 [!DNL Experience Manager] 桌面应用程序中，您必须遵循列于以下位置的最佳实践来进行转换 [从以前的版本升级](install-upgrade.md#upgrade-from-previous-version).

## 有关应用程序工作方式的重要说明 {#how-app-works}

请务必了解关于应用程序及其工作方式的以下信息。

* 对于需要在来回完全传输资产二进制文件的操作，该应用程序会提供完全控制权 [!DNL Experience Manager] (**打开**， **编辑**， **上载更改**、和 **上传Assets**)。

   * 如果要在桌面上处理资产，则必须明确地在某个文件夹中逐个或通过多选方式打开、编辑资产或将其下载到桌面。

   * 如果要将对资产所做的本地更改上传到 [!DNL Experience Manager]，您需要选择 [!UICONTROL Upload Changes]，逐个或通过多选实现。

   * 该应用程序不是跨桌面同步资产的“同步客户端”，并且 [!DNL Experience Manager].

   * 应用程序不提供映射 [!DNL Experience Manager] 存储库作为虚拟文件夹结构。

* 应用程序显示的资源列表基于Assets存储库的状态。 从本地下载并随后在本地文件或缓存文件夹中重命名的文件不会显示或通过该应用程序进行管理。

* 如果应用程序不显示预期结果，请单击顶栏中的刷新图标。

* 使用 [!UICONTROL Reveal File] 操作时显示的本地网络共享，仅显示本地可用的文件（和文件夹）。[!UICONTROL Reveal File] 和 [!UICONTROL Reveal Folder] 会预下载资产，以帮助在本地网络共享中显示正确的资产。

* 当Adobe Creative Cloud应用程序读取链接/放置在Creative Cloud应用程序本机文件中的资源文件时，会使用SMB (Mac)/WebDAV (Win)本地网络共享。

下图说明了由用户操作启动的资产和文件从云端到本地文件系统和相反方向的流程。

![资产流自 [!DNL Experience Manager] 通过桌面应用程序从服务器到本机桌面应用程序](assets/da20_flow_diagram.png)

## 已知问题 {#known-issues-v2}

**用户界面问题：**

* 有时，桌面应用程序的界面可能会变为空白。 右键单击，然后单击 [!UICONTROL Refresh] 以重新加载应用程序。 进行此类刷新后，您将从DAM存储库的根目录开始。 将保留对资源的更新或状态。 <!-- CQ-4270267 -->

* 在没有轨迹板或鼠标指针的情况下，很难导航文件夹/搜索结果。 使用无滚轮鼠标设备时，不会显示滚动条。 <!-- CQ-4269947 -->

* 在少数情况下，上传资产更改时，无法正确显示进度栏。

* 在应用筛选器以查找所有本地编辑的资产和删除筛选器后，应用程序不会为用户呈现搜索结果或者用户开始执行筛选时所在的文件夹视图。应用程序会显示 DAM 存储库的根文件夹。

* 有时，当您连接到的URL不包含 [!DNL Experience Manager] 服务器运行时，“连接”屏幕将变得无响应。 可退出应用程序后重新启动。

**CRUD（创建、读取、更新和删除）问题：**

* 在上传包含注释的资源更改时，注释会与资源一起存储在中 [!DNL Experience Manager] 但不会显示为版本控制注释。 此问题已在中解决 [!DNL Experience Manager] 6.4.5和 [!DNL Experience Manager] 6.5.1。Adobe建议安装最新的Service Pack。 <!-- CQ-4268990 -->

* 用户无法取消资产传输。 如果意外触发了大量传输，请退出应用程序后重新启动。<!-- CQ-4278940 -->

**平台问题：**

* 有时，在 Windows 上，打开资产后其状态可能会立即变为 [!UICONTROL Edited Locally]，即使您可能没有进行任何编辑也是如此。可单击 [!UICONTROL Refresh] 进行更新。

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service)
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] [!DNL Assets] 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview)
>* [使用方法 [!DNL Experience Manager] 桌面应用程序](using.md)
>* [安装和升级桌面应用程序](install-upgrade.md)
>* [最佳实践和故障诊断提示](troubleshoot.md)
