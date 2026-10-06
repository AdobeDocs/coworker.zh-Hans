---
title: 与同事一起规划Customer Journey Analytics或流媒体实施
description: 了解同事的实施指南技能如何通过可导出的核对表，将发现对话转换为个性化、有序的实施计划。
hold: true
source-git-commit: 94cf399a48d13ee83c702804b50fdccd4baa9d71
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 1%
---

# 与同事一起规划实施

合作者包括五种实施指南技能，每种产品表面各一种：Customer Journey Analytics、Adobe Analytics到Customer Journey Analytics的升级、Content Analytics (ACA)、Marketing Campaign Analytics (MCA)和流媒体。 每项技能都可以将简短的调查对话转变为个性化、依赖性感知的实施计划，并提供交互式核对清单和随时可用的导出，所有这些都可以在一个同事聊天对话中完成。

如果您正在站起来或迁移到其中任何产品，则可以使用这些技能获得有序的分步计划，而无需手动研究Adobe的实施要求或从头开始构建项目计划。

>[!NOTE]
>
>请考虑以下事项：
>
>* 这些实施指南技能是更大的可选工作流程的一部分：自定义实施或升级步骤（这些指南）、实施（请参阅[生成同事项目的实施核对清单](./intelligent-checklist.md)）和验证（例如，[验证Adobe Analytics是否升级到Customer Journey Analytics](./data-validation-aa-cja.md)或[验证您的流媒体实施](./streaming-media-validation.md)）。 您无需使用所有三个阶段。 例如，您无需生成计划或核对清单即可验证数据。
>* 这些技能不会访问您的Adobe系统或进行任何更改。 它们可帮助您规划实施。 他们不会执行它或针对实时租户验证它。

使用这些技能可以：

* 获得从头开始支持Customer Journey Analytics的个性化、有序计划，包括每个步骤的所有者、工作量估计和依赖项。

* 在停用Adobe Analytics之前，获取有关从Adobe Analytics升级到Customer Journey Analytics的迁移计划，包括Adobe Analytics功能对等映射、历史回填顺序和验证门。

* 获取实施Content Analytics (ACA)的引导式计划，包括许可、隐私和PII范围界定以及引导式配置向导。

* 获取适用于您的摄取路径的Marketing Campaign Analytics (MCA)入门计划，无论您使用的是Adobe源连接器、您自己的数据集还是混合方法。

* 获取Edge上流媒体收集的实施计划，包括数据流配置、每个平台的SDK/API实施和媒体事件模型。

## 开始之前

<!-- FLAG: Best guess, not confirmed by source docs. Requirements doc doesn't state explicit prerequisites for starting a discovery conversation — verify with skills-overview.md or SME before publishing. -->

### 所需信息

要开始实施指南对话，您需要：

* 以下五种实施路径中的哪一种适用于您：Customer Journey Analytics (net-new)、Adobe Analytics到Customer Journey Analytics的升级、Content Analytics (ACA)、Marketing Campaign Analytics (MCA)或流媒体。

* 有关当前环境的基本详细信息，例如您当前是否实施了Adobe Analytics、许可状态或计划的数据摄取路径。 发现对话会要求您提供这些详细信息，但让这些详细信息准备就绪可加快该过程。

### 限制

在使用这些技能之前，请牢记以下限制：

* **仅计划**：这些技能不会访问您的Adobe系统或进行任何更改。 他们不会执行实施或针对实时租户验证它。
* **每个技能一个产品表面**：每个技能都涵盖一个实施路径。 如果您的请求适用于不同的产品表面，则该技能会引导您找到正确的表面，而不是直接回答。
* **本身不是项目跟踪体验**：这些技能可生成计划和导出，但不会单独跟踪正在进行的状态、协作或审批。 要在一段时间内跟踪您的计划，请使用预定义的行动手册将其转换为同事项目。 请参阅[生成同事项目的实施核对清单](./intelligent-checklist.md)。

## 开始实施规划会议

1. 登录到同事。

1. 选择&#x200B;[!UICONTROL **新聊天**]。

1. 在文本字段中，描述要计划的实施或迁移。 例如：

   **提示**

   > 帮助我规划Customer Journey Analytics的实施。

   您的请求将被路由到匹配的实施指南技能，该技能将启动交互式发现对话。

1. （视情况而定）如果技能无法确定哪条实施路径适用于您，请回答其提出的澄清问题，然后继续。

## 选择实施路径

每个实施指南技能涵盖一个产品表面。

### Customer Journey Analytics

获得个性化、有序的实施计划，以便在没有现有Customer Journey Analytics部署可迁移的情况下从头开始支持Adobe Analytics。 您的计划包括每个步骤的所有者、工作量估计和依赖项。

示例提示：

* 帮助我规划Customer Journey Analytics的实施。
* 我从头开始站起Customer Journey Analytics。 为我制定一个实施计划。

### Adobe Analytics到Customer Journey Analytics的升级

获取一个将Adobe Analytics功能等同性映射到Customer Journey Analytics的迁移计划，对历史回填进行排序，并在停用Adobe Analytics之前包含一个验证和并行运行关口。

示例提示：

* 帮助我规划从Adobe Analytics到Customer Journey Analytics的升级。
* 构建从Adobe Analytics到Customer Journey Analytics的迁移计划。

### Content Analytics (ACA)

获取实施Content Analytics (ACA)的引导式计划，包括许可、隐私和PII范围界定以及引导式配置向导。 由于ACA没有DULE、CMK或HIPAA涵盖范围，因此您的计划包括隐私审核步骤。

示例提示：

* 帮助我规划Content Analytics的实施。
* 为我制定ACA实施计划。

### Marketing Campaign Analytics (MCA)

获取适用于您的摄取路径的Marketing Campaign Analytics (MCA) Essentials入门计划，无论您使用的是Adobe源连接器、您自己的数据集，还是混合方法，以便funnel映射和数据对齐步骤与您的环境相匹配。

示例提示：

* 帮助我规划Marketing Campaign Analytics的实施。
* 使用我自己的数据集为我制定MCA载入计划。

### 流媒体

获取在Edge上收集流媒体的实施计划，该计划涵盖数据流配置、每平台SDK/API实施和媒体事件模型，以便您正确检测Customer Journey Analytics和/或Adobe Analytics报表的会话、Ping和完成情况。

示例提示：

* 帮我规划我的流媒体实施。
* 制定在Edge上检测流媒体的计划。

## 查看结果

同事将您的实施计划作为交互式核对清单和摘要返回到同一对话中。

**交互式核对清单**

HTML核对清单，可将您的实施步骤分组为各个阶段和里程碑。 对于每个步骤，此清单都包括：

* 投入估计
* 主要所有者和任何支持所有者
* 对其他步骤的硬依赖性
* 是否可以跳过该步骤
* 相关Experience League或developer.adobe.com文档的链接

**导出**

以适合您工作流的格式下载计划：

| 导出 | 其中包含的内容 |
| --- | --- |
| CSV | 简单的步骤列表 |
| Jira导入CSV | 使用故事点、优先级和标签格式化的步骤以导入Jira |
| WORKFRONT CSV | 带有持续时间和前置任务格式的步骤，用于导入Workfront |
| Markdown | 可粘贴到文档或Wiki中的核对清单 |

**聊天摘要**

除了核对表，同事在对话中直接提供了三部分摘要：

1. 计划概述
1. 完整步骤表
1. 每次导出的下载链接

## 如何构建计划

每个实施指南技能都遵循相同的四个阶段过程：

* **发现**：分阶段的对话会询问针对您的实施路径的5到9组问题，以了解您的环境和目标。
* **计算**： LLM确定哪些条件步骤和依赖项覆盖适用于您的答案。 计划本身不是由它编写的。
* **汇编并渲染**：确定性进程解析步骤之间的依赖关系，对它们进行排序，计算关键路径（最长的依赖步骤链），并生成核对清单和导出。
* **交付**：同事提供下载链接和您计划的聊天摘要。

这种引导式发现和确定性组装的结合意味着计划是根据您的答案一致地生成的，而不是用手写的。
