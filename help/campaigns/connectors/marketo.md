---
description: 了解如何将您的Marketo Engage帐户关联到同事营销活动，以便同步Marketo智能列表和静态列表。
title: 连接到Marketo Engage
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%
---
# 连接到Marketo Engage {#marketo}

Adobe同事营销活动允许您连接Marketo Engage帐户以拉入智能和静态列表。

>[!PREREQUISITES]
>
>要使用此连接器，您必须首先具有：
>
>* 有效的Marketo Engage帐户
>* 您的Marketo **实例URL**
>* 为Marketo中的同事营销活动创建的[自定义服务](https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/rest/custom-services#custom-services-1)，它有[客户端ID和客户端密钥](https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/rest/authentication#creating-an-access-token)

## 如何连接

1. 在[同事营销活动主页](https://coworker-campaigns.experience.adobe.com/)上，单击&#x200B;**自定义**&#x200B;并选择&#x200B;**连接器**。

   ![同事营销活动左导航，已展开自定义并突出显示连接器](./assets/marketo-1.png)

1. 单击&#x200B;**添加集成**。

   在Connectors屏幕中![添加集成按钮](./assets/marketo-2.png)

   >[!NOTE]
   >
   >如果这不是您的首次集成，则该按钮将显示“添加连接器”。

1. 在Marketo行中，单击&#x200B;**连接**。

   使用“连接”按钮的![Marketo连接器磁贴](./assets/marketo-3.png)

1. 输入您的Marketo **实例URL**、**客户端ID**&#x200B;和&#x200B;**客户端密钥**。 单击&#x200B;**连接**。

   >[!NOTE]
   >
   >查看“我的Marketo”页面时，您可以在浏览器的地址栏中找到您的Marketo实例URL。

   ![使用实例URL、客户端ID和客户端密码的字段连接Marketo对话框](./assets/marketo-4.png)

连接后，Marketo将显示在连接器列表中，并在将联系人列表链接到从Marketo同步时进行选择。

**断开连接：**

1. 在Connectors屏幕中，找到Marketo拼贴，然后单击&#x200B;**管理**。

   ![Connectors屏幕，Marketo拼贴显示“已连接”状态和“管理”按钮](./assets/marketo-5.png)

1. 单击&#x200B;**断开连接**（此时无需重新输入您的客户端密钥）。

   ![使用实例URL和客户端ID字段以及“断开连接”按钮管理Marketo对话框](./assets/marketo-6.png)

   >[!NOTE]
   >
   >首次添加实例URL后，它将默认为REST终结点URL，以`*.mktorest.com`结尾。

1. 再次单击&#x200B;**断开连接**&#x200B;以确认。

   ![断开连接确认对话框](./assets/marketo-7.png)
