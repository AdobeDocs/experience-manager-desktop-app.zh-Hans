---
title: '[!DNL Adobe Experience Manager]桌面应用发行说明'
description: ' [!DNL Adobe Experience Manager] 桌面应用程序的发行详细信息、增强功能、新增功能、兼容性以及下载链接。'
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: b1fad118e1ffbd0809afe9a33bcb848648cd8bdd
workflow-type: tm+mt
source-wordcount: '2470'
ht-degree: 9%

---

# [!DNL Adobe Experience Manager]桌面应用发行说明 {#release-notes-v2}

下面是最新桌面应用程序版本3.0.0的发行信息。 发行日期为2025年7月31日。

最新版本的桌面应用程序包括以下错误修复和增强功能：

* 您可以将新创建的资源从本地计算机上传到AEM（存储了中央存储库），并在桌面应用程序中查看这些资源。
* 自动刷新功能可自动实时更新内容，确保您始终能够看到最新信息，而无需手动重新加载页面并获取已更新资产的列表。
* 固定或取消固定文件夹功能允许您通过固定重要文件夹来轻松访问它们，或者在不再需要重要文件夹时通过取消固定来取消固定视图。
* 重命名标题功能可让您轻松更新或修改资源的标题，帮助您随着内容的发展保持名称准确和有条理性。
* 通过使用复制文件操作，您可以跨本地和云位置复制文件，从而保留原始文件并对类似文件进行更改。
* 签入和签出功能允许您通过锁定文件以进行编辑（签出）并保存所做的更改而管理文件访问，同时使其对其他人可用（签入）。
* 您可以查看、下载和浏览收藏集。
* 创建新文件夹时，您可以分配元数据。
* Experience Manager桌面应用程序现在可让您将资源或文件夹移动到新位置，同时保留其元数据，从而帮助组织和简化文件系统。
* 添加了对下载收藏集中可用文件夹的支持。
* 现在，导出选项允许将选定的文件和文件夹从桌面应用程序以平面结构下载到其特定目标位置。
* 桌面应用程序现在会自动识别在本地文件系统上已下载文件夹下创建的新文件，并将它们上传到AEM。 必须保持桌面应用程序处于打开状态，才能识别本地文件系统上的新文件。
* 自动同步功能现在使收藏集中下载的资源定期将AEM资源管理与本地文件系统同步。
* AEM桌面应用程序现在允许您查看文件夹属性，如文件夹缩略图、大小、路径、创建日期、标记、元数据等。
* 您现在可以访问“卡片”视图、“网格”视图或“树”视图中的资产，以便获得干净、有条理、美观的资产布局。
* 能够将资产从桌面应用程序拖到目标Creative Cloud应用程序。 桌面应用程序会自动签出资产并将其下载到本地文件系统。
* 当您更新属于某个收藏集的资产时，系统会自动在临时缓存文件夹和桌面应用程序UI中更新该资产。
* UI上更新了各种选项的各种标签，使应用程序更加直观。

**支持的[!DNL Experience Manager]版本**&#x200B;包括：

* [!DNL Experience Manager]作为[!DNL Cloud Service]。 请参阅[发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/release-notes/home)。
* [!DNL Experience Manager] 6.5.0或更高版本，位于Adobe Managed Services (AMS)或内部部署上。 请参阅[service pack发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/release-notes/release-notes)。

[!DNL Adobe Experience Manager]桌面应用程序可用于以下&#x200B;**操作系统**：

* macOS X 10.14或更高版本，带有最新的错误修复。
* Windows 10，带有最新的Service Pack和错误修复。

Windows安装程序有两个版本可用于AEM桌面应用程序版本2.3.1及更高版本。 基本安装程序将在用户的本地应用程序数据目录下安装AEM桌面应用程序。 Adobe建议为其大多数用户执行此安装过程。 企业版Windows安装程序也可用，它将AEM桌面应用程序安装在共享程序文件目录下。 这两种安装程序安装相同版本的AEM桌面应用程序，并且在功能上没有任何差异。

支持的操作系统的&#x200B;**下载URL**&#x200B;包括：

| 操作系统 | [!DNL Experience Manager] as a [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v3.0.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-3.0.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-3.0.0.dmg) |
| macOS Apple Silicon (M1) (v3.0.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-3.0.0.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-3.0.0.dmg) |
| Windows 64位(v3.0.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-3.0.0.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-3.0.0.exe) |
| Windows 64位企业版(v3.0.0) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-ent-3.0.0.msi) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-ent-3.0.0.msi) |
| macOS (v2.3.3) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.3.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.3.dmg) |
| macOS Apple Silicon (M1) (v2.3.3) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.3.dmg) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.3.dmg) |
| Windows 64位(v2.3.3) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.3.exe) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.3.exe) |
| Windows 64位企业版(v2.3.3) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.3.msi) | [下载链接](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.3.msi) |
| macOS (v2.3.1) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081954149%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=mwSX5ilZL0he2raIx8t5ecQ%2FWuizky4MpcCXX3mEN38%3D&reserved=0) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081981239%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=LJH3OCFq7yRykN4wU8HN9%2FBXC%2BjfXLJH4QizeFZfRHE%3D&reserved=0) |
| macOS Apple Silicon (M1) (v2.3.1) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081965822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=2YENn0tDduiucogClt6aBZHDOE6dbzBdigq8VQawIO0%3D&reserved=0) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081986151%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=jCepldg4dMej0%2BrK2mUonXwqsWL8ksE8%2BLMSgsH9qTA%3D&reserved=0) |
| Windows 64位(v2.3.1) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081970892%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=sRn2UWW%2Bi7SMEvSO74ZGGvJ40vHh1KhLc7zAfKc37Es%3D&reserved=0) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081991004%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=aQWZtEK%2F3cWX8n8Au%2FwZ5Zd9xPVo5phvk%2FuF%2Be0HRrE%3D&reserved=0) |
| Windows 64位企业版(v2.3.1) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081976350%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=v9C0sLDSkuL%2FMIyae2WkbitJPVgSlAw2BqcaH5Im0uw%3D&reserved=0) | [下载链接](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081995827%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=2btCh0aIrUBiyeG37K9YorvzTeIJOggbq%2FRauUMn4LY%3D&reserved=0) |
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

应用程序支持存储在[!DNL Experience Manager]中的资产，这些资产代表用于其基本操作的二进制文件。 在本机桌面应用程序中打开文件，取决于特定文件类型（如 PNG 或 JPG）与特定应用程序（如 Mac Preview 或 Adobe Photoshop）的操作系统关联。

一些文件类型支持将链接的资产放入二进制文件中。使用桌面应用程序打开此类二进制文件时，如果资产存在于[!DNL Experience Manager]存储库中，则应用程序会预下载链接的资产。 当前支持的文件类型有：

* [!DNL Adobe InDesign]文件（INDD格式）
* [!DNL Adobe Illustrator]文件（AI格式）
* [!DNL Adobe Photoshop]文件（PS格式）

上述应用程序的[!DNL Adobe Creative Cloud] 2018和[!DNL Adobe Creative Cloud] 2019版本支持该功能。 应用程序使用启发式的最佳匹配方法将链接资产的本地桌面路径映射到[!DNL Experience Manager]服务器上的URL。 这是基于以下假设：

* 本机应用程序中放置文件的路径使用全局桌面路径（从带有[!UICONTROL Reveal]选项的本地网络共享放置）。

* 路径由本机应用程序存储在文件的XMP记录中。

* [!DNL Experience Manager]已提取XMP记录，其中包含资源元数据记录的路径。

* 路径可以与[!DNL Experience Manager]中的资源匹配，也就是说，放置的文件也位于匹配路径下的[!DNL Experience Manager]中。

## 新增功能、增强功能和错误修复 {#what-is-new}

要了解详细信息，请参阅[v2.0](introduction.md#whats-new-v2)的新增功能。

**应用程序v2.3.1**&#x200B;中的更新

* 新的Enterprise Windows Installer将应用程序安装在Program Files下。
* 在AEM和SSO登录期间支持&#x200B;**基本身份验证**。
* 上传操作期间允许的资源可配置数量

**应用程序v2.3.0**&#x200B;中的更新

* 添加了对IMS登录的支持。 IMS集成允许桌面应用程序自动执行访问令牌刷新，允许用户保持登录最多14天。

* 改进了对企业代理和Web过滤的支持。

**应用程序v2.2.2**&#x200B;中的更新

* （仅限Windows）安装2.2.0和2.2.1发行版后，桌面应用程序显示一个空白屏幕。

**应用程序v2.2.1**&#x200B;中的更新

* 单击&#x200B;**[!UICONTROL Sign In]**&#x200B;时，桌面应用会显示会话超时错误消息。

* 在macOS上访问桌面应用程序v2.2.0时出现问题。

* 通过单击&#x200B;**[!UICONTROL Edited Locally]**&#x200B;对资源进行排序时，桌面应用会显示错误消息。

**应用程序v2.2.0**&#x200B;中的更新

* 支持Apple硅(M1)。

* 在登录到桌面应用程序时能够记住连接字符串。

**应用程序v2.1.5.0**&#x200B;中的更新

* 上传包含中文字符的文件夹中的文件时，桌面应用程序停止响应(ASSETS-9237)。

* 桌面应用程序在文件名中使用短划线替换圆点(ASSETS-10955)。

**应用程序v2.1.4.0**&#x200B;中的更新

应用程序的新版本提供了错误修复。

**应用程序v2.1.3.4**&#x200B;中的更新

应用程序的新版本提供了错误修复。

**应用程序v2.1.3.3**&#x200B;中的更新

应用程序的新版本提供了错误修复。

**应用程序v2.1.3.2**&#x200B;中的更新

此版本的应用程序提供了错误修复。

**应用程序v2.1.3.1**&#x200B;中的更新

此版本中修复的错误为：

* 即使对于大型资产，资产上传和下载速度也得到了改进。 此版本修复了在上载超大文件时，有时通过[!DNL desktop app]上载资产失败的问题。

**在应用程序v2.1.2.0**&#x200B;中更新

* [!UICONTROL Clear Cookies]的新选项已添加到应用程序的主菜单。 它有助于解决潜在的登录问题，例如，在将连接从服务器更改为另一个服务器时。 在连接[之前查看](/help/using/troubleshoot.md#cannot-login-cookies-issue)清除Cookie。

* 新增了一个选项，如果选定该选项，则允许应用程序上传节点名称在[!DNL Adobe Experience Manager]中与本地文件和文件夹名称匹配的文件夹和文件。 此过程可确保本地名称和上传名称之间的一致性。

  此行为类似于桌面应用程序版本1中的默认行为。 而在当前版本中，如果未启用该选项，则文件夹名称中的空格和字符`% ; # , + ? ^ { } "`将被文件夹路径中的破折号替换。 此外，文件夹路径中的大写字符将转换为小写。 但是，在文件名中，字符`# % { } ? &`被替换为短划线；但保留空格和大小写。 有关详细信息，请参阅[应用程序首选项](/help/using/install-upgrade.md#set-preferences)和[上传并添加新资源](/help/using/upload-assets.md#upload-and-add-new-assets-to-aem)。

**在应用程序v2.1.1.0**&#x200B;中更新

* 高级设置允许应用程序在上传文件夹时模拟v1.10应用程序行为。 在v1.10中，在存储库中创建的节点名称会遵循用户提供的文件夹名称的空格和大小写。 在版本2.1中，默认行为保持不变：文件夹名称中的多个空格在存储库节点名称中被替换为连字符，节点名称转换为小写。 查看[应用程序首选项](/help/using/install-upgrade.md#set-preferences)。

**在应用程序v2.1.0.0**&#x200B;中更新

* 要上传资源，用户现在可以直接从Windows资源管理器或Mac Finder将文件或文件夹拖动到应用程序界面上。 除了应用程序中提供的上传选项外，此过程还有效。 查看[上传资源](/help/using/upload-assets.md#upload-and-add-new-assets-to-aem) <!-- CQ-4309527 -->

**在应用程序v2.0.3**&#x200B;中更新

此版本中修复的错误为：

* 修复了Windows上尝试访问[!DNL Adobe Experience Manager] 6.5.5.0上的DAM存储库的应用程序用户的登录问题。

**应用程序v2.0.2**&#x200B;中的更新

错误修复和更新包括：

* 现在提供上传加速设置以提高上传性能。 打开此设置后，应用程序将使用更多本地CPU线程来更快地上传，并且会更加耗费资源。

* 修复了包含特定GB18030字符的文件名或路径时上传资源。<!-- CQ-4283494 -->

* 在搜索结果中切换到其他排序类型后，可以按相关性排序选项。<!-- CQ-4286874 -->

* 现在，桌面应用程序会列出子文件夹，而无需显式刷新。<!-- CQ-4285711 -->

* (Windows)修复了某些Windows计算机上应用程序界面不可用的罕见问题。 用户无法单击应用程序界面，因为它似乎因界面元素的单击区域向侧“偏移”而被扭曲。<!-- CQ-4280785 -->

**应用程序v2.0.1**&#x200B;中的更新

错误修复和更新包括：

* 允许选项配置`%Temp%`目录以匹配`%APPDATA%`路径。<!-- CQ-4282665 -->

* 允许用户通过Okta SAML身份验证登录[!DNL Experience Manager]作者。<!-- CQ-4278134 -->

## 安装说明 {#installation-instructions-v2}

要了解如何安装和配置应用程序，请参阅[安装 [!DNL Experience Manager] 桌面应用程序](install-upgrade.md)。

如果您是从以前的[!DNL Experience Manager]桌面应用程序升级，则必须按照[中列出的从以前的版本](install-upgrade.md#upgrade-from-previous-version)进行升级的最佳实践进行转换。

## 有关应用程序工作方式的重要说明 {#how-app-works}

请务必了解关于应用程序及其工作方式的以下信息。

* 对于需要在与[!DNL Experience Manager]之间完全传输资源二进制文件的操作，应用程序提供了完全控制权(**打开**、**编辑**、**上传更改**&#x200B;和&#x200B;**上传Assets**)。

   * 如果要在桌面上处理资产，则必须明确地在某个文件夹中逐个或通过多选方式打开、编辑资产或将其下载到桌面。

   * 如果要将对资产所做的本地更改上传到[!DNL Experience Manager]，您需要逐个或通过多选方式选择[!UICONTROL Upload Changes]。

   * 该应用程序不是在桌面和[!DNL Experience Manager]之间同步资产的“同步客户端”。

   * 应用程序不提供将[!DNL Experience Manager]存储库映射为虚拟文件夹结构的网络共享。

* 应用程序显示的资源列表基于Assets存储库的状态。 从本地下载并随后在本地文件或缓存文件夹中重命名的文件不会显示或通过该应用程序进行管理。

* 如果应用程序不显示预期结果，请单击顶栏中的刷新图标。

* 使用 [!UICONTROL Reveal File] 操作时显示的本地网络共享，仅显示本地可用的文件（和文件夹）。[!UICONTROL Reveal File] 和 [!UICONTROL Reveal Folder] 会预下载资产，以帮助在本地网络共享中显示正确的资产。

* 当Adobe Creative Cloud应用程序读取链接/放置在Creative Cloud应用程序本机文件中的资源文件时，会使用SMB (Mac)/WebDAV (Win)本地网络共享。

下图说明了由用户操作启动的资产和文件从云端到本地文件系统和相反方向的流程。

![资产通过桌面应用程序从[!DNL Experience Manager]服务器流向本机桌面应用程序](assets/da20_flow_diagram.png)

## 已知问题 {#known-issues-v2}

**用户界面问题：**

* 有时，桌面应用程序的界面可能会变为空白。 右键单击并单击[!UICONTROL Refresh]以重新加载应用程序。 进行此类刷新后，您将从DAM存储库的根目录开始。 将保留对资源的更新或状态。<!-- CQ-4270267 -->

* 在没有轨迹板或鼠标指针的情况下，很难导航文件夹/搜索结果。 使用无滚轮鼠标设备时，不会显示滚动条。<!-- CQ-4269947 -->

* 在少数情况下，上传资产更改时，无法正确显示进度栏。

* 在应用筛选器以查找所有本地编辑的资产和删除筛选器后，应用程序不会为用户呈现搜索结果或者用户开始执行筛选时所在的文件夹视图。应用程序会显示 DAM 存储库的根文件夹。

* 有时，当您连接到未运行[!DNL Experience Manager]服务器的URL时，连接屏幕会变得无响应。 可退出应用程序后重新启动。

**CRUD（创建、读取、更新和删除）问题：**

* 在上传包含注释的资源更改时，这些注释会与资源一起存储在[!DNL Experience Manager]中，但不会显示为版本控制注释。 此问题已在[!DNL Experience Manager] 6.4.5和[!DNL Experience Manager] 6.5.1中解决。Adobe建议安装最新的Service Pack。<!-- CQ-4268990 -->

* 用户无法取消资产传输。 如果意外触发了大量传输，请退出应用程序后重新启动。<!-- CQ-4278940 -->

**平台问题：**

* 有时，在 Windows 上，打开资产后其状态可能会立即变为 [!UICONTROL Edited Locally]，即使您可能没有进行任何编辑也是如此。可单击 [!UICONTROL Refresh] 进行更新。

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] 作为 [!DNL Cloud Service] 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service)
>* [[!DNL Experience Manager] as a [!DNL Cloud Service] [!DNL Assets]文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview)
>* [如何使用 [!DNL Experience Manager] 桌面应用程序](using-desktop-app.md)
>* [安装和升级桌面应用程序](install-upgrade.md)
>* [最佳实践和故障诊断提示](troubleshoot.md)
