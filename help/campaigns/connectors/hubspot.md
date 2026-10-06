---
description: 使用Service Key将您的HubSpot帐户连接到Co-worker Campaigns以同步联系人列表，然后随时管理或断开集成。
title: 连接到HubSpot
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%
---
# 连接到HubSpot {#hubspot}

Adobe同事营销活动允许您连接HubSpot帐户以拉入联系人列表。

>[!PREREQUISITES]
>
>要使用此连接器，您必须首先具有：
>
>* 有效的HubSpot帐户
>* 已添加使用以下范围创建的[服务密钥](https://developers.hubspot.com/docs/apps/developer-platform/build-apps/authentication/account-service-keys#create-a-service-key)： `crm.objects.contacts.read`、`crm.objects.leads.read`、`crm.schemas.contacts.read`、`crm.lists.read`、`crm.export`

## 如何连接

1. 在[同事营销活动主页](https://coworker-campaigns.experience.adobe.com/)上，单击&#x200B;**自定义**&#x200B;并选择&#x200B;**连接器**。

   ![在侧栏中展开自定义菜单，并选择了连接器](./assets/hubspot-1.png)

1. 单击&#x200B;**添加集成**。

   在Connectors屏幕上![添加集成按钮](./assets/hubspot-2.png)

   >[!NOTE]
   >
   >如果这不是您的首次集成，则该按钮将显示“添加连接器”。

1. 在HubSpot行中，单击&#x200B;**连接**。

   ![突出显示了“连接”按钮的HubSpot拼贴](./assets/hubspot-3.png)

1. 此时将显示一个模式窗口，其中显示了必要的权限（本文顶部的先决条件中列出了这些权限）。 单击&#x200B;**继续**。

1. 输入HubSpot **服务密钥**&#x200B;并单击&#x200B;**连接**。

   ![使用“服务密钥”字段和“连接”按钮连接HubSpot对话框](./assets/hubspot-4.png)

连接后，HubSpot将出现在Connectors列表中，在链接联系人列表以从HubSpot进行同步时可以选择。

**断开连接：**

1. 在Connectors屏幕中，找到HubSpot拼贴，然后单击&#x200B;**管理**。

   ![Connectors屏幕显示与“管理”按钮连接的HubSpot高亮显示](./assets/hubspot-5.png)

1. 单击&#x200B;**断开连接**（此时无需重新输入您的服务密钥）。

   ![突出显示了“断开连接”按钮的“管理HubSpot”对话框](./assets/hubspot-6.png)

1. 再次单击&#x200B;**断开连接**&#x200B;以确认。

   ![断开连接确认对话框，突出显示“断开连接”按钮](./assets/hubspot-7.png)
