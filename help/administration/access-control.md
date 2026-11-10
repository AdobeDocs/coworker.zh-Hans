---
title: 同事的访问控制
description: 了解Adobe CX Enterprise Coworker的访问控制以及兼容Adobe产品中的权限。 查找管理员控制并获取有关访问权限的帮助。
last-substantial-update: 2026-11-04
level: beginner
role: Admin
jira: KT-22980
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: d9dae093a2a6366154366a9da320f07a891114f2
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%
---
# 同事的访问控制 {#access-control}

使用Adobe CX Enterprise Coworker访问控制来管理谁可以使用同事以及他们可以使用哪些功能。

访问控制适用于右边栏和全屏体验中的同事。

>[!NOTE]
>
>访问控制正在逐步推广到所有具有同事访问权限的客户。 您可能尚未在组织中看到[!UICONTROL 访问控制]。 有关详细信息，请参阅[获取有关访问权限的帮助](#get-help-with-access)。

## 如何确定访问权限 {#how-access-is-determined}

同事访问权限由组织范围的设置和可选的用户或组覆盖控制。 组织范围的设置可启用或禁用组织中用户的同事访问权限。 默认情况下，为每个人启用访问权限。

| 设置 | 它如何影响访问 |
| --- | --- |
| 组织范围设置 | 为每个人启用同事访问权限或为您的组织禁用它。 |
| 用户或用户组覆盖 | 通过覆盖，管理员可以控制特定用户或用户组的同事访问权限。 |
| 兼容的应用程序权限 | 同事访问控制确定您是否可以访问任何一般可用的同事功能。 同事从与同事兼容的CX Enterprise应用程序继承您的用户权限，并尊重每个应用程序已强制执行的权限。 |


## 同事管理员 {#add-coworker-admins}

同事管理员是作为组织的系统管理员&#x200B;**[!UICONTROL 或作为[!DNL Adobe Admin Console]中[!DNL Adobe Experience Platform]的**&#x200B;[!UICONTROL &#x200B;产品管理员&#x200B;]&#x200B;**分配的用户。]**

## 管理用户访问权限 {#manage-user-access}

1. 打开同事体验。 有关说明，请参阅[登录到同事](/help/chat/ui-guide.md#sign-in)。
2. 打开配置文件菜单，然后选择&#x200B;**[!UICONTROL 管理员设置]**。

   ![突出显示配置文件菜单控件的同事主页。](./assets/access-control/coworker-home.png)

   ![突出显示管理员设置的“同事配置文件”菜单。](./assets/access-control/admin-settings.png)

3. 选择&#x200B;**[!UICONTROL 访问控制]**。

   ![访问控制卡突出显示的管理员设置。](./assets/access-control/access-control.png)

   使用本视频了解如何管理同事用户。

   >[!VIDEO](https://video.tv.adobe.com/v/3507159?captions=chi_hans&learn=on){transcript=true}

4. 在同事中，使用&#x200B;**[!UICONTROL 用户]**&#x200B;管理个人的访问权限，或使用&#x200B;**[!UICONTROL 用户组]**&#x200B;管理用户组的同事访问权限。 用户组设置适用于其成员。

   辅助用户组与[!DNL Adobe Admin Console]组不同。 即将从[!DNL Adobe Admin Console]将用户组同步到同事。

   “用户”列表包括您组织中的用户。 默认情况下，为这些用户启用了同事访问。

   * **已启用：**&#x200B;用户或用户组处于活动状态。
   * **已禁用：**&#x200B;用户或用户组处于非活动状态。

   禁用每个人的访问权限后，打开&#x200B;**[!UICONTROL 允许覆盖]**&#x200B;并选择&#x200B;**[!UICONTROL 添加覆盖]**&#x200B;以添加仍应具有访问权限的用户或组。

## 与同事兼容的CX Enterprise应用程序中的权限 {#permissions-in-compatible-applications}

与同事兼容的CX Enterprise应用程序将继续强制实施其自身的权限。

同事尊重兼容应用程序中的权限。 例如，如果您无法访问[!DNL Adobe Experience Platform]中的数据集，则同事无法为您检索或处理该数据集。

## 获取有关访问权限的帮助 {#get-help-with-access}

如果您没有看到[!UICONTROL 访问控制]，请联系您的Adobe管理员或Adobe代表。 他们可以确认是否为您的组织启用了该功能以及您是否有权访问其设置。

如果您被拒绝访问，请要求管理员查看组织范围的默认设置以及任何用户或组设置。 对于与同事兼容的CX Enterprise应用程序，请要求他们检查针对该应用程序单独管理的权限。

## 有关此主题的更多帮助 {#more-help}

使用这些资源了解有关同事和管理的更多信息。

* [同事聊天概述](/help/chat/overview.md)
* [同事聊天入门](/help/chat/ui-guide.md)
* [管理插件和市场](/help/customizations/plugins/manage-plugins-for-your-org.md)
