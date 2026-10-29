---
title: 通过同事聊天分析客户历程和流失
description: 使用同事聊天构建漏斗，查找客户流失的位置，诊断转化下降情况，并比较分析数据中不同时段的历程。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 1ec3a8bf6dff44df068529cf1f7ceb699a027d65
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 2%
---

# 历程分析概述

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

使用Adobe CX Enterprise Coworker Chat可跨渠道、设备和区段查找客户从历程中退出的位置以及原因。 使用简单的语言描述历程，Co-worker Chat构建funnel，显示每一步的流失情况，并帮助您调查原因。

历程分析是同事聊天中的几个分析域之一。 要查看所有域，请参阅使用同事聊天分析数据中的[开始同事聊天分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最适合：**&#x200B;分析师、商业用户

## 先决条件

要使用此页面上的用例，您需要：

* 同事聊天已连接到您的Customer Journey Analytics数据视图或Adobe Analytics报表包。 查看[开始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析数据。
* 查看对要分析的数据视图或报表包的访问权限。 同事聊天从Customer Journey Analytics或Adobe Analytics继承您的权限。

## 用例

| 用例 | 函数 |
| --- | --- |
| [分析Customer Journey Analytics和Adobe Analytics数据](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![分析Customer Journey Analytics和Adobe Analytics数据](../../assets/coworker-funnel-response-card.png)</p> | 回答有关数据视图或报表包的自然语言问题，构建漏斗和其他可视化图表，并找出客户流失的位置。 您可以在Analysis Workspace中打开任何可视化图表以供进一步分析。<p>**示例提示：**“显示过去30天的页面查看次数”</p><p>有关详细信息，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。</p> |
| [查找客户流失的位置](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) | 用一句直白的问题构建一个funnel，对最大的漏洞进行排名，并建议下一步行动。<p>**最适合：**&#x200B;商业用户</p><p>**示例提示：**</p><ul><li>“在采购途中，我们在哪里失去了一些人？”</li><li>“带我逛逛结帐funnel”</li></ul><p>有关详细信息，请参阅[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。</p> |
| 诊断转化下降 | 调查客户退出的位置，并评估促成更改的原因。<p>**示例提示：**</p><ul><li>“为什么上周的转化率下降了？”</li><li>“网站更改后，客户从哪里退出？”</li></ul> |
| 找出流失的原因 | “Rule Out（排除）”导致一次一个隔离问题背后的通道、设备或区段。<p>**示例提示：**</p><ul><li>“在移动设备或台式机上放弃购物车的情况更糟糕吗？”</li><li>“哪些渠道在购物车和购买之间泄露的最多？”</li></ul> |
| 跨期间比较历程 | 逐步显示您发送的更改是否移动了funnel。<p>**最适合：**&#x200B;商业用户</p><p>**示例提示：**</p><ul><li>“比较本季度的结账转化率与上一季度的结账转化率”</li><li>“重新设计后，我的funnel发生了什么变化？”</li></ul> |

## 示例：查找客户流失的位置

有关从第一个问题到建议的完整示例对话，请参阅“开始使用同事聊天分析数据”中的[示例：查找客户流失的位置](/help/chat/use-cases/data-insights/analytics-chat.md#example-find-where-customers-drop-off)。

## 使用的技能

<!-- FLAG: Confidence: High for `cja` and `aa` (the Skills and limitations table lists funnel and fallout analysis and side-by-side comparison of time periods). Medium for the root cause analysis skills: workflows.md maps the prompt "Why did conversions drop last week?" to them, but the mapping to the slide rows "Diagnose conversion declines" and "Isolate the cause of a drop-off" is inferred. Confirm with the PM. -->

对于本文中介绍的用例，Co-worker使用以下技能。 有关所有分析技能的列表，包括所需权限以及未涵盖的内容，请参阅使用同事聊天分析数据中的[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用于 |
| --- | --- |
| `cja`, `aa` | 分析Customer Journey Analytics和Adobe Analytics数据<br>找出客户流失的位置<br>比较不同期间的历程 |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 诊断转化下降<br>确定下降的原因 |

## 获得更好结果的提示

<!-- FLAG: Confidence: High, except the first bullet (Medium), which moved here from Prerequisites and is inferred from how funnel prompts work. The rest are adapted from the best practices in analytics-overview.md. -->

* 命名要分析的历程步骤，如产品页面、购物车、结账和购买。
* 命名要分析的维度、量度和日期范围，并按其确切名称引用组件。
* 需要设置funnel或流失可视化图表（如果这是您希望查看的内容）。
* 指定要包含、排除或比较的区段、渠道或设备。
* 提及您已有的任何假设，例如最近的网站更改，因此“同事聊天”可以验证或排除此假设。
* 如果您希望同事聊天提供后续问题建议，请咨询建议的后续步骤。
* 需要更多手动控制时，可在Analysis Workspace中打开任意可视化图表。 请参阅[在Analysis Workspace中打开可视化图表](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace)。

## 后续步骤

* 有关使用同事聊天进行数据分析的概述，包括其他分析域和最佳实践，请参阅[使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要设置同事聊天并浏览工作示例，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。
