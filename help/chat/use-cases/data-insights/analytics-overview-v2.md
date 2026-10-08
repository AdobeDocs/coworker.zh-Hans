---
title: 通过同事聊天分析Customer Journey Analytics数据
description: 了解如何使用Adobe CX Enterprise Coworker Chat分析Customer Journey Analytics数据、构建漏斗并查找客户在旅程中的流失位置。
hold: true
product_v2:
  internal-label: CX Enterprise Coworker
feature_v2:
  internal-label: CX Enterprise Coworker
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 1%
---

# 通过同事聊天分析数据

本页上的信息概述了Adobe CX Enterprise Coworker Chat，以及它如何帮助您分析组织的数据。

Co-worker Chat使团队能够使用自然语言自动执行Adobe产品任务，通过灵活的规划、可自定义的技能和智能的执行快速将想法转化为行动。 有关同事的更多常规信息，请参阅[CX Enterprise Coworker概述](/help/home.md)。

>[!VIDEO](https://video.tv.adobe.com/v/3503519/?learn=on&enablevpops)

## 数据分析的工作方式

Co-worker Chat可以执行以前仅在Analysis Workspace中才有的高级数据分析。 Co-worker Chat可访问来自Customer Journey Analytics数据视图或Adobe Analytics报表包的数据，从而允许您浏览数据并通过自然语言提示获得答案。

同事聊天从Customer Journey Analytics或Adobe Analytics继承权限。 您只能访问Analysis Workspace中可供您访问的数据视图、报表包、维度、量度和区段。

在同事聊天中创建可视化图表时，您可以随时在Analysis Workspace中打开该可视化图表，以便进行更多手动控制。

## 快速解答和深思熟虑

您可以通过两种方式使用同事聊天，具体取决于您需要的分析量：

* **快速回答** — 直接问一个纯语言的问题，并立即获得答案。 商业用户通常以这种方式使用同事聊天，而分析师在需要为利益相关者提供快速答案时也会使用这种聊天。
* **深思熟虑的工作** — 与同事聊天进行多轮次的扩展对话，以调查业务问题、排除原因并得出建议。 分析人员通常使用此方法在提出推荐之前深入浏览数据。

## 在同事聊天中开始分析

首先以简单的语言描述您想要了解的信息。 Co-worker Chat规划分析，查询您的数据视图或报告包，并创建可视化和摘要。

以下用例按您要完成的任务分组。 每个组都列出了最适合的角色。

### 衡量绩效

**最适合：**&#x200B;分析师、商业用户

| 用例 | 函数 |
| --- | --- |
| [分析Customer Journey Analytics和Adobe Analytics数据](/help/chat/use-cases/data-insights/analytics-chat.md)<p>![分析Customer Journey Analytics和Adobe Analytics数据](../../assets/coworker-funnel-response-card.png)</p> | 回答有关数据视图或报表包的自然语言问题，构建漏斗和其他可视化图表，并找出客户流失的位置。 您可以在Analysis Workspace中打开任何可视化图表以供进一步分析。<p>**示例提示：**“显示过去30天的页面查看次数”</p><p>有关详细信息，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。</p> |
| [比较性能](#skills-and-limitations) | 并排比较各个渠道、时间段或区段之间的量度。<p>**示例提示：**“按渠道比较每月的收入”</p><p>有关详细信息，请参阅[技能和限制](#skills-and-limitations)。</p> |
| [衡量促销活动效果](/help/chat/use-cases/overview.md#data-insights) | 了解在给定时间段内营销活动、渠道和Web属性的执行情况。<p>**示例提示：**“上个月我们的Acrobat Web营销活动表现如何？”</p><p>有关详细信息，请参阅同事聊天用例中的[数据分析](/help/chat/use-cases/overview.md#data-insights)。</p> |
| [分析漏斗](#skills-and-limitations) | 浏览多步转化漏斗，并查看每个阶段的流失情况。<p>**最适合：**&#x200B;分析师</p><p>**示例提示符：** &quot;引导我完成结帐funnel&quot;</p><p>有关详细信息，请参阅[技能和限制](#skills-and-limitations)。</p> |

### 了解量度发生更改的原因

**最适合：**&#x200B;分析师

| 用例 | 函数 |
| --- | --- |
| [探索趋势和根本原因](/help/chat/use-cases/data-insights/root-cause-analysis.md)<p>![探索趋势和根本原因](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | 无需手动查询，即可识别Customer Journey Analytics和Adobe Analytics数据的趋势以及导致性能发生变化的因素。<p>**示例提示：**“上周为什么转化率下降？”</p><p>有关详细信息，请参阅[Customer Journey Analytics和同事](/help/chat/use-cases/data-insights/root-cause-analysis.md)。</p> |
| [分析运行趋势和原因](/help/chat/use-cases/overview.md#data-insights) | 查询受众、数据集和历程的历史时间序列数据，并确定导致更改的原因。<p>**最适合于：**&#x200B;管理员、分析师</p><p>**示例提示：**“向我显示过去90天的受众规模趋势”</p><p>有关详细信息，请参阅同事聊天用例中的[数据分析](/help/chat/use-cases/overview.md#data-insights)。</p> |

### 预测未来性能

**最适合：**&#x200B;分析师

| 用例 | 函数 |
| --- | --- |
| [预测指标](#skills-and-limitations) | 根据历史Customer Journey Analytics或Adobe Analytics数据预测未来的量度值，例如您是否有望实现收入目标。<p>**示例提示：**“预测未来30天的会话”</p><p>有关详细信息，请参阅[技能和限制](#skills-and-limitations)。</p> |

### 与利益相关者共享见解

**最适合：**&#x200B;分析师、商业用户

| 用例 | 函数 |
| --- | --- |
| [创建执行摘要和KPI摘要](#skills-and-limitations) | 制作适用于利益相关者的性能摘要、建议和幻灯片组概述。<p>**示例提示：**“给我上个月的执行摘要”</p><p>有关详细信息，请参阅[技能和限制](#skills-and-limitations)。</p> |

### 规划实施或升级

**最适合于：**&#x200B;管理员

| 用例 | 函数 |
| --- | --- |
| [计划您的实施](/help/chat/use-cases/data-insights/implementation-guide.md)<p>![计划您的实施](../../assets/ui-guide-6.png)</p> | 创建个性化的分步计划，以在Edge上实施Customer Journey Analytics、从Adobe Analytics升级或设置Content Analytics、Marketing Campaign Analytics或流媒体收集。 计划包括所有者、工作量估计、依赖项和验证步骤等详细信息。<p>**示例提示：** “帮助我规划Customer Journey Analytics的实施”</p><p>有关详细信息，请参阅[与同事一起规划实施](/help/chat/use-cases/data-insights/implementation-guide.md)。</p> |
| [生成实施核对清单](/help/chat/use-cases/data-insights/intelligent-checklist.md)<p>![生成实施核对清单](../../assets/data-validation-aa-cja/date-detail.png)</p> | 将您的Customer Journey Analytics实施计划转换为同事项目中的核对清单，团队可以在其中分配步骤、跟踪状态和添加批准审核。<p>有关详细信息，请参阅[生成同事项目的实施核对清单](/help/chat/use-cases/data-insights/intelligent-checklist.md)。</p> |

### 确认您的数据是准确的

**最适合于：**&#x200B;管理员

| 用例 | 函数 |
| --- | --- |
| [从Adobe Analytics升级到Customer Journey Analytics时验证数据](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)<p>![从Adobe Analytics升级到Customer Journey Analytics时验证数据](../../assets/data-validation-aa-cja/trend-bar-card.png)</p> | 比较Adobe Analytics报表包和Customer Journey Analytics数据视图之间的维度、量度和趋势，然后建议进行修复以支持您的升级。<p>**最适合于：**&#x200B;管理员、分析师</p><p>**示例提示：**“将我的AA报表包与我的CJA数据视图进行比较”</p><p>有关详细信息，请参阅[从Adobe Analytics升级到Customer Journey Analytics时，与同事验证数据](/help/chat/use-cases/data-insights/data-validation-aa-cja.md)。</p> |
| [验证您的流媒体实施](/help/chat/use-cases/data-insights/streaming-media-validation.md)<p>![验证您的流媒体实施](../../assets/ui-guide-8.png)</p> | 检查您的数据流、架构、数据集、数据视图和会话数据，以确认流媒体跟踪已配置并正确收集数据。<p>**示例提示：**“我的流媒体实施总体运行状况如何？”</p><p>有关详细信息，请参阅[与同事验证您的流媒体实施](/help/chat/use-cases/data-insights/streaming-media-validation.md)。</p> |
| [验证Customer Journey Analytics的数据集质量](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)<p>![验证Customer Journey Analytics的数据集质量](../../assets/data-validation-aep/dataset-validation.png)</p> | 识别用于提供Customer Journey Analytics报表的数据集，然后检查架构、身份质量和字段质量，以便在构建功能板之前解决问题。<p>有关详细信息，请参阅[使用协同工作进程中的数据验证技能验证Customer Journey Analytics数据](/help/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)。</p> |
| [将数据摄取到Experience Platform后验证数据](/help/chat/use-cases/data-insights/data-validation-aep.md)<p>![将数据摄取到Experience Platform后验证数据](../../assets/data-validation-aep/null-values.png)</p> | 对Experience Platform数据集和字段运行统计和语义检查以查找数据质量问题，例如无效值或映射问题。<p>**示例提示：**“验证数据集电子示例1000”</p><p>有关详细信息，请参阅[与同事验证Experience Platform数据](/help/chat/use-cases/data-insights/data-validation-aep.md)。</p> |

### 自动执行您重复的分析

**最适合：**&#x200B;分析师

| 用例 | 函数 |
| --- | --- |
| [创建自定义Customer Journey Analytics技能](#skills-and-limitations) | 将您重复的分析转换为可重复使用的技能，该技能会在各个会话中持续存在。<p>**示例提示：**“将此每周收入分析转换为可重复使用的技能”</p><p>有关详细信息，请参阅[技能和限制](#skills-and-limitations)。</p> |

有关这些用例的更多信息，包括它们使用的技能和更多示例提示，请参阅[数据分析用例](/help/chat/use-cases/overview.md#data-insights)。

## 技能和限制

具备以下技能以分析Customer Journey Analytics或Adobe Analytics数据。

| 技能 | 使用它可以 | 所需的权限 | 超出范围 |
| --- | --- | --- | --- |
| `cja`, `aa` | 实时查询Customer Journey Analytics数据视图(`cja`)或Adobe Analytics报表包(`aa`)：<ul><li>提取量度、维度、区段、数据视图和报表包</li><li>并排比较渠道、时间段或区段</li><li>运行多步骤funnel和流失分析</li><li>基于历史趋势的预测指标</li></ul> | 查看对要查询的数据视图或报表包的访问权限 | <ul><li>创建或编辑数据视图或报表包组件</li><li>您有权访问的数据视图或报表包以外的数据</li><li>超出量度预测的预测建模</li></ul> |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 调查量度发生更改而非仅报告其更改的原因：<ul><li>调查某个已知量度在已知时段内的变化</li><li>显示促成更改的维度和区段</li></ul> | 查看对正在分析的数据视图或报表包的访问权限 | <ul><li>检测您未询问的异常（无自动或实时警报）</li><li>针对您有权访问的数据视图或报表包外部的量度进行根本原因分析</li></ul> |
| `cja-executive-summary` | 生成适用于利益相关者的数据摘要：<ul><li>汇总指定期间的性能</li><li>根据数据生成规范性建议</li><li>幻灯片演示或利益相关者阅读的概要内容</li></ul> | 查看对摘要中涵盖的数据视图或报表包的访问权限 | <ul><li>构建最终幻灯片幻灯片或演示文件</li><li>跨您无权访问的数据视图或报表包的摘要</li></ul> |
| `aa-cja-validation` | 比较、审核和协调[!DNL Adobe Analytics]与Customer Journey Analytics之间的数据：<ul><li>比较报表包和数据视图之间的量度值</li><li>标记两个数据源之间的差异</li></ul> | 查看对正在比较的[!DNL Adobe Analytics]报表包和Customer Journey Analytics数据视图的访问权限 | <ul><li>解决数据差异的根本原因</li><li>验证[!DNL Adobe Analytics]和Customer Journey Analytics以外的数据源</li></ul> |
| `cja-skill-creator` | 将您已经掌握的分析变成一项可重复使用的技能：<ul><li>将完成的分析转换为已命名的、可重用的技能</li><li>使已保存的技能在未来的聊天会话中可用</li></ul> | 管理技能 | <ul><li>自动与其他用户共享保存的技能（组织级别的技能库需要管理员设置）</li><li>编辑技能引用的数据视图或报告包组件</li></ul> |

## 使用同事聊天分析数据时的最佳实践

### 组织级别的最佳实践

* 指定贵组织的分析师作为同事冠军。

* 创建一个经过审核的提示和技能库，这些提示和技能与用户可用的数据和组件相关联。

* 创建一个或多个技能，指导同事聊天仅使用您要在分析中使用的组件。 这有助于同事聊天为您的组织中的用户提供最相关的数据。

* 教育用户何时请求同事聊天以获得快速答案以及何时使用它进行深入思考工作。

### 用户级别的最佳实践

* 使用计划模式。

  此模式对于复杂任务特别有用，但也可以为简单任务产生更好的结果，因为它允许同事在采取行动之前提出后续问题。 有关详细信息，请参阅[计划模式](/help/chat/ui-guide.md#plan-mode)。

* 创建提示时，请尽可能具体一些：

  * 命名要分析的维度、量度和日期范围。
  * 按元件的确切名称引用元件。
  * 指定要包含、排除或比较的任何区段、受众、渠道或设备。
  * 指明您是要获取特定的可视化图表类型，如funnel、趋势表还是同类群组表。
  * 如果您希望同事聊天提供后续问题建议，请咨询建议的后续步骤。
  * 在预测指标时要求提供预测时限，例如“未来30天”。
  * 提及您已有的任何假设，这样同事聊天即可验证或排除该假设。
  * 如果您希望划分量度更改，请询问参与维度。
  * 指定摘要的受众，如领导力或营销团队，如果您计划展示调查结果，请要求幻灯片组概述。
  * 命名验证数据时要比较的特定报表包和数据视图。
  * 首先完成分析，然后让同事聊天将分析保存为技能，为分析提供一个清楚的描述性名称，并指出您计划重复使用分析的频率。

* 将标准方向添加到“同事聊天”内存。 例如，如果始终使用来自相同数据视图或报表包的数据，请将其添加到内存中。 有关详细信息，请参阅使用同事聊天开始分析数据中的[在内存中添加数据视图或报告包首选项](/help/chat/use-cases/data-insights/analytics-chat.md#add-a-data-view-or-report-suite-preference-in-memory)。

## 后续步骤

若要设置同事聊天并浏览工作示例，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。


