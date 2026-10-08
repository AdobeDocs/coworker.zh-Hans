---
title: 与同事验证您的Experience Platform数据
description: 了解如何使用CX Enterprise Coworker数据验证技能，通过聊天检查Adobe Experience Platform数据集和字段的质量。
feature: AI Tools
role: User
level: Intermediate
doc-type: Tutorial
last-substantial-update: 2026-08-27T00:00:00.000Z
jira: PLAT-302857
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%
---

# 与同事验证Experience Platform数据

Adobe CX Enterprise Coworker包括数据验证技能，可检查Experience Platform数据集的数据质量。 使用它来对数据集运行统计和语义验证，分析数据集字段，并识别数据质量问题，所有这些操作都通过一个同事聊天对话进行。

数据工程师、数据管理员和实施工程师使用它进行快速质量检查，而无需SQL查询或复杂的架构层次结构。

使用此技能可以：

* 在新的实施或实施更新后验证密钥标识和事件字段。
* 通过检查字段的顶值和无效值来调查可疑的映射问题。
* 对关键数据集运行持续的数据管理检查，以尽早捕获回归。

<!--TODO: skill display name "Data Validation skill" confirmed via the published KT-22622 video page (validate-dataset-quality-for-cja.md, merged 2026-09-16). Still need the technical skill ID from engineering (Petru Adrian Snep) for the use-cases overview table row. That page didn't add one either.-->

>[!NOTE]
>
>此技能为只读。 它不会更改您的数据、架构或映射。

## 开始之前

要与同事验证您的数据，您需要：

* 要验证的数据集的名称或ID。
* （可选）如果不想让技能自动选择字段，则为要验证的特定字段的名称。

## 启动验证会话

1. 登录到同事。

1. 选择&#x200B;[!UICONTROL **新建聊天**]。

1. 在文本字段中，提示代理验证字段或数据集。 例如：

   **提示**

   > 验证数据集“电子产品示例1000”

   ![同事聊天主屏幕，带有在消息字段中输入的提示验证数据集Electronics Sample 1000。](../../assets/data-validation-aep/start-session.png)

   >[!TIP]
   >
   >在数据集名称前面加上“dataset”一词，以便技能能够正确识别它。 例如，使用“验证数据集Electronics Sample 1000”而不是“验证Electronics Sample 1000”。

   您的请求将被路由到“数据验证”技能，该技能会分析数据集的示例并在同一对话中返回结果。

## 选择要验证的内容

您可以验证单个字段或整个数据集。

>[!BEGINTABS]

>[!TAB 字段验证]

验证数据集中的特定字段。 此选项提供：

* 空计数和非重复值计数。
* 顶部非重复值及其频率。
* 人工智能辅助的语义验证，根据字段的元数据及其实际值标记与字段预期格式不匹配的值。

示例提示：

* 验证Customers_2024数据集中的email字段。
* 验证数据集customer_events_2024的字段状态。
* 验证客户数据集的字段person.address.city。

>[!TAB 数据集验证]

一次验证数据集中最多五个字段。 您可以自行指定字段，也可以让技能分析数据集并自动选择最相关的字段。 在您验证的每个字段中，此选项会返回与字段验证相同的信息。

示例提示：

* 验证Customer Data 2024数据集
* 验证字段email、phone for Customers_2024。
* 汇总客户数据的firstName、lastName、birthDate。

>[!ENDTABS]

## 查看结果

对于每个已验证的字段，结果将作为一行显示在具有以下列的表中：

| 列 | 描述 |
| --- | --- |
| [!UICONTROL 字段名称] | 字段名称。 |
| [!UICONTROL 字段路径] | 架构中字段的完整路径。 |
| [!UICONTROL 字段类型] | 字段的数据类型。 |
| [!UICONTROL 有效值] | 通过验证的采样值的百分比。 |
| [!UICONTROL 不同的值] | 不同的采样值的百分比。 |
| [!UICONTROL Null值] | 空的采样值的百分比。 |
| [!UICONTROL 前5个不同的值] | 最常见的五个值及其频率。 |
| [!UICONTROL 前5个无效值] | 最常见的五个无效值，并针对每个值给出说明，例如“不是有效的电子邮件格式”。 |
| [!UICONTROL 其他insight] | 有关字段质量的简短自然语言注释。 |

在结果下，同事添加了一个&#x200B;**后续步骤**&#x200B;列表，该列表建议后续提示，例如验证另一个字段或重新运行数据集。

验证单个字段时，Co-worker还会返回一个图表：

![同事聊天显示Brand字段的圆环图和书面摘要，报告79.5%的有效值、20.5%的null值以及未检测到无效值。](../../assets/data-validation-aep/null-values.png)

选择&#x200B;[!UICONTROL **图表**]&#x200B;或&#x200B;[!UICONTROL **表**]&#x200B;以在相同结果的视图之间切换。

验证数据集时，结果将显示在表中，每个字段有一行。 您自行命名的字段会按您指定的方式显示：

![标题为Electronics Sample 1000 Field Validation的同事聊天表，显示用户在提示中命名的类别、品牌和价格字段的验证结果。](../../assets/data-validation-aep/field-validation.png)

技能选择的字段自动以相同方式显示：

![同事聊天表显示Electronics Sample 1000数据集中五个自动选择的字段的验证结果：类别、品牌、价格、库存和条件。](../../assets/data-validation-aep/dataset-validation.png)

选择&#x200B;[!UICONTROL **CSV**]&#x200B;以下载完整的结果表。

## 由数据验证执行的检查

该技能对每个字段和数据集执行以下操作：

* **完整性检查**： null和缺少计数和百分比。
* **分布检查**：顶部非重复值及其分布，以及高基数检测。
* **针对架构的语义检查**：使用XDM字段名称、类型和描述推断有效值是什么样的，然后标记异常。
* **数据类型感知检查**，如果适用：
  * 电子邮件：格式和域的可行性。
  * 电话：格式准备就绪，例如E.164。
  * 日期和时间戳：基本格式检查，例如ISO-8601。

这些检查将确定性统计与LLM辅助的语义验证相结合，以检测看起来错误的值，即使它们在技术上与架构匹配也是如此。

## 限制

在验证数据之前，请牢记以下限制。 这些约束在性能和功能之间取得平衡，并设置了您可以期待的分析和见解的期望值。

* **仅采样**：该技能验证数据集（通常是最近的1,000行）的示例，而不是整个数据集。 完整数据集扫描不可用。
* **字段数限制**：验证数据集时，技能会分析每个请求最多五个字段。 您可以指定这些字段，或让技能自动选择它们。
* **概率语义**：无效值的检测部分依赖于基于LLM的推理，这种推理偶尔会遗漏细微的错误或标记边界值。
* **只读**：该技能不会更改您的数据或其架构。 它突出显示潜在问题，但不会执行自动修复。

如果您的验证需求更详尽或需要复杂的业务逻辑，请使用其他工具（如查询服务或数据准备验证）来补充这些结果。

**相关信息**

* [升级时验证Adobe Analytics到Customer Journey Analytics的数据](./data-validation-aa-cja.md)
* [使用Co-worker中的数据验证技能验证Customer Journey Analytics数据](./validate-dataset-quality-for-cja.md)
* [验证数据（AI助手）](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/agents/data-validation)
* [信任您的Customer Journey Analytics报告：Adobe CX Enterprise Coworker中的数据验证技能](https://www.youtube.com/watch?v=gCSm_QYSYhk)（视频）
