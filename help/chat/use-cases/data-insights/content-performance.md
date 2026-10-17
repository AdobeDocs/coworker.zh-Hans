---
title: 通过同事聊天分析内容和Creative性能
description: 使用同事聊天功能查找入选内容的共同之处，将收入归因于客户看到的图像，并在各个渠道和受众之间比较创意内容。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: e3d485f7cd1c45bf3fd1217ffcceeccfd4242c7b
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 1%
---

# 内容性能概述

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

使用Adobe CX Enterprise Coworker Chat了解哪些内容入选以及入选原因（具体到每项资源的属性），以便您可以投资于有效的内容。 跳出单击哪些文件以查看哪些图像、消息传递和主题可促进跨渠道和受众的参与和收入。

内容性能是“同事聊天”中的几个分析域之一。 要查看所有域，请参阅使用同事聊天分析数据中的[开始同事聊天分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最适合：**&#x200B;商业用户

## 先决条件

<!-- FLAG: Confidence: High for the first two bullets (sourced from analytics-chat.md and the Skills and limitations table). Low for the third bullet: the attribute-level and image exposure descriptions suggest that these use cases rely on Content Analytics data in Customer Journey Analytics, and implementation-guide.md lists Content Analytics as an implementation path, but no source confirms this. It's a shared bullet rather than a table row because it would apply to every use case on this page. The paid channel row ("Compare Meta ad creative to our web banners") may need an additional data source, which would become an "Additional prerequisite" note on that row in the Use cases table. Confirm with the PM. -->

要使用此页面上的用例，您需要：

* 同事聊天已连接到您的Customer Journey Analytics数据视图或Adobe Analytics报表包。 查看[开始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析数据。
* 查看对要分析的数据视图或报表包的访问权限。 同事聊天从Customer Journey Analytics或Adobe Analytics继承您的权限。
* 在Customer Journey Analytics中设置Content Analytics，以便同事聊天可以分析内容属性和图像曝光。 要计划Content Analytics实施，请参阅[与同事一起计划实施](/help/chat/use-cases/data-insights/implementation-guide.md)。

## 用例

| 用例 | 函数 |
| --- | --- |
| 查找入选内容的共同点<p>![查找获胜内容共有的内容](assets/content-performance.png)</p> | 显示哪些图像和消息在属性级别起作用，而不仅仅是哪些文件被点击。<p>**示例提示：**</p><ul><li>“我们表现最好的图像有哪些共同点？”</li><li>“哪些内容属性带来的参与度最高？”</li></ul> |
| 将收入归因于客户看到的内容 | 将图像曝光与收入、转化以及与算法归因的参与度联系起来。<p>**最适合：**&#x200B;分析师、商业用户</p><p>**示例提示：**</p><ul><li>“哪些英雄形象上季度带来的收入最多？”</li><li>“此横幅带来了多少收入？”</li></ul> |
| 跨付费和自有渠道比较创意内容 | 显示哪些可视化图表和主题在一个视图中跨Web、移动和付费渠道获胜。<p>**示例提示：**</p><ul><li>“在我们的网站上，哪些创意主题在付费广告中获胜？”</li><li>“比较Meta广告创意与我们的网络横幅”</li></ul> |
| 了解哪些可视化图表会移动每个受众 | 显示哪些可视化图表适合每个受众以指导个性化和创意摘要。<p>**示例提示：**</p><ul><li>“哪些视觉效果最适合每个区段？”</li><li>“哪些图像适合首次来访的访客？”</li></ul> |

<!--
HIDDEN until the skills are confirmed. To publish, remove this comment wrapper.

## Skills used

FLAG: Confidence: Low. No source in the repo (workflows.md, the Skills and limitations table, or any data insights article) names the skills behind these use cases. Get the skill IDs from the PM, replace the placeholder rows, and add the skills to the Skills and limitations table on analytics-overview.md so that the link above the table covers them. When you unhide this section, wrap this FLAG note in its own HTML comment.

Coworker uses the following skills for the use cases described in this article. For a list of all analytics skills, including the permissions they require and what they don't cover, see [Skills and limitations](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations) in Analyze data with Coworker Chat.

| Skill | Used for |
| --- | --- |
| *[Skill to be confirmed]* | Find what winning content has in common<br>Attribute revenue to the content customers see<br>Compare creative across paid and owned channels<br>Know which visuals move each audience |

-->

## 获得更好结果的提示

<!-- FLAG: Confidence: Medium. The first two bullets are adapted from the best practices in analytics-overview.md. The third bullet is inferred from the row descriptions. -->

* 命名要分析的量度和日期范围，如上一季度收入。
* 指定要比较的区段、受众或渠道。
* 当您想知道内容表现如何时，请咨询内容属性，例如图像、主题或消息，而不是单个文件。

## 后续步骤

* 有关使用同事聊天进行数据分析的概述，包括其他分析域和最佳实践，请参阅[使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要设置同事聊天并浏览工作示例，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。
