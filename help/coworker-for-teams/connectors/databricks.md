---
description: Co-worker for Teams允许您连接和查询数据库工作区中的Unity Catalog表，以构建和激活活动受众。
title: 连接到数据库
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# 连接到数据库 {#databricks}

Co-worker for Teams允许您连接和查询数据库工作区中的Unity Catalog表，以构建和激活活动受众。

>[!PREREQUISITES]
>
>要使用此连接器，您必须首先具有：
>
>* 活动数据库帐户
>* 您的Databricks Workspace主机、[SQL仓库路径](https://docs.databricks.com/aws/en/compute/sql-warehouse/create){target="_blank"}、[个人访问令牌](https://learn.microsoft.com/en-us/azure/databricks/dev-tools/auth/pat){target="_blank"}和[Unity目录](https://learn.microsoft.com/en-us/azure/databricks/discover/database-objects){target="_blank"}很方便。

## 如何连接

1. 在[Co-worker for teams主页](https://coworker-campaigns.experience.adobe.com/){target="_blank"}上，单击&#x200B;**上下文**&#x200B;并选择&#x200B;**连接器**。

   ![团队的同事左侧导航，上下文已展开，连接器已突出显示](./assets/databricks-1.png)

1. 单击&#x200B;**添加集成**。

   在Connectors屏幕中![添加集成按钮](./assets/databricks-2.png)

   >[!NOTE]
   >
   >如果这不是您的首次集成，则该按钮将显示“添加连接器”。

1. 在“数据库”行中，单击&#x200B;**连接**。

   ![带有“连接”按钮的“数据库连接器”拼贴](./assets/databricks-3.png)

1. 输入您的数据库&#x200B;**Workspace主机**、**SQL仓库路径**、**个人访问令牌**&#x200B;和&#x200B;**Unity目录**。 单击&#x200B;**连接**。

   >[!NOTE]
   >
   >在数据库主页上，可以直接在浏览器的地址栏中找到Workspace主机。 要找到所有其他凭据，请参阅本文顶部的&#x200B;**先决条件**&#x200B;中的链接。

   ![使用Workspace主机、SQL仓库路径、个人访问令牌和Unity目录的字段连接数据库对话框](./assets/databricks-4.png)

连接后，Databricks将显示在Connectors列表中。

**断开连接：**

1. 在Connectors屏幕中，找到Databricks拼贴，然后单击&#x200B;**管理**。

1. 单击&#x200B;**断开连接**（此时无需重新输入您的个人访问令牌）。

1. 再次单击&#x200B;**断开连接**&#x200B;以确认。
