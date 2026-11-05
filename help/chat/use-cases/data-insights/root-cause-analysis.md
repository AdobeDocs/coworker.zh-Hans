---
title: 使用Adobe Analytics和Customer Journey Analytics分析根本原因
description: 使用Adobe CX Enterprise Coworker调查量度变化，识别贡献的维度和区段，并测试Adobe Analytics和CJA中的假设。
feature: AI Tools
role: User
level: Beginner
doc-type: Feature Video
duration: 186
last-substantial-update: 2026-08-10T00:00:00.000Z
jira: KT-22082
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
source-git-commit: 7e096fc9cda2157c02501ee909a80bf4df9a2f32
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%
---

# 使用[!DNL Adobe Analytics]和[!DNL Customer Journey Analytics]分析根本原因

使用Adobe CX Enterprise Coworker Chat调查Adobe Analytics或Customer Journey Analytics (CJA)中量度发生更改的原因。 Co-worker会分析您指定的更改，显示构成维度和区段，并帮助您使用自然语言测试假设。

## 使用Customer Journey Analytics数据进行根本原因分析

以下视频演示了同事如何将对话式人工智能与Customer Journey Analytics相结合。 了解如何使用自然语言提出问题、可视化结果、识别有意义的趋势以及揭示无需构建手动查询即可提高性能的因素。

>[!VIDEO](https://video.tv.adobe.com/v/3496847/?learn=on&enablevpops)

### 先决条件

开始之前：

1. **有权访问同事聊天并连接Customer Journey Analytics。** 确认贵组织已配置所需的集成。
1. **具有您要分析的CJA数据视图的查看访问权限。** Co-worker只能使用您可用的数据视图和组件。
1. **选择包含相关量度和维度的数据视图。** 如果您可以访问多个数据视图，请命名您希望Co-worker使用的视图。
1. **确定您要调查的更改。** 指定指标、日期范围和比较时段。 您还可以提供维度、区段或假设验证，以集中进行分析。

### Customer Journey Analytics的示例提示

使用数据视图中的组件名称和时间段替换带括号的文本。

* 在&#x200B;**[数据视图名称]**&#x200B;数据视图中，为什么在&#x200B;**[日期范围]**&#x200B;内有&#x200B;**[指标]**&#x200B;与&#x200B;**[比较日期范围]**&#x200B;相比发生了变化？ 按&#x200B;**[维度]**&#x200B;划分更改并显示贡献最大的区段。
* 在&#x200B;**[数据视图名称]**&#x200B;数据视图中，**[维度或区段]**&#x200B;是否造成了&#x200B;**[量度]**&#x200B;从&#x200B;**[日期范围A]**&#x200B;到&#x200B;**[日期范围B]**&#x200B;的减少？ 比较两个时段的值并解释更改了哪些内容。
* 在&#x200B;**[数据视图名称]**&#x200B;数据视图中，比较&#x200B;**[日期范围]**&#x200B;内&#x200B;**[区段A]**&#x200B;和&#x200B;**[区段B]**&#x200B;的&#x200B;**[量度]**。 哪些维度对差异的贡献最大？
* 在&#x200B;**[数据视图名称]**&#x200B;数据视图中，测试此假设验证： **[说明您的假设验证]**。 分析&#x200B;**[日期范围]**&#x200B;的&#x200B;**[量度]**，并显示支持或不支持它的维度或区段。

## 使用Adobe Analytics数据进行根本原因分析

同事可以调查Adobe Analytics报表包中量度发生更改的原因。 它使用`aa-root-cause-analysis`技能来分析您指定的更改，并识别对更改有贡献的维度和区段。

### 先决条件

开始之前：

1. **有权访问同事聊天并连接Adobe Analytics。** 在协同工作中，转到&#x200B;**自定义项>集成**，并确认已列出并连接`aa-mcp`集成。 如果不可用，请要求管理员检查组织的设置。 有关设置指导，请参阅[开始使用同事聊天](https://experienceleague.adobe.com/zh-hans/docs/coworker/content/chat/use-cases/data-insights/analytics-chat)分析数据。
1. **具有您要分析的Adobe Analytics报表包的查看访问权限。** 同事继承您的Adobe Analytics权限，只能使用您在Analysis Workspace中可用的报表包和组件。
1. **选择包含相关数据的报表包。** 如果您可以访问多个报表包，请命名您希望同事使用的报表包。
1. **确定您要调查的更改。** 指定指标和时段。 要进行更集中的分析，请包括比较期、相关维度或区段，以及您希望Co-worker测试的任何假设。

### Adobe Analytics的示例提示

将带方括号的文本替换为报表包中的组件名称和时间段。

* 在&#x200B;**[报表包名称]**&#x200B;报表包中，为什么在&#x200B;**[日期范围]**&#x200B;期间有&#x200B;**[指标]**&#x200B;与&#x200B;**[比较日期范围]**&#x200B;发生更改？ 按&#x200B;**[维度]**&#x200B;划分更改并显示贡献最大的区段。
* 在&#x200B;**[报表包名称]**&#x200B;报表包中，**[维度或区段]**&#x200B;是否造成了&#x200B;**[量度]**&#x200B;从&#x200B;**[日期范围A]**&#x200B;到&#x200B;**[日期范围B]**&#x200B;的减少？ 比较两个时段的值并解释更改了哪些内容。
* 在&#x200B;**[报表包名称]**&#x200B;报表包中，比较&#x200B;**[日期范围]**&#x200B;内&#x200B;**[区段A]**&#x200B;和&#x200B;**[区段B]**&#x200B;的&#x200B;**[量度]**。 哪些维度对差异的贡献最大？

## 相关资源

* [使用Adobe CX Enterprise Coworker Chat分析数据](https://experienceleague.adobe.com/zh-hans/docs/coworker/content/chat/use-cases/data-insights/analytics-overview)
* [开始使用同事聊天分析数据](https://experienceleague.adobe.com/zh-hans/docs/coworker/content/chat/use-cases/data-insights/analytics-chat)
