---
title: 使用Adobe CX Enterprise Coworker Chat分析Analytics数据
description: 使用Adobe CX Enterprise Coworker Chat分析Customer Journey Analytics和Adobe Analytics数据，找到根本原因，并在Analysis Workspace中打开结果。
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: f1ffc050071fc0ca48ae36c7aea8bc66eff2a147
workflow-type: tm+mt
source-wordcount: '1358'
ht-degree: 1%
---

# 通过同事聊天分析数据

本页上的信息概述了Adobe CX Enterprise Coworker Chat，以及它如何帮助您分析组织的数据。

Co-worker Chat使团队能够使用自然语言自动执行Adobe产品任务，通过灵活的规划、可自定义的技能和智能的执行快速将想法转化为行动。 有关同事的更多常规信息，请参阅[CX Enterprise Coworker概述](/help/home.md)。

## 数据分析的工作方式

Co-worker Chat可以执行以前仅在Analysis Workspace中才有的高级数据分析。 Co-worker Chat可访问来自Customer Journey Analytics数据视图或Adobe Analytics报表包的数据，从而允许您浏览数据并通过自然语言提示获得答案。

同事聊天从Customer Journey Analytics或Adobe Analytics继承权限。 您只能访问Analysis Workspace中可供您访问的数据视图、报表包、维度、量度和区段。

在同事聊天中创建可视化图表时，您可以随时在Analysis Workspace中打开该可视化图表，以便进行更多手动控制。 请参阅[在Analysis Workspace中打开可视化图表](/help/chat/use-cases/data-insights/analytics-chat.md#open-a-visualization-in-analysis-workspace)。

## 快速解答和深思熟虑

您可以通过两种方式使用同事聊天，具体取决于您需要的分析量：

* **快速回答** — 直接问一个纯语言的问题，并立即获得答案。 商业用户通常以这种方式使用同事聊天，而分析师在需要为利益相关者提供快速答案时也会使用这种聊天。
* **深思熟虑的工作** — 与同事聊天进行多轮次的扩展对话，以调查业务问题、排除原因并得出建议。 分析人员通常使用此方法在提出推荐之前深入浏览数据。

## 在同事聊天中开始分析

首先以简单的语言描述您想要了解的信息。 Co-worker Chat规划分析，查询您的数据视图或报告包，并创建可视化和摘要。

以下用例按分析域分组。 每个域都有其自己的页面，其中包含用例、示例提示、先决条件及其使用的技能。

| 域 | 您可以做什么 | 最适合 |
| --- | --- | --- |
| [智能实施和管理](/help/chat/use-cases/data-insights/data-governance-and-validation.md) | 设置、迁移和管理您的实施，并确保您可以信任每个答案背后的数据。 | 管理员 |
| [历程分析](/help/chat/use-cases/data-insights/journey-analysis.md) | 跨渠道、设备和区段了解客户从历程中退出的位置以及原因。 | 分析师、商业用户 |
| [受众和区段分析](/help/chat/use-cases/data-insights/audience-and-segment-analysis.md) | 了解哪些客户组表现不同以及具体方式，以便您能够专注于最重要的客户组。 | 分析师、商业用户 |
| [业务绩效](/help/chat/use-cases/data-insights/business-performance.md) | 了解业务开展情况、量度移动的原因、移动方向，以及下一步要做什么。 | 分析师、商业用户 |
| [内容性能](/help/chat/use-cases/data-insights/content-performance.md) | 了解哪些内容获胜以及获胜原因（具体到每个资产的属性），以便您能够对有效内容进行投资。 | 商业用户 |
| [营销度量和归因](/help/chat/use-cases/data-insights/marketing-measurement-and-attribution.md) | 了解每个营销渠道和促销活动的增量影响，以便您可以分配支出以优化ROI。 | 分析师、商业用户 |

## 技能和限制

具备以下技能以分析Customer Journey Analytics或Adobe Analytics数据。

| 技能 | 使用它可以 | 所需的权限 | 超出范围 |
| --- | --- | --- | --- |
| `cja`, `aa` | 实时查询Customer Journey Analytics数据视图(`cja`)或Adobe Analytics报表包(`aa`)：<ul><li>提取量度、维度、区段、数据视图和报表包</li><li>并排比较渠道、时间段或区段</li><li>运行多步骤funnel和流失分析</li><li>基于历史趋势的预测指标</li></ul> | 查看对要查询的数据视图或报表包的访问权限 | <ul><li>创建或编辑数据视图或报表包组件</li><li>您有权访问的数据视图或报表包以外的数据</li><li>超出量度预测的预测建模</li></ul> |
| `cja-root-cause-analysis`, `aa-root-cause-analysis` | 调查量度发生更改而非仅报告其更改的原因：<ul><li>调查某个已知量度在已知时段内的变化</li><li>显示促成更改的维度和区段</li></ul> | 查看对正在分析的数据视图或报表包的访问权限 | <ul><li>检测您未询问的异常（无自动或实时警报）</li><li>针对您有权访问的数据视图或报表包外部的量度进行根本原因分析</li></ul> |
| `cja-executive-summary` | 生成适用于利益相关者的数据摘要：<ul><li>汇总指定期间的性能</li><li>根据数据生成规范性建议</li><li>幻灯片演示或利益相关者阅读的概要内容</li></ul> | 查看对摘要中涵盖的数据视图或报表包的访问权限 | <ul><li>构建最终幻灯片幻灯片或演示文件</li><li>跨您无权访问的数据视图或报表包的摘要</li></ul> |
| `analyze-content`<!-- FLAG: Confirm the Out of scope items with the PM. --> | 在Customer Journey Analytics中使用Content Analytics数据回答有关您内容的一般或特定问题：<ul><li>找出性能最佳的资源和体验的共同点</li><li>将内容风险与转化和收入联系起来</li><li>跨渠道和受众比较内容</li></ul>有关详细信息，请参阅[询问有关您内容的问题](/help/chat/use-cases/data-insights/ask-content-questions.md)。 | 查看对为Content Analytics配置的数据视图的访问权限 | <ul><li>设置或配置Content Analytics</li><li>Content Analytics未收集的内容</li></ul> |
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

* 若要设置同事聊天并浏览工作示例，请参阅[开始使用同事聊天分析数据](/help/chat/use-cases/data-insights/analytics-chat.md)。
* 要查看每个同事聊天工作流及其背后的技能，请参阅[同事聊天工作流](/help/chat/use-cases/workflows.md)。


