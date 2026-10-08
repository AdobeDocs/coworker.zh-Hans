---
title: CX Coworker Gateway中的Journey Optimizer Tools
description: 了解可通过CX Coworker Gateway使用的Adobe Journey Optimizer工具。
hide: true
source-git-commit: 6c126810936bea3e883d74e6ff685991cb40cd4a
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 2%
---
# CX Coworker Gateway中的Adobe Journey Optimizer工具 {#ajo-mcp}

使用Adobe Journey Optimizer产品工具从与MCP兼容的客户端检查营销活动、历程和渠道配置。 当您的组织已启用，并且您的用户帐户具有所需的Journey Optimizer权限时，可以通过[CX Coworker网关](overview.md)使用这些工具。

有关详细信息，请参阅Adobe Journey Optimizer文档中的[使用MCP客户端](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/combine/ajo-mcp){target="_blank"}。

如需创建、分析和模拟旅程的对话式代理体验，请改为查看[Journey Agent](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-ai/experience-cloud-ai/agents/ajo-agent)。

>[!AVAILABILITY]
>
>Journey Optimizer产品工具位于Beta中。 访问仅通过邀请进行，并且需要Adobe组织启用。 请参阅[访问CX Coworker网关工具](access.md)。

## 主要功能 {#mcp-capabilities}

Journey Optimizer工具为营销活动、历程和渠道配置审核提供了一个只读界面。 您可以：

- 列出Journey Optimizer营销活动并按状态筛选。
- 检索营销活动详细信息，包括定位、计划、渠道和内容配置元数据。
- 列出和检查沙盒中的历程，包括分支、条件和操作。
- 列出电子邮件、短信、推送和WhatsApp渠道的渠道配置。
- 列出可用于数据治理策略实施的营销操作。
- 无需导航产品屏幕，即可使用自然语言查看促销活动、历程和渠道设置。

>[!IMPORTANT]
>
>当前Beta中的所有Journey Optimizer工具均为只读。 不支持创建、更新、删除、启动、停止或发布营销活动或历程。

## 可用工具 {#mcp-tools}

| 工具 | 描述 |
| --- | --- |
| `ajo_campaign_list` | 浏览Journey Optimizer营销活动。 支持按状态筛选，如`DRAFT`、`LIVE`、`STOPPED`和`COMPLETED`。 |
| `ajo_campaign_get` | 按ID获取特定营销活动的详细信息和配置，包括受众定位、计划、渠道和内容设置元数据。 |
| `ajo_journey_list` | 浏览Journey Optimizer沙盒中的所有历程。 |
| `ajo_journey_get` | 按ID获取特定历程的完整详细信息，包括其分支、条件和操作。 |
| 历程可视化 | 渲染历程的结构和流程，以进行交互式可视化探索。 |
| `ajo_channel_configuration_list`, `ajo_channel_configuration_get` | 查看电子邮件、短信、推送或[!DNL WhatsApp]渠道的表面预设和品牌策略设置。 |
| `ajo_channel_configuration_resource_list`, `ajo_channel_configuration_resource_get` | 列出并检索由渠道配置引用的支持配置资源，如推送凭据、电子邮件子域、IP池、SMS凭据和[!DNL WhatsApp]凭据。 |
| `ajo_marketing_action_list` | 列出用于实施数据治理策略的可用营销操作。 |

## 示例提示 {#mcp-use-cases}

| 目标 | 示例提示 |
| --- | --- |
| Campaign 概述 | “向我显示我的所有Journey Optimizer营销活动。” |
| 状态审核 | “哪些营销活动当前处于实时状态？” |
| 营销活动详细信息 | “获取营销活动`[campaign ID]`的完整详细信息。” |
| 历程概述 | “给我看看我所有的Journey Optimizer旅程。” |
| 历程详细信息 | “获取历程`[journey ID]`的完整详细信息，包括分支和条件。” |
| 受众和定位 | “营销活动`[campaign ID]`的目标受众是哪些受众？” |
| 时间表和计时 | “计划何时运行营销活动`[campaign ID]`？” |
| 故障排除 | “查看营销活动`[campaign ID]`的设置并标记可能的问题。” |
| 渠道配置 | “提供了哪些电子邮件渠道配置？” |
| 渠道审核 | “哪些渠道配置缺失或不完整？” |
| 治理 | “我的沙盒中提供了哪些营销操作？” |

## 内容管理工具 {#mcp-content-management}

除了上述只读产品工具之外，Journey Optimizer用户还可以使用自然语言提示直接从CX Coworker发现和管理内容资源（内容模板、片段、登陆页面以及历程或营销活动内联消息内容）。 此功能由一组单独的读写功能MCP工具提供支持，适用于Journey Optimizer内容，并且可供有权访问CX Coworker的所有客户使用。

有关详细信息，请参阅Adobe Journey Optimizer文档中的[内容管理工具](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/essentials/ajo-coworker-skills#content-management){target="_blank"}。

内容管理工具允许您：

- 浏览内容模板、片段和登陆页，并检索其结构、元数据和状态。
- 检索在历程或营销活动操作节点上配置的内联消息内容。
- 为任何渠道创建和更新内容模板。
- 创建、更新、克隆和发布片段。
- 替换历程或营销活动操作节点的内联消息上的渠道变体。

>[!IMPORTANT]
>
>与上述只读产品工具不同，内容管理工具支持写入操作。 不支持跨模板或片段进行全文搜索、模板或片段验证、创建或发布登陆页面，以及删除内容模板、片段或登陆页面。

## 产品上下文和权限 {#mcp-context}

您的用户帐户必须有权查看您查询的Journey Optimizer促销活动、历程和渠道配置。 MCP不会绕过产品权限。

如果您的组织使用多个沙盒，请在需要来自特定沙盒的结果时，在提示中指定沙盒或环境上下文。

## 已知限制 {#mcp-limitations}

| 限制 | 描述 | 解决方法 |
| --- | --- | --- |
| 只读表面 | Journey Optimizer工具仅公开检索操作。 您无法创建、更新、删除、开始、停止或发布营销活动或历程。 | 使用Journey Optimizer UI或API进行写入操作。 |
| 无参与或绩效指标 | 工具不会返回展示次数、点进率、转化率或投放统计信息等报表数据。 | 使用Journey Optimizer报表、Customer Journey Analytics工具或Adobe Analytics工具来了解性能指标。 |
| 营销活动列表分页有限 | 营销活动列表返回结果的第一页，最多可返回50个营销活动按字母顺序排序。 不应用偏移和限制值。 | 如果已知促销活动ID，则直接使用`Get Campaign`。 使用Journey Optimizer UI进行完全浏览和过滤。 |
| 无按日期、渠道或计划进行服务器端筛选 | 营销活动列表支持状态筛选，但不支持发布日期、计划日期、渠道或营销活动类型筛选。 | 使用Journey Optimizer UI促销活动列表进行本机日期和渠道筛选。 |
| 无法通过产品工具检索消息内容 | 无法通过上述只读产品工具访问消息HTML、主题行、个性化令牌和选件内容。 | 使用[内容管理工具](#mcp-content-management)检索和更新内联消息内容，或直接在Journey Optimizer UI中查看内容。 |