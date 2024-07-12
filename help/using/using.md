---
title: 使用 [!DNL Experience Manager] 桌面应用程序
description: 使用 [!DNL Adobe Experience Manager] 桌面应用程序，从您的Win或Mac桌面直接使用 [!DNL Adobe Experience Manager] DAM资源并在其他应用程序中使用。
mini-toc-levels: 1
feature: Desktop App,Asset Management
exl-id: fa19d819-231a-4a01-bfd2-6bba6fec2f18
source-git-commit: ba980c1a1bad4a9627fc28ac7f6619b644fb1f04
workflow-type: tm+mt
source-wordcount: '4060'
ht-degree: 0%

---

# 使用[!DNL Adobe Experience Manager]桌面应用 {#use-aem-desktop-app-v2}

使用[!DNL Adobe Experience Manager]桌面应用程序访问本地桌面上[!DNL Adobe Experience Manager] DAM存储库中存储的数字资产。 然后，您可以在任何桌面应用程序中使用这些资产。 您可以在桌面应用程序中本地打开和编辑资产。 进行更改后，使用版本控制将它们上载回[!DNL Experience Manager]以与其他用户共享更新。 您还可以将新文件和文件夹层次结构上传到[!DNL Experience Manager]，创建文件夹，以及从[!DNL Experience Manager] DAM中删除资源或文件夹。

通过集成，组织中的各种角色可以在[!DNL Experience Manager Assets]中集中管理资源，并在Windows或macOS上的本机应用程序中访问本地桌面上的资源。

在注销后或首次打开应用程序时，请以`https://[aem-server-url]:[port]/`格式提供[!DNL Experience Manager]服务器的URL。 然后选择[!UICONTROL Connect]选项。 提供凭据以将应用程序与服务器连接。

使用[!DNL Adobe Experience Manager]桌面应用程序执行的主要任务包括：

![您可以使用[!DNL Experience Manager]桌面应用程序完成的工作流和任务](assets/aem_desktop_app_usecases_v2.png "可以使用 [!DNL Adobe Experience Manager] 桌面应用程序完成的工作流和任务")

下载[此](assets/aem_desktop_app_usecases_print.pdf)可打印的PDF文件。

## 桌面应用程序的工作原理 {#how-app-works2}

在开始使用应用程序之前，请先了解[应用程序的工作方式](release-notes.md#how-app-works)。 此外，请熟悉以下术语：

* **[!UICONTROL Desktop Actions]**：在Assets Web界面中，您可以在浏览器中浏览资源位置或签出并打开资源以在本机桌面应用程序中编辑。 这些操作可从Web界面中获取，并且可使用桌面应用程序功能。 请参阅[如何启用桌面操作](using.md#desktopactions-v2)。

* 文件状态为&#x200B;**[!UICONTROL Cloud Only]**：此类资源未下载到本地计算机上，仅在[!DNL Experience Manager]服务器上可用。

* 文件状态为&#x200B;**[!UICONTROL Available locally]**：资源已下载并在本地计算机上可用。 资产不变。

* 文件状态为&#x200B;**[!UICONTROL Edited locally]**：此类资源已在本地修改，更改仍保留在上传到[!DNL Experience Manager]服务器中。 上传后，状态将更改为[!UICONTROL Available locally]。 请参阅[编辑资源](using.md#edit-assets-upload-updated-assets)。

* 文件状态为&#x200B;**[!UICONTROL Editing conflict]**：如果您和其他人同时编辑某个资产，则应用程序指示发生了编辑冲突。 该应用程序还提供了保留或放弃更改的选项。 请参阅[如何避免编辑冲突](using.md#adv-workflow-collaborate-avoid-conflicts)。

* 文件状态为&#x200B;**[!UICONTROL Modified remotely]**：应用程序指示您下载的资源是否在[!DNL Experience Manager]服务器上发生更改。 该应用程序还提供了下载最新版本和更新本地副本的选项。 请参阅[如何避免编辑冲突](using.md#adv-workflow-collaborate-avoid-conflicts)。

* **[!UICONTROL Check-out]**：如果您正在编辑文件或打算编辑文件，请将状态切换为签出。 它在应用程序和[!DNL Experience Manager] Web界面中的资产上添加了锁图标。 锁定图标会向其他用户指示以避免同时编辑相同的资源，因为它会导致编辑冲突。

* **[!UICONTROL Check-in]**：将资产标记为可供其他用户编辑的安全资产，而不会导致编辑冲突。 上传更改时，锁定图标将自动移除。 切换签入状态也会删除锁定图标，但Adobe建议您避免手动签入而不上传更改。 如果您放弃更改，请手动切换签入。

* **[!UICONTROL Open]**&#x200B;操作：只需打开资源即可在本机应用程序中预览它。 Adobe建议您避免使用此操作编辑资源。 原因是它不会签出资产。 同时，其他用户也可以进行编辑，导致编辑冲突。

* **[!UICONTROL Edit]**&#x200B;操作：使用操作修改图像。 单击[!UICONTROL Edit]可签出资产并在该资产上添加一个锁定图标。 单击“编辑”后，如果不想编辑该资产，请单击[!UICONTROL Toggle check-in]。 要删除、重命名或移动[!DNL Experience Manager] DAM文件夹层次结构中的资产，请使用[!DNL Experience Manager] Web界面操作，而不是编辑操作。

* **[!UICONTROL Download]**&#x200B;操作：将资源下载到本地计算机。 您可以立即下载资产并稍后编辑；脱机工作并稍后上传更改。 Assets将下载到您文件系统的缓存文件夹中。

* **[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**&#x200B;操作：将资产下载到本地缓存文件夹时，应用程序将模拟本地网络驱动器。 它为每个资源提供本地路径。 要了解此路径，请使用应用程序中的相应显示选项。 在Creative Cloud应用程序中放置资源时，需要执行展现操作。 查看[放置资源](using.md#place-assets-in-native-documents)。

* **[!UICONTROL Open In Web]**&#x200B;操作：要在[!DNL Experience Manager] Web界面中查看资产，请在Web中打开该资产。 您可以从[!DNL Experience Manager]界面启动更多工作流，如更新元数据或资源发现。

* **[!UICONTROL Delete]**&#x200B;操作：从[!DNL Experience Manager] DAM存储库中删除资产。 该操作会删除Experience Manager服务器上的资源原始副本。 如果只想放弃对本地资产的修改，请参阅[放弃更改](using.md#edit-assets-upload-updated-assets)。

* **[!UICONTROL Upload Changes]**：仅在您明确上载到[!DNL Experience Manager]服务器时，桌面应用才会上载更新的资产。 在保存编辑时，更改仅保存在本地计算机上。 上传时，资产会自动签入，并且锁图标会被移除。 请参阅[编辑资源](using.md#edit-assets-upload-updated-assets)。

## 在[!DNL Experience Manager] Web界面中启用桌面操作 {#desktopactions-v2}

从浏览器的[!DNL Assets]用户界面中，您可以浏览资产位置或签出并打开资产以在桌面应用程序中编辑。 这些选项称为[!UICONTROL Desktop Actions]，默认不启用。 要启用此功能，请执行以下步骤。

1. 在[!DNL Assets]控制台中，单击工具栏中的&#x200B;**[!UICONTROL User]**&#x200B;图标。
1. 单击&#x200B;**[!UICONTROL My Preferences]**&#x200B;以显示&#x200B;**[!UICONTROL Preferences]**&#x200B;对话框。

1. 在[!UICONTROL User Preferences]对话框中，选择&#x200B;**[!UICONTROL Show Desktop Actions For Assets]**，然后单击&#x200B;**[!UICONTROL Accept]**。

   ![选择“显示Assets的桌面操作”以启用桌面操作](assets/enable_desktop_actions.png)

   *图：选择[!UICONTROL Show Desktop Actions For Assets]以启用桌面操作。*

## 浏览、搜索和预览资源 {#browse-search-preview-assets}

您可以在[!DNL Experience Manager]存储库中浏览到、搜索和预览可用资源，所有这些操作都来自桌面应用程序。 在应用程序中尝试以下操作：

1. 浏览到文件夹并查看文件夹中可用资源的一些基本信息，以及所有资源的小型缩略图。

   ![浏览DAM文件和文件夹](assets/browse_folder_da2.png "浏览DAM文件和文件夹")

1. 要查看单个资产的更多信息和更大的缩略图，请单击文件名。

   ![查看更大的资产和操作预览](assets/large_preview_actions_da2.png "查看更大的资产和操作预览")

1. 单击&#x200B;**[!UICONTROL Open]**&#x200B;或&#x200B;**[!UICONTROL Edit]**&#x200B;可本地下载文件，并分别在本地应用程序中查看或编辑该文件。
1. 使用关键字搜索以在[!DNL Experience Manager]存储库中查找相关资源。 使用`?`和`*`作为通配符。 这些通配符分别替换单个字符或多个字符。 根据需要筛选和排序结果。

   ![使用星号通配符的示例搜索](assets/search_wildcard_da2.png "使用星号通配符的示例搜索")

   ![另一个使用星号通配符的示例搜索](assets/search_wildcard2_da2.png "另一个星号通配符位置不同的示例搜索")

>[!NOTE]
>
>应用程序通过跨多个元数据字段匹配搜索条件来显示资源，而不只是资源的标题或文件名。

## 下载资源 {#download-assets}

您可以在本地文件系统上下载资产。 应用程序从[!DNL Experience Manager]服务器获取资产，并将相同的副本保存在本地文件系统中。

单击![更多选项图标](assets/do-not-localize/more2_da2.png)查看选项，然后单击![下载图标](assets/do-not-localize/download_cloud_da2.png)进行下载。

![资源的下载选项](assets/download_option_da2.png "资源的下载选项")

>[!NOTE]
>
>下载或上传大文件或许多文件时，应用程序会关闭对资源和文件夹的操作。 下载或上传完成后，这些操作将可用。

如果队列过大，或者遇到网络问题，下载多个资源可能会导致性能不佳。 此外，在下载文件夹时，您可能会无意中将许多资产排入下载队列。 为避免过长的等待时间，应用程序会限制单次下载的资产数量。 要了解如何对其进行配置，请参阅[设置首选项](install-upgrade.md#set-preferences)。 即使低于此限制，应用程序有时也可能在下载明显较大的文件夹之前寻求确认。

![应用程序确认下载相对大量资产](assets/download_confirmation_da2.png "应用程序确认下载相对大量资产")

如果选择并下载文件夹，则应用程序仅下载直接存储在[!DNL Experience Manager]中的文件夹中的资产。 它不会自动从子文件夹下载资产。

## 在桌面上打开资产 {#openondesktop-v2}

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

单击文件夹上的&#x200B;**[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**，以使用本地计算机上预先选定的文件或文件夹打开Windows资源管理器或Mac Finder。 例如，在支持放置或链接本地文件的本地应用程序中放置[!DNL Experience Manager]文件时，选项非常有用。 若要了解如何在Adobe InDesign中放置文件，请参阅[放置图形](https://helpx.adobe.com/indesign/using/placing-graphics.html)。

**[!UICONTROL Reveal File]**&#x200B;操作将打开本地网络共享。 它仅显示本地可用的资源。 也就是说，它会显示使用应用程序显示、下载或打开/编辑的资产。 本地网络共享没有将任何更改上传到[!DNL Experience Manager]。 要上载更改，请在应用程序中显式使用&#x200B;**[!UICONTROL Upload Changes]**&#x200B;或&#x200B;**[!UICONTROL Upload]**&#x200B;操作。

>[!NOTE]
>
>为了与[!DNL Experience Manager]桌面应用程序v1.x向后兼容，显示的文件是从本地网络共享提供的，仅公开本地可用文件。 显示文件的桌面路径与应用程序v1.x创建的路径相同。

>[!CAUTION]
>
>请勿使用&#x200B;**[!UICONTROL Reveal File]**&#x200B;选项编辑本机应用程序中的资产。 请改用&#x200B;**[!UICONTROL Edit]**&#x200B;操作。 要了解更多信息，请参阅[高级工作流：对相同的文件进行协作并避免编辑冲突](#adv-workflow-collaborate-avoid-conflicts)。

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

### 管理资源名称中的特殊字符 {#special-characters-in-filename}

在旧版应用程序中，在存储库中创建的节点名称会保留用户提供的文件夹名称的空格和大小写。 若要让当前应用程序模拟v1.10应用程序的节点命名规则，请在[!UICONTROL Preferences]中启用[!UICONTROL Use legacy conventions when creating nodes for assets and folders]。 查看[应用程序首选项](/help/using/install-upgrade.md#set-preferences)。 默认情况下，此旧版首选项处于禁用状态。

>[!NOTE]
>
>应用程序使用以下命名惯例仅更改存储库中的节点名称。 应用程序保留资产的`Title`不变。

<!-- TBD: Do NOT use this table.

| Where do characters occur | Characters | Legacy preference | Renaming convention | Example |
|---|---|---|---|---|
| In file name extension | `.` | Enabled or disabled | Retained as is | NA |
| File or folder name | `. / : [ ] | *` | Enabled or disabled | Replaced with a `-` (hyphen) | `myimage.jpg` remains as is and `my.image.jpg` changes to `my-image.jpg`. |
| Folder name | `% ; # , + ? ^ { } "` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | `% # ? { } &` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Whitespaces | Enabled or disabled | Retained as is | NA |
| Folder name | Whitespaces | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Uppercase characters | Disabled | Retained as is | tbd |
| Folder name | Uppercase characters | Disabled | Replaced with a `-` (hyphen) | tbd |
-->

| 字符‡ | 应用程序中的旧版偏好设置 | 当出现在文件名中时 | 当出现在文件夹名称中时 | 示例 |
|---|---|---|---|---|
| `. / : [ ] \| *` | 启用或禁用 | 已替换为`-`（连字符）。 文件扩展名中的`.` （点）将按原样保留。 | 已替换为`-`（连字符）。 | `myimage.jpg`保持原样，`my.image.jpg`更改为`my-image.jpg`。 |
| `% ; # , + ? ^ { } "`和空格 | ![取消选择图标](assets/do-not-localize/deselect-icon.png)已禁用 | 保留空格 | 已替换为`-`（连字符）。 | `My Folder.`更改到`my-folder-`。 |
| `# % { } ? & .` | ![取消选择图标](assets/do-not-localize/deselect-icon.png)已禁用 | 已替换为`-`（连字符）。 | 不用。 | `#My New File.`更改到`-My New File-`。 |
| 大写字符 | ![取消选择图标](assets/do-not-localize/deselect-icon.png)已禁用 | 外壳保持原样。 | 更改为小写字符。 | `My New Folder`更改到`my-new-folder`。 |
| 大写字符 | ![已选中图标](assets/do-not-localize/selection-checked-icon.png)已启用 | 外壳保持原样。 | 外壳保持原样。 | 不用。 |

‡字符列表是以空格分隔的列表。

<!-- TBD: Check if the following is to be included in the footnote.

Do not use &#92;&#92; in the names of files and &#92;&#116; &#38; in the names of folders. 
-->


<!-- TBD: Securing the below presentation of the same content in a comment.

**File names**

| Characters | Replaced by |
|---|---|
| &#35; &#37; &#123; &#63; &#125; &#38; &#46; &#47; &#58; &#91; &#124; &#93; &#42; | hyphen (-) |
| whitespaces | whitespaces are retained |
| capital case | casing is retained |

>[!CAUTION]
>
>Avoid using &#92;&#92; in file names.

**Folder names**

| Characters | Replaced by |
|---|---|
| Characters | Replaced by |
| &#37; &#59; &#35; &#44; &#43; &#63; &#94; &#123; &#123; &#34; &#46; &#47; &#59; &#91; &#93; &#124; &#42; | hyphen (-) |
| whitespaces | hyphen (-) |
| capital case | lower case |

>[!CAUTION]
>
>Avoid using &#92;&#92; &#92;&#116; &#38; in folder names.

>[!NOTE]
>
>If you enable [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in app [!UICONTROL Preferences], then the app emulates v1.10 app behavior when uploading folders. In v1.10, the node names created in the repository respect spaces and casing of the folder names provided by the user. For more information, see [app Preferences](/help/using/install-upgrade.md#set-preferences).

-->

## 使用多个资产 {#work-with-multiple-assets}

用户可以使用各种操作轻松处理和管理多个资源，例如一次性上传所有编辑内容或单击几下上传嵌套文件夹。

### 浏览大型文件夹 {#browse-large-folders}

使用包含许多资源的文件夹时，请滚动查看更多资源。 要使用键盘滚动，请按几次Tab键以选择顶部的资产。 请注意高亮显示的资产，以了解何时选择该资产。 现在，使用向下箭头键在资源列表中移动。

### 所选资产的快速操作 {#quick-actions-for-selected-assets}

单击几个资源的缩略图以选择资源。 要选择所有资源，请单击应用程序顶栏中的复选框。 这组操作共同适用于所有选定资产，并将显示在应用程序底部的工具栏中。

![底部的工具栏显示与选定资源相关的操作](assets/actions_bottom_toolbar1_da2.png "底部的工具栏显示选定资源的常用操作")

![没有针对所选内容的常用操作时，工具栏中没有操作](assets/actions_bottom_toolbar2_da2.png "当所选内容没有可用的常用操作时，工具栏中不会显示任何操作。")

底部工具栏中的可用操作取决于所选文件的状态。 例如，如果只选择&#x200B;**[!UICONTROL Edited Locally]**&#x200B;文件，您会看到&#x200B;**[!UICONTROL Upload Changes]**&#x200B;图标。 如果您选择&#x200B;**[!UICONTROL Edited locally]**&#x200B;和&#x200B;**[!UICONTROL Cloud only]**&#x200B;的组合，则&#x200B;**[!UICONTROL Upload Changes]**&#x200B;操作不可用。

### 查找所有已编辑的图像 {#find-all-edited-images}

该应用程序提供了一个名为&#x200B;**[!UICONTROL Edited locally]**&#x200B;的视图，通过该视图，您可以快速访问本地下载的所有文件（通过[!UICONTROL Open]或[!UICONTROL Edit]操作），然后对其进行修改。 该应用程序允许您选择所有本地编辑的资产并单击几下以上传更改。 此视图还会显示存在编辑冲突的本地编辑的资源。

![筛选以查看所有本地编辑的资源](assets/edited_locally_filter_da2.png "例如，筛选以查看所有本地编辑的资源以进行批量编辑上传")

### 批量上传资产 {#bulk-upload-assets}

用户或组织（如摄影师或创意公司）可以在照片拍摄、修饰或从较大范围选择等活动中创建大量本地资产。 这些任务通常在[!DNL Experience Manager]之外完成。 他们可以直接从桌面应用程序将这些大型本地文件夹上传到[!DNL Assets]。 文件夹层次结构将保留，并且所有嵌套的子文件夹和包含的资产将上传。 上传的资产也可立即供同一服务器上的其他用户使用。 Assets将在后台上传，因此该操作不会绑定到Web浏览器会话。

![将多个本地文件夹从桌面批量上传到[!DNL Experience Manager]](assets/upload_local_folders_da2.png "将多个本地文件夹从桌面批量上传到Experience Manager")

上传后，如果预期更改未反映在应用程序中，请单击刷新图标![刷新图标](assets/do-not-localize/refresh.png)。

>[!NOTE]
>
>请勿使用上传功能跨两个[!DNL Experience Manager]部署迁移资产。 请参阅[迁移指南](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide)。

### 已转移的资产列表 {#list-of-transferred-assets}

要查看在给定会话中转移的资产列表，请参阅[将资产上传到 [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem)。

## 高级工作流：从[!DNL Assets] Web界面启动 {#adv-workflow-start-from-aem-ui}

如有必要，请从Assets Web界面启动工作流。 该桌面应用程序与[!DNL Experience Manager]集成，以便在使用桌面操作请求时接管。

从Web界面启动工作流的一个特殊情况是资产发现。 Assets用户界面中的Omnisearch栏提供了丰富而高级的搜索体验。 您可能希望首先在Web上找到所需的资产，然后使用[!UICONTROL Desktop Actions]在应用程序中启动工作流。 一些示例示例示例示例包括使用Facet筛选搜索结果、查找从Adobe Stock许可的特定资源，或由您的组织实施的自定义项，该自定义项允许您更好地从Web界面中发现。

当您尝试在Assets Web界面上执行以下操作时，将会使用桌面应用程序功能：

* 允许[!UICONTROL Open]、[!UICONTROL Edit]和[!UICONTROL Reveal]的[!UICONTROL Desktop Actions]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] 或 [!UICONTROL check-in]

例如，对于应用程序中签出的资产，Web界面上的可用操作为[!UICONTROL Open]、[!UICONTROL Reveal]和[!UICONTROL Check in]。

![Web界面中的[!DNL Experience Manager]桌面操作](assets/assets_web_actions_da2.png "Experience ManagerWeb界面中的")桌面操作

>[!NOTE]
>
>浏览器可能会提示您允许启动[!DNL Adobe Experience Manager]桌面。 要使每次从浏览器传输至应用程序时不会出现中断，请选中相应的复选框以允许应用程序接管任务。

使用Web界面无法找到以下信息或工作流。 使用桌面应用程序，因为Web界面不跟踪本地更改，并且不知道以下内容：

* 在本地编辑文件。
* 存在编辑冲突的文件以及解决该冲突的方法。
* 将本地更改上载到[!DNL Experience Manager]。
* 本地可用文件的各种状态。

相反，您可以使用&#x200B;**[!UICONTROL Open In Web]**&#x200B;操作从桌面应用程序开始在Web界面中打开资产。

## 高级工作流：对相同的文件进行协作并避免编辑冲突 {#adv-workflow-collaborate-avoid-conflicts}

在协作环境中，多个用户可能处理一组相同的资产，这可能会导致版本冲突。 要防止冲突，请遵循以下最佳实践：

* 不要通过单击[!UICONTROL Open]编辑任何资源。 不要通过从文件系统文件夹打开来编辑本地下载的资源。 其他用户不知道该资产正在编辑中。
* 要编辑资源，请始终单击[!UICONTROL Edit]。 它将在本机应用程序中打开资产，并在资产上添加一个锁定图标，以便其他用户知道资产正在编辑中。
* 如果您不小心开始编辑而未单击[!UICONTROL Edit]，请单击[!UICONTROL Toggle Check-in]。 此功能为资源添加一个锁图标。 即使您计划稍后编辑资产但希望避免其他人编辑它，请单击[!UICONTROL Toggle Check-in]以锁定该资产。
* 在编辑资源之前，请确保其他用户未编辑该资源。 在资源上查找锁图标。
* 完成编辑后，上传所有更改，然后签入资产。

![编辑冲突状态](assets/edits_conflicts_status_da2.png "编辑冲突状态")

如果在[!DNL Experience Manager]服务器上更新了本地下载的资产，则应用会显示&#x200B;**[!UICONTROL Modified remotely]**&#x200B;状态。 通过分别单击[!UICONTROL Remove]或[!UICONTROL Update]，您可以删除本地副本或刷新本地副本。 通过对话框中的链接，可以查看资产的两个版本。

![远程修改资源时解决冲突的选项](assets/modified_remotely_dialog_da2.png "远程修改资源时解决冲突的选项")

如果您正在本地编辑的资产也在您不知情的情况下在服务器上更新，则应用程序会显示&#x200B;**[!UICONTROL Editing Conflict]**&#x200B;状态。 您可以保留一组更改 — 保留您的更新（单击&#x200B;**[!UICONTROL Keep Mine]**）并删除其他用户的编辑，或遵循其他用户的更新并删除您的更新(**[!UICONTROL Overwrite Mine]**)。

![解决编辑冲突的选项](assets/editing_conflict_dialog_da2.png "解决编辑冲突的选项")

## 高级工作流：在InDesign文件中放置和链接资源 {#adv-workflow-place-assets-indesign}

当您使用[!DNL Experience Manager]桌面应用程序打开包含链接资源的文件时，这些资源会预先下载并显示在本机应用程序中。 要使此工作流正常工作，您的本机应用程序必须支持放置指向本地资产的链接，并且[!DNL Experience Manager]必须支持在二进制文件中将这些链接解析为服务器端引用。

[!DNL Experience Manager]桌面应用程序通过一些选定的Adobe Creative Cloud桌面应用程序和文件格式(Adobe InDesign、Adobe Illustrator和Adobe Photoshop)支持此工作流。 利用工作流，可高效地处理支持的Creative Cloud文件。 如果用户A将资源添加到InDesign文件并将其签入[!DNL Experience Manager]，则用户B可以在文件中查看资源，即使它们不属于该文件。 这些资产将在用户B的计算机上本地下载。

>[!NOTE]
>
>该桌面应用程序可以映射到Windows上的任何驱动器。 但是，为了顺利操作，请勿更改默认驱动器号。 如果同一组织的用户使用不同的驱动器号，则他们看不到其他用户放置的资产。 路径更改时，不会获取所放置的资产。 置入的资产将继续置于二进制文件（如INDD）中，并且不会被删除。

要了解此工作流的限制，请参阅[系统要求和支持的版本](release-notes.md)。

要使用图像资源和InDesign尝试此工作流，请执行以下步骤：

1. 将已放置资源的INDD文件保存在[!DNL Experience Manager]中。 要了解如何创建此类INDD文件，请参阅[放置图形](https://helpx.adobe.com/indesign/using/placing-graphics.html)。
1. 从桌面应用程序中，**[!UICONTROL Edit]**&#x200B;包含置入了[!DNL Experience Manager]中的资产的INDD文件。
1. 应用程序下载InDesign文件和链接的资源。 当InDesign打开文档时，将解析链接，下载资源，并在InDesign文档中显示资源。
1. 若要在InDesign文件中放置新图形，请对资源使用&#x200B;**[!UICONTROL Reveal File]**&#x200B;操作。 该操作将在本地下载资产，并在Windows资源管理器或Mac Finder中打开本地网络共享位置。
1. 将显示的资源放在InDesign文档中。 这样做会在文档中创建链接。
1. 在InDesign文档中完成编辑后，保存该文档并使用桌面应用程序将其上传到[!DNL Experience Manager]。

## 高级工作流：在本地下载资产 {#adv-workflow-download-assets-locally}

应用程序经常将资产从[!DNL Experience Manager]服务器下载到您的本地文件系统。 下载占用带宽和磁盘空间。 了解这些情况可以帮助您优化完成下载的等待时间。

您可以按需从应用程序中下载资产。 请参阅[下载资源](#download-assets)。

当您使用[!UICONTROL Open]操作在本机桌面应用程序中打开资产时，如果资产在本地尚不可用，则会本地下载该资产。 查看[打开资产](#openondesktop-v2)。

当您从应用程序中揭示资产或文件夹的位置时，资产或文件夹会首先在本地下载，然后在本地网络共享中的计算机上打开。 查看[打开资产](#openondesktop-v2)。

当您使用[!UICONTROL Edit]操作编辑本地桌面应用程序中的资产时，如果资产在本地尚不可用，则会本地下载该资产。 查看[编辑资源并将更新的资源上传到 [!DNL Experience Manager]](#edit-assets-upload-updated-assets)。

如果已安装应用程序并允许该应用程序，则它会在您从[!DNL Experience Manager] Web界面使用[!UICONTROL Desktop Actions]时完成操作。 应用程序先下载资产，然后完成操作。
