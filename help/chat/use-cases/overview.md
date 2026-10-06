---
description: 浏览同事聊天用例和示例提示，按区域在数据见解、受众、历程和平台操作之间组织。
title: 同事聊天用例
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 2d4922c334bcc2ec93dec46098a9c021623034ad
workflow-type: tm+mt
source-wordcount: '7086'
ht-degree: 6%
---
# 同事聊天用例 {#use-cases}

Co-worker Chat允许您使用自然语言查询、分析和处理[!DNL Experience Platform]数据，而不是手动导航多个UI或编写查询。 此页面按工作区域整理了从业人员最依赖的用例目录：数据分析、受众、历程、忠诚度、基本元素和沙盒工具。 每个条目都包括它调用的技能、与它一起使用的应用程序以及示例提示，您可以复制、适应自己的数据，并通过对话进行细化。

>[!NOTE]
>
>即将推出：
>
>通过CX Enterprise Coworker推出的新AEM代理功能，旨在帮助您更快完成更多工作。
>
>所有符合条件的客户都可以在Co-worker中以滚动方式访问Adobe Experience Manager代理功能。
>
>另请参阅AEM中的[AI - AEM中的代理功能概述](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/overview)。

## 品牌体验

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [更新AEM页面](brand-visibility/author-web-pages.md) | 执行更新、删除、替换或添加内容元素等操作，以保持体验准确且最新。 输入内容可以是自然语言或可视批注，如PDF或屏幕截图。 | `aem-sites-pages-update` | Adobe Experience Manager (AEM) - AEM Sites | 在&lt;URL>上将标题更新为Hello World<br><br>在&lt;URL>上将“参加我们的咖啡测验”按钮更改为更吸引人的版本<br><br>根据附加的<br><br>在&lt;URL>上更新&lt;URL>我想在页面底部添加一个新的Teaser部分，介绍我们在8月份举行的促销活动，购买咖啡机并免费获得2袋咖啡。 还可以找到朋友喝咖啡的图像，并在Teaser中使用 |
| 批量更新AEM | 同时跨多个页面执行批量操作，例如删除、替换或添加内容元素，以保持体验准确且最新。 | `aem-sites-pages-bulkreplace` | Adobe Experience Manager (AEM) - AEM Sites | 在&lt;aem path>上，将包含副本“MyBarista\”的所有页面更新为“BrewPass” |
| 从图转到可视内容片段 | 使用自然语言将设计直接从Figma导入Adobe Experience Manager。 该技能会自动创建所需的内容模型、内容片段、资源和可视化模板，使业务用户能够在几分钟内从设计转移到支持Web的内容，而无需手动设置。 | `aem-sites-visualcontentfragments-create` | Adobe Experience Manager (AEM) - AEM Sites | 从&lt;Figma_URL>导入 |

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 创建表单 | 从纯语言描述、附加的摘要、图像或PDF生成新的自适应表单 | `aem-forms-adaptiveform-create` | Adobe Experience Manager (AEM) - AEM Forms | “创建员工入门培训表单”<br><br>“使用附加的摘要（图像或PDF）创建表单”<br><br>“创建&lt;form type>自适应表单” |
| 编辑/更新表单 | 修改现有表单 — 添加/编辑字段、调整简单布局、配置提交操作或应用附加准则文档的更改 | `aem-forms-adaptiveform-edit` | Adobe Experience Manager (AEM) - AEM Forms | “在名字字段下添加中间名字段”<br><br>“将名字和姓氏字段置于2列布局中，50/50”<br><br>“配置表单以将数据发送到REST端点”<br><br>“更新此表单以匹配附加的准则文档”<br><br>“在&lt;现有字段>字段下添加&lt;字段名称>字段” |
| 添加业务逻辑 | 创建简单规则，例如根据其他字段的值显示或隐藏字段 | `aem-forms-adaptiveform-edit` | Adobe Experience Manager (AEM) - AEM Forms | “仅在员工类型为承包商时显示‘公司’字段”<br><br>“仅在&lt;其他字段>为&lt;值>时显示&lt;字段>字段” |
| 嵌入表单 | 将现有表单或新创建的表单放置到指定的AEM Sites页面上（仅在Edge Delivery Services页面上受支持） | `aem-forms-adaptiveform-embed` | Adobe Experience Manager (AEM) - AEM Forms | “将此表单嵌入到我们网站的主页上”<br><br>“将此表单嵌入到&lt;页面路径>” |

**相关信息**

* [AEM中的代理功能：Brand Experience - Experience Production - Sites](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-sites)

* [AEM中的代理功能：Brand Experience - Experience Production - Forms](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-forms)

### 开发

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 管理Cloud Manager管道 | 创建、运行和监控AEM Cloud Manager管道，包括日志、工件、变量和设置 | `cloud-manager-pipeline-management` | Adobe Experience Manager (AEM) | “列出项目12345的管道”<br><br>“我最近管道的状态是什么？” |
| 管理Cloud Manager环境 | 创建、配置和维护AEM Cloud Manager环境，包括RDE、环境变量、日志和备份 | `cloud-manager-environment-management` | Adobe Experience Manager (AEM) | 为程序12345列出我的环境&quot;<br><br>&quot;重置我的RDE&quot; |
| 管理Cloud Manager程序 | 列出、检查和删除AEM Cloud Manager程序，包括其管道和环境 | `cloud-manager-program-management` | Adobe Experience Manager (AEM) | “列出我的Cloud Manager程序”<br><br>“获取程序12345的详细信息” |
| 管理AEM版本更新计划 | 为自动维护配置每日免打扰时间和免更新时段，并查看Adobe的全局代码冻结窗口 | `cloud-manager-release-management` | Adobe Experience Manager (AEM) | “我当前的安静时间窗口是什么？”<br><br>“安排12月20日至1月2日的无更新时段” |

**相关信息**

* [AEM中的代理功能：Brand Experience — 开发](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/development/use-cases)

### 入门

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 引导式端到端载入 | 协调完整的入门培训生命周期、存储库选择、文件夹委派、标记、元数据、导入和搜索子技能（如果您不知道需要的特定入门培训任务）。 | `aem-onboarding-workflow` | Adobe Experience Manager (AEM) - AEM Assets | “将我们的团队载入AEM Assets”<br><br>“带我了解AEM DAM载入” |
| 设计和创建文件夹层次结构 | 根据业务需求或CSV输入，在AEM Assets中（在`/content/dam`下）建议和创建可伸缩的文件夹结构。 | `aem-folder-management` | Adobe Experience Manager (AEM) - AEM Assets | “推荐生活方式营销资产的文件夹结构”<br><br>“根据此CSV文件创建文件夹” |
| 设计和创建标记 | 在`/content/cq:tags`下设计和创建受控标记词汇 — 命名空间、分层标记和批量标记操作。 | `aem-tag-taxonomy` | Adobe Experience Manager (AEM) - AEM Assets | “使用产品类别的命名空间设计标记分类”<br><br>“从此CSV导入标记”<br><br>“在AEM中创建这些层次结构标记” |
| 创建和分配元数据表单 | 设计和创建创作UI内容作者使用的自定义元数据表单（从CSV、表、要求文档或描述），然后可以选择将它们分配给文件夹。 | `aem-metadata-form` | Adobe Experience Manager (AEM) - AEM Assets | 从此字段列表创建元数据表单&quot;<br><br>&quot;将此表单分配给`campaigns`文件夹&quot; |

**相关信息**

* [AEM中的代理功能：品牌体验 — 入门](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/onboarding/use-cases)

## 内容审查程序

### 内容发现

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 按语义主题搜索 | 使用AI支持的语义匹配功能，按概念、情绪或视觉主题查找资产。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | “给我找一副晨间咖啡生活方式图片” |
| 按自定义元数据搜索 | 按自定义元数据字段筛选资源（例如，Coffee Blend、品牌、Roast级别）。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | “查找`Coffee Blend`为`Morning Muse`的资源”<br><br>“获取许可证未过期的资源”<br><br>“查找营销活动名称未设置的资源（必须为属性编制索引以获取相应的结果）。” |
| 按审批状态搜索 | 根据审批状态筛选资源。 例如，已批准、正在审查、已拒绝或缺少状态。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | “显示`Campaign`文件夹中所有已批准的资产” |
| 按文件夹/路径搜索 | 通过解释引用AEM中文件夹名称的自然语言提示来识别资源。 您只需在其提示中提及文件夹，而无需手动浏览存储库，即可显着减少找到正确内容所需的点击次数。 | `aem-assets-discovery` | Adobe Experience Manager (AEM) - AEM Assets | “文件夹`WKND`中是否有任何svg”？<br><br>“在文件夹`WKND`中显示在2025年11月1日之后修改的资源” |

**相关信息**

* [AEM中的代理功能：内容顾问 — 内容发现](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/discovery/use-cases)

### 内容优化

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 高分辨率演绎版创建和通道优化的演绎版 | 以指定的分辨率和质量级别生成资产的新演绎版，从而无需手动编辑即可轻松准备渠道就绪的变体。 您还可以根据平台特定要求制作演绎版，如Instagram故事，确保资产自动满足格式、比例和质量准则。 | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | 使用`80% quality`创建`2000px`演绎版作为`JPEG`&quot;<br><br>&quot;为Instagram故事创建演绎版&quot; |
| 标记叠加和复合生成 | 通过精确放置将促销图形、叠加或徽章应用于现有资源，支持快速创建营销活动就绪的合成内容。 | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | “在促销横幅上叠加带有`30%`折扣图表的图像，从中心放置`100px`” |
| 图像增强、背景颜色调整、方向转换 | 应用视觉改进（锐化图像）、替换背景颜色和执行方向转换。 | `aem-assets-content-optimisation` | Adobe Experience Manager (AEM) - AEM Assets | “将`PNG`的背景颜色更改为`#ff8932`”<br><br>“锐化图像”<br><br>“水平镜像图像” |

**相关信息**

* [AEM中的代理功能：内容顾问 — 内容优化](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/content-optimization/use-cases)

## 品牌治理

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 准则和区段查找 | 检索详细的品牌指南，按区段、市场或类别划分范围 | 企业上下文 | Adobe Experience Manager (AEM) | “这个品牌的声调准则是什么？”<br>“列出垂直健康领域使用的索赔类别” |
| 根据品牌指南评估内容 | 根据配置的品牌检查评估已发布/创作的页面、文本块或图像 | aem-governance | Adobe Experience Manager (AEM) | “根据SecurBank准则评估此登陆页面”<br>“此标语是否通过我们的语调检查？” |
| 调试AEM权限 | 调试/了解权限策略、ACL和继承规则。 | aem-governance | Adobe Experience Manager (AEM) | “为什么主体管理员可以在`https://author/`上写`/content/folder/us`？”<br>“为什么无法在`https://author`上的`/content/dam`中采样作者写” |

**相关信息**

* [AEM中的代理功能：品牌管理](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-governance/use-cases)

## 数据分析

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [提取CJA和AA报告与指标](data-insights/analytics-chat.md) | 实时查询CJA或AA以提取量度、维度、区段、数据视图和报表包 | `cja`, `aa` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | “显示过去30天的页面查看次数”<br>“列出主数据视图中的热门区段” |
| 比较分析 | 并排比较各个渠道、时间段或区段之间的量度 | `cja-root-cause-analysis`, `cja`, `aa-root-cause-analysis`, `aa`, `dx-api`, `knowledge-graph` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | “按渠道逐月比较收入”<br>“本季度移动与桌面转化情况如何？” |
| 营销活动效果 | 测量在给定时间段内促销活动、渠道和Web属性的执行情况。 | `cja`, `aa`, `dx-api`, `knowledge-graph` | | “上个月，我们的Acrobat网络营销活动表现如何？” |
| funnel分析 | 逐步了解每个阶段都存在流失的多步转化漏斗 | `cja`, `aa` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | &quot;带我浏览funnel&quot; <br> &quot;显示从PDP到购买的转化funnel&quot; |
| 预测 | 基于历史CJA或AA数据预测未来量度值 | `cja`, `aa` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | “未来30天的预测会话”<br>“我们是否即将实现收入目标？” |
| [根本原因分析](data-insights/root-cause-analysis.md) | 调查量度发生更改的原因：诊断下降、尖峰和异常 | `cja-root-cause-analysis`, `aa-root-cause-analysis` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | “上周为什么转化率下降？” <br> “是什么导致了1月15日的收入激增？” |
| 执行摘要和KPI摘要 | 制作为利益相关者准备的性能摘要、规范性建议和幻灯片组概述 | `cja-executive-summary`, `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, `cja-reporting`, `cja`, `aa`, `dx-api` | Customer Journey Analytics (CJA)、Adobe Analytics (AA) | “给我上个月的执行摘要”<br>“根据本季度的数据创建一个幻灯片组大纲” |
| [AA ↔ CJA数据验证](data-insights/data-validation-aa-cja.md) | 在Adobe Analytics和Customer Journey Analytics之间比较、审核和协调数据，尤其是在从Adobe Analytics升级到Customer Journey Analytics时 | `aa-cja-validation`, `cja`, `aa`, `dx-api` | ADOBE ANALYTICS + CJA | “将我的AA报表包与CJA数据视图进行比较”<br>“验证AA和CJA之间的页面视图” |
| [验证数据集和字段质量](data-insights/data-validation-aep.md) | 对Experience Platform数据集和字段运行统计和语义验证，以在执行后或持续进行<!--TODO: confirm skill ID(s) with engineering before publishing-->时捕获数据质量问题 | `data-validation` | Adobe Experience Platform | “验证数据集Electronics Sample 1000” <br>“验证Customers_2024数据集中的电子邮件字段” |
| 运行时间序列和因果分析 | 查询和分析受众、数据集和具有因果归因的历程的历史时间序列数据 | `operational-stats-causal-analysis` | 所有符合条件的应用程序 | “显示过去90天的受众规模趋势” <br>“为什么我的数据集行数在3月3日激增？” |
| 创建自定义CJA技能 | 将分析模式转变为可重用、可重复的技能，这些技能可在不同会话间持续保留 | `cja-skill-creator` | Customer Journey Analytics (CJA) | “将此每周收入分析转换为可重复使用的技能”<br>“将此技能另存为每月funnel报告的技能” |

## 受众

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [从自然语言创建受众](audiences/create-audience-from-natural-language.md) | 在每个阶段都通过用户批准来编排受众创建的分步过程 | `audience-creation-flow` | Real-Time CDP (RTCDP) | “创建过去30天内购买的用户受众”<br>“为加利福尼亚州的高价值忠诚度会员构建区段” |
| 构建PQL定义 | 从XDM属性、行为事件或现有受众收集受众定义；支持聚合和时间窗口 | `segment-definition-assembly` | Real-Time CDP (RTCDP) | “为查看了3个以上产品但未购买的用户创建PQL”<br>“向我的事件条件添加7天时间范围” |
| 搜索和查找受众 | 按ID、名称、语义搜索查找受众；检测重复项并分析重叠 | `audience-search` | Real-Time CDP (RTCDP) | “查找所有忠诚受众”<br>“我的‘节假日购物者’区段是否存在重复项？” |
| 估计受众规模 | 使用带有轮询的Adobe Experience Platform预览API估算PQL表达式的配置文件访问范围 | `audience-size-estimate` | Real-Time CDP (RTCDP) | “此受众有多大？”<br> “此PQL表达式的预计范围” |
| 受众规模瀑布 | 将PQL分解为子谓词，并显示每个条件对最终受众规模的贡献 | `audience-size-waterfall` | Real-Time CDP (RTCDP) | “向我显示此PQL的瀑布图”<br>“细分每个条件如何减少受众” |
| 发现用于定位的XDM字段 | 按名称、描述或数据值搜索字段；查看字段的生活位置和使用位置 | `field-discovery` | Real-Time CDP (RTCDP) | “我可以使用哪些字段来定位忠诚度客户？”<br> “查找与购买历史记录相关的字段” |
| 发布/保存受众 | 通过命名约定和合规性检查将受众定义保留到Experience Platform分段服务 | `audience-publish` | Real-Time CDP (RTCDP) | “将此内容另存为草稿”<br>“发布名称为‘春季促销买家’的受众” |

## 历程

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [从自然语言创建历程](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-create){target="_blank"} | 在AJO中通过文本提示或上传的图像/流程图编排旅程创建 | `journey-create` | Adobe Journey Optimizer (AJO) | “创建一个欢迎历程，注册后发送电子邮件，等待3天，然后发送跟进”<br>“从此上传的流程图图像构建历程” |
| [分析历程冲突](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 检测活动历程之间的受众重叠、计划冲突和重复数据删除问题 | `journey-analyze-conflict` | Adobe Journey Optimizer (AJO) | “我的购物车放弃历程是否与任何其他历程冲突？” <br> “检查我的活动历程之间的受众重叠” |
| [分析历程流失](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 识别客户在旅程中的流失位置和原因，并检测导致脱离接触的行为模式 | `journey-analyze-fallout` | Adobe Journey Optimizer (AJO) | “在我的重新参与历程中，客户从哪里流失？”<br> “历程X中的哪些节点的流失率最高？” |
| [分析自定义操作错误](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 识别历程中自定义操作何时失败或错误率激增，并在故障升级为更广泛中断之前诊断根本原因 | `journey-analyze-custom-action` | Adobe Journey Optimizer (AJO) | “为什么自定义操作在我的忠诚度注册历程中失败？” <br> “在我的欢迎历程中向我显示自定义操作ExternalPush的错误率。” |
| [检测历程异常](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 检测并确认历程的进入、退出或发送计数中相对于历史基线的意外尖峰、下降或扁平化，并揭示可能的根本原因 | `journey-analyze-anomaly` | Adobe Journey Optimizer (AJO) | “为什么昨天我的欢迎历程的条目减少了？” <br> “本周购物车放弃历程的退出次数是否激增？” |
| [比较历程版本](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journeys-coworker-skills#journey-analyze){target="_blank"} | 比较两个历程版本并查看节点、连接和历程级别属性更改的结构化差异 | `journey-analyze-version-comparison` | Adobe Journey Optimizer (AJO) | “比较我的欢迎历程的版本2和3”<br>“这两个历程版本之间发生了什么变化？” |

**相关信息**

* [使用AI](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}概述Adobe Journey Optimizer中的同事和可用技能。

## Journey Optimizer内容管理


| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [应用品牌指南](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 查找、选择并应用适用于营销活动语音、书写、图像、术语和法律指南的已批准品牌指南。 | `brand-lookup` | Adobe Journey Optimizer (AJO) | “拉出我们Acme品牌的文字和视觉指南。” |
| [检查内容准备情况](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 审查营销活动内容，了解品牌声音、编辑质量、参与度、清晰度和准备情况。 | `check-content-readiness` | Adobe Journey Optimizer (AJO) | “此电子邮件副本是否已准备就绪，可以发送？ 检查品牌声音、清晰度、可访问性和合规性。” |
| [编排内容创作](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 跨支持的渠道规划、创建、审查、分析和保存营销活动内容。 | `orchestrate-content-authoring` | Adobe Journey Optimizer (AJO) | “根据此简短的介绍，为我们的秋季销售电子邮件促销活动运行完整的内容创作，然后查看并保存最终的HTML。” |
| [评估内容设计](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 分析可视化实施，确定布局和设计差距，并推荐层级、间距、图像和行动动员方面的改进。 | `assess-content-design` | Adobe Journey Optimizer (AJO) | “这封电子邮件的视觉效果如何？ 检查层级、间距、密度、图像和CTA。” |
| [从Figma生成电子邮件](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 当副本可供发送时，从实时图形框架中生成最终电子邮件HTML；不需要单独的布局计划。 | `build-email-from-figma` | Adobe Journey Optimizer (AJO) | “从这张图框构建最终的电子邮件HTML；设计中的副本是应该送出的内容。” |
| [浏览内容策略](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 比较接触点、渠道、受众和消息主题之间的营销活动策略，并在编写之前规划每条消息。 | `explore-content-strategy` | Adobe Journey Optimizer (AJO) | “比较一个回送电子邮件与三点式电子邮件和短信程序。” |
| [生成内容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 为受支持的渠道（包括电子邮件、短信、推送、WhatsApp和登陆页面）编写或草稿新的受限营销消息。 | `generate-content` | Adobe Journey Optimizer (AJO) | “从批准的营销活动方向为电子邮件、推送和短信创建品牌内启动副本。” |
| [创建内容简介](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 将批准的营销活动方向转换为对选件、音调、关键消息、渠道、区域设置、变体和所需内容的需求。 | `content-brief` | Adobe Journey Optimizer (AJO) | “将这份简报转变为向已失效的美国订阅者发送温暖回信的要求：到星期日将有20%的折扣，以CTR作为KPI。” |
| [生成图像](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 创建或转换已批准投放位置的Campaign可视化图表，包括主页图像、裁剪、叠加、变体和签名资产。 | `generate-image` | Adobe Journey Optimizer (AJO) | “使用批准的品牌方向生成此春季销售电子邮件的优质主页图像。” |
| [保存渠道内容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 将批准的营销活动内容另存为草稿资源，或将其填写到AJO或其他支持的操作解决方案中的源模板。 | `save-channel-content` | Adobe Journey Optimizer (AJO) | “将批准的内容填写到源模板中，并准备对其进行审查。” |
| [修改并重新生成内容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills#ce-channel-content){target="_blank"} | 将确认的更改应用于现有促销活动内容，包括措辞、语气、翻译、主题行、行动要求和审核结果。 | `revise-regenerate-content` | Adobe Journey Optimizer (AJO) | “在保留已批准的报价和CTA的同时，让气氛更加温暖。” |

**相关信息**

* [使用AI](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}概述Adobe Journey Optimizer中的同事和可用技能。

## 营销计划

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 构建项目 | 将现有项目模板调整为新项目，其中的Smart Campaigns、计划和占位符电子邮件由纯语言描述或上传的简介生成 | `build-programs` | Adobe Marketo Engage | “为我们8月份的产品演示创建一个网络研讨会注册计划”<br><br>“构建一个程序，当潜在客户点击得分为50分时触发该程序”<br><br>“为未活动的潜在客户创建3封电子邮件的重新参与系列90天” |
| 从简短的节目中站出来 | 将纯语言简报或上传的活动文档转换为工作程序：克隆最接近的匹配模板，结转智能营销活动和令牌，并更新事件详细信息。 新的智能营销活动保持停用以供您审阅 | `build-programs` | Adobe Marketo Engage | “我将于9月10日在芝加哥举办一次网络研讨会。 为我设置计划“<br><br>”从此简介设置下个月的路演计划并更新活动令牌“ |
| 克隆和调整现有程序 | 复制新城市、季度或区域的先前项目并更新日期、令牌和命名。 子智能营销活动会延期并保留为已停用，直到您激活它们 | `build-programs` | Adobe Marketo Engage | “在10月17日克隆我们纽约办事处的上季度活动计划并更新日期和令牌”<br><br>“复制我们英国受众的芝加哥路演计划” |
| 使用资格逻辑构建智能营销活动 | 创建触发器或批处理智能营销活动，添加智能列表规则（如填写表单或达到分数），并配置流程步骤（如发送电子邮件） | `build-programs` | Adobe Marketo Engage | “创建一个触发器营销活动，在商机填写“联系我们”表单时发送我们的欢迎电子邮件”<br><br>“为点击50分的商机构建批处理营销活动并添加“发送电子邮件”步骤” |

## 忠诚度

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [创建、编辑和管理忠诚度挑战](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/loyalty-challenges/loyalty-coworker-skills#loyalty-challenge-management){target="_blank"} | 简化并加快忠诚度计划管理 | `loyalty` | Adobe Journey Optimizer (AJO) | “创建挑战，鼓励会员尝试新的季节性饮品”<br>“向我展示会员流失率最高的忠诚度挑战。” |
| [分析忠诚度计划绩效](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/loyalty-challenges/loyalty-coworker-skills#loyalty-data-insight){target="_blank"} | 使用自然语言查询和分析忠诚度积分、成员层、赎回和收入指标 | `loyalty-insights` | Adobe Journey Optimizer (AJO) | “2026年8月期间授予了多少忠诚度积分？” <br> “显示2026年8月按天划分的忠诚度计划总收入。” |

**相关信息**

* [使用AI](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-features#cx-coworker-skills){target="_blank"}概述Adobe Journey Optimizer中的同事和可用技能。

## Journey Optimizer中的内容创建

使用同事聊天来规划、生成、评估和优化活动消息副本和向HTML发送电子邮件，然后直接将批准的内容保存或交付给Journey Optimizer。

### 消息复制

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [捕获营销简报](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 捕获营销活动策略并播种创意摘要。 | `capture-marketing-brief` | Adobe Journey Optimizer (AJO) | “为季节性产品发布创建营销简报”<br>“将此营销活动策略转变为营销简报” |
| [捕获创意摘要](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 构建复制执行规范并构建内容计划矩阵。 | `capture-creative-brief` | Adobe Journey Optimizer (AJO) | “根据此批准的营销简报创建创意简报”<br>“为我们的电子邮件和短信营销活动构建内容计划矩阵” |
| [计划内容策略](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 在生成副本之前头脑风暴式消息地图、叙述弧和渠道角色。 | `plan-content-strategy` | Adobe Journey Optimizer (AJO) | “通过电子邮件和推送为我们的产品发布计划消息策略”<br>“为我们的欢迎活动提供叙述弧线” |
| [生成副本](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 为电子邮件、短信、推送、WhatsApp、社交和横幅生成全新的品牌内副本。 | `generate-copy` | Adobe Journey Optimizer (AJO) | “撰写品牌内电子邮件，宣布我们新的季节性系列”<br>“为那些使用废弃购物车的客户草拟短信提醒” |
| [生成图像](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 使用Firefly生成、裁切、覆盖、更改和标记营销活动图像。 | `generate-image` | Adobe Journey Optimizer (AJO) | “为我们的季节性促销活动电子邮件生成主页图像” <br>“从此批准的促销活动图像创建横幅变体” |
| [评估副本](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 根据品牌和渠道标准评估现有文案并打分。 | `evaluate-copy` | Adobe Journey Optimizer (AJO) | “根据我们的品牌指南评估此电子邮件副本” <br>“检查此推送消息是否符合我们的渠道标准” |
| [编辑副本](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 对现有副本进行就地编辑 — 评估修复、重新措辞调整、翻译和定向修订。 | `edit-copy` | Adobe Journey Optimizer (AJO) | &quot;修订此电子邮件副本以处理评估反馈&quot; <br>&quot;将此已批准的SMS副本翻译为法语&quot; |
| [展开促销活动内容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 跨渠道、区域设置、受众和变体将批准的内容计划矩阵按单位压缩为副本。 | `expand-campaign` | Adobe Journey Optimizer (AJO) | “为此批准的内容计划中的每个渠道生成副本”<br>“将此营销活动扩展到每个受众的英语和法语变体” |
| [分析可视化HTML](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 将HTML副本渲染到屏幕快照以进行可视检查。 | `analyze-visual-html` | Adobe Journey Optimizer (AJO) | “在HTML中呈现此电子邮件，以便我检查布局”<br>“向我显示此营销活动HTML的屏幕截图” |
| [保存内容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 将批准的内容保存回Adobe Journey Optimizer、Adobe Campaign v8或Marketo。 | `save-content` | Adobe Journey Optimizer (AJO) | “将此批准的电子邮件内容保存到Journey Optimizer”<br>“将批准的短信副本保存到Journey Optimizer” |

### 电子邮件设计

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [撰写电子邮件](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 计划从营销目标和品牌投入中阻止结构和样式。 | `compose-email` | Adobe Journey Optimizer (AJO) | “使用我们的品牌指南为我们的产品发布计划电子邮件布局”<br>“使用主页部分、产品亮点和call to action撰写欢迎电子邮件” |
| [生成电子邮件](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 从布局计划、屏幕快照或Figma设计链接构建、调整、编辑和优化电子邮件HTML。 | `build-email` | Adobe Journey Optimizer (AJO) | “从此批准的布局计划生成电子邮件HTML”<br>“从此Figma设计链接创建电子邮件” |
| [维护设计系统](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 维护品牌的可重用电子邮件设计系统 — 令牌、布局模式和品牌语言。 | `maintain-design-system` | Adobe Journey Optimizer (AJO) | “使用这些批准的品牌颜色更新我们的电子邮件设计系统”<br>“将此可重复使用的产品布局添加到我们的电子邮件设计系统” |
| [审核合规性](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 根据品牌和渠道准则以及可投放性标准审核组合电子邮件。 | `review-compliance` | Adobe Journey Optimizer (AJO) | “对照我们的品牌和渠道准则查看此电子邮件”<br>“在移交前审核此电子邮件中的可投放性问题” |
| [审核设计](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 提供关于层级、间距、叙述流程和品牌契合度的主观设计反馈。 | `review-design` | Adobe Journey Optimizer (AJO) | “查看此电子邮件的视觉层次结构和间距”<br>“评估此电子邮件设计是否符合我们的品牌” |
| [查看辅助功能](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 运行WCAG 2.1 AA辅助功能审核。 | `review-accessibility` | Adobe Journey Optimizer (AJO) | “审核此电子邮件是否存在WCAG 2.1 AA辅助功能问题”<br>“检查此电子邮件的颜色对比度和图像替换文本” |
| [发送电子邮件](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"} | 将获得批准的HTML导出并发送到Adobe Journey Optimizer或Adobe Campaign。 | `handoff-email` | Adobe Journey Optimizer (AJO) | “将此批准的电子邮件导出到HTML Journey Optimizer”<br>“将批准的电子邮件提交到Journey Optimizer” |

**相关信息**

* [内容管理的同事](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-management-coworker-skills){target="_blank"}提供了有关Adobe Journey Optimizer中的内容管理工具和可用技能的详细信息。

## 优化

使用同事聊天来浏览、分析和规划实验，以及创建、运行和排查Adobe Target活动、受众和推荐。

### 实验分析和策略

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 浏览和浏览试验 | 查找试验概述、列表、计数、原始结果、见解和机会 | `experiment-explorer` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | “显示我的实验” · “列出活动的测试” · “有多少实验正在运行？” |
| 分析实验性能 | 使用量度获取项目组合细分、单次试验运行状况检查、执行简报和跨试验报告，并可以选择使用CJA数据丰富这些数据 | `experiment-analysis` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | “我的A/B测试表现如何？” · “使用CJA指标生成活动报表” · “此测试是否正常？” |
| 计划和设计实验 | 获取要运行的影响最大的下一个测试、针对指定主题的设计、目标到量度的转换、失败测试的恢复指导或序列化多试验路线图 | `experiment-strategist` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | “下一步应该测试什么？” · “帮助我设计一个实验来改进结账转化” · “构建第3季度的测试路线图” |
| 搜索试验历史记录 | 从过去的实验中检索假设、学习、结果和治疗，按主题查找以前的实验，或摄取外部CSV以丰富结果 | `experiment-knowledge-base` | ADOBE TARGET / ADOBE JOURNEY OPTIMIZER | “我们对X实验了解多少？” · “我们以前测试过这个假设吗？” · “摄取此CSV” |

### Target活动和受众

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 浏览目标实体 | 发现、检查和计数活动、选件、受众、mbox、属性、工作区、AT.js配置、响应令牌和修订历史记录。 还可以捕获活动强制体验的屏幕截图 | `target-browse` | Adobe Target | “列出我的A/B测试” · “本月启动的活动有多少？” · “显示活动12345的详细信息” |
| 分析活动绩效 | 获取单个活动的转化率、提升度、置信区间、收入和风险计数。 只陈述事实，从不宣布赢家 | `target-analyze` | Adobe Target | “活动X的性能如何？” · “显示转化提升” · “什么是结账测试的AOV？” |
| 开船或叫停判决 | 获取活动的SHIP、WAIT、STOP或FIX推荐，其计算依据为原始计数的两倍重要性加上配置缺陷检查 | `target-activity-verdict` | Adobe Target | “我应该送出这个测试吗？” · “哪个变体赢了？” · “这有意义吗？” |
| 创建和配置活动 | 创建、更新和配置活动、选件和响应令牌，生成QA预览URL，以及创作或优化选件内容 | `target-design` | Adobe Target | &quot;为主页创建A/B测试&quot; · &quot;更新流量分摊&quot; · &quot;优化此选件的JS&quot; |
| 创建可视化体验编辑器活动 | 创建和编辑可视化体验编辑器(VEC)活动，针对实时页面URL以及覆盖变体的页面交付受众创作作为DOM修改的变体 | `target-vec` | Adobe Target | &quot;创建主页的VEC A/B测试&quot; · &quot;更改可视编辑器中的主页标题&quot; |
| 从头开始设置完整的测试 | 获得针对A/B、XT和VEC测试的引导式端到端活动创建，包括要求收集、先决条件、创建、计划和优先级、QA链接和可选激活 | `target-setup` | Adobe Target | “指导我设置完整的A/B测试” · “我是Target的新用户，帮我创建第一个测试” |
| 审计计划运行状况 | 获取整个项目的运行状况审核，其中涵盖风险和冲突检测、配置错误调查结果、受众和提供卫生以及速赢建议 | `target-intelligence` | Adobe Target | “审核我的Target活动” · “查找有风险或配置错误的测试” · “我应该清理哪些内容？” |
| 查找入选模式 | 挖掘Target中成功模式、有效策略以及高性能受众或内容的历史记录，然后根据您自己的数据获取下一步测试内容的建议 | `target-strategist` | Adobe Target | “什么对我们有用？” · “显示我的入选模式” · “下一步应该根据过去的结果测试什么？” |
| 计算样本大小和持续时间 | 规划A/B/n样本量、测试持续时间以及转化率和每位访客带来的收入指标的可检测提升，并进行Bonferroni校正 | `target-test-calculator` | Adobe Target | “我的A/B测试应该运行多久？” · “我需要什么样本量？” · “我的测试是否已提供动力？” |
| 获取项目级性能汇总 | 获取概述面板、最近推出的表格以及所有活动的综合赢/亏/提升情况普查，外加单活动趋势和动机的读数 | `target-portfolio-report` | Adobe Target | “给我一次Target计划的运行状况检查” · “哪些是我最好和最差的测试？” · “活动X是否趋向于获胜？” |
| 从自然语言创建受众 | 通过自然语言描述、显式规则条件或内联或上传的值列表创建或编辑Target本地受众。 将请求映射到规则语法，并在写入之前验证规则树 | `target-audience-composer` | Adobe Target | “创建加利福尼亚回访访客的受众” · “从这些邮政编码构建受众” · “缩小回访访客的受众X ” |

### 推荐

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 浏览推荐实体 | 浏览并检查推荐标准、收藏集、设计、促销活动、排除项、目录和信息源，并获取清理建议和目录属性指导 | `target-recs` | Adobe Target | “列出我的推荐标准” · “我有哪些设计？” · “我们可以清理哪些记录？” |
| 诊断推荐问题 | 跟踪活动、标准、信息源、收藏集和设计链，以解释为何推荐为空、过时或无法显示 | `target-recs-diagnose` | Adobe Target | “我的推荐为何为空？” · “为什么我的推荐活动在48小时内一直是‘结果未准备就绪’？” |
| 作者推荐 | 创建和更新“推荐”标准、收藏集、设计、排除项、促销活动、信息源和recs活动，包括一次跨多个活动的封闭批量操作 | `target-recs-design` | Adobe Target | “创建‘查看次数最多’的标准”·“构建价格低于50美元的库存产品集合”·“在所有销售活动中应用黑色星期五的日期” |

## 基本元素

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 产品知识和文档 | 从官方Adobe文档中回答操作方法、概念、故障排除和最佳实践问题 | `product-knowledge` | 所有符合条件的应用程序 | “如何设置流目标？”<br> “批量分段与流式分段之间有何区别？” |
| 查询Experience Platform/Journey Optimizer实体 | 作为有关平台实体的问题的主要入口点；根据需要路由到KG 、字段发现或API | `operational-insights` | 所有符合条件的应用程序 | “我有多少数据集？” <br> “显示所有活动的历程”<br>“列出我的目标” |
| 知识图查询 | 通过单个SQL查询进行聚合计数、跨实体联接、关系查找和元数据探索 | `knowledge-graph` | 所有符合条件的应用程序 | “哪些受众使用此数据集？”<br> &quot;向我显示架构和数据集之间的关系&quot; |
| Experience Platform / Journey Optimizer / Customer Journey Analytics API操作 | 提供直接API网关，用于处理知识图中没有的突变、实时状态检查和实体类型 | `cxo-api` | 所有符合条件的应用程序 | “删除数据集X”<br>“检查我的批次摄取作业的状态” |
| 实体解析和链接 | 使用语义和词法搜索将实体提及解析为实际的Experience Platform实体并发现XDM字段 | `entity-linking` | Adobe Experience Platform | “将‘假日购物者’解析为实际受众”<br>“查找与购买历史记录相关的字段” |
| 管理自定义技能 | 保存、修改或删除跨会话保留的用户拥有的可重用技能 | `manage-skill` | 所有符合条件的应用程序 | “将该工作流另存为技能” <br>“删除我的每周报告技能” <br>“将此技能转换为可重复使用的技能” |
| 监控流容量和违规情况 | 检查沙盒中的当前和历史流使用情况、容量和违规状态 | `observability-streaming-capacity`, `observability-streaming-usage`, `observability-capacity-breaches` | Adobe Experience Platform | “我的当前沙盒中的当前流容量是多少？” <br> “我当前的沙盒在上周是否超出了容量限制？” |
| [查看运行状况检查评估结果](https://experienceleague.adobe.com/en/docs/experience-platform/run-and-operate/health-checks/overview) | 查看沙盒的最新运行状况检查评估，深入研究未通过检查，并查看受影响的实体 | `rao-view-latest-health-checks-assessment` | Adobe Experience Platform | “我的沙盒有什么问题？” <br> “告诉我关于我最新的运行状况检查评估的信息” <br> “自定义命名空间描述检查有哪些问题？” |
| 修复运行状况检查问题 | 在进行任何更改之前，经您批准，可直接从聊天中修复标记的身份命名空间、合并策略和架构问题 | `rao-remediate-identity-namespace-description`, `rao-remediate-merge-policy-duplicate-name`, `rao-remediate-missing-audit-field-group`, `rao-remediate-default-merge-policy-naming` | Adobe Experience Platform | “修复身份命名空间描述”<br>“修复重复的合并策略名称”<br>“修复缺少审核字段组的架构”<br>“修复默认合并策略命名” |

## 数据管理

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [查找值得优化或清理的数据](./data-management/manage-data-lake-retention.md#find-data-worth-optimizing) | 了解是否可以通过将最大、使用率最低或遗忘的数据集显示为候选清理或数据湖保留策略而优化Experience Event数据 | `List datasets` | Adobe Experience Platform | “我感觉我的数据可以优化”<br> “帮助我了解我的数据的价值”<br> “优化我的沙盒数据”<br> “清理我的沙盒数据集” |
| [调查数据集的使用情况并管理保留](./data-management/manage-data-lake-retention.md#check-how-actively-a-dataset-is-used) | 找到值得仔细研究的数据集后，可了解其使用积极性，对潜在数据湖保留策略的影响进行建模，并在准备就绪时设置、更改或删除该策略，并在进行任何更改之前进行审核和批准 | `Analyze dataset usage`, `Analyze dataset retention`, `Manage dataset retention` | Adobe Experience Platform | “我的Web事件数据集的使用情况如何？” <br> “如果在此数据集中设置60天的保留期，将会产生什么影响？” |

## 沙盒工具

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| [跨沙盒移动对象](/help/chat/use-cases/sandbox-tooling/sandbox-tooling.md) | 通过自动解析依赖关系，跨沙盒无缝迁移架构、受众和其他对象配置 | `sandbox-tooling-workflow` | Adobe Experience Platform | “将架构Luma忠诚度会员白金从当前沙盒移动到生产沙盒”<br>“将美国黄金忠诚度会员受众提升到暂存环境” |

## 客户警报

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 管理警报订阅 | 通过自然语言对话查看和管理警报订阅。 | `alerts-subscribe` | Adobe Experience Platform | “我订阅了哪些警报？”<br><br>“为我订阅此警报。”<br><br>“删除此警报的订阅。” |
| 查看警报活动 | 查看指定时间段内的当前警报状态和历史警报活动。 | `alerts-list` | Adobe Experience Platform | “过去24小时内发生了什么？”<br><br>“过去24小时内触发了哪些警报？”<br><br>“显示过去七天的活动警报。” |
| 识别定期警报模式 | 分析警报历史记录，以识别频繁触发的警报类型和操作趋势。 | `alerts-list` | Adobe Experience Platform | “显示前3个触发的警报类型。”<br><br>“哪些警报类型本月发生得最频繁？”<br><br>“您最近七天看到了哪些警报模式？” |
| 关注高度优先的问题 | 按严重程度筛选警报活动以安排调查工作的优先级。 | `alerts-list` | Adobe Experience Platform | “仅显示高严重性警报。”<br><br>“本周触发了哪些严重性警报？”<br><br>“显示过去30天的严重性警报。” |
| 了解警报的影响范围 | 确定受警报影响最大的对象并确定应从何处开始调查。 | `alerts-list` | Adobe Experience Platform | “前5个受影响的对象是什么？”<br><br>“哪些对象与最高级别警报关联？” |
| 将警报类型连接到受影响的对象 | 分析警报类型和受影响资源之间的关系。 | `alerts-list` | Adobe Experience Platform | “哪些警报类型最常影响此数据集？”<br><br>“显示警报类型与受影响对象之间的关系。”<br><br>“哪些警报类型最常影响最受影响的对象？” |
| 关注我的警报 | 分析您订阅并负责监视的警报。 | `alerts-list` | Adobe Experience Platform | “显示我订阅的高严重性警报。”<br><br>“本周触发了来自我的警报的哪些警报？”<br><br>“我的任何订阅警报需要关注吗？” |

## 工作流和规划

| 用例 | 描述 | 技能 | 应用程序 | 示例提示 |
| --- | --- | --- | --- | --- |
| 管理规划工作区 | 构建和改进Workfront Planning工作区、部分、记录类型和字段，以组织项目和跟踪工作 | `manage-workfront-planning`, `wf-planning-solution-architect` | Workfront规划 | “创建一个名为MKG Hub的工作区并设置记录类型以按地区跟踪程序”<br>“设置跨渠道和区域跟踪MKG程序所需的记录类型和关系” |
| 管理规划记录 | 在工作区中创建和更新规划记录（营销活动、摘要）及其字段值 | `manage-workfront-planning` | Workfront规划 | “为秋季品牌发布活动创建简报，包括目标、目标受众和关键消息”<br>“使用预算和主要渠道更新秋季品牌发布简报” |
| 创建和管理项目 | 启动和构建项目：应用模板、设置优先级和预算、对任务进行排序、添加阶段和依赖项以及分配人员或角色 | `manage-workfront-workflow` | Workfront工作流程 | “创建春季营销活动，使用$200K预算将其设置为高优先级，然后排列任务顺序” <br> “从[项目模板]创建名为[项目名称]的Workfront项目计划” <br> “为秋季发布构建项目计划：包含概念、设计、复制和审阅任务的社交营销活动” <br> “添加新电子邮件营销任务并将其分配给Rachel Smith” |
| 加快审查和批准 | 设置多阶段批准、应用批准模板、添加/删除批准者、发送提醒并进行批量更新 | `manage-workfront-workflow` | Workfront工作流程 | “创建多阶段批准（复制、设计、法律），并提醒未批准的人”<br>“将Chris Smith从所有未完成的批准中移除并替换为Jane Francis” |
| 更新任务和工作状态 | 标记任务完成、更新完成百分比并关闭您的工作 | `manage-workfront-workflow` | Workfront工作流程 | “将我在秋季启动项中的‘生成关键艺术’任务标记为完成”<br>“100%关闭我的秋季启动项复制任务” |
| 表面工作分析 | 提出探索性问题以查找存在风险的工作、未分配任务、未完成的问题和跨项目的状态 | `query-workfront` | Workfront工作流程 | “查找未分配给任何人和本周到期的当前项目中的未完成任务”<br>“当前项目中有多少个未完成的问题？” |
| 项目和任务摘要 | 项目、任务、问题和分配的拉取列表、表和计数 | `query-workfront` | Workfront工作流程 | “显示已准备开始的任务的表，其中具有项目名称、任务到期日期和分配的用户”<br>“获取分配给[用户名]的所有任务” |
| 跟踪批准和项目组合状态 | 检查审批状态，并按项目组合汇总未完成的工作 | `query-workfront` | Workfront工作流程 | “显示我的审批状态”<br>“显示包含未完成问题的表，这些问题是[Portfolio名称]项目组合的一部分” |
