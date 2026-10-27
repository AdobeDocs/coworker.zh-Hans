---
title: 通过同事聊天分析内容和Creative性能
description: 使用同事聊天功能查找入选内容的共同之处，将收入归因于客户看到的图像，并在各个渠道和受众之间比较创意内容。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 8e88ec793bd4ae6fe4692c1d5107fe01fe14bf7f
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%
---

# 内容性能概述

<!-- FLAG: Confidence: High for the first sentence and "Best for" (carried over from analytics-overview.md). Medium for the second sentence, which summarizes the row descriptions from the slides. -->

使用Adobe CX Enterprise Coworker Chat了解哪些内容入选以及入选原因（具体到每项资源的属性），以便您可以投资于有效的内容。 跳出单击哪些文件以查看哪些图像、消息传递和主题可促进跨渠道和受众的参与和收入。

内容性能是“同事聊天”中的几个分析域之一。 要查看所有域，请参阅使用同事聊天分析数据中的[开始同事聊天分析](/help/chat/use-cases/data-insights/analytics-overview.md#start-analyzing-in-coworker-chat)。

**最适合：**&#x200B;商业用户

## 先决条件

<!-- FLAG: Confidence: High for the first two bullets (sourced from analytics-chat.md and the Skills and limitations table). High for the third bullet: attribute-level and asset analysis needs Content Analytics components, which are available only in data views that are configured for Content Analytics (report/report.md in analytics-platform.en). This applies whichever skill runs the analysis. It's a shared bullet rather than a table row because it applies to every use case on this page. The SME confirmed (October 2026) that the skill doesn't support paid media yet, so the paid channel use case was rewritten for web and mobile. Support is planned, either in this skill or in a separate add-on skill (not decided). When it ships, consider restoring paid channels to that row with an "Additional prerequisite" note: paid media needs the Paid Media channel enabled in Content Analytics through an Experience Platform paid media source connector, such as Meta Ads or Google Ads, and comparing paid creative with on-site revenue needs custom tracking-key mapping (config/paid-media.md in analytics-platform.en). -->

要使用此页面上的用例，您需要：

* 同事聊天已连接到您的Customer Journey Analytics数据视图或Adobe Analytics报表包。 查看[开始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析数据。
* 查看对要分析的数据视图或报表包的访问权限。 同事聊天从Customer Journey Analytics或Adobe Analytics继承您的权限。
* 为Content Analytics配置的数据视图。 请参阅Customer Journey Analytics指南中的[配置Content Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/configuration/configuration)。

## 用例

| 用例 | 函数 |
| --- | --- |
| 查找入选内容的共同点<p>![查找获胜内容共有的内容](assets/content-performance.png)</p> | 显示哪些图像和消息在属性级别起作用，而不仅仅是哪些文件被点击。<p>**示例提示：**</p><ul><li>“我们表现最好的图像有哪些共同点？”</li><li>“哪些内容属性带来的参与度最高？”</li></ul> |
| 将收入归因于客户看到的内容 | 将图像曝光与收入、转化以及与算法归因的参与度联系起来。<p>**最适合：**&#x200B;分析师、商业用户</p><p>**示例提示：**</p><ul><li>“哪些图片带来的上季度收入最多？”</li><li>“https://www.example.com/images/spring-sale.jpg上的映像带来了多少收入？”</li></ul> |
| 跨Web和移动比较创意 | 在一个视图中显示在您的网站和移动应用程序中获胜的视觉效果和主题。<p>**示例提示：**</p><ul><li>“哪些创意主题在我们的移动应用程序和网站上获胜？”</li><li>“比较我们的移动应用程序与网站上的图像性能”</li></ul> |
| 了解哪些可视化图表会移动每个受众 | 显示哪些可视化图表适合每个受众以指导个性化和创意摘要。<p>**示例提示：**</p><ul><li>“哪些视觉效果最适合每个区段？”</li><li>“哪些图像适合首次来访的访客？”</li></ul> |

## 使用的技能

<!-- FLAG: Confidence: Medium. The `analyze-content` skill is a foundational skill for content questions, so it's listed for every use case on this page. Confirm with the PM that it covers all four. -->

对于本文中介绍的用例，Co-worker使用以下技能。 有关所有分析技能的列表，包括所需权限以及未涵盖的内容，请参阅使用同事聊天分析数据中的[技能和限制](/help/chat/use-cases/data-insights/analytics-overview.md#skills-and-limitations)。

| 技能 | 用于 |
| --- | --- |
| `cja`，`analyze-content` <br/> （有限可用性） | 查找获胜内容中哪些共同点<br>将收入归因于客户看到的内容<br>跨Web和移动比较创意<br>了解哪些视觉效果可移动每个受众<p>有关详细信息，请参阅[询问有关您内容的问题](/help/chat/use-cases/data-insights/ask-content-questions.md)。</p> |

## 获得更好结果的提示

<!-- FLAG: Confidence: High for the first bullet (SME feedback, October 2026). Medium for the rest: the second and third bullets are adapted from the best practices in analytics-overview.md, and the fourth bullet is inferred from the row descriptions. -->

* 当您询问特定图像时，请包括其URL或资产ID。 同事无法通过其在页面上的角色来识别图像，例如主页图像或横幅。
* 命名要分析的量度和日期范围，如上一季度收入。
* 指定要比较的区段、受众或渠道。
* 当您想知道内容表现如何时，请咨询内容属性，例如图像、主题或消息，而不是单个文件。

## 后续步骤

* 要了解同事如何回答内容问题，请参阅[询问有关您内容的问题](/help/chat/use-cases/data-insights/ask-content-questions.md)（限量发布）。
* 有关使用同事聊天进行数据分析的概述，包括其他分析域和最佳实践，请参阅[使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-overview.md)。
* 若要设置同事聊天并浏览工作示例，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。
