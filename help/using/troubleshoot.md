---
title: ' [!DNL Adobe Experience Manager] 桌面应用程序的最佳实践和疑难解答'
description: 按照最佳实践和疑难解答来解决与安装、升级、配置等相关的偶然问题。
exl-id: f388e4ac-907d-4093-ba6f-86ecdafeb015
source-git-commit: 5676e7ece8bb43f051dae72d17e15ab1c34caefc
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager]桌面应用疑难解答 {#troubleshoot-v2}

[!DNL Adobe Experience Manager]桌面应用程序连接到[!DNL Experience Manager]部署的数字资产管理(DAM)存储库。 该应用程序可在您的计算机上获取存储库信息和搜索结果，下载和上传文件和文件夹，并包含用于管理与Assets用户界面冲突的功能。

请阅读并了解应用程序疑难解答、最佳实践以及限制。

## 最佳实践 {#best-practices-to-prevent-troubles}

请遵循以下最佳实践，防止出现一些常见问题和疑难解答。

* **了解桌面应用程序的工作方式**：在开始使用应用程序之前，请花一些时间了解该应用程序的工作方式。 了解[!DNL Experience Manager] Web界面与桌面之间的链接、存储库映射、资产缓存、本地保存和后台上传。 查看[工作方式](release-notes.md#how-app-works)。

* **避免在文件夹名称中使用不受支持的字符**：在创建或上传文件夹时，请勿使用空格和无效字符。 在[在 [!DNL Adobe Experience Manager Assets]](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/assets/managing/manage-assets#creating-folders)中创建文件夹中查看字符列表。 文件夹名称中不受支持的字符可能会影响某些[!DNL Experience Manager]用例。

* **避免冲突的最佳实践**：为避免在协作处理多个资产时潜在冲突，请转到[避免编辑冲突](using.md#adv-workflow-collaborate-avoid-conflicts)。

* **为大型分层文件夹使用文件夹上载**：使用[!DNL Experience Manager]桌面应用程序上载大型文件夹，而不使用Assets Web界面或其他方法。 应用程序会通过日志记录和监控在后台上传资产。 请参阅[批量上传资产](using.md#bulk-upload-assets)。

* **使用最新版本**：使用最新应用程序版本。 在安装新的应用版本或升级到较新的[!DNL Experience Manager]版本之前，请务必检查兼容性。 请参阅[发行说明](release-notes.md)。

* **使用相同的驱动器号**：在组织内使用相同的驱动器号映射到[!DNL Experience Manager] DAM。 要查看其他用户放置的资源，路径必须相同。 使用相同的驱动器号可确保到DAM资产的固定路径。 即使不同的用户使用不同的驱动器号，资产仍会放置且不会被删除。

* **请注意网络**：网络性能对于[!DNL Experience Manager]桌面应用程序的性能至关重要。 如果您遇到文件传输或批量操作响应缓慢的问题，请关闭可能导致大量网络流量的功能或应用程序。

* **桌面应用程序不受支持的用例**：避免使用该应用程序迁移资源，因为它需要规划和额外的工具。 此外，它也不适合执行高负载DAM操作，例如移动大型文件夹、大型上传或高级元数据搜索。 此外，请勿将其用作同步客户端，因为其设计原则和使用模式与Microsoft OneDrive或Adobe Creative Cloud桌面同步等同步客户端不同。

* **超时**：当前，桌面应用程序不具有可配置的超时值，该超时值在固定时间间隔后断开[!DNL Experience Manager]服务器和桌面应用程序之间的连接。 上传大型资产时，如果连接在一段时间后超时，应用程序会重试上传资产，方法是增加上传超时时间。 没有更改默认超时设置的推荐方法。

## 如何排除故障 {#troubleshooting-prep}

要对桌面应用程序问题进行故障诊断，请注意以下信息。 此外，如果您选择寻求支持，它还将帮助您更好地向Adobe客户支持部门传达问题。

### 日志文件的位置 {#check-log-files-v2}

[!DNL Experience Manager]桌面应用会根据操作系统将其日志文件存储在以下位置：

在Windows上： `%LocalAppData%\Adobe\AssetsCompanion\Logs`

在Mac上： `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

上传多个资产时，如果某些文件上传失败，请参阅`backend.log`文件以识别失败的上传。

>[!NOTE]
>
>在支持请求或票证上与Adobe客户支持部门合作时，可能会要求您共享日志文件，以帮助客户支持团队了解此问题。 存档整个`Logs`文件夹并与您的客户支持联系人共享。

### 更改日志文件中的详细信息级别 {#level-of-details-in-log}

要更改日志文件中的详细信息级别，请执行以下操作：

1. 确保应用程序未运行。

1. 在Windows系统上：

   1. 打开命令窗口。

   1. 通过运行以下命令启动[!DNL Adobe Experience Manager]桌面应用程序：

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   在Mac系统上：

   1. 打开终端窗口。

   1. 通过运行以下命令启动[!DNL Adobe Experience Manager]桌面应用程序：

   ```shell
   AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app
   ```

有效的日志级别为DEBUG、INFO、WARN或ERROR。 日志的详细程度在DEBUG中最高，在ERROR中最低。

### 启用调试模式 {#enable-debug-mode}

要进行故障排除，您可以启用调试模式并在日志中获取更多信息。

>[!NOTE]
>
>有效的日志级别为DEBUG、INFO、WARN或ERROR。 日志的详细程度在DEBUG中最高，在ERROR中最低。

要在Mac上的调试模式下使用应用程序，请执行以下操作：

1. 打开终端窗口或命令提示符。

1. 通过运行以下命令启动[!DNL Experience Manager]桌面应用程序：

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`。

要在Windows上启用调试模式，请执行以下操作：

1. 打开命令窗口。

1. 通过运行以下命令启动[!DNL Experience Manager]桌面应用程序：

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`。

### 了解[!DNL Adobe Experience Manager]桌面应用程序版本 {#know-app-version-v2}

要查看版本号，请执行以下操作：

1. 启动应用程序。

1. 单击右上角的省略号，将鼠标悬停在[!UICONTROL Help]上，然后单击[!UICONTROL About]。

   此屏幕中列出了版本号。

### 清除缓存 {#clear-cache-v2}

执行以下步骤：

1. 启动应用程序并连接到[!DNL Experience Manager]的实例。

1. 单击右上角的省略号并选择[!UICONTROL Preferences]以打开应用程序的首选项。

1. 找到显示[!UICONTROL Current Cache Size]的条目。 单击此元素旁边的垃圾桶图标。

要手动清除缓存，请执行以下操作：

>[!CAUTION]
>
>这些步骤具有潜在的破坏性。 如果存在未上载到[!DNL Adobe Experience Manager]的本地文件更改，则这些更改将丢失。

通过删除应用程序的缓存目录（可在应用程序的首选项中找到）来清除缓存。

1. 启动应用程序。

1. 通过选择右上角的省略号并选择[!UICONTROL Preferences]打开应用程序的首选项。

1. 记下[!UICONTROL Cache Directory]值。

   此目录中存在以编码的[!DNL Adobe Experience Manager]端点命名的子目录。 这些名称是目标[!DNL Adobe Experience Manager] URL的编码版本。 例如，如果应用程序面向`localhost:4502`，则目录名称为`localhost_4502`。

要清除缓存，请删除所需的编码[!DNL Adobe Experience Manager]终结点目录。 或者，删除首选项中指定的整个目录会清除应用程序已使用的所有实例的高速缓存。

清除[!DNL Adobe Experience Manager]桌面应用程序的缓存是一项初步的故障排除任务，可以解决多个问题。 从应用程序首选项中清除缓存。 请参阅[设置首选项](install-upgrade.md#set-preferences)。 缓存文件夹的默认位置为：

## 看不到已放置的资产 {#placed-assets-missing}

如果您看不到您或其他创意专业人士放置在支持文件（如INDD文件）中的资产，请检查以下内容：

* 与服务器的连接。 不稳定的网络连接可能会延迟资产下载。

* 文件大小。 大型资源的下载和显示时间较长。

* 驱动器号一致性。 如果您或其他协作者在将[!DNL Experience Manager] DAM映射到其他驱动器号时放置了资产，则放置的资产不会显示。

* 权限。要检查您是否有权获取所放置的资产，请与[!DNL Experience Manager]管理员联系。

### 对桌面应用程序用户界面上的文件的编辑不会立即在[!DNL Adobe Experience Manager]中反映 {#changes-on-da-not-visible-on-aem}

[!DNL Adobe Experience Manager]桌面应用程序由用户决定何时完成对文件的所有编辑。 根据文件的大小和复杂性，将文件的新版本传输回[!DNL Adobe Experience Manager]需要花费大量时间。 该应用程序旨在最大限度地减少文件传输的次数，而不是根据猜测的编辑完成情况自动上传文件。 建议用户通过选择上载文件的更改来启动将文件传输回[!DNL Adobe Experience Manager]的操作。

### 在macOS上升级时出现问题 {#issues-when-upgrading-on-macos}

在macOS上升级[!DNL Experience Manager]桌面应用程序时，有时可能会出现问题。 [!DNL Experience Manager]桌面应用程序的旧系统文件夹导致这些问题。 这些文件夹阻止正确加载[!DNL Experience Manager]桌面应用程序的新版本。 要解决此问题，可以手动删除以下文件夹和文件。

运行以下步骤之前，请将`Adobe Experience Manager Desktop`应用程序从macOS Applications文件夹拖到垃圾桶中。 然后打开终端，运行以下命令，并在出现提示时提供密码。

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## 无法上传文件 {#upload-fails}

如果您正在使用带有[!DNL Experience Manager] 6.5.1或更高版本的桌面应用程序，请将S3或Azure连接器升级到版本1.10.4或更高版本。 它解决了与[OAK-8599](https://issues.apache.org/jira/browse/OAK-8599)相关的文件上传失败问题。 请参阅[安装说明](install-upgrade.md#install-v2)。

## [!DNL Experience Manager]桌面应用连接问题 {#connection-issues}

如果您遇到一般连接问题，可通过以下方法获取有关[!DNL Experience Manager]桌面应用程序所执行操作的更多信息。

**检查请求日志**

[!DNL Experience Manager]桌面应用程序将所有发送的请求以及每个请求的响应代码记录在专用日志文件中。

1. 在应用程序的日志目录中打开`request.log`以查看这些请求。

1. 日志中的每一行表示请求或响应。 请求后面跟有请求的URL的`>`字符。 响应中包含`<`字符，后跟响应代码和所请求的URL。 可以使用每行的GUID匹配请求和响应。

**检查由应用程序的嵌入式浏览器加载的请求**

大多数应用程序的请求可在请求日志中找到。 但是，如果其中没有有用的信息，则查看应用程序的嵌入式浏览器发送的请求会很有用。
有关如何查看这些请求的说明，请参阅[SAML部分](#da-connection-issue-with-saml-aem)。

### SAML登录身份验证不起作用 {#da-connection-issue-with-saml-aem}

[!DNL Experience Manager]桌面应用可能未连接到已启用SSO (SAML) [!DNL Adobe Experience Manager]部署。 应用程序的设计试图适应SSO连接和过程的变化和复杂性。 但是，设置可能需要额外的疑难解答。

有时，SAML进程不会重定向回最初请求的路径。 或者，最终重定向到的主机与[!DNL Adobe Experience Manager]桌面应用程序中配置的主机不同。 要验证此问题是否不是这种情况，请执行以下操作：

1. 打开Web浏览器。 访问`https://[aem_server]:[port]/content/dam.json` URL。

1. 登录到[!DNL Adobe Experience Manager]部署。

1. 登录完成后，在地址栏中查看浏览器的当前地址。 它应该与最初输入的URL完全匹配。

1. 另外，请验证`/content/dam.json`之前的所有内容是否与在[!DNL Adobe Experience Manager]桌面应用程序的设置中配置的目标[!DNL Adobe Experience Manager]值相匹配。

**登录SAML进程按照上述步骤正确运行，但用户仍然无法登录**

[!DNL Adobe Experience Manager]桌面应用中显示登录过程的窗口只是显示目标[!DNL Adobe Experience Manager]实例的Web用户界面的Web浏览器：

* Mac版本使用[WebView](https://developer.apple.com/documentation/webkit/webview)。

* Windows版本使用基于Chromium的[CefSharp](https://cefsharp.github.io/)。

确保SAML进程支持这些浏览器。

要进一步排除故障，可以查看浏览器尝试加载的确切URL。 要查看此信息，请执行以下操作：

1. 按照说明在[调试模式](#enable-debug-mode)下启动应用程序。

1. 重现登录尝试。

1. 导航到应用程序的[日志目录](#check-log-files-v2)。

1. 对于Windows：

   1. 打开“aemcompanionlog.txt”。

   1. 搜索以“登录浏览器地址已更改为”开头的消息。 这些条目还包含应用程序加载的URL。

   对于Mac：

   1. 在`com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`中，最新文件名中的数字将替换&#x200B;**n**。

   1. 搜索以“加载的帧”开头的消息。 这些条目还包含应用程序加载的URL。

查看正在加载的URL序列有助于在SAML末尾进行故障排除，以确定错误的具体内容。

### SSL配置问题 {#ssl-config-v2}

[!DNL Experience Manager]桌面应用程序用于HTTP通信的库使用严格的SSL强制执行。 有时，使用浏览器连接可能会成功，但在使用[!DNL Experience Manager]桌面应用程序时失败。 要正确配置SSL，请在Apache中安装缺少的即时证书。 请参阅[如何在Apache中安装中间CA证书](https://access.redhat.com/solutions/43575)。

[!DNL Experience Manager]桌面应用程序用于HTTP通信的库使用严格的SSL强制执行。 因此，在某些情况下，通过浏览器成功的SSL连接会因[!DNL Adobe Experience Manager]桌面应用程序而失败。 此结果非常好，因为它鼓励正确配置SSL并提高安全性，但当应用程序无法连接时可能会令人沮丧。

在这种情况下，推荐使用工具来分析服务器的SSL证书，并识别问题以便进行更正。 有些网站通过提供服务器的URL来检查服务器的证书。

作为临时措施，可以在[!DNL Adobe Experience Manager]桌面应用程序中禁用严格的SSL强制实施。 此方法不是推荐的长期解决方案，因为它通过隐藏错误配置SSL的根源来降低安全性。 要禁用严格实施，请执行以下操作：

1. 使用您选择的编辑器编辑应用程序的JavaScript配置文件，该文件（默认情况下）位于以下位置（具体取决于操作系统）：

   在Mac上： `/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   在Windows上： `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. 在文件中找到以下部分：

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. 通过添加`"strictSSL": false`修改部分，如下所示：

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. 保存文件并重新启动[!DNL Adobe Experience Manager]桌面应用。

### 切换到其他服务器时出现登录问题 {#cannot-login-cookies-issue}

使用[!DNL Experience Manager]服务器后，当您尝试更改与其他服务器的连接时，可能会遇到登录问题。 这是由于旧Cookie干扰新身份验证所致。 主菜单中的[!UICONTROL Clear Cookies]选项很有帮助。 注销应用程序中的当前会话并选择[!UICONTROL Clear Cookies]，然后再继续连接。

切换服务器时![清除Cookie](assets/main_menu_logout_da2.png)

## 应用程序无响应 {#unresponsive}

极少数情况下，应用程序可能会变得无响应、仅显示白屏，或在界面底部显示错误，而不在界面上提供任何选项。 请按顺序尝试以下操作：

* 右键单击应用程序界面，然后单击&#x200B;**[!UICONTROL Refresh]**。
* 退出应用程序并再次打开。

在这两种方法中，应用程序都从根DAM文件夹启动。

## 隐藏已过期的资源 {#hide-expired-assets}

从[!DNL Experience Manager]用户界面中浏览资源时，不显示过期的资源。 管理员可以配置设置，以防止在从桌面应用程序和Asset Link进行浏览时查看、搜索和获取过期的资产。 这样做可确保这些操作期间无法访问过期的资产。 该配置适用于所有用户，而不管管理员权限如何。

* Experience Manager6.5中用于隐藏过期资源的[配置](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/assets/managing/manage-assets#hide-expired-assets-via-acp-api)。
* 在Experience Manageras a Cloud Service中配置[以隐藏过期的资源](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets#hide-expired-assets-via-acp-api)。

<!--
### Need additional help with [!DNL Experience Manager] desktop app {#additional-help}

Create Jira ticket with the following information:

* Use `DAM - Companion App` as the [!UICONTROL Component].

* Detailed steps to reproduce the issue in [!UICONTROL Description].

* DEBUG level logs that were captured while reproducing the issue.

* Target Experience Manager version.

* Operating system version.

* [!DNL Adobe Experience Manager] desktop app version. To know your app version, see [finding the desktop app version](#know-app-version-v2).
-->

>[!MORELIKETHIS]
>
>* [已知问题](release-notes.md#known-issues-v2)
>* [避免编辑冲突](using.md#adv-workflow-collaborate-avoid-conflicts)
