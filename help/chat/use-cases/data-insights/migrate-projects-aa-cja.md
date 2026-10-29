---
title: 将Adobe Analytics项目迁移到Customer Journey Analytics
description: 使用同事验证、映射Adobe Analytics Workspace项目及其组件，并将其迁移到Customer Journey Analytics，然后检查迁移状态。
feature: AI Tools
role: Admin
level: Intermediate
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '1785'
ht-degree: 1%
---

# 与同事一起将Adobe Analytics项目迁移到Customer Journey Analytics

<!-- FLAG: Confidence: High for the conversation flow, which is sourced from screenshots of the Coworker UI (October 2026) and the aa-mcp tool descriptions. The component migration tools run through the aa-mcp integration; there's no dedicated skill yet. Medium for statements that Coworker shares mappings and migration rules with migrations in the Adobe Analytics user interface; the user believes this is likely. Confirm with engineering. -->

使用Adobe CX Enterprise Coworker可在单个对话中将Adobe Analytics项目及其关联的组件迁移到Customer Journey Analytics。

同事会验证项目中的维度和量度是否已映射到Customer Journey Analytics数据视图，帮助您映射任何未映射的维度和量度，然后在Customer Journey Analytics中重新创建项目。

<!-- FLAG: Add the planned general availability date when it's confirmed. -->

>[!AVAILABILITY]
>
>本文中描述的功能处于版本的有限测试阶段，可能尚未在您的环境中可用。 当功能正式可用时，将删除此注释。

>[!IMPORTANT]
>
>在迁移任何项目之前，请阅读Adobe Analytics文档中的[准备将组件和项目从Adobe Analytics迁移到Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration)。 它介绍了如何准备迁移、包含的内容、哪些元素会导致错误以及映射如何影响整个组织。 此信息适用于协同工作中的迁移。

## 与Adobe Analytics用户界面中迁移的区别

<!-- FLAG: Add rows as differences are confirmed. Who can migrate and How you migrate: SME Scott Tomko (October 2026); Coworker matches the Analytics 2.0 Component Migration APIs, and functionally both methods do much the same thing. Project owner: Coworker behavior is from a test conversation (October 2026); the Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. Mapping dimensions and metrics: Confidence Medium for the Coworker column, which is based on the aa-mcp tool descriptions and a test conversation, not on an observed failed validation. Confirm that Coworker suggests and updates mappings, and whether it asks for confirmation before it updates a mapping. The Adobe Analytics user interface behavior is from component-migration.md in the Adobe Analytics docs. -->

通过同事迁移项目与在Adobe Analytics用户界面中迁移项目有所不同，其具体方式如下：

| | Coworker | Adobe Analytics用户界面 |
| --- | --- | --- |
| **谁可以迁移项目** | Adobe Analytics管理员和具有&#x200B;[!UICONTROL **组件迁移**]&#x200B;权限的用户 | 仅限Adobe Analytics管理员 |
| **项目所有者** | 正在执行迁移的用户 | 您在&#x200B;[!UICONTROL **项目所有者**]&#x200B;字段中指定的用户 |
| **映射维度和量度** | 同事将验证项目并列出每个维度和量度的映射方式。 对于任何无法自动映射的维度，Co-worker会在您的数据视图中建议一个维度或量度，并更新映射。 | 在&#x200B;[!UICONTROL **映射架构**]&#x200B;部分中，您选择每个具有&#x200B;[!UICONTROL **未映射**]&#x200B;状态的维度或量度并手动映射它。 |
| **如何迁移** | 在提示中描述所需的内容。 同事负责工作，并在此过程中提出一些问题。 例如，Co-worker可以使用您命名的组件创建一个项目，然后对其进行迁移。 请参阅[从特定组件启动](#start-from-specific-components)。 | 在Analysis Workspace中创建项目，添加要迁移的组件，然后保存项目。 然后，在&#x200B;[!UICONTROL **组件迁移**]&#x200B;中，选择项目，指定项目所有者，映射每个报表包的架构，然后选择&#x200B;[!UICONTROL **迁移**]。 |

## 先决条件

<!-- FLAG: Confidence: High for the Adobe Analytics MCP and permission bullets, which come from the release announcement and SME Scott Tomko (October 2026): like the Analytics 2.0 Component Migration APIs, Coworker lets non-admins with the Component Migration permission migrate projects, while the Adobe Analytics UI is admin-only. Open question: Coworker makes the user who runs the migration the owner of the new project, but the aa-mcp tool description says the owner "should be an admin" and the Adobe Analytics component migration docs say the owner must be a Customer Journey Analytics administrator. Confirm whether a non-admin who runs a migration needs Customer Journey Analytics admin rights, or whether Coworker assigns a different owner. -->

要与同事迁移项目，您需要：

* 访问Adobe Analytics MCP。 对于具有Adobe Analytics MCP访问权限的客户，组件迁移工具会自动启用。 要确认&#x200B;[!UICONTROL **aa-mcp**]&#x200B;已连接，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。

* Adobe Analytics管理员权限，或Admin Console中的&#x200B;[!UICONTROL **组件迁移**]&#x200B;权限。 您无需成为管理员。

* Adobe Analytics文档中的组件迁移的[先决条件](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#prerequisites)。

* 使用基本报表包的项目。 无法迁移虚拟报表包。<!-- FLAG: Sourced from Coworker's response in the UI. The Adobe Analytics component migration docs don't mention virtual report suites. Confirm, and consider adding it to those docs. -->

## 在迁移之前查看报表包映射

<!-- FLAG: Confidence: Medium. The recommendation to review mappings before the first migration from a report suite is inferred from the Adobe Analytics guidance to decide mappings as an organization; Coworker also validates mappings during each migration. Confirm with Scott. -->

在首次从该报表包迁移之前，请考虑查看报表包的维度和量度是如何进行映射的。 映射将应用于您的组织迁移的每个项目，因此先处理它们有助于后续项目通过验证。 有关选择映射的指导，请参阅Adobe Analytics文档中的[决定作为组织如何映射组件](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#decide-as-an-organization-how-you-will-map-components)。

若要查看映射，请在&#x200B;[!UICONTROL **作用域**]&#x200B;选项卡上选择&#x200B;[!UICONTROL **仅查看映射**]，或直接询问同事：

**提示**

* “显示我的报表包中的维度和量度如何映射到我的数据视图”
* “我的报表包中的哪些维度和量度未映射到我的数据视图？”

您还可以要求同事更新映射。

如果跳过此审核，则同事仍会[为您迁移的每个项目检查映射](#review-the-validation-results-and-mappings)。

## 开始迁移

<!-- FLAG: Confidence: High that migration works at the project level and that components migrate with their project (component-migration.md in the Adobe Analytics docs), and that components that already exist in Customer Journey Analytics aren't re-created (prepare-component-migration.md). Medium-low for when to use each method and for combining them; this guidance is inferred and isn't in the Adobe Analytics docs. Confirm with Scott. Also confirm whether Coworker creates a project automatically when you ask it to migrate only components (for example, "Migrate my Spring sale segments to CJA"), or whether you must ask it to create the project. -->

同事始终迁移项目及其相关组件。 要迁移特定组件，请要求同事将这些组件添加到新项目中，然后迁移该项目。

不会重新创建Customer Journey Analytics中已存在的组件，因此您可以使用这两种方法。 例如，首先迁移最重要的项目，然后迁移任何剩余的组件。 根据您在Customer Journey Analytics中所需的内容选择开始位置：

* **如果要在Customer Journey Analytics中保留项目的面板和可视化图表，请迁移项目**。 请参阅[从项目开始](#start-from-a-project)。
* **迁移特定组件**。 例如，您可能计划在Customer Journey Analytics中构建包括这些项目的新项目。 请参阅[从特定组件启动](#start-from-specific-components)。

### 从项目开始

要迁移项目及其关联的组件，请执行以下操作：

1. 登录到同事。

1. 选择&#x200B;**[!UICONTROL 新聊天]**。

1. 在文本字段中，提示同事迁移项目。 例如：

   **提示**

   > 我希望将组件从Adobe Analytics迁移到Customer Journey Analytics。

   同事介绍可以迁移的内容，并启动调查问卷。

1. 在&#x200B;[!UICONTROL **作用域**]&#x200B;选项卡上，选择以下选项之一，然后选择&#x200B;[!UICONTROL **下一步**]：

   <!-- FLAG: Confidence: Medium for the "Plan a full upgrade" description. It likely hands off to the implementation guide skill and leaves the migration flow. Confirm with engineering. Also confirm what the Source & target tab asks; it was skipped in the screenshots. The Next and Submit buttons on the first questionnaire's Source & target and Review tabs are assumed to work like the second questionnaire. -->

   | 选项 | 说明 |
   | --- | --- |
   | [!UICONTROL **特定AA项目**] | 迁移您命名的项目。 执行本节中的其余步骤。 |
   | [!UICONTROL **仅查看映射**] | 检查报表包的量度和维度如何映射到数据视图，而不迁移任何内容。 在迁移[&#128279;](#review-report-suite-mappings-before-you-migrate)之前，请参阅查看报表包映射。 |
   | [!UICONTROL **计划完全升级**] | 获取从Adobe Analytics迁移到Customer Journey Analytics的端到端计划。 请参阅[与同事一起规划实施](/help/chat/use-cases/data-insights/implementation-guide.md)。 |

1. （可选）回答&#x200B;[!UICONTROL **Source &amp; target**]&#x200B;选项卡上的问题，然后选择&#x200B;[!UICONTROL **下一步**]。

1. 在&#x200B;[!UICONTROL **审核**]&#x200B;选项卡上，确认您的答案，然后选择&#x200B;[!UICONTROL **提交**]。

   同事会检查您有权访问哪些Adobe Analytics公司以及每个公司具有多少个基础报表包，然后启动第二个调查表。

1. 回答以下问题，并在每个问题之后选择&#x200B;[!UICONTROL **下一步**]：

   | 选项卡 | 问题 | 其他上下文 |
   | --- | --- | --- |
   | [!UICONTROL **项目**] | 要迁移的AA项目名称是什么？ | 部分名称没有问题。 |
   | [!UICONTROL **报告包**] | 项目使用哪个报表包？ | 从列表中选择一个报表包，或键入另一个报表包的名称。 |
   | [!UICONTROL **数据视图**] | 它应该迁移到哪个CJA数据视图？ | （可选）键入数据视图的名称，或将其留空，Co-worker将建议匹配的数据视图。 |

1. 在&#x200B;[!UICONTROL **审核**]&#x200B;选项卡上，确认您的答案，然后选择&#x200B;[!UICONTROL **提交**]。

   若要在任意步骤跳过调查问卷，请选择&#x200B;[!UICONTROL **跳过调查问卷**]，并描述您希望在聊天中看到的内容。

1. 继续[查看验证结果和映射](#review-the-validation-results-and-mappings)。

### 从特定组件开始

<!-- FLAG: Sourced from a prompt that SME Scott Tomko ran in Coworker (October 2026). The example is generalized; the original prompt named a customer. Coworker may ask a few questions along the way. Confirm what happens to the project that Coworker creates in Adobe Analytics, and to its migrated copy in Customer Journey Analytics, if you only wanted the components. -->

要迁移特定组件，请执行以下操作：

1. 要求同事使用这些组件创建项目，然后对其进行迁移。 例如：

   **提示**

   > 我想将名称中包含“春季促销”的所有Analytics区段迁移到CJA。 添加所有这些区段后，创建新的Workspace项目，然后将该项目迁移到CJA。

   同事在Adobe Analytics中创建项目。

1. 继续下面的部分，[查看验证结果和映射](#review-the-validation-results-and-mappings)。

## 查看验证结果和映射

<!-- FLAG: Confidence: Medium for the steps that fix a failed validation. They're based on the aa-mcp tool descriptions and on a test conversation where validation passed only after the project's panel was switched to a base report suite. Confirm how Coworker presents a failed validation, and whether it asks for confirmation before it updates a mapping. -->

同事将根据您选择的数据视图验证项目，然后报告是否可以迁移项目。 结果将列出项目中的每个维度和量度，以及它映射到的Customer Journey Analytics维度或量度。 例如：

* **量度：**&#x200B;发生次数成为事件
* **Dimension：**&#x200B;小时将保留

有关迁移的组件和项目元素，请参阅Adobe Analytics文档中的[了解迁移中包含的内容](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-what-is-included-in-a-migration)。

如果验证未通过：

* **无法自动映射的维度或量度：**&#x200B;同事在数据视图中建议将每个维度或量度映射到，更新映射，然后再次验证项目。 您还可以告诉同事要将它映射到哪个维度或量度，例如“将页面查看映射到web.webPageDetails.pageViews.value”。

* **不支持的元素：**&#x200B;从Adobe Analytics的项目中删除任何不支持的元素。 例如，确保每个面板都使用基本报表包，而不是虚拟报表包。 然后要求同事再次检查项目。 有关不支持的元素列表，请参阅Adobe Analytics文档中的[了解导致错误的不支持的元素](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration#understand-unsupported-elements-that-cause-errors)。

若要在迁移之前检查整个报表包的映射，请参阅[在迁移之前查看报表包映射](#review-report-suite-mappings-before-you-migrate)。

## 迁移项目

1. 验证通过后，Co-worker会询问是否在您选择的数据视图上创建项目的Customer Journey Analytics版本。 选择&#x200B;[!UICONTROL **是，迁移**]，然后选择&#x200B;[!UICONTROL **提交**]。

   要停止而不迁移，请选择&#x200B;[!UICONTROL **否，在此停止**]。

   同事在Customer Journey Analytics中重新创建项目，您作为项目所有者。 您原始的Adobe Analytics项目不会发生更改。

1. 继续下面的部分，[检查迁移状态](#check-the-migration-status)。

## 检查迁移状态

迁移在后台运行，因此新项目可能未立即准备就绪。

1. 提示同事检查迁移的状态：

   **提示**

   > 检查状态

   <!-- FLAG: The Failed row links to Retry a failed migration in the Adobe Analytics docs, but those steps use the Component migration page in the Adobe Analytics UI, which is admin-only. A non-admin with the Component Migration permission can't follow them. Confirm with Scott whether Coworker can retry a failed migration (for example, "Retry the migration"). If so, replace the link with a prompt. -->

   同事报告以下状态之一：

   | 状态 | 它的含义 |
   | --- | --- |
   | 已排队 | 迁移正在等待开始。 |
   | 已开始 | 迁移正在进行中。 |
   | 已完成 | 迁移已完成。 Co-worker提供了迁移内容的摘要，包括项目名称和数据视图。 |
   | 失败 | 迁移失败。 您可以重试迁移。 请参阅Adobe Analytics文档中的[重试失败的迁移](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration#retry-a-failed-migration)。 |

1. 迁移完成后，在Customer Journey Analytics Workspace中从项目列表中打开新项目。

1. （可选）将项目的所有权转移给Customer Journey Analytics中的任何用户。 有关详细信息，请参阅[转移资产](https://experienceleague.adobe.com/en/docs/analytics-platform/using/tools/asset-transfer/transfer-assets)。

迁移完成后，同事可以建议另一个项目以便下次迁移。

## 获得更好结果的提示

* 如果您不确定要使用哪个数据视图，请将调查问卷中的数据视图保留为空。 同事建议与报表包匹配的数据视图。
* 迁移后，比较Adobe Analytics和Customer Journey Analytics数据以确认报表匹配。 从Adobe Analytics升级到Customer Journey Analytics时，请参阅[与同事验证数据](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)。

## 后续步骤

* 要改为在Adobe Analytics用户界面中迁移项目，请参阅Adobe Analytics文档中的[将组件和项目从Adobe Analytics迁移到Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/component-migration)。
* 有关其他实施和管理用例，请参阅[智能实施和管理概述](/help/chat/use-cases/data-insights/data-governance-and-validation.md)。
