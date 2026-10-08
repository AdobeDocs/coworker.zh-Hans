---
title: 在同事项目中生成实施核对清单
description: 了解同事项目如何根据您的《实施指南》计划生成预填充的实施核对清单，以及您可以分配和跟踪的步骤。
hold: true
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%
---

# 生成与同事项目的实施核对清单

Adobe CX Enterprise Coworker可以在同事项目中生成一个实施核对清单项目，该项目已预先填充了您在实施指南计划中针对Customer Journey Analytics、Adobe Analytics到Customer Journey Analytics的升级、Content Analytics (ACA)、Marketing Campaign Analytics (MCA)或流媒体的按顺序步骤。 在技术上，同事可自动完成或协助完成尽可能多的步骤，因此您和您的团队可以在一个单一、可跟踪的位置完成实施。

如果您正在领导实施、执行技术步骤，或只是需要了解进度，则可以使用此核对清单在不离开同事的情况下分配工作、跟踪状态并与团队协作。

>[!NOTE]
>
>请考虑以下事项：
>
>* 此功能是一个更大的可选工作流程的一部分：自定义实施或升级步骤（请参阅[与同事一起计划实施](./implementation-guide.md)）、实施（此核对清单）和验证（例如，[验证Adobe Analytics以升级到Customer Journey Analytics](./data-validation-aa-cja.md)，或[验证您的流媒体实施](./streaming-media-validation.md)）。 您无需使用所有三个阶段，但生成此核对清单确实需要完成实施指南计划。
>* Co-worker通过执行或协助执行的步骤自动包括置信度或验证信号。 在标记完成之前查看这些步骤 — 同事不会将自动化结果显示为已验证的事实。

使用此核对清单可以：

* 为您的产品路径预填充一组有序的步骤，而不是手动汇编计划，从而开始实施或迁移。

* 在实施过程中检查状态，包括阻止的内容和后续内容，而无需直接询问实施主管。

* 规划多平台或多区域实施，其中步骤并行或分阶段运行，而不是使用一条直线。

* 让同事尽可能直接执行步骤，例如在Adobe Analytics和Customer Journey Analytics配置之间运行验证检查。

* 在团队继续下一步之前，为需要签核的步骤引入批准审核。


## 开始之前

<!-- FLAG: Open question — release note confirms a "predefined playbook" transforms the guide plan into a Coworker Project, but it's unconfirmed whether Coworker runs that playbook automatically or the user has to trigger/follow it manually. Written below as if Coworker does it automatically; verify before publishing. Exact UI mechanics also unconfirmed since Coworker Projects platform documentation doesn't exist yet. -->

### 所需信息

要生成实施核对清单，您需要：

* 有关您的产品路径的已完成的实施指南对话。 请参阅[与同事一起规划实施](./implementation-guide.md)。 Co-worker使用预定义的行动手册自动将此计划转换为Co-worker项目 — 您无需自行导出任何内容。

* 访问组织中的同事项目。

### 限制

在使用此功能之前，请牢记以下几点：

* **不拥有指南内容**：此功能使用实施指南技能中的计划。 它不会创作或维护该基础内容。
* **同步行为尚未完全定义**：清单旨在与实施指南计划的更新保持同步，但确切的同步机制仍在定义中。 如果您的实施时间较长，请手动检查指南计划更新。
* **需要同事项目**：此功能取决于组织中可用的同事项目平台。

## 生成清单

<!-- FLAG: Best guess, not confirmed by source docs. Coworker Projects UI isn't documented in this repo yet — verify exact navigation and UI labels once available. -->

1. 登录到同事。

1. 在导航边栏中选择&#x200B;[!UICONTROL **项目**]。

1. 选择&#x200B;[!UICONTROL **新建项目**]，然后选择与您的实施指南计划匹配的预定义行动手册。

   Co-worker可将您的计划转换为项目，该项目已为您路径预填充了排序的步骤。

## 查看结果

同事将生成您的实施核对清单作为您和您的团队可以使用的同事项目。

**项目视图**

您的项目按照计划的顺序对实施步骤进行分组。 对于每个步骤，您可以：

* 分配所有者
* 更新状态，如进行中或完成
* 将步骤标记为不适用，或者如果它不适用于您的实施，则跳过该步骤
* 添加评论并与团队协作
* 对于需要签名的步骤，在某个步骤被视为完成之前需要批准

**自动和辅助步骤**

在技术可行的情况下，同事直接执行或协助执行某个步骤，例如从Adobe Analytics或Customer Journey Analytics中显示配置或状态数据。 这些步骤包括如上所述的置信度或验证信号。

**导出**

将清单或其摘要级进度导出到Jira、Workfront或Excel，以便将其折叠到现有项目管理工作流中。

**多个核对清单**

如果您同时管理多个实施（如多个报表包、区域或品牌），则可以维护多个实施核对清单项目，而不是限制为仅一个项目。
