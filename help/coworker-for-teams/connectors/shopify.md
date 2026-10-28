---
description: Adobe Co-worker for Teams允许您连接Shopify帐户以拉入客户和区段。
title: 连接到Shopify
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 55ee8ef8f43e03720e75c9e68fccf12da8595f9c
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%
---
# 连接到Shopify {#shopify}

Adobe Co-worker for Teams允许您连接Shopify帐户以拉入客户和区段。

>[!PREREQUISITES]
>
>要使用此连接器，您必须首先具有：
>
>* 有效的Shopify帐户
>* Shopify中的以下权限： `read_customers`
>* 您的Shopify Store URL和[管理员API访问令牌](https://shopify.dev/docs/apps/build/authentication-authorization){target="_blank"}很方便

## 如何连接

1. 在[Co-worker for teams主页](https://coworker-campaigns.experience.adobe.com/){target="_blank"}上，单击&#x200B;**上下文**&#x200B;并选择&#x200B;**连接器**。

   ![团队的同事左侧导航，上下文已展开，连接器已突出显示](./assets/shopify-1.png)

1. 单击&#x200B;**添加集成**。

   在Connectors屏幕中![添加集成按钮](./assets/shopify-2.png)

   >[!NOTE]
   >
   >如果这不是您的首次集成，则该按钮将显示“添加连接器”。

1. 在Shopify行中，单击&#x200B;**连接**。

   使用“连接”按钮的![Shopify连接器磁贴](./assets/shopify-3.png)

1. 查看所需的权限并单击&#x200B;**继续**。

   使用“继续”按钮![Shopify所需的权限审核屏幕](./assets/shopify-4.png)

1. 输入您的Shopify **商店URL**&#x200B;和&#x200B;**管理员API访问令牌**。 单击&#x200B;**连接**。

>[!NOTE]
>
>在Shopify中，通过&#x200B;**设置**“**应用程序**”**开发应用程序**“**创建旧版自定义应用程序**”**管理员API配置**“**添加所需的作用域**”获取管理员API访问令牌。

![使用商店URL和管理员API访问令牌的字段连接Shopify对话框](./assets/shopify-5.png)

连接后，“Shopify”出现在“连接器”列表中。

**断开连接：**

1. 在Connectors屏幕中，找到Shopify拼贴，然后单击&#x200B;**管理**。

1. 单击&#x200B;**断开连接**（此时无需重新输入管理员API访问令牌）。

1. 再次单击&#x200B;**断开连接**&#x200B;以确认。
