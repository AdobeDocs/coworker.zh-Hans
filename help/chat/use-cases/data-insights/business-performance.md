---
title: 通过同事聊天分析业务绩效和KPI
description: 使用同事聊天来解释量度移动的原因、预测量度的发展方向、准备绩效评估并将重复分析转化为可重复使用的技能。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 2%
---

# 业务绩效概述

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions. -->

使用Adobe CX Enterprise Coworker Chat了解业务开展情况、量度移动的原因、前往的位置，以及下一步要做什么。 调查关键量度的变化，将其向前投影，并将您的调查结果转化为适用于利益相关者的摘要和可重复使用的技能。

业务绩效是“同事聊天”中的几个分析域之一。 要查看所有域，请参阅使用同事聊天分析数据中的[开始同事聊天分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最适合：**&#x200B;分析师、商业用户

## 先决条件

要使用此页面上的用例，您需要：

* 同事聊天已连接到您的Customer Journey Analytics数据视图或Adobe Analytics报表包。 查看[开始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析数据。
* 查看对要分析的数据视图或报表包的访问权限。 同事聊天从Customer Journey Analytics或Adobe Analytics继承您的权限。

## 用例

| 用例 | 函数 |
| --- | --- |
| [探索趋势和根本原因](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![探索趋势和根本原因](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | 无需手动查询，即可识别Customer Journey Analytics和Adobe Analytics数据的趋势以及导致性能发生变化的因素。<p>**示例提示：**“上周为什么转化率下降？”</p><p>有关详细信息，请参阅[Customer Journey Analytics和同事](/help/chat/use-cases/data-insights/root-cause-analysis.md)。</p> |
| [解释量度移动的原因](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 运行根本原因分析，该分析显示变更后的尺寸和区段，并排除其余的尺寸和区段。<p>**示例提示：**</p><ul><li>“为什么周二收入会激增？”</li><li>“是什么促使本月会议发生了变化？”</li></ul><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [准备业务绩效审核](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 将受信任的量度转换为已说明的性能故事，其中包含调查结果以及建议的后续步骤。<p>**示例提示：**</p><ul><li>“给我一份上个月的摘要”</li><li>“总结领导团队的绩效”</li></ul><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [量度标题的预测](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 从历史数据中投影一个量度，以便您能够看到缺失即将出现。<p>**示例提示：**</p><ul><li>“未来30天的预测会话”</li><li>“我们的收入目标是否有望实现？”</li></ul><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [创建自定义Customer Journey Analytics技能](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 将您重复的分析转换为可重复使用的技能，该技能会在各个会话中持续存在。<p>**示例提示：**“将此每周收入分析转换为可重复使用的技能”</p><p>**其他必备项：**&#x200B;除了[常规必备项](#prerequisites)之外，此用例还需要“管理技能”权限。</p><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| [跨市场重复成功分析](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 跨品牌、地区或业务部门应用成熟的分析方法。<p>**最适合：**&#x200B;分析师</p><p>**示例提示：**“针对EMEA数据视图运行我的每周funnel技能”</p><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |

## 使用的技能

<!-- FLAG: Confidence: High for the root cause analysis skills, `cja-executive-summary`, forecasting with `cja` and `aa`, and `cja-skill-creator` for creating skills. All are listed in the Skills and limitations table and in workflows.md. Medium for mapping Repeat successful analysis across markets to `cja-skill-creator`: the row describes running a saved skill, which is inferred. workflows.md also lists `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, and `cja-reporting` for executive summaries. They're left out because they look org-specific. Confirm with the PM. -->

对于本文中介绍的用例，Co-worker使用以下技能。 有关所有分析技能的列表，包括所需权限以及未涵盖的内容，请参阅使用同事聊天分析数据中的[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用于 |
| --- | --- |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 探索趋势和根本原因<br>解释量度移动的原因 |
| `cja-executive-summary` | 准备业务绩效审查 |
| `cja`, `aa` | 量度标题的预测 |
| `cja-skill-creator` | 创建自定义Customer Journey Analytics技能<br>跨市场重复成功分析 |

## 获得更好结果的提示

* 命名要调查的更改的度量和时段。 根本原因分析可在已知时段内对已知量度起作用。
* 如果您希望划分量度更改，请询问参与维度。
* 在预测指标时要求提供预测时限，例如“未来30天”。
* 指定摘要的受众，如领导力或营销团队，如果您计划展示调查结果，请要求幻灯片组概述。
* 首先完成分析，然后请求Co-worker Chat将其另存为技能。 为该技能提供一个清楚的描述性名称，并记下您计划重复使用该技能的频率。

## 后续步骤

* 有关使用同事聊天进行数据分析的概述，包括其他分析域和最佳实践，请参阅[使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 要查看正在执行的根本原因分析，请参阅[Customer Journey Analytics和同事](/help/chat/use-cases/data-insights/root-cause-analysis.md)。
