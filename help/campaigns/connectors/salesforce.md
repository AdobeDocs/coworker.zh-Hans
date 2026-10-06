---
description: 描述。
title: 连接到Salesforce
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 12ee914ed944c82694b9373f611e19cf040e2229
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%
---
# 连接到Salesforce {#salesforce}

Adobe同事营销活动允许您连接Salesforce帐户以访问潜在客户和联系人。

>[!PREREQUISITES]
>
>要使用此连接器，您必须首先具有：
>
>* 有效的Salesforce帐户
>* Salesforce中的以下权限： `api`、`sobjects.Contact.read`、`sobjects.Campaign.read`、`sobjects.CampaignMember.read`
>* 您的Salesforce实例URL、[客户端ID和客户端密钥](https://help.salesforce.com/s/articleView?id=xcloud.remoteaccess_oauth_client_credentials_flow.htm&type=5#:~:text=DESCRIPTION-,client_id,-The%20consumer%20key)很方便

## 如何连接

1. 在[同事营销活动主页](https://coworker-campaigns.experience.adobe.com/)上，单击&#x200B;**自定义**&#x200B;并选择&#x200B;**连接器**。

   ![同事营销活动左导航，已展开自定义并突出显示连接器](./assets/salesforce-1.png)

1. 单击&#x200B;**添加集成**。

   在Connectors屏幕中![添加集成按钮](./assets/salesforce-2.png)

   >[!NOTE]
   >
   >如果这不是您的首次集成，则该按钮将显示“添加连接器”。

1. 在Salesforce行中，单击&#x200B;**连接**。

   ![](./assets/salesforce-3.png)

1. 输入您的Salesforce **实例URL**、**客户端ID**&#x200B;和&#x200B;**客户端密钥**。 单击&#x200B;**连接**。

   >[!NOTE]
   >
   >* 在Salesforce中，客户端ID =使用者密钥，而客户端密钥=使用者密钥。
   >
   >* 在您的Salesforce帐户中，您可以在浏览器的地址栏中找到实例URL，也可以导航到&#x200B;**设置** > **公司设置** > **我的域**。

   ![](./assets/salesforce-4.png)

连接后，Salesforce将显示在连接器列表中，并在关联潜在客户或联系人列表以从Salesforce同步时进行选择。

**断开连接：**

1. 在Connectors屏幕中，找到Salesforce拼贴，然后单击&#x200B;**管理**。

   ![](./assets/salesforce-5.png)

1. 单击&#x200B;**断开连接**（此时无需重新输入您的客户端密钥）。

   ![](./assets/salesforce-6.png)

1. 再次单击&#x200B;**断开连接**&#x200B;以确认。

   ![](./assets/salesforce-7.png)
