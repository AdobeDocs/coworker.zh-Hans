---
description: 了解如何将团队的同事连接到您的Salesforce帐户以访问您的潜在客户和联系人。
title: 连接到Salesforce
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%
---
# 连接到Salesforce {#salesforce}

Co-worker for teams允许您连接您的Salesforce帐户以访问潜在客户和联系人。

>[!PREREQUISITES]
>
>要使用此连接器，您必须首先具有：
>
>* 有效的Salesforce帐户
>* Salesforce中的以下权限： `api`、`sobjects.Contact.read`、`sobjects.Campaign.read`、`sobjects.CampaignMember.read`
>* 您的Salesforce实例URL、[客户端ID和客户端密钥](https://help.salesforce.com/s/articleView?id=xcloud.remoteaccess_oauth_client_credentials_flow.htm&type=5#:~:text=DESCRIPTION-,client_id,-The%20consumer%20key){target="_blank"}很方便

## 如何连接

1. 在[Co-worker for teams主页](https://coworker-campaigns.experience.adobe.com/){target="_blank"}上，单击&#x200B;**上下文**&#x200B;并选择&#x200B;**连接器**。

   ![团队的同事左侧导航，上下文已展开，连接器已突出显示](./assets/salesforce-1.png)

1. 单击&#x200B;**添加集成**。

   在Connectors屏幕中![添加集成按钮](./assets/salesforce-2.png)

   >[!NOTE]
   >
   >如果这不是您的首次集成，则该按钮将显示“添加连接器”。

1. 在Salesforce行中，单击&#x200B;**连接**。

   使用“连接”按钮的![Salesforce连接器磁贴](./assets/salesforce-3.png)

1. 输入您的Salesforce **实例URL**、**客户端ID**&#x200B;和&#x200B;**客户端密钥**。 单击&#x200B;**连接**。

   >[!NOTE]
   >
   >* 在Salesforce中，客户端ID =使用者密钥，而客户端密钥=使用者密钥。
   >
   >* 在您的Salesforce帐户中，您可以在浏览器的地址栏中找到实例URL，也可以导航到&#x200B;**设置** > **公司设置** > **我的域**。

   ![使用实例URL、客户端ID和客户端密码的字段连接Salesforce对话框](./assets/salesforce-4.png)

连接后，Salesforce将显示在连接器列表中，并在关联潜在客户或联系人列表以从Salesforce同步时进行选择。

**断开连接：**

1. 在Connectors屏幕中，找到Salesforce拼贴，然后单击&#x200B;**管理**。

   ![连接器屏幕显示与“管理”按钮突出显示的Salesforce连接](./assets/salesforce-5.png)

1. 单击&#x200B;**断开连接**（此时无需重新输入您的客户端密钥）。

   ![突出显示了“断开连接”按钮的“管理Salesforce”对话框](./assets/salesforce-6.png)

1. 再次单击&#x200B;**断开连接**&#x200B;以确认。

   ![断开连接确认对话框，突出显示“断开连接”按钮](./assets/salesforce-7.png)
