---
title: 通过同事聊天衡量营销影响和归因
description: 使用Co-worker Chat衡量每个渠道的增量影响，找出支出饱和的地方，构建假设预算方案，并检查营销模型的质量。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: f914f4a123216985ae9b562413f26e7b8c29eb0f
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 2%
---

# 营销衡量和归因概述

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

使用Adobe CX Enterprise Coworker Chat了解每个营销渠道和促销活动的增量影响，以便您可以分配支出以优化ROI。 了解渠道如何协同工作、额外支出在哪里停止了支付，以及提交之前不同的预算分配比较情况。

营销衡量和归因是同事聊天中的几个分析域之一。 要查看所有域，请参阅使用同事聊天分析数据中的[开始同事聊天分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最适合：**&#x200B;分析师、商业用户

## 先决条件

<!-- FLAG: Confidence: High for the shared bullets (sourced from analytics-chat.md and the Skills and limitations table). They're confirmed for Measure campaign performance only; whether the marketing mix modeling use cases also need a data view or report suite connection is unknown. Low for the "Additional prerequisite" notes on the four marketing mix modeling rows in the Use cases table: incremental impact, response curves, budget scenarios, and model retraining describe a marketing mix model, but no source names the product or data that these use cases need. It could be Adobe Mix Modeler or Marketing Campaign Analytics (listed as an implementation path in implementation-guide.md). Confirm with the PM before publishing. -->

要使用此页面上的用例，您需要：

* 同事聊天已连接到您的Customer Journey Analytics数据视图或Adobe Analytics报表包。 查看[开始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析数据。
* 查看对要分析的数据视图或报表包的访问权限。 同事聊天从Customer Journey Analytics或Adobe Analytics继承您的权限。

## 用例

| 用例 | 函数 |
| --- | --- |
| 了解每个渠道的增量影响 | 显示每个渠道的增量值、渠道如何相互放大以及外部因素的作用。<p>**示例提示：**</p><ul><li>“哪些渠道带来了最大的增量转化？”</li><li>“付费搜索和展示如何相互促进？”</li></ul><p>**其他先决条件：**&#x200B;除了[常规先决条件](#prerequisites)之外，此用例还需要经过训练的营销衡量模型。 *[有待确认的产品和设置要求。]*</p> |
| 找出支出开始饱和的地方<p>![查找支出开始饱和的位置](assets/marketing-measurement.png)</p> | 显示反映额外支出停止支付情况的响应曲线。<p>**示例提示：**</p><ul><li>“付费搜索支出从哪里开始饱和？”</li><li>&quot;显示每个渠道的响应曲线&quot;</li></ul><p>**其他先决条件：**&#x200B;除了[常规先决条件](#prerequisites)之外，此用例还需要经过训练的营销衡量模型。 *[有待确认的产品和设置要求。]*</p> |
| 构建假设预算方案 | 并排比较分配选项以支持计划决策。<p>**最适合：**&#x200B;商业用户</p><p>**示例提示：**</p><ul><li>“构建下一季度的预算方案”</li><li>“如果我将10%的支出从展示转移到搜索，该怎么办？”</li></ul><p>**其他先决条件：**&#x200B;除了[常规先决条件](#prerequisites)之外，此用例还需要经过训练的营销衡量模型。 *[有待确认的产品和设置要求。]*</p> |
| 检查模型质量以及何时重新训练 | 检查模型质量、培训详细信息和评分量度，以便您了解对答案的信任程度。<p>**最适合：**&#x200B;分析师</p><p>**示例提示：**</p><ul><li>“这种模式还需要其它因素吗？”</li><li>“这个模式需要再培训吗？”</li></ul><p>**其他先决条件：**&#x200B;除了[常规先决条件](#prerequisites)之外，此用例还需要经过训练的营销衡量模型。 *[有待确认的产品和设置要求。]*</p> |
| [衡量促销活动效果](/help/chat/use-cases/workflows.md#data-insights) | 了解在给定时间段内营销活动、渠道和Web属性的执行情况。<p>**示例提示：**“上个月我们的Acrobat Web营销活动表现如何？”</p><p>有关详细信息，请参阅同事聊天用例中的[数据分析](/help/chat/use-cases/workflows.md#data-insights)。</p> |

## 使用的技能

<!-- FLAG: Confidence: High for Measure campaign performance (workflows.md lists `cja`, `aa`, `dx-api`, and `knowledge-graph` for "Campaign performance"). `dx-api` and `knowledge-graph` aren't in the Skills and limitations table on analytics-overview.md. Low for the other four use cases: no source names their skills. Get the skill IDs from the PM, replace the placeholder row, and add the skills to the Skills and limitations table. -->

对于本文中介绍的用例，Co-worker使用以下技能。 有关所有分析技能的列表，包括所需权限以及未涵盖的内容，请参阅使用同事聊天分析数据中的[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用于 |
| --- | --- |
| `cja`, `aa`, `dx-api`, `knowledge-graph` | 衡量营销活动效果 |
| *[技能待确认]* | 了解每个渠道的增量影响<br>找出支出开始饱和的位置<br>构建假设预算方案<br>检查模型质量以及何时重新培训 |

## 获得更好结果的提示

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the sample prompts. -->

* 命名要分析的渠道、营销活动和日期范围。
* 提及您已有的任何假设，例如两个渠道协同工作，因此“同事聊天”可以验证或排除这些假设。
* 说明构建假设情景时要测试的特定预算转移，例如将10%的支出从一个渠道转移到另一个渠道。

## 后续步骤

* 有关使用同事聊天进行数据分析的概述，包括其他分析域和最佳实践，请参阅[使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要设置同事聊天并浏览工作示例，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。
