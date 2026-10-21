---
title: 将受众和客户区段与同事聊天进行比较
description: 使用同事聊天功能比较客户群体、找到被忽视的增长机会、跟踪受众趋势，并将见解转化为您可以构建的受众。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 5973a87d21b23d7621366108716cbd476e6f66ae
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 2%
---

# 受众和区段分析概述

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

使用Adobe CX Enterprise Coworker Chat了解哪些客户组表现不同以及行为方式，以便您可以专注于最重要的客户组。 并排比较渠道、时间段和区段，跟踪受众随时间的变化，并将找到的内容转化为可以构建的受众。

受众和区段分析是同事聊天中的几个分析域之一。 要查看所有域，请参阅使用同事聊天分析数据中的[开始同事聊天分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最适合：**&#x200B;分析师、商业用户

## 先决条件

<!-- FLAG: Confidence: High for the shared bullets (sourced from the Skills and limitations table and analytics-chat.md). Medium for the "Additional prerequisite" notes on the operational trends rows in the Use cases table: workflows.md lists the operational time-series skill as available for "All Eligible Applications" but doesn't state required permissions. Mapping Track audience size trends to the same requirement is inferred. Low for the "Additional prerequisite" note on the Take an insight into an audience row: inferred from the Audiences section of workflows.md, which lists Real-Time CDP as the application for audience creation. Confirm with the PM. -->

要使用此页面上的用例，您需要：

* 同事聊天已连接到您的Customer Journey Analytics数据视图或Adobe Analytics报表包。 查看[开始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析数据。
* 查看对要分析的数据视图或报表包的访问权限。 同事聊天从Customer Journey Analytics或Adobe Analytics继承您的权限。

## 用例

| 用例 | 函数 |
| --- | --- |
| [比较性能](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 并排比较各个渠道、时间段或区段之间的量度。<p>**示例提示：**“按渠道比较每月的收入”</p><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [比较客户组](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 显示哪些组的行为不同，而不需要您编写区段逻辑。<p>**最适合：**&#x200B;商业用户</p><p>**示例提示：**</p><ul><li>“付费社交访客的转化情况是否与电子邮件不同？”</li><li>“比较新访客和旧访客的收入”</li></ul><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| 发现被忽视的增长机会 | 探索受众、历程和渠道，以识别整体性能数字可以掩盖的机会。<p>**示例提示：**</p><ul><li>“哪些受众的转化率高于平均水平，但获得的流量却很少？”</li><li>“哪些渠道的转化率利用不足？”</li></ul> |
| [分析运行趋势和原因](/help/chat/use-cases/workflows.md#data-insights) | 查询受众、数据集和历程的历史时间序列数据，并确定导致更改的原因。<p>**最适合于：**&#x200B;管理员、分析师</p><p>**示例提示：**“向我显示过去90天的受众规模趋势”</p><p>**其他必备项：**&#x200B;除了[常规必备项](#prerequisites)之外，此用例还需要访问要分析的受众、数据集或历程。</p><p>有关详细信息，请参阅同事聊天用例中的[数据分析](/help/chat/use-cases/workflows.md#data-insights)。</p> |
| 跟踪受众规模趋势 | 发现正在增长或萎缩的受众，并寻找原因。<p>**最适合于：**&#x200B;管理员、分析师</p><p>**示例提示：**“哪些受众本季度增长最快？”</p><p>**其他先决条件：**&#x200B;除了[常规先决条件](#prerequisites)之外，此用例还要求访问要跟踪的受众。</p> |
| 将insight引入受众 | 从insight转到您可以构建的受众，而无需重新开始。<p>**示例提示：**</p><ul><li>“在Analysis Workspace中打开此比较”</li><li>“帮助我构建该组的受众”</li></ul><p>**其他先决条件：**&#x200B;除了[常规先决条件](#prerequisites)之外，此用例还需要访问Real-Time Customer Data Platform以及创建受众的权限。</p> |

## 使用的技能

<!-- FLAG: Confidence: High for Compare performance and Analyze operational trends and causes (skills listed for "Comparative analysis" and "Operational time-series & causal analysis" in workflows.md). Medium for Compare customer groups and Track audience size trends, which are mapped to the same skills based on their descriptions. Low for `audience-creation-flow`: inferred from the Audiences section of workflows.md. No skill is listed for Find overlooked growth opportunities because no source names one. Only `cja`, `aa`, and the root cause analysis skills currently appear in the Skills and limitations table on analytics-overview.md. -->

对于本文中介绍的用例，Co-worker使用以下技能。 有关所有分析技能的列表，包括所需权限以及未涵盖的内容，请参阅使用同事聊天分析数据中的[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用于 |
| --- | --- |
| `cja`, `aa` | 比较绩效<br>比较客户组 |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 比较性能 |
| `operational-stats-causal-analysis` | 分析运营趋势和原因<br>跟踪受众规模趋势 |
| `audience-creation-flow` | 将insight引入受众 |

## 获得更好结果的提示

* 指定要包含、排除或比较的区段、受众、渠道或设备。
* 按区段和其他组件的确切名称引用它们。
* 命名要比较的量度和日期范围，例如收入月收入。
* 如果您想知道为什么一个组的行为与另一个组不同，请询问参与维度。

## 后续步骤

* 有关使用同事聊天进行数据分析的概述，包括其他分析域和最佳实践，请参阅[使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 要直接在同事聊天中构建受众，请参阅[评估Experience Platform运行状况并与同事一起使用自然语言构建受众](/help/chat/use-cases/audiences/create-audience-from-natural-language.md)。
