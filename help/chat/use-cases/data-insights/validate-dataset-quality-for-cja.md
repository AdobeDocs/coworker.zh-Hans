---
title: 使用Co-worker中的数据验证技能验证Customer Journey Analytics数据
description: 了解如何使用Co-worker中的数据验证技能验证Customer Journey Analytics数据，并在构建仪表板之前解决问题。
feature: AI Tools
role: User
level: Beginner, Intermediate
doc-type: Feature Video
duration: 330
last-substantial-update: 2026-09-16
jira: KT-22622
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%
---
# 使用[!DNL Coworker]中的数据验证技能验证Customer Journey Analytics数据

数据质量是Adobe Customer Journey Analytics (CJA)中准确报表的基础。 在构建量度、功能板、区段或客户历程之前，了解底层Adobe Experience Platform (AEP)数据是否可信至关重要。

在本视频中，您将了解如何使用Adobe CX Enterprise Coworker中的&#x200B;**数据验证技能**&#x200B;快速评估为Customer Journey Analytics实施提供支持的数据集的质量，而无需编写查询或手动检查数据。

>[!VIDEO](https://video.tv.adobe.com/v/3503519/?learn=on&enablevpops)

## 了解CJA报表背后的数据集

了解同事如何识别：

- 哪些数据集已连接到Customer Journey Analytics
- 与特定沙盒关联的连接和数据视图
- 数据集为报告提供主动支持
- 关键数据集特征，如流状态和身份命名空间

通过准确地了解哪些数据集为您提供报表，您可以将验证工作集中在最重要的地方。

## 浏览数据集架构和可用字段

了解如何直接从Adobe Experience Platform检查数据集架构。

同事检索架构详细信息和界面：

- Commerce和交易字段
- 产品信息
- Web交互数据
- 身份标识字段
- 营销活动和营销属性
- 设备和地理尺寸

这会提供可用于分析的字段清单，并突出显示架构中存在的字段与包含可用数据的字段之间的差异。

## 验证身份质量

身份数据对于Customer Journey Analytics至关重要，因为它支持人员级别报表和跨渠道历程分析。

在本视频中，您将看到同事如何：

- 验证身份字段
- 检查空值和数据完整性
- 评估标识符质量
- 表面缺少身份属性或身份属性不可用

示例验证显示，ECID和电子邮件标识已完全填充并在示例中有效，而无法检索Analytics ID。 这在决定哪些标识符可以支持用户档案拼接和报告时提供了一个有用的信号。

## 分析单个字段质量

字段可能存在于数据集中，但仍不适合报告。

观看同事如何验证营销活动跟踪字段和报告：

- 人口比率
- 空百分比
- 数据一致性
- 无效值检测

在本例中，显示的跟踪代码值是干净和一致的，但大约85%的行为空。 这显示在基于字段构建CJA维度或营销活动量度之前的主要报表盲点。

## 执行AI支持的数据集验证

Co-worker可以评估整个数据集，而不是一次验证一个字段。

您将学习数据验证技能：

- 选择要验证的重要字段
- 评估完整性和质量
- 跨字段比较数据运行状况
- 突出显示优势和潜在报告风险

验证结果为CJA提供了可行性图。 网页名称和电子邮件代码等清理字段可能已准备好进行报告，而稀疏字段（如购买值、促销活动名称和跟踪代码）需要调查。

## 确定收入和归因风险

此视频还演示了数据验证如何发现影响报表准确性的问题，包括：

- 稀疏的营销活动数据
- 缺少归因信息
- 未完成的交易记录值
- 收入衡量差距

在显示的数据集中，采购计数可用，但订单金额无法可靠地填充。 在信任收入报告之前，需要调查此问题。

## 为何数据验证对Customer Journey Analytics很重要

Customer Journey Analytics的可靠性取决于其背后的数据。

在生成报表之前验证数据集可帮助团队：

- 增加对Analytics结果的信心
- 改进数据治理实践
- 减少报告错误
- 尽早发现实施问题
- 更有效地排除意外量度

使用Co-worker，可以使用自然语言提示启动这些检查，从而使技术用户和非技术用户更容易访问数据验证。

