---
description: 了解同事营销活动如何自动附加并保留图像上的C2PA元数据，从生成一直到电子邮件投放。
title: 同事营销活动中的C2PA元数据
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
source-git-commit: dbee38135a5491fd21b65fdbb70ba60d949d7560
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 4%
---
# 同事营销活动中的C2PA元数据 {#overview}

围绕创新型人工智能透明度的新法律正在出现，Adobe正在努力满足跨司法辖区的适用要求。 [C2PA元数据](https://c2pa.org/)是Adobe用于满足这些法律要求的源工具。

C2PA元数据是持久的、不可见的元数据，记录一段内容的创建或编辑方式。 在Co-worker Campaigns中使用创作AI工具生成或编辑图像时，C2PA元数据会自动附加到该图像。 您无需执行任何操作。

## 电子邮件营销活动中的C2PA元数据 {#c2pa-metadate-email}

在您的电子邮件促销活动中发送的图像将其C2PA元数据保持不变，因此收件人可以直接从投放的电子邮件中验证任何图像的来源和真实性。

## 附加C2PA元数据的操作 {#actions}

下表基于在同事营销活动中生成图像时执行的图像操作，总结了附加C2PA元数据的时间。

| 操作 | 描述 | 是否附加C2PA元数据？ | 用例示例 |
| --- | --- | --- | --- |
| **生成图像** | 从文本提示或参考图像创建新图像，或从现有图像生成类似图像。 | 一直。 由于图像是由创成式人工智能生成的，因此它总是带有新的C2PA元数据。 | 从描述所需视觉效果的文本提示生成电子邮件促销活动的横幅图像。 |

## 内容类型及其范围 {#content-types}

* **图像**：已覆盖。 使用创作AI生成图像时，会附加C2PA元数据，并通过在Co-worker Campaigns中通过图像生成执行的裁切、文本叠加和图像叠加操作来保留。
* **文本**：不适用。 合作营销活动中的纯文本输出（如副本生成、翻译和品牌调整建议）不需要C2PA元数据。

## 内容移动时发生的情况 {#content-moves}

同事营销活动会保留与支持的图像资产关联的C2PA元数据。 如果导入到同事营销活动中的图像包含C2PA元数据，则在生成的营销活动内容和出站电子邮件体验中使用资产时，将保留这些凭据。

## 其他资源 {#resources}

* [创作AI内容透明度](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency){target="_blank"}
* [Adobe Experience Cloud创作AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [护栏和限制](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/generate-content/gs-generative#generative-guardrails){target="_blank"}
