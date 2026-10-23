---
title: 通过同事聊天询问有关您内容的问题
description: 以简单的语言（从一般到具体）咨询同事讨论您的内容，并在没有分析师专业知识的情况下获得准确的Content Analytics答案。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: b54085a497ca4bbf0003d5837d816206a4d40396
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 2%
---

# 提出有关您内容的问题

<!-- FLAG: Confirm with the PM: (1) availability (GA, beta, or experimental) and whether this page needs an AVAILABILITY note or `hide: true` until launch, and (2) any required Coworker entitlement. Content Analytics itself has no separate permission: users get access through data views that are configured for Content Analytics (Access control section of analytics-platform.en/help/content-analytics/config/configuration.md). -->

使用Adobe CX Enterprise Coworker Chat从Adobe Content Analytics获取有关您内容的准确答案。 提出特定问题，例如“哪些主页图像带来的上一季度收入最多？”，或者提出一般问题，例如“我应该优先考虑哪种内容？” 同事将您的问题转化为合理的分析。

同事了解Content Analytics数据的结构并应用经验丰富的分析师所制定的报表规则，因此营销人员和其他业务用户无需深入了解Content Analytics专业知识即可获得可靠的结果。

有关其他内容性能用例，请参阅[内容性能概述](/help/chat/use-cases/data-insights/content-performance.md)。

**最适合：**&#x200B;商业用户、分析师

## 先决条件

<!-- FLAG: Confidence: High. The first two bullets match the other data insights pages. The third bullet follows the Content Analytics docs in analytics-platform.en: Content Analytics components are available only in data views that are configured for Content Analytics (report/report.md), and there's no separate Content Analytics permission (config/configuration.md). -->

要询问有关您内容的问题，您需要：

* 同事聊天已连接到您的Customer Journey Analytics数据视图。 查看[开始使用同事聊天](/help/chat/use-cases/data-insights/analytics-chat.md)分析数据。
* 查看对要分析的数据视图的访问权限。 同事聊天从Customer Journey Analytics继承您的权限。
* 为Content Analytics配置的数据视图。 请参阅Customer Journey Analytics指南中的[配置Content Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/configuration/configuration)。

## 提出内容问题

1. 登录到同事。

1. 选择&#x200B;**[!UICONTROL 新聊天]**。

1. 在文本字段中，询问有关内容的问题。 例如：

   **提示**

   > 我应该优先处理哪种内容？

   <!-- FLAG: The skill includes activation words and phrases, but they weren't provided. Confirm with the PM whether customers need to use specific words to trigger the skill, or whether any content question routes to it automatically. If specific words are needed, list them here. -->

   同事使用`analyze-content`技能回答内容问题。

1. （视情况而定）如果您的问题不限于一种解释，请回答同事提出的澄清问题，例如您指的是哪种内容类型、渠道或日期范围。

1. 查看结果。

1. （可选）在同一次对话中提出后续问题以更深入地探讨，或在Analysis Workspace中打开可视化图表以进行更多手动控制。 请参阅[在Customer Journey Analytics中分析](/help/chat/use-cases/data-insights/analytics-chat.md#analyze-in-customer-journey-analytics)。

## 示例提示

下表显示了不同类型内容问题的示例提示。 使用它们作为起点，并根据您自己的内容对其进行调整。

| 问题类型 | 示例提示 |
| --- | --- |
| 广泛或探索 | <ul><li>“我应该优先处理哪种内容？”</li><li>“我们的内容表现如何？”</li></ul> |
| 属性级别 | <ul><li>“我们表现最好的图像有哪些共同点？”</li><li>“哪些内容属性带来的参与度最高？”</li></ul> |
| 收入和转化率 | <ul><li>“哪些英雄形象上季度带来的收入最多？”</li><li>“此横幅带来了多少收入？”</li></ul> |
| 渠道和受众 | <ul><li>“在我们的网站上，哪些创意主题在付费广告中获胜？”</li><li>“哪些图像适合首次来访的访客？”</li></ul> |

## 同事如何回答内容问题

<!-- FLAG: Confidence: High for the list of what the skill includes, metric matching, filtering pages by Experience ID, and choosing an attribution model per question (sourced from the PM's skill description and feature summary). Medium for the remaining details, which combine the skill description with the Content Analytics component reference in the Customer Journey Analytics guide. The skill's specific query defaults, attribution models, and visualization rules weren't provided. Confirm with the PM before adding them. -->

同事使用`analyze-content`技能回答内容问题，其中包括以下上下文和护栏。 这些技能与`cja`技能配对，并通过相同的Customer Journey Analytics工具针对Customer Journey Analytics数据视图运行所有查询。

### 查询默认值和澄清问题

如果你的问题漏掉了一个细节，那么技能就适用一个合理的缺省值。 如果技能不能肯定你的意思，它会问一个澄清的问题，而不是猜测。

### 资产和体验的量度匹配

<!-- FLAG: The table covers web and mobile content. Paid media content uses separate summary metrics, such as Impressions, Clicks, and Spend with a reporting-level suffix (for example, Clicks | Asset Summary), that can't be combined with event metrics such as Asset Views (config/paid-media.md in analytics-platform.en). Confirm with the PM how the skill handles paid media, then add a row or note. -->

Content Analytics跟踪两种类型的内容：资源和体验。 每个报表都有自己的量度。 该技能始终将量度与您询问的内容类型配对。

| 内容类型 | 内容 | 技能使用的量度 |
| --- | --- | --- |
| 资产 | 单个内容，如图像 | 资产查看次数、资产点击次数、资产点进率(CTR) |
| 体验 | 网页上的所有文本，或移动应用程序中文本、资产和行动动员的组合 | 体验查看次数、体验点击次数、体验点进率(CTR) |

### Content Analytics数据架构

此技能可帮助您了解Content Analytics数据的结构方式。 例如：

* **体验ID：**&#x200B;当您询问有关特定页面的问题时，技能会按标识该页面的内容体验ID进行过滤。
* **AI生成的属性：**&#x200B;每个资源和体验都由诸如摄影样式、颜色、色调和说服策略等属性进行描述。 该技能使用这些属性来解释内容性能良好的原因，而不仅仅是哪些内容性能良好。

有关组件的完整列表，请参阅Customer Journey Analytics指南中的[Content Analytics组件](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/components)。

### 归因

技能会选择适合您问题的归因模型。 例如，有关图像点击量的问题与有关图像对收入贡献多少的问题答案不同。 有关详细信息，请参阅Customer Journey Analytics指南中的[归因模型](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/attribution/models#attribution-models)。

### 常见分析和工作流

该技能包括常用内容分析的说明，例如：

* 查找表现最好的资源或体验所共有的属性。
* 将内容风险与转化和收入挂钩。
* 比较Web、移动和付费媒体渠道中的内容。
* 比较哪些内容适用于不同的受众和区段。
* 标识过度使用或未充分使用的内容。

### 可视化

该技能会选择符合您的问题和数据的可视化图表，以便轻松地阅读和共享结果。

## 获得更好结果的提示

* 如果你不确定要问什么，就从宽开始。 同事可以将一般问题转换为重点分析，您可以从中进行改进。
* 讲一下是意味着单个资产（如图像），还是整个体验（如页面），只要您知道自己想要的是哪种体验。
* 命名要分析的量度和日期范围，如上一季度收入。
* 指定要比较的区段、受众或渠道。
* 当您想知道内容表现如何时，请咨询内容属性，例如图像、主题或消息，而不是单个文件。
* 如果您始终分析同一数据视图，请将您的首选数据视图添加到同事聊天内存中。 请参阅[在内存中添加数据视图或报表包首选项](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory)。

## 后续步骤

* 有关更多内容性能用例，请参阅[内容性能概述](/help/chat/use-cases/data-insights/content-performance.md)。
* 要了解有关Content Analytics的更多信息，请参阅Customer Journey Analytics指南中的[Content Analytics概述](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/content-analytics/content-analytics)。
* 有关使用同事聊天进行数据分析的概述，包括最佳实践，请参阅[使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-overview.md)。
