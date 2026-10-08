---
title: 与同事验证您的流媒体实施
description: 了解同事的流媒体验证技能如何检查您的配置、会话和日志，以确认您的实施正确跟踪。
hold: true
source-git-commit: 2bf31c1348054a16ba7e7c0c26c0ff913634aa27
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%
---

# 与同事验证您的流媒体实施

Adobe CX Enterprise Coworker包括“流媒体验证”技能，可检查您在Edge Network上实施的Adobe Streaming Media(Video and Audio Analytics)，以馈送Customer Journey Analytics和/或Adobe Analytics。 您将获得一个验证报告，而不是手动交叉引用Assurance、数据集配置、XDM架构字段组、Customer Journey Analytics数据视图设置和原始网络日志。

如果您要实施流媒体跟踪或排除流媒体跟踪故障，则可以使用此技能确认您的实施已正确配置、按预期收集数据并捕获您打算跟踪的内容，所有这些都可以在一个“同事聊天”对话中完成。

>[!NOTE]
>
>请考虑以下事项：
>
>* 此技能属于更大的可选工作流：自定义实施或升级步骤（请参阅[与同事一起计划实施](./implementation-guide.md)）、实施（请参阅[生成与同事项目的实施核对清单](./intelligent-checklist.md)）和验证（此技能）。 您无需使用所有三个阶段。 例如，您可以验证您的流媒体实施，而无需生成计划或核对清单。
>* 此技能可验证和诊断问题。 它不会修复您的配置或数据。 利用其发现结果指导您自己的补救措施。

使用此技能可以：

* 跨数据流、XDM架构、数据集和Customer Journey Analytics数据视图运行配置审核，并将第一个损坏的检查点标记为可能的原因。

  此功能当前处于“有限可用”状态。

* 验证特定的视频会话ID，并准确地查看哪个跃点、数据集摄取或Customer Journey Analytics映射，在出现了差异。

* 通过上传的Charles或HAR日志或更简单的URL列表验证会话，而无需实时Assurance会话。

  此功能当前处于“有限可用”状态。

* 获取带有单个提示的整体运行状况检查，无需会话ID或日志，该提示将汇总您的配置和近期会话的示例。

## 开始之前

<!-- FLAG: General access prerequisite is inferred, not stated explicitly in source docs. Per-mode inputs (session ID, log file) are directly sourced from Functional Requirements. -->

### 所需信息

要验证您的流媒体实施，您需要：

* 访问与您组织的Adobe Experience Platform和Customer Journey Analytics数据连接的同事。

* 对于会话ID验证，需要检查的视频会话ID。

* 用于基于日志的验证，Charles或HAR日志文件，或者更简单的.txt、.md或.json格式的URL列表。

配置审核或整体运行状况检查不需要任何特定输入。 Co-worker自动读取现有配置并示例最近的会话。

### 限制

在使用本技能之前，请牢记以下几点：

* **仅诊断**：此技能无法修复您的配置或数据。 它标识问题；您进行更改。
* **仅限流媒体**：此技能涵盖Edge Network上的流媒体实施。 其他同事验证技能涵盖非媒体数据集和标准Web或应用程序分析实施。
* **仅限按需**：此技能不提供实时或连续监视。 在需要检查时运行它，而不是作为持续的警报。
* **无内置爬虫**：此技能不会抓取您的网站或应用程序。 如果要验证作为抓取的覆盖范围，请提供爬虫或headless-browser输出作为证据。
* 仅&#x200B;**Edge Network实施**：不支持旧版Media SDK和仅Analytics实施路径。
* **尚未包含更广泛的功能**：计划于以后的版本中推出实时活动和心率流验证、客户剧本或方案验证、多平台历史仪表板汇总以及下游Real-Time CDP或Adobe Journey Optimizer激活验证。

## 启动验证会话

1. 登录到同事。

1. 选择&#x200B;[!UICONTROL **新聊天**]。

1. 在文本字段中，说明要验证的内容。 例如：

   **提示**

   > 验证视频会话ID #123。

   您的请求将被路由到流媒体验证技能，该技能运行匹配验证模式。

1. （视情况而定）如果技能需要更多信息（如会话ID或日志文件），请在询问时提供此信息。

## 选择您的验证模式

流媒体验证技能包括四种模式。

### 配置审核

此功能当前处于“有限可用”状态。

验证从数据流到Customer Journey Analytics数据视图的整个Adobe Experience Platform流程，包括XDM架构、数据集以及任何数据准备规则或Customer Journey Analytics派生字段。 同事会报告每跳通过/失败记分卡，并将第一个损坏的检查点标记为可能的原因。

示例提示：

* 验证数据视图、数据集和数据流的流媒体配置。
* 检查我的流媒体配置是否端对端。
* 是否为Customer Journey Analytics正确设置了我的Media Analytics数据流？

### 会话ID验证

针对特定视频会话的Adobe Experience Platform数据视图交叉检查Customer Journey Analytics数据集行，并查明差距是数据集摄取问题还是Customer Journey Analytics映射问题。

示例提示：

* 验证视频会话ID #123。
* 为什么会话abc-123没有显示在Customer Journey Analytics中？
* 比较数据集和Customer Journey Analytics数据视图之间的会话xyz 。

### 基于日志的验证

此功能当前处于“有限可用”状态。

通过您上传的Charles或HAR日志或者更简单的URL列表验证会话，而无需实时Assurance会话。 Co-worker将验证端点模式、响应代码、事件顺序和Ping节奏，并说明哪些检查是按完全置信度运行、置信度降低还是被跳过。

示例提示：

* 验证附加的流媒体数据日志。
* 查看此Charles日志以了解会话ID #456。
* 根据预期的媒体Ping验证此URL列表。

### 验证仪表板

通过单个提示获得整体运行状况检查。 Co-worker将配置审核和轻量级的采样会话检查汇总到一个状态，并明确说明如果未提供日志，则基于日志的检查不会运行。

示例提示：

* 检查流媒体数据。
* 给我一个关于我的流媒体实施的报告。
* 我的流媒体实施总体情况如何？

## 查看结果

每种模式都会以适合您验证的格式返回结果。

**配置审核结果**

一个每跳传递/失败的记分卡，涵盖数据流、XDM架构、数据集、Customer Journey Analytics数据视图、数据准备或派生的字段规则。 Co-worker将第一个失败的跃点识别为可能的根本原因。

**会话ID验证结果**

仅限Customer Journey Analytics的报表摘要，包括会话ID、内容元数据、按事件类型划分的行计数、关键量度值和完整性说明。 如果存在空隙，Co-worker会标识空隙发生在数据集摄取时还是Customer Journey Analytics映射步骤中。

>[!NOTE]
>
>默认情况下，会话ID和经过身份验证的身份值将从任何导出或共享的摘要中排除。

**基于日志的验证结果**

对上传的日志进行结构和顺序验证，包括端点模式、响应代码、事件顺序和Ping频率。 Co-worker根据您提供的是完整日志捕获还是更简单的URL列表，指出哪些检查是满负荷运行的，哪些检查是满负荷运行的，哪些检查是满负荷运行的，哪些检查是低负荷运行的，哪些检查被跳过。

**报告面板结果**

标记为“Configuration + Available Data”（配置+可用数据）的单个统一状态，将配置审核结果与最近会话的采样检查相结合。 对会话进行采样的协同工作名称，并明确说明由于未提供日志而未运行基于日志的检查。

## 验证的工作方式

每种模式都映射到专用引擎：

* **配置验证引擎**：读取您的数据流、XDM架构、数据集和Customer Journey Analytics数据视图配置，并根据一组固定的检查点对其进行评估。
* **会话交叉检查引擎**：给定会话ID，查询您的数据集和Customer Journey Analytics数据视图，计算该会话的预期行数和类型，并比较每个跃点的实际结果。
* **Log Parser and Validator**：解析上载的日志或URL列表，重新构建请求序列和计时，并应用结构化、排序和网络层检查。
* **仪表板聚合引擎**：运行配置验证引擎和会话交叉检查引擎的采样运行，并在您未提供会话ID、日志或行动手册时，将它们组合为单个状态。
